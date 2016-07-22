:data-transition-duration: 2000
:skip-help: true
:css: css/campus02.css

.. role:: html(code)
  :language: html

.. _RFC 7230: http://tools.ietf.org/html/rfc7230
.. _RFC 7231: http://tools.ietf.org/html/rfc7231
.. _RFC 7232: http://tools.ietf.org/html/rfc7232
.. _RFC 7233: http://tools.ietf.org/html/rfc7233
.. _RFC 7234: http://tools.ietf.org/html/rfc7234
.. _RFC 7235: http://tools.ietf.org/html/rfc7235
.. _MIME-Types: http://www.iana.org/assignments/media-types/
.. _HTTP Status Codes: http://www.iana.org/assignments/http-status-codes
.. _Uniform Resource Identifier (URI): http://tools.ietf.org/html/rfc3986
.. _IANA: http://www.iana.org/assignments/urn-namespaces

.. title: HyperText Transfer Protocol

----


HTTP
====

Hypertext Transfer Protocol


----

Agenda
======

* HTTP-Grundlagen
* Medientypen
* HTTP-Nachrichten
* HTTP-Adressierung
* HTTP-Authentifizierung


----

Wie spricht ein Browser mit einem Webserver?
--------------------------------------------

* Client-Server-Technologie
* Transportprotokoll
* TCP über IPv4 oder IPv6


----


Webserver verwaltet Ressourcen
------------------------------

.. image:: figures/http-content.svg
  :alt: Statisch/Dynamisch


----

Austausch von HTTP-Nachrichten
------------------------------

*Request-Response-Prinzip*

.. image:: figures/http.svg
  :alt: Request-Response


----

HTTP im Schichtenmodell
-----------------------

.. image:: figures/http-osi.svg
  :alt: HTTP/OSI


----

HTTP-Anforderung (Request)
--------------------------

.. image:: figures/http-request.svg
  :alt: HTTP Request


----

.. code:: http

  GET /DE/Homepage.aspx HTTP/1.1
  Host: www.campus02.at
  User-Agent: Mozilla/5.0
  Accept: text/html
  Accept-Language: en-US,en;q=0.5
  Accept-Encoding: gzip, deflate
  Cookie: ASP.NET_SessionId=1234
  Connection: keep-alive
  Cache-Control: max-age=0


----

Methoden (HTTP/1.1)
-------------------

+---------------+------------------------------------------------------------------------------------------------------------+
| **`GET`**     | Anforderung einer HTML-Datei oder einer anderen Ressource                                                  |
+---------------+------------------------------------------------------------------------------------------------------------+
| **`POST`**    | Übermittlung von Formular-Daten, Postings, Kommentaren, Dateiuploads                                       |
+---------------+------------------------------------------------------------------------------------------------------------+
| **`PUT`**     | Erstellung oder Änderung einer Ressource auf dem Server                                                    |
+---------------+------------------------------------------------------------------------------------------------------------+
| **`DELETE`**  | Löschung der angegebenen Ressource vom Server                                                              |
+---------------+------------------------------------------------------------------------------------------------------------+
| **`HEAD`**    | Ident der GET-Methode, allerdings sendet der Server in seiner Antwort nur den Header (keinen Message-Body) |
+---------------+------------------------------------------------------------------------------------------------------------+
| **`OPTIONS`** | Abfrage der Eigenschaften einer Resource oder des gesamten Servers                                         |
+---------------+------------------------------------------------------------------------------------------------------------+
| **`TRACE`**   | Reflektiert die Anfrage im Message-Body                                                                    |
+---------------+------------------------------------------------------------------------------------------------------------+
| **`CONNECT`** | Umschalten der Verbindung auf HTTPS für einen Proxy                                                        |
+---------------+------------------------------------------------------------------------------------------------------------+


----

HTTP-Antwort (Response)
-----------------------

.. image:: figures/http-response.svg
  :alt: HTTP Response


----

.. code:: http

  HTTP/1.1 200 OK
  Cache-Control: no-cache
  Pragma: no-cache
  Content-Type: text/html; charset=utf-8
  Expires: -1
  Server: Microsoft-IIS/7.5
  X-AspNet-Version: 2.0.50727
  X-Powered-By: ASP.NET
  Date: Fri, 18 Sep 2015 19:26:05 GMT
  Content-Length: 22858

  <html>...</html>


----

HTTP-Statuscodes
----------------

Startzeile der Antwortnachricht enthält einen Statuscode und eine Kurzerklärung:

+--------------+-----------------------+-------------------------------+
| **Code**     | **Beschreibung**      | **Beispiel**                  |
+==============+=======================+===============================+
| *1xx*        | Informational         | `100 Continue`                |
+--------------+-----------------------+-------------------------------+
| *2xx*        | Success               | `200 OK`                      |
+--------------+-----------------------+-------------------------------+
| *3xx*        | Redirection           | `301 Moved Permanently`       |
+--------------+-----------------------+-------------------------------+
| *4xx*        | Client Error          | `401 Unauthorized`            |
+--------------+-----------------------+-------------------------------+
| *5xx*        | Server Error          | `503 Service Unavailable`     |
+--------------+-----------------------+-------------------------------+


