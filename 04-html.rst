:data-transition-duration: 2000
:skip-help: true
:css: css/campus02.css

.. role:: html(code)
  :language: html

.. _World Wide Web Consortium (W3C): http://www.w3.org/
.. _RFC 1866: http://www.ietf.org/rfc/rfc1866.txt
.. _Unicode-Zeichen-Tabelle: http://unicode-table.com/de/
.. _Demo-Videos: http://www.sample-videos.com/
.. _Demo-Anwendung: https://campus02.fladi.at/web/form-data

.. title: HyperText Markup Language

----

HTML
====

*HyperText Markup Language*

.. raw:: html

  <div class="corner-ribbon top-right sticky yellow shadow">CAMPUS02</div>

----

Agenda
------

 * Einführung
 * Entwicklung von HTML bis HTML5
 * HTML5 Grundlagen
 * Unterschiede HTML5
 * HTML5 Varianten
 * Ausgewählte HTML Elemente
 * Übungsbeispiele

----

Was ist HTML?
=============

HTML ist das Dokumentformat des WWW

----

Anwendung & Eigenschaften
-------------------------

-  HTML dient der Strukturierung von Texten (Tags)
-  Trennung von Aufbau (HTML) und Darstellung (CSS)
-  Weiterentwicklung durch das `World Wide Web Consortium (W3C)`_

----

Text ohne Auszeichnung
----------------------

Leonato. I learn in this letter that Don Peter of Arragon comes this night to Messina.
Messenger. He is very near by this: he was not three leagues off when I left him.
Leonato. How many gentlemen have you lost in this action?
Messenger. But few of any sort, and none of name.

----

Text mit Auszeichnung
---------------------

.. raw:: html

  <p>
  <strong>Leonato.</strong> I learn in this letter that <em>Don Peter</em> of
  <em>Arragon</em> comes this night to <em>Messina</em>.
  </p>

  <p>
  <strong>Messenger.</strong> He is very near by this: he was not three leagues off when I
  left him.
  </p>

  <p>
  <strong>Leonato.</strong> How many gentlemen have you lost in this action?
  </p>

  <p>
  <strong>Messenger.</strong> But few of any sort, and none of name.
  </p>

----

Text mit Auszeichnung ohne Darstellung
--------------------------------------

.. code:: html

  <p>
  <strong>Leonato.</strong> I learn in this letter that <em>Don Peter</em> of <em>Arragon</em> comes this night to <em>Messina</em>.
  </p>

  <p>
  <strong>Messenger.</strong> He is very near by this: he was not three leagues off when I left him.
  </p>

  <p>
  <strong>Leonato.</strong> How many gentlemen have you lost in this action?
  </p>

  <p>
  <strong>Messenger.</strong> But few of any sort, and none of name.
  </p>

----

Auszeichnung
------------

* Semantische Auszeichnung = Beschreibung von Text
* Festlegung der Art einer Textstelle über Markierungen

----

Entwicklung von HTML
====================

Von HTML 1.0 bis 5

----

HTML 1.0 (1989)
---------------

Erster Entwurf von Sir Tim Berners-Lee.

.. image:: images/Sir_Tim_Berners-Lee.jpg
  :alt: Sir Tim Berners Lee (Picture licensed CC BY-SA 4.0)
  :target: https://commons.wikimedia.org/wiki/User:Paulrclarke

----

HTML 2.0 (1995)
---------------

Erster offizieller Sprachstandard für HTML (`RFC 1866`_).

Neuerungen:

* Formulare

----

HTML 3.2 (1996)
---------------


Neuerungen:

* Tabellen
* Client-Side-Maps
* Einbindung von Java-Applets
* Attribute zur Text-/Bildausrichtung

----

HTML 4.0 (1998)
---------------

Neuerungen:

* Stylesheets, Skripte und Frames
* Trennung in Strict, Frameset und Transitional

----

HTML 4.01 (1999)
----------------

Erweiterungen und Korrekturen.

----

XHTML
=====

Extensible HyperText Markup Language

----

