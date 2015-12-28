HTML
====

*HyperText Markup Language*

.. raw:: html

   <div class="corner-ribbon top-right sticky yellow shadow">

CAMPUS02

.. raw:: html

   </div>

Was ist HTML?
=============

HTML ist das Dokumentformat des WWW
-----------------------------------

Anwendung & Eigenschaften
-------------------------

-  HTML dient der Strukturierung von Texten (Tags)
-  Trennung von Aufbau (HTML) und Darstellung (CSS)
-  Weiterentwicklung durch das `World Wide Web Consortium
   (W3C) <http://www.w3.org/>`__

Text mit Auszeichnung
---------------------

Leonato. I learn in this letter that Don Peter of Arragon comes this
night to Messina.

Messenger. He is very near by this: he was not three leagues off when I
left him.

Leonato. How many gentlemen have you lost in this action?

Messenger. But few of any sort, and none of name.

Auszeichnung
------------

-  Semantische Auszeichnung = Beschreibung von Text
-  Festlegung der Art einer Textstelle über Markierungen

HTML 1.0 (1989)
---------------

Erster Entwurf von Sir Tim Berners-Lee.

.. figure:: images/Sir_Tim_Berners-Lee.jpg
   :alt: Sir Tim Berners Lee

   Sir Tim Berners Lee

\ `Picture licensed CC BY-SA
4.0 <https://commons.wikimedia.org/wiki/User:Paulrclarke>`__\ 

HTML 3.2 (1996)
---------------

Neuerungen:

-  Tabellen
-  Client-Side-Maps
-  Einbindung von Java-Applets
-  Attribute zur Text-/Bildausrichtung

HTML 4.01 (1999)
----------------

Erweiterungen und Korrekturen.

XHTML 1.0 (2000)
----------------

Neudefinition von HTML 4.01 in XML.

HTML 5
------

-  In "permanenter" Entwicklung
-  Modularisierung; Sammelbegriff für verschiedene Technologien
-  W3C Candidate Recommendation 6.8.2013

HTML-Syntax
===========

Attribute
---------

-  Zusatz zur Beschreibung einer Eigenschaft
-  Im Opening-Tag eines Elements notiert
-  Name-Wert-Paar: ``name="Wert"``

::

        &lt;a href="http://www.campus02.at/"&gt;FH CAMPUS02&lt;/a&gt;

Zeichenreferenzen / Entitäten
-----------------------------

-  Für Umlaute, Zeichen mit Bedeutung in HTML5
-  Zur Vermeidung von Fehlinterpretationen

+---------------------+------------------+------------------+
| **Sonderzeichen**   | **Entität**      | **Unicode**      |
+=====================+==================+==================+
| &                   | ``&amp;amp;``    | ``&amp;#38;``    |
+---------------------+------------------+------------------+
| <                   | ``&amp;lt;``     | ``&amp;#60;``    |
+---------------------+------------------+------------------+
| >                   | ``&amp;gt;``     | ``&amp;#62;``    |
+---------------------+------------------+------------------+
| "                   | ``&amp;quot;``   | ``&amp;#34;``    |
+---------------------+------------------+------------------+
| ä                   | ``&amp;auml;``   | ``&amp;#228;``   |
+---------------------+------------------+------------------+

Unicode-Zeichen können in der
`Unicode-Zeichen-Tabelle <http://unicode-table.com/de/>`__
nachgeschlagen werden.

.. figure:: figure/html5-abstract-language.svg
   :alt: Die zwei Serialisierungen von HTML5

   Die zwei Serialisierungen von HTML5

Welche Inhalte einer Website kennen Sie?
========================================

Block-Elemente
--------------

-  Erzeugen einen eigenen Absatz
-  Unterschiedlicher Abstand je nach Element
-  Können Text, Inline-Elemente und teilweise andere Block-Elemente
   enthalten

+--------------------------------------+------------------------------------+
| **Element**                          | **Bedeutung**                      |
+======================================+====================================+
| ``&lt;p&gt;``                        | Textabsatz                         |
+--------------------------------------+------------------------------------+
| ``&lt;h1&gt;`` bis ``&lt;h6&gt;``    | Überschrift 1. bis 6. Ordnung      |
+--------------------------------------+------------------------------------+
| ``&lt;div&gt;``                      | allgemeine Gruppierung             |
+--------------------------------------+------------------------------------+
| ``&lt;blockquote&gt;``               | Zitatblock                         |
+--------------------------------------+------------------------------------+
| ``&lt;pre&gt;``                      | vorformatierter Text               |
+--------------------------------------+------------------------------------+
| ``&lt;ul&gt;`` bzw. ``&lt;ol&gt;``   | unsortierte bzw. sortierte Liste   |
+--------------------------------------+------------------------------------+