----

Medientypen
-----------

*MIME-Types*

* Datentyp einer Ressource
* Anzeige durch den Browser
* Multipurpose Internet Mail Extensions (MIME)
* Angabe des Medientypes und eines Subtypes


----

Beispiel
--------

Als Header im HTTP Response, um anzuzegen, dass der Body HTML enthält:

.. code:: http

  HTTP/1.1 200 OK
  Content-Type: text/html

  <html>...</html>


----

Die wichtigsten MIME-Types
--------------------------

+-----------------------+-------------------------------------------------------+-------------------------------------------------------+
| **MIME-Type**         | **Beschreibung**                                      | **Beispiel**                                          |
+=======================+=======================================================+=======================================================+
| **`text`**            | Textdateien                                           | `text/html`, `text/plain`                             |
+-----------------------+-------------------------------------------------------+-------------------------------------------------------+
| **`image`**           | Bilder, Fotos, Grafiken                               | `image/jpeg`, `image/png`                             |
+-----------------------+-------------------------------------------------------+-------------------------------------------------------+
| **`video`**           | Videos                                                | `video/mpeg`, `video/ogg`                             |
+-----------------------+-------------------------------------------------------+-------------------------------------------------------+
| **`audio`**           | Audiodateien                                          | `audio/mpeg`, `audio/ogg`                             |
+-----------------------+-------------------------------------------------------+-------------------------------------------------------+
| **`application`**     | Ressourcen, die an eine Applikation gebunden sind     | `application/pdf` `application/vnd.ms-powerpoint`     |
+-----------------------+-------------------------------------------------------+-------------------------------------------------------+


----

HTTP-Adressierung
-----------------

* URI
* URL
* URN


----

URI
---

*Uniform Resource Identifier*

* RFC 3986
* Einheitlicher Bezeichner für eine Ressource
* Übermenge von URL und URN


----

URL
---

*Uniform Resource Locator*

* Standardisierte Adresse einer Ressource
* Spezifischer Typ einer URI
* Definiert, wie auf eine Resource zugegriffen werden kann
* Sind an DNS gebunden

Beispiel: `http://www.campus02.at/`

Adressiert Resourcen in HTTP.


----

URN
---

*Uniform Resource Name*

* Einheitlicher Name für eine Ressource
* Ortsunabhängig
* `IANA`_ verwaltet Namensräume

Beispiel: `urn:isbn:3827370191`

Findet bei HTTP keine direkte Verwendung.

----

Aufbau einer URL
----------------

::

    scheme://user:password@host:port/path?query#fragment
             ^------authority------^


::

    https://bob:123@campus02.at:80/Homepage?d=true#toc
    https://google.at
    https://en.wikipedia.org/wiki/Uniform_Resource_Locator
    http://science.orf.at/stories/1763011/
    ftp://ftp.funet.fi/pub/standards/RFC/rfc959.txt


----

Komponenten einer URL
---------------------

+---------------------+--------------------------------------------+---------------------------+
| **Komponente**      | **Beschreibung**                           | **Beispiel**              |
+=====================+============================================+===========================+
| **`scheme`**        | Transportprotokoll                         | `http`                    |
+---------------------+--------------------------------------------+---------------------------+
| **`authority`**     | `[userinfo"@"]host[":"port]`               | `bob:123@example.com`     |
+---------------------+--------------------------------------------+---------------------------+
| **`host`**          | Domainname oder IP-Adresse des Servers     | `www.example.com`         |
+---------------------+--------------------------------------------+---------------------------+
| **`port`**          | Nummer eines TCP oder UDP Port             | `443`                     |
+---------------------+--------------------------------------------+---------------------------+
| **`path`**          | Pfad der Ressource                         | `/document.html`          |
+---------------------+--------------------------------------------+---------------------------+
| **`query`**         | übergebenes Argument                       | `page=4`                  |
+---------------------+--------------------------------------------+---------------------------+
| **`fragment`**      | Verweis innerhalb einer Ressource          | `#index`                  |
+---------------------+--------------------------------------------+---------------------------+


----

HTTP-Authentifizierung
----------------------

*RFC 2617*

* eingeschränkter Zugriff auf Ressourcen
* Benutzername / Passwort
* einseitige Authentifizierung des Clients
* Basic HTTP Authentication
* Digest Access Authentication (verschlüsselte Übertragung)


----

Referenzen
----------

* Hypertext Transfer Protocol HTTP/1.1

  * `RFC 7230`_
  * `RFC 7231`_
  * `RFC 7232`_
  * `RFC 7233`_
  * `RFC 7234`_
  * `RFC 7235`_

* `MIME-Types`_
* `HTTP Status Codes`_
* `Uniform Resource Identifier (URI)`_