XHTML 1.0 (2000)
----------------

Neudefinition von HTML 4.01 in XML.

----

XHTML 1.1 (2001)
----------------

Weitere Modularisierung sowie geringere Fehlertoleranz.

----

HTML 5
------

* In "permanenter" Entwicklung
* Modularisierung; Sammelbegriff für verschiedene Technologien
* W3C Candidate Recommendation 6.8.2013

----

Ein Beispiel (HTML 5)
---------------------

.. code:: html

  <!DOCTYPE html>
  <html>
    <head>
      <meta charset="utf-8">
      <title>Ein erstes Beispiel</title>
    </head>
    <body>
      <h1>Hello World</h1>
      <p>This is my first HTML file</p>
    </body>
  </html>

----

HTML-Syntax
===========

* Wie wird HTML in einem Dokument verwendet?
* Welchen Regeln unterliegt es?

----

Elemente
--------

* Konkrete Ausprägung eines Elementtyps
* Gekennzeichnet durch Tags (in spitzen Klammern :html:`<>`)
* Einleitendes (öffnendes) Tag :html:`<elementname>`
* Abschließendes (schließendes) Tag :html:`</elementname>`
* Elementinhalt [optional]: Text oder weitere Elemente

.. code:: html

  <p>Hello World!</p>

----

Attribute
---------

* Zusatz zur Beschreibung einer Eigenschaft
* Im Opening-Tag eines Elements notiert
* Name-Wert-Paar: `name="Wert"`

.. code:: html

  <a href="http://www.campus02.at/">FH CAMPUS02</a>

----

Text
----

* Ist immer von einem Element umgeben: :html:`<element>text</element>`
* Einige Zeichen müssen maskiert werden – Verwendung einer Zeichenreferenz (z.B.  `<`, `>`, `"`)

----

Zeichenreferenzen / Entitäten
-----------------------------

* Für Umlaute, Zeichen mit Bedeutung in HTML5
* Zur Vermeidung von Fehlinterpretationen

+---------------+-----------+------------+
| Sonderzeichen | Entität   | Unicode    |
+===============+===========+============+
| &             | `&amp;`   | `&#38;`    |
+---------------+-----------+------------+
| <             | `&lt;`    | `&#60;`    |
+---------------+-----------+------------+
| >             | `&gt;`    | `&#62;`    |
+---------------+-----------+------------+
| "             | `&quot;`  | `&#34;`    |
+---------------+-----------+------------+
| ä             | `&auml;`  | `&#228;`   |
+---------------+-----------+------------+

Unicode-Zeichen können in der `Unicode-Zeichen-Tabelle`_ nachgeschlagen werden.

----

HTML5
=====

HTML5 Spezifikation definiert 2 mögliche Serialisierungen

----

.. image :: figures/html5-abstract-language.svg
  :alt: Die zwei Serialisierungen von HTML5

----

Unterschiede in der Serialisierung
----------------------------------

+-----------------------------+-----------------------------------------------+
| HTML5                       | HTML5 (XML)                                   |
+=============================+===============================================+
| `text/html`                 | `application/xhtml+xml`                       |
+-----------------------------+-----------------------------------------------+
| `<html>`                    | `<html xmlns="http://www.w3.org/1999/xhtml">` |
+-----------------------------+-----------------------------------------------+
| `<br>`                      | `<br/>`                                       |
+-----------------------------+-----------------------------------------------+
| `<input disabled>`          | `<input disabled="disabled"/>`                |
+-----------------------------+-----------------------------------------------+
| `<input disabled=disabled>` | `<input disabled="disabled"/>`                |
+-----------------------------+-----------------------------------------------+
| `<p>1. Absatz<p>2. Absatz`  | `<p>1. Absatz</p><p>2. Absatz</p>`            |
+-----------------------------+-----------------------------------------------+

----

Welche Inhalte einer Website kennen Sie?
========================================

Denken Sie an einzelne Komponenten die sich auf verschiedenen Websites wiederholen.

----

Ausgewählte HTML(5) Elemente
----------------------------