Inline-Elemente
---------------

-  Erzeugen KEINEN Zeilenumbruch
-  Als untergeordnete Elemente für Block-Elemente gedacht
-  Können Text oder weitere Inline-Elemente enthalten

+----------------------+---------------------------------------------------------------------+
| **Element**          | **Bedeutung**                                                       |
+======================+=====================================================================+
| ``&lt;strong&gt;``   | betonter Text (wird fett dargestellt)                               |
+----------------------+---------------------------------------------------------------------+
| ``&lt;b&gt;``        | fetter Text                                                         |
+----------------------+---------------------------------------------------------------------+
| ``&lt;span&gt;``     | zur Gruppierung bzw. Auszeichnung von Inline-Elementen und Texten   |
+----------------------+---------------------------------------------------------------------+
| ``&lt;code&gt;``     | Quellcode                                                           |
+----------------------+---------------------------------------------------------------------+

Ungeordnete Liste
-----------------

.. raw:: html

   <ul>

.. raw:: html

   <li>

Eintrag

.. raw:: html

   </li>

.. raw:: html

   <li>

Eintrag

.. raw:: html

   </li>

.. raw:: html

   <li>

Eintrag

.. raw:: html

   </li>

.. raw:: html

   </ul>

::

    &lt;ul&gt;
      &lt;li&gt;Eintrag&lt;/li&gt;
      &lt;li&gt;Eintrag&lt;/li&gt;
      &lt;li&gt;Eintrag&lt;/li&gt;
    &lt;/ul&gt;

Definitionsliste
----------------

.. raw:: html

   <dl>

.. raw:: html

   <dt>

Bezeichnung 1. Eintrag

.. raw:: html

   </dt>

.. raw:: html

   <dd>

Beschreibung zu erstem Eintrag.

.. raw:: html

   </dd>

.. raw:: html

   <dt>

Bezeichnung 2. Eintrag

.. raw:: html

   </dt>

.. raw:: html

   <dd>

Beschreibung zu zweitem Eintrag.

.. raw:: html

   </dd>

.. raw:: html

   </dl>

::

    &lt;dl&gt;
      &lt;dt&gt;Bezeichnung 1. Eintrag&lt;/dt&gt;
      &lt;dd&gt;Beschreibung zu erstem Eintrag.&lt;/dd&gt;
      &lt;dt&gt;Bezeichnung 2. Eintrag&lt;/dt&gt;
      &lt;dd&gt;Beschreibung zu zweitem Eintrag.&lt;/dd&gt;
    &lt;/dl&gt;

Links
-----

-  Sind Inline-Elemente
-  Links zu anderen Dokumenten:

   ::

       &lt;a href="http://www.campus02.at/index.asp?menuId=5"&gt;
         sichtbarer Linktext
       &lt;/a&gt;

-  Sprungziel in einem Dokument:

   ::

       &lt;a name="ankername"&gt;Sprungziel-Text&lt;/a&gt;
       &lt;h1 id="ankername"&gt;Sprungziel-Text&lt;/h1&gt;

-  Link zu einem Sprungziel im gleichen Dokument:

   ::

       &lt;a href="#ankername"&gt;sichtbarer Linktext&lt;/a&gt;

-  Link zu einem Sprungziel in einem anderen Dokument:

   ::

       &lt;a href="http://www.campus02.at/index.asp#ankername"&gt;
         sichtbarer Linktext
       &lt;/a&gt;

Absolute URIs
-------------

Die einfachste, aber auch am wenigsten flexibel anwendbare Variante. Sie
geben den Ort der Resource absolut an ohne die aktuelle URI zu
berücksichtigen.

-  ``http://www.example.org/``
-  ``http://www.example.org/index.htm``
-  ``http://www.example.org/index.htm#toc``
-  ``https://www.example.org/cgi-bin/suche.cgi?ausdruck=Lorem``
-  ``ftp://www.example.org/documents/invoice.pdf``
-  ``http://www.example.org:8082/backend/admin.html``

Absolute Pfade
--------------

Referenzieren Resource absolut auf einer Authority (siehe URLs). Pfade
beginnen an der **Document-Root** des Webservers.

-  ``/``
-  ``/index.htm``
-  ``/index.htm#toc``
-  ``/cgi-bin/suche.cgi?ausdruck=Lorem``
-  ``/documents/invoice.pdf``
-  ``/backend/admin.html``

