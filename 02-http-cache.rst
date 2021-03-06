:data-transition-duration: 2000
:skip-help: true
:css: css/campus02.css

.. role:: html(code)
  :language: html

.. _Hypertext Transfer Protocol (HTTP/1.1) - Caching: http://tools.ietf.org/html/rfc7234
.. _Hypertext Transfer Protocol (HTTP/1.1) - Conditional Requests: http://tools.ietf.org/html/rfc7232

.. title: HTTP: Cache und Proxies

----

HTTP: Cache und Proxies
=======================


----

Mehrfaches Anfordern verhindern
-------------------------------

Eine Ressource wird mehrfach abgerufen. Zum Beispiel eine Logo-Grafik, die auf
jeder Seite einer Homepage verwendet wird.

Jeder neue Abruf würde die selben Daten erneut übertragen.


----

Ressource wird abgerufen
------------------------

.. image:: figures/http-request-repeated-1.svg
  :alt: Ressource wird einfach abgerufen


----

Ressource wird erneut abgerufen
-------------------------------

.. image:: figures/http-request-repeated-2.svg
  :alt: Ressource wird erneut abgerufen


----

Lösung: Lokaler Zwischenspeicher
--------------------------------

*Browser-Cache*

Der Webbrowser speichert automatisch einmal abgerufene Ressourcen zwischen und
verwendet die lokale Kopie falls die Ressource erneut angezeigt werden soll.


----

Browser-Cache
-------------

.. image:: figures/http-request-repeated-3.svg
  :alt: Ressource wird aus dem Cache bedient


----

Mehrere Benutzer
----------------

Mehrere Benutzer in einem gemeinsamen Netzwerk wollen nacheinander die selbe
Ressource abrufen. Jeder neue Abruf würde die Ressource unnötig oft übertragen.

Ein lokaler Cache ist keine Lösung, weil dieser nur für den Benutzer (bzw.
seinen eigenen Webbrowser) verfügbar ist.

----

Erste Ressource wird abgerufen
------------------------------

.. image:: figures/http-request-multiple-1.svg
  :alt: Ressource wird vom ersten Browser abgerufen


----

Andere Benutzer rufen Ressource ab
----------------------------------

.. image:: figures/http-request-multiple-2.svg
  :alt: Ressource wird vom zweiten Browser abgerufen


----

Lösung: HTTP-Proxy
------------------

Ein eigener Server im lokalen Netzwerk übernimmt die Rolle eines zentrallen
Caches, der einmal abgerufene Ressourcen zwischenspeichert und diese bei Bedarf
ausliefert, ohne sie erneut vom Ursprungs-Webserver neu zu übertragen.


----

HTTP-Steuerung
--------------

Nicht alle Inhalte sind gleich:

* Logo: ändert sich selten / für alle gleich
* Nachrichtenseite: ändert sich häufig / für alle gleich
* Personalisierte Seite: nur für eine Person


----

HTTP-Steuerung
--------------

Drei HTTP-Header haben Einfluss:

* Expires
* Cache-Control
* Etag

Sowie:

* Last-Modified
* Pragma


----

HTTP-Header: Expires
--------------------

* Absolutes Ablaufdatum + Uhrzeit
* Solange nicht abgelaufen: Zwischengespeicherte Ressource verwendbar
* Danach: Ressource neu laden


----

Beispiel für Expires
--------------------

Im HTTP-Response:

.. code:: http

  HTTP/1.1 200 OK
  Date: Thu, 18 Sep 2015 15:31:51 GMT
  Expires: Thu, 18 Sep 2015 15:36:51 GMT

  ...

Empfangene Resource kann zwischengespeichert werden, bis der in `Expires`
angegebene Zeitpunkt überschritten wurde. Danach muss erneut angefordert werden.


----

HTTP-Header: Etag
-----------------

* Ressource wird mit Versionsnummer (z.B. Hash) versehen
* Basiert auf Veränderungsdatum, Dateigröße etc.
* Wird automatisch von Server bzw. Webanwendung erzeugt


----

Beispiel für Etag (1/2)
-----------------------

Im HTTP-Response:

.. code:: http

  HTTP/1.1 200 OK
  Date: Thu, 18 Sep 2014 15:31:51 GMT
  Etag: "1668fa-a63-46bb3da3dc"

  Inhalt der Ressource ...

Im nächsten HTTP-Request für gleiche Ressource:

.. code:: http

  GET /logo.png HTTP/1.1
  If-None-Match: "1668fa-a63-46bb3da3dc"


----

Beispiel für Etag (2/2)
-----------------------

Falls angeforderte Ressource noch immer unverändert am Webserver:

.. code:: http

  HTTP/1.1 304 Not Modified