* Block und Inline-Elemente
* Listen
* Tabellen
* Links
* Bilder und Grafiken
* Formulare
* (Frames)
* Semantische Elemente (HTML5)
* Eingebettete Elemente

----

Block-Elemente
--------------

* Erzeugen einen eigenen Absatz
* Unterschiedlicher Abstand je nach Element
* Können Text, Inline-Elemente und teilweise andere Block-Elemente enthalten

+-------------------+---------------------------------+
| Element           | Bedeutung                       |
+===================+=================================+
| `<p>`             | Textabsatz                      |
+-------------------+---------------------------------+
| `<h1>` bis `<h6>` | Überschrift 1. bis 6. Ordnung   |
+-------------------+---------------------------------+
| `<div>`           | allgemeine Gruppierung          |
+-------------------+---------------------------------+
| `<blockquote>`    | Zitatblock                      |
+-------------------+---------------------------------+
| `<pre>`           | vorformatierter Text            |
+-------------------+---------------------------------+
| `<ul>` und `<ol>` | unsortierte und sortierte Liste |
+-------------------+---------------------------------+

----

Block-Elemente (HTML5)
----------------------

+-------------+-------------------------------+
| Element     | Bedeutung                     |
+=============+===============================+
| `<article>` | Inhalt eines Artikels         |
+-------------+-------------------------------+
| `<canvas>`  | Fläche für Zeichenoperationen |
+-------------+-------------------------------+
| `<header>`  | Kopfzeile einer Seite         |
+-------------+-------------------------------+
| `<footer>`  | Fußzeile einer Seite          |
+-------------+-------------------------------+
| `<section>` | Abschnitt einer Seite         |
+-------------+-------------------------------+
| `<video>`   | Video-Anzeige                 |
+-------------+-------------------------------+

----

Inline-Elemente
---------------

* Erzeugen KEINEN Zeilenumbruch
* Als untergeordnete Elemente für Block-Elemente gedacht
* Können Text oder weitere Inline-Elemente enthalten

+------------+-------------------------------------------------------------------+
| Element    | Bedeutung                                                         |
+============+===================================================================+
| `<strong>` | betonter Text (wird fett dargestellt)                             |
+------------+-------------------------------------------------------------------+
| `<b>`      | fetter Text                                                       |
+------------+-------------------------------------------------------------------+
| `<span>`   | zur Gruppierung bzw. Auszeichnung von Inline-Elementen und Texten |
+------------+-------------------------------------------------------------------+
| `<code>`   | Quellcode                                                         |
+------------+-------------------------------------------------------------------+

----

Listen
------

Zählen zu den Block-Elementen und werden für drei Listentypen definiert:

* Ungeordnete Listen (Bullet als Aufzählungszeichen)
* Geordnete Listen (Nummerierung)
* Definitionslisten (Bezeichnung und Beschreibung)

----

Ungeordnete Liste
-----------------

.. raw:: html

  <ul>
    <li>Eintrag</li>
    <li>Eintrag</li>
    <li>Eintrag</li>
  </ul>

.. code:: html

  <ul>
    <li>Eintrag</li>
    <li>Eintrag</li>
    <li>Eintrag</li>
  </ul>

----

Geordnete Liste
---------------

.. raw:: html

  <ol>
    <li>Erster Eintrag</li>
    <li>Zweiter Eintrag</li>
    <li>Dritter Eintrag</li>
  </ol>

.. code:: html

  <ol>
    <li>Erster Eintrag</li>
    <li>Zweiter Eintrag</li>
    <li>Dritter Eintrag</li>
  </ol>

----

Definitionsliste
----------------

.. raw:: html

  <dl>
    <dt>Bezeichnung 1. Eintrag</dt>
    <dd>Beschreibung zu erstem Eintrag.</dd>
    <dt>Bezeichnung 2. Eintrag</dt>
    <dd>Beschreibung zu zweitem Eintrag.</dd>
  </dl>