Zurück zu HTML
==============

Formulare
---------

-  Block-Elemente
-  Definition des Formularbereiches mit **``&lt;form&gt;``**
-  Pflichtattribut **``action``** definiert die Zieladresse der Daten
-  Attribut **``method``** bestimmt wie die Daten übertragen werden
   **``(method="post | get")``**
-  Interaktion mit dem Benutzer über Formularelemente

::

    &lt;form action="/blog/article/save" method="post"&gt;
      ...
    &lt;/form&gt;

Eingabefelder, Radio-Buttons, Checkboxen, …
-------------------------------------------

::

    &lt;input type="..." name="..." /&gt;

Attribut **``type``**: ``text`` \| ``password`` \| ``radio`` \|
``checkbox`` \| …

Textfelder
----------

.. raw:: html

   <textarea cols="50" rows="10 cols=" 50" rows="10" ">

Hier kann mehrzeiliger Text eingegeben werden ... Dies ist die zweite
Zeile ...

.. raw:: html

   </textarea>

::

    &lt;textarea name="..."&gt;
    ... Text...
    ... mehrzeilig ...
    &lt/textarea&gt;

Frames
------

-  Definition eines Framesets mittels **``&lt;frameset&gt;``**. Die
   Attribute **``cols``** und **``rows``** definieren die Spalten und
   Zeilen.
-  Definition eines einzelen Frames mittels **``&lt;frame&gt;``**. Das
   Attribut **``src``** legt den URL zum Inhalte des Frames fest.
-  Framesets können ineinander geschachtelt werden.
-  Veraltet und haben Probleme (Bookmarks, Ausdrucke, neu laden,
   vor/zurück).

::

    &lt;frameset cols="50%,50%"&gt;
      &lt;frame src="page.html" /&gt;
      &lt;frame src="http://example.com/main.html" /&gt;
    &lt;/frameset&gt;

Videos
------

.. raw:: html

   <video width="640" height="360" autoplay="autoplay" loop="loop" muted="muted">

.. raw:: html

   </video>

::

    &lt;video width="640" height="360"
      muted="muted" autoplay="autoplay" loop="loop"&gt;
      &lt;source src="video/bunny.mp4" type="video/mp4"/&gt;
      &lt;source src="video/bunny.webm" type="video/webm"/&gt;
      &lt;source src="video/bunny.ogv" type="video/ogg"/&gt;
    &lt;/video&gt;

`Demo-Videos <http://www.sample-videos.com/>`__ zum Download.

Externe Plugins
---------------

-  Flash
-  Java Applets
-  Silverlight
-  ActiveX
-  ...

::

    &lt;object width="40" height="50" data="flash.swf"&gt;&lt;/object&gt;

Die Tabelle
-----------

``tabelle.html``

.. raw:: html

   <iframe src="tabelle.html" class="embedded-website">

.. raw:: html

   </iframe>

Das Formular
------------

``formular.html``

.. raw:: html

   <iframe src="formular.html" class="embedded-website">

.. raw:: html

   </iframe>

POST-Request sollen vom Formular an die
`Demo-Anwendung <https://campus02.fladi.at/web/form-data>`__ geschickt
werden.

Einzelarbeit
============

Erstellen Sie eine Website für einen Tee-Shop mit diesen Seiten:

-  Startseite
-  Produktübersicht
-  Mehrere Detail-Seiten
-  Bestellformular

Daten zu den Tee-Sorten finden Sie auf
`Moodle <https://moodle.campus02.at/>`__.

Produktübersicht
----------------

-  Tabelle der Tee-Sorten mit Name, Art, Abbild, Herkunft, Brühzeit und
   Preis/100g (min. 5 Tee-Sorten)
-  Verlinkung jeder Teesorte auf eine Detail-Seite
-  Internes Sprungziel am Anfang der Seite
-  Link auf internes Sprungziel am Ende der Tabelle
-  Link zurück zur Startseite

Bestellformular (1/2)
---------------------

Verwenden Sie folgende URL als ``action`` Attribut am Formular:
``https://campus02.fladi.at/web/order?pkz=12345678``

-  Ersetzen Sie ``12345678`` durch ihre Personen-Kennzahl.
-  Sie müssen das Formular mit allen Feldern korrekt implementiert haben
   (Feld-Namen beachten!) damit eine Bestellung gespeichert wird.

Folgende Elemente sollen enthalten sein:

-  Link zurück zur Produktübersicht
-  Link zurück zur Startseite