Resource wurde in der Zwischenzeit am Webserver verändert:

.. code:: http

  HTTP/1.1 200 OK
  Date: Thu, 18 Sep 2015 15:33:51 GMT
  Etag: "5a4511-b66-3456aab211"

  Inhalt der Ressource ...

Bei nächstem Abruf wird der neue Wert von `Etag` in `If-None-Match` abgefragt.

----

HTTP-Header: Cache-Control
--------------------------

In HTTP-Response vom Webserver:

+-----------------------+-------------------------------------------------------------------------------------------+
| **Anweisung**         | **Beschreibung**                                                                          |
+=======================+===========================================================================================+
| **`max-age=sec`**     | Maximales Alter der Version im Cache in Sekunden                                          |
+-----------------------+-------------------------------------------------------------------------------------------+
| **`must-revalidate`** | Zwischenspeichern möglich; Client muss aber nach Ablauf Server erneut kontaktieren        |
+-----------------------+-------------------------------------------------------------------------------------------+
| **`no-cache`**        | Nicht (bzw. nur bedingt) zwischenspeichern (Nachfragen bei Server immer notwendig)        |
+-----------------------+-------------------------------------------------------------------------------------------+
| **`no-store`**        | Nicht (lokal) speichern (z.B. in Temporäre Internetdateien); für sensible Inhalte gedacht |
+-----------------------+-------------------------------------------------------------------------------------------+
| **`private`**         | Nur in einem privaten Cache ablegen                                                       |
+-----------------------+-------------------------------------------------------------------------------------------+
| **`public`**          | Ressource kann von verschiedenen Benutzern verwendet werden                               |
+-----------------------+-------------------------------------------------------------------------------------------+

Server gibt Cache-Verhalten vor.


----

Beispiel für Cache-Control (Server)
-----------------------------------

Im HTTP-Response:

.. code:: http

  HTTP/1.1 200 OK
  Cache-Control: public, max-age=86400


----

HTTP-Header: Cache-Control
--------------------------

In HTTP-Request vom Webbrowser:

+---------------------+----------------------------------------------------------------------------------------+
| **Anweisung**       | **Beschreibung**                                                                       |
+=====================+========================================================================================+
| **`max-age=sec`**   | Maximales Alter der Version im Cache in Sekunden                                       |
+---------------------+----------------------------------------------------------------------------------------+
| **`min-fresh=sec`** | Ressource muss mindestens noch #sec Sekunden frisch sein, d.h. im Cache nicht ablaufen |
+---------------------+----------------------------------------------------------------------------------------+
| **`max-stale=sec`** | Client akzeptiert auch abgelaufene Cache-Ressourcen (maximal #sec Sekunden abgelaufen) |
+---------------------+----------------------------------------------------------------------------------------+
| **`no-cache`**      | Client möchte Ressource, die nicht zwischengespeichert ist (d.h. frisch vom Server)    |
+---------------------+----------------------------------------------------------------------------------------+

Client weist Server (und Proxies) an, welche Aktualität die angeforderten Inhalte erfüllen sollen.


----

Beispiel für Cache-Control (Client)
-----------------------------------

Im HTTP-Request:

.. code:: http

  GET /logo.png HTTP/1.1
  Cache-Control: no-cache


----

Cache-Control Entscheidungshilfe
--------------------------------

.. image:: figures/http-cache-control-flow.svg
  :alt: Cache-Control


----

HTTP-Header: Last-Modified
--------------------------

Im HTTP-Response:

.. code:: http

  HTTP/1.1 200 OK
  Last-Modified: Tue, 15 Nov 1994 12:45:26 GMT

* Gibt Datum der letzten Änderung der Ressource an
* Manche Browser verwenden Datum für eine Heuristik
* Von Client-Seite auch ähnlich wie Etag If-Abfrage möglich
* Falls unverändert, antwortet Server wieder mit 304-Statuscode


----

Beispiel für Last-Modified
--------------------------

Im HTTP-Request:

.. code:: http

  GET /foto.jpg HTTP/1.1
  If-Modified-Since: Sun, 31 May 2015 03:14:07 GMT

Der Webbrowser fragt ab, ob die Ressource seit ihrem letzten Abruf verändert
wurde. Der Webserver muss entscheiden, wie die Anfrage zu beantworten ist.


----

HTTP-Header: Pragma
-------------------

* Veraltet und nur für Anfragen (bei Antworten eigentlich zweckentfremdet)
* Dennoch noch häufig anzutreffen


----


Referenzen
----------

* `Hypertext Transfer Protocol (HTTP/1.1) - Caching`_
* `Hypertext Transfer Protocol (HTTP/1.1) - Conditional Requests`_