.. code:: html

  <dl>
    <dt>Bezeichnung 1. Eintrag</dt>
    <dd>Beschreibung zu erstem Eintrag.</dd>
    <dt>Bezeichnung 2. Eintrag</dt>
    <dd>Beschreibung zu zweitem Eintrag.</dd>
  </dl>

----

Tabellen
--------

Sind Block-Elemente.

.. raw:: html

  <table>
    <thead>
      <tr>
        <th>Header 1</th>
        <th>Header 2</th>
      </tr>
    </thead>
    <tbody>
      <tr>
        <td>Zeile 1, Spalte 1</td>
        <td>Zeile 1, Spalte 2</td>
      </tr>
      <tr>
        <td>Zeile 2, Spalte 1</td>
        <td>Zeile 2, Spalte 2</td>
      </tr>
    </tbody>
  </table>

----

Tabellen
--------

.. code:: html

  <table>
    <thead>
      <tr>
        <th>Header 1</th>
        <th>Header 2</th>
      </tr>
    </thead>
    <tbody>
      <tr>
        <td>Zeile 1, Spalte 1</td>
        <td>Zeile 1, Spalte 2</td>
      </tr>
      <tr>
        <td>Zeile 2, Spalte 1</td>
        <td>Zeile 2, Spalte 2</td>
      </tr>
    </tbody>
  </table>

----

Links
-----

* Sind Inline-Elemente
* Links zu anderen Dokumenten:

.. code:: html

  <a href="http://www.campus02.at/index.asp?menuId=5">
    sichtbarer Linktext
  </a>

* Sprungziel in einem Dokument:

.. code:: html

    <a name="ankername">Sprungziel-Text</a>
    <h1 id="ankername">Sprungziel-Text</h1>

* Link zu einem Sprungziel im gleichen Dokument:

.. code:: html

    <a href="#ankername">sichtbarer Linktext</a>

* Link zu einem Sprungziel in einem anderen Dokument:

.. code:: html

    <a href="http://www.campus02.at/index.asp#ankername">
      sichtbarer Linktext
    </a>

----

Exkurs: Verlinkung
==================

* absolute URLs
* relative URLs
* absolute Pfade
* relative Pfade

----

Absolute URLs
-------------

Die einfachste, aber auch am wenigsten flexibel anwendbare Variante. Sie geben
den Ort der Resource absolut an ohne die aktuelle URI zu berücksichtigen.

* `http://www.example.org/`
* `http://www.example.org/index.htm`
* `http://www.example.org/index.htm#toc`
* `https://www.example.org/cgi-bin/suche.cgi?ausdruck=Lorem`
* `ftp://www.example.org/documents/invoice.pdf`
* `http://www.example.org:8082/backend/admin.html`

----

Relative URLs
-------------

Ermöglichen das Auffinden von Resouren, abhängig vom aktuell verwendeten Schema
(`http` oder `https`).

* `//static.example.org/jquery.js`
* `//www.example.org/style.css`

----

Absolute Pfade
--------------

Referenzieren Resource absolut auf einer Authority (siehe URLs). Pfade beginnen
an der **Document-Root** des Webservers.

* `/`
* `/index.htm`
* `/index.htm#toc`
* `/cgi-bin/suche.cgi?ausdruck=Lorem`
* `/documents/invoice.pdf`
* `/backend/admin.html`

----

Relative Pfade
--------------

Verweisen auf Resource, relativ zur aktuellen Resource. Dadurch sind auch
Verzeichniswechsel möglich. Auch werden Verlinkungen zu anderen Dokumenten
unabhängig somit unabhängig von der Position innerhalb der **Document-Root**.

* `./`
* `farben.htm`
* `./farben.htm`
* `bilder/grafik.gif`
* `./bilder/grafik.gif`
* `../`
* `../../../../woanders/datei.htm`

----

Zurück zu HTML

----

Bilder
------

* Inline-Elemente
* Elemente ohne eigenen Inhalt

.. raw:: html

  <img src="images/cat.jpg" width="800" height="600" alt="Turkish Angora Cat">

.. code:: html

  <img src="images/cat.jpg"
    width="800"
    height="600"
    alt="Turkish Angora Cat">

----

Formulare
---------

* Block-Elemente
* Definition des Formularbereiches mit **`<form>`**
* Pflichtattribut **`action`** definiert die Zieladresse der Daten
* Attribut **`method`** bestimmt wie die Daten übertragen werden **`(method="post | get")`**
* Interaktion mit dem Benutzer über Formularelemente

.. code:: html

  <form action="/blog/article/save" method="post">
    ...
  </form>

----

Formularelemente
----------------

Formulare können verschiedene Arten von Elementen zur Eingabe von daten
beinhalten. Jedes dieser Elemente muss über ein Attribut mit dem Namen
**`name`** verfügen, welches den Namen des Eingabelements definiert.

.. code:: html

  <element name="vorname" />

----

Eingabefelder, Radio-Buttons, Checkboxen, …
-------------------------------------------

.. raw:: html

  <input type="text" value="Hier Text eingeben ...">
  <input type="checkbox" checked="checked">
  <input type="radio" checked="checked">

.. code:: html

  <input type="..." name="..." />

Attribut **`type`**: `text` | `password` | `radio` | `checkbox` | …

----

## Auswahlfelder

.. raw:: html

  <select>
    <option>Bitte auswählen ...</option>
  </select>

.. code:: html

  <select name="...">
    <option>Wert 1</option>
    <option>Wert 2</option>
    <option>Wert 3</option>
  </select>

Option in einem Auswahlfeld :html:`<option>`

----

Textfelder
----------

.. raw:: html

  <textarea cols="50" rows="10 cols="50" rows="10"">
  Hier kann mehrzeiliger Text eingegeben werden ...
  Dies ist die zweite Zeile ...
  </textarea>

.. code:: html

  <textarea name="...">
  ... Text...
  ... mehrzeilig ...
  </textarea>

----

Buttons
-------

Kein `name` Attribut nötig, da meist keine Daten direkt am Button eingegeben werden.

.. raw:: html

  <button>Button mit Text</button>
  <input type="submit" value="Input-Submit mit Text">

.. code:: html

  <button type="button | submit | reset">
  <input type="submit | reset">

----

Frames
------

* Definition eines Framesets mittels **`<frameset>`**. Die Attribute **`cols`**
  und **`rows`** definieren die Spalten und Zeilen.
* Definition eines einzelen Frames mittels **`<frame>`**. Das Attribut **`src`**
  legt den URL zum Inhalte des Frames fest.
* Framesets können ineinander geschachtelt werden.
* Veraltet und haben Probleme (Bookmarks, Ausdrucke, neu laden, vor/zurück).

.. code:: html

  <frameset cols="50%,50%">
    <frame src="page.html" />
    <frame src="http://example.com/main.html" />
  </frameset>

----

Eingebettete Frames
-------------------

Betten den Inhalt einer URL in einer Seite ein.

.. raw:: html

  <iframe src="https://www.campus02.at/" class="embedded-website"></iframe>

.. code:: html

  <iframe src="https://www.campus02.at/"></iframe>

----

Videos
------

.. raw:: html

  <video width="640" height="360" autoplay="autoplay" loop="loop" muted="muted">
    <source src="videos/bunny.mp4" type="video/mp4"/>
    <source src="videos/bunny.webm" type="video/webm"/>
    <source src="videos/bunny.ogv" type="video/ogg"/>
  </video>

.. code:: html

  <video width="640" height="360" muted="muted" autoplay="autoplay" loop="loop">
    <source src="videos/bunny.mp4" type="video/mp4"/>
    <source src="videos/bunny.webm" type="video/webm"/>
    <source src="videos/bunny.ogv" type="video/ogg"/>
  </video>

`Demo-Videos`_ zum Download.

----

Audio
-----

.. code:: html

  <audio controls="controls">
    <source src="foo.wav" type="audio/wav">
  </audio>

----

Externe Plugins
---------------

* Flash
* Java Applets
* Silverlight
* ActiveX
* ...

.. code:: html

  <object width="40" height="50" data="flash.swf"></object>

----

Übung
=====

Wir erstellen gemeinsam eine Trouble-Ticket-Website, bestehend aus drei
HTML-Dokumenten:

* Einer Tabelle mit allen offenen Tickets (`tabelle.html`)
* Mindestens einer Detail-Seite zu einem Ticket (`2.html`)
* Einem Formular für neue Tickets (`formular.html`)

----

Die Tabelle
-----------

`tabelle.html`

.. raw:: html

  <iframe src="examples/tabelle.html" class="embedded-website"></iframe>

----

## Die Detail-Seite

`2.html`

.. raw:: html

  <iframe src="examples/2.html" class="embedded-website"></iframe>

----

## Das Formular

`formular.html`

.. raw:: html

  <iframe src="examples/formular.html" class="embedded-website"></iframe>

POST-Request sollen vom Formular an die `Demo-Anwendung`_ geschickt werden.

----

Referenzen
==========

* [HTML 4.01](http://www.w3.org/TR/html401/)
* [XHTML 1.0](http://www.w3.org/TR/xhtml1/)
* [HTML5](http://www.w3.org/TR/html5/)
* [SELFHTML](http://de.selfhtml.org/)
* [HTML Tutorial](http://www.w3schools.com/html/default.asp)

----

# Einzelarbeit

Erstellen Sie eine Website für einen Tee-Shop mit diesen Seiten:

* Startseite
* Produktübersicht
* Mehrere Detail-Seiten
* Bestellformular

Daten zu den Tee-Sorten finden Sie auf [Moodle](https://moodle.campus02.at/).

----

## Startseite

* Name des Shops
* Logo als Vektor-Grafik
* Begrüßungstext
* Ein Zitat (vielleicht zum Theme Tee?)
* Links zu Produktübersicht und Bestellformular

----

## Produktübersicht

* Tabelle der Tee-Sorten mit Name, Art, Abbild, Herkunft, Brühzeit und Preis/100g (min. 5 Tee-Sorten)
* Verlinkung jeder Teesorte auf eine Detail-Seite
* Internes Sprungziel am Anfang der Seite
* Link auf internes Sprungziel am Ende der Tabelle
* Link zurück zur Startseite

----

## Detail-Seiten

Für jede Tee-Sorte aus der Tabelle soll ein eigenes HTML-Dokument erstellt
werden, das neben den Daten aus der Tabellenzeile auch eine Produktvorschau in
Form von einer Abbilung enthält.

Die Bilder dazu finden Sie in der Datei auf [Moodle](https://moodle.campus02.at/).

Folgende Elemente sollen noch enthalten sein:

* Link zurück zur Produktübersicht
* Link zurück zur Startseite

----

## Bestellformular (1/2)

Verwenden Sie folgende URL als `action` Attribut am Formular:
`https://campus02.fladi.at/web/order?pkz=12345678`

* Ersetzen Sie `12345678` durch ihre Personen-Kennzahl.
* Sie müssen das Formular mit allen Feldern korrekt implementiert haben (Feld-Namen beachten!) damit eine Bestellung gespeichert wird.

Folgende Elemente sollen enthalten sein:

* Link zurück zur Produktübersicht
* Link zurück zur Startseite

----

## Bestellformular (2/2)

Folgende Felder sollen enthalten sein:

* Vorname [`first_name`]
* Nachname [`last_name`]
* Adresse [`address`]
* PLZ [`zip_code`]
* Ort [`city`]
* Email [`email`]
* Produktauswahl als Dropdown [`product`]
* Menge als Dropdown [`amount`]
* Auswahl aus 3 Versandoptionen als Radio-Button [`delivery`]
* Bestätigung Geschenkoption als Checkbox [`gift`]
* Dateiupload für Bilder als Motiv auf Verpackung [`image`]
* Mehrzeiliges Textfeld für Anmerkungen [`comment`]
* Bestell-Button zum Absenden

Die Namen in **[]** sind für die `name` Attribute der Formular-Felder zu verwenden.

