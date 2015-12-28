---
author: Dr. Xiaoshan Liu, DI Michael Fladischer
title: Web Grundlagen

---
# HTML

*HyperText Markup Language*

<a href="https://www.campus02.at/">
<div class="corner-ribbon top-right sticky yellow shadow">CAMPUS02</div>
</a>

---
## Agenda

 * Einführung
 * Entwicklung von HTML bis HTML5
 * HTML5 Grundlagen
 * Unterschiede HTML5
 * HTML5 Varianten
 * Ausgewählte HTML Elemente
 * Übungsbeispiele

---
# Was ist HTML?

## HTML ist das Dokumentformat des WWW

---
## HyperText Markup Language

 * *HyperText* … Verknüpfung von HTML Dokumenten durch Verweise (Hyperlinks)
 * *Markup* … Auszeichnung - Festlegung logischer Bestandteile
 * *Language* … Sprache mit definierter Syntax und Semantik

---
## Anwendung & Eigenschaften

* HTML dient der Strukturierung von Texten (Tags)
* Trennung von Aufbau (HTML) und Darstellung (CSS)
* Weiterentwicklung durch das [World Wide Web Consortium (W3C)](http://www.w3.org/)

---
## Text ohne Auszeichnung

<pre>
Leonato. I learn in this letter that Don Peter of Arragon comes this night to Messina.

Messenger. He is very near by this: he was not three leagues off when I left him.

Leonato. How many gentlemen have you lost in this action?

Messenger. But few of any sort, and none of name.
</pre>

---
## Text mit Auszeichnung

<strong>Leonato.</strong> I learn in this letter that <em>Don Peter</em> of
<em>Arragon</em> comes this night to <em>Messina</em>.

<strong>Messenger.</strong> He is very near by this: he was not three leagues off when I
left him.

<strong>Leonato.</strong> How many gentlemen have you lost in this action?

<strong>Messenger.</strong> But few of any sort, and none of name.

---
## Text mit Auszeichnung ohne Darstellung

&lt;strong&gt;Leonato.&lt;/strong&gt; I learn in this letter that
&lt;em&gt;Don Peter&lt;/em&gt; of &lt;em&gt;Arragon&lt;/em&gt; comes
this night to &lt;em&gt;Messina&lt;/em&gt;.

&lt;strong&gt;Messenger.&lt;/strong&gt; He is very near by this: he was not three leagues off when I
left him.

&lt;strong&gt;Leonato.&lt;/strong&gt; How many gentlemen have you lost in this action?

&lt;strong&gt;Messenger.&lt;/strong&gt; But few of any sort, and none of name.

---
## Auszeichnung

* Semantische Auszeichnung = Beschreibung von Text
* Festlegung der Art einer Textstelle über Markierungen

---
# Entwicklung von HTML

---
## HTML 1.0 (1989)

Erster Entwurf von Sir Tim Berners-Lee.

![Sir Tim Berners Lee](images/Sir_Tim_Berners-Lee.jpg)

<small>[Picture licensed CC BY-SA 4.0](https://commons.wikimedia.org/wiki/User:Paulrclarke)</small>

---
##  HTML 2.0 (1995)

Erster offizieller Sprachstandard für HTML ([RFC 1866](http://www.ietf.org/rfc/rfc1866.txt)).

Neuerungen:

* Formulare

---
## HTML 3.2 (1996)


Neuerungen:

* Tabellen
* Client-Side-Maps
* Einbindung von Java-Applets
* Attribute zur Text-/Bildausrichtung

---
## HTML 4.0 (1998)

Neuerungen:

* Stylesheets, Skripte und Frames
* Trennung in Strict, Frameset und Transitional

---
## HTML 4.01 (1999)

Erweiterungen und Korrekturen.


---
# XHTML

## Extensible HyperText Markup Language


---
## XHTML 1.0 (2000)

Neudefinition von HTML 4.01 in XML.

---
## XHTML 1.1 (2001)

Weitere Modularisierung sowie geringere Fehlertoleranz.

---
## HTML 5

* In "permanenter" Entwicklung
* Modularisierung; Sammelbegriff für verschiedene Technologien
* W3C Candidate Recommendation 6.8.2013

---
## Ein Beispiel (HTML 5)

    &lt;!DOCTYPE html&gt;
    &lt;html&gt;
      &lt;head&gt;
        &lt;meta charset="utf-8"&gt;
        &lt;title&gt;Ein erstes Beispiel&lt;/title&gt;
      &lt;/head&gt;
      &lt;body&gt;
        &lt;h1&gt;Hello World&lt;/h1&gt;
        &lt;p&gt;This is my first HTML file&lt;/p&gt;
      &lt;/body&gt;
    &lt;/html&gt;

---
# HTML-Syntax

---
## Elemente

* Konkrete Ausprägung eines Elementtyps
* Gekennzeichnet durch Tags (in spitzen Klammern `&lt;&gt;`)
* Einleitendes (öffnendes) Tag `&lt;elementname&gt;`
* Abschließendes (schließendes) Tag `&lt;/elementname&gt;`
* Elementinhalt [optional]: Text oder weitere Elemente

```
    &lt;p&gt;Hello World!&lt;/p&gt;
```

---
## Attribute

* Zusatz zur Beschreibung einer Eigenschaft
* Im Opening-Tag eines Elements notiert
* Name-Wert-Paar: `name="Wert"`

```
    &lt;a href="http://www.campus02.at/"&gt;FH CAMPUS02&lt;/a&gt;
```

---
## Text

* Ist immer von einem Element umgeben: `&lt;element&gt;text&lt;/element&gt;`
* Einige Zeichen müssen maskiert werden – Verwendung einer Zeichenreferenz (z.B.  &lt;, &gt;, ")

---
## Zeichenreferenzen / Entitäten

* Für Umlaute, Zeichen mit Bedeutung in HTML5
* Zur Vermeidung von Fehlinterpretationen

| **Sonderzeichen** |  **Entität** |  **Unicode** |
|:-----------------:|:------------:|:------------:|
|       &amp;       |  `&amp;amp;` |  `&amp;#38;` |
|        &lt;       |  `&amp;lt;`  |  `&amp;#60;` |
|        &gt;       |  `&amp;gt;`  |  `&amp;#62;` |
|       &quot;      | `&amp;quot;` |  `&amp;#34;` |
|       &auml;      | `&amp;auml;` | `&amp;#228;` |

Unicode-Zeichen können in der [Unicode-Zeichen-Tabelle](http://unicode-table.com/de/) nachgeschlagen werden.

---
# HTML5

HTML5 Spezifikation definiert 2 mögliche Serialisierungen

---

![Die zwei Serialisierungen von HTML5](figure/html5-abstract-language.svg)

---
## Unterschiede in der Serialisierung

| **HTML5**                              | **HTML5 (XML)**                                            |
|----------------------------------------|------------------------------------------------------------|
| `text/html`                            | `application/xhtml+xml`                                    |
| `&lt;html&gt;`                         | `&lt;html xmlns="http://www.w3.org/1999/xhtml"&gt;`        |
| `&lt;br&gt;`                           | `&lt;br/&gt;`                                              |
| `&lt;input disabled&gt;`               | `&lt;input disabled="disabled"/&gt;`                       |
| `&lt;input disabled=disabled&gt;`      | `&lt;input disabled="disabled"/&gt;`                       |
| `&lt;p&gt;1. Absatz&lt;p&gt;2. Absatz` | `&lt;p&gt;1. Absatz&lt;/p&gt;&lt;p&gt;2. Absatz&lt;/p&gt;` |

---
# Welche Inhalte einer Website kennen Sie?

---
## Ausgewählte HTML(5) Elemente

* Block und Inline-Elemente
* Listen
* Tabellen
* Links
* Bilder und Grafiken
* Formulare
* (Frames)
* Semantische Elemente (HTML5)
* Eingebettete Elemente

---
## Block-Elemente

* Erzeugen einen eigenen Absatz
* Unterschiedlicher Abstand je nach Element
* Können Text, Inline-Elemente und teilweise andere Block-Elemente enthalten

|           **Element**          |           **Bedeutung**          |
|:------------------------------:|:--------------------------------:|
|           `&lt;p&gt;`          |            Textabsatz            |
|  `&lt;h1&gt;` bis `&lt;h6&gt;` |   Überschrift 1. bis 6. Ordnung  |
|          `&lt;div&gt;`         |      allgemeine Gruppierung      |
|      `&lt;blockquote&gt;`      |            Zitatblock            |
|          `&lt;pre&gt;`         |       vorformatierter Text       |
| `&lt;ul&gt;` bzw. `&lt;ol&gt;` | unsortierte bzw. sortierte Liste |

---
## Block-Elemente (HTML5)

|    **Element**    |         **Bedeutung**         |
|:-----------------:|:-----------------------------:|
| `&lt;article&gt;` |     Inhalt eines Artikels     |
|  `&lt;canvas&gt;` | Fläche für Zeichenoperationen |
|  `&lt;header&gt;` |     Kopfzeile einer Seite     |
|  `&lt;footer&gt;` |      Fußzeile einer Seite     |
| `&lt;section&gt;` |     Abschnitt einer Seite     |
|  `&lt;video&gt;`  |         Video-Anzeige         |

---
## Inline-Elemente

* Erzeugen KEINEN Zeilenumbruch
* Als untergeordnete Elemente für Block-Elemente gedacht
* Können Text oder weitere Inline-Elemente enthalten

|    **Element**   |                           **Bedeutung**                           |
|:----------------:|:-----------------------------------------------------------------:|
| `&lt;strong&gt;` |               betonter Text (wird fett dargestellt)               |
|    `&lt;b&gt;`   |                            fetter Text                            |
|  `&lt;span&gt;`  | zur Gruppierung bzw. Auszeichnung von Inline-Elementen und Texten |
|  `&lt;code&gt;`  |                             Quellcode                             |

---
## Listen

Zählen zu den Block-Elementen und werden für drei Listentypen definiert:

* Ungeordnete Listen (Bullet als Aufzählungszeichen)
* Geordnete Listen (Nummerierung)
* Definitionslisten (Bezeichnung und Beschreibung)

---
## Ungeordnete Liste

<ul>
  <li>Eintrag</li>
  <li>Eintrag</li>
  <li>Eintrag</li>
</ul>

    &lt;ul&gt;
      &lt;li&gt;Eintrag&lt;/li&gt;
      &lt;li&gt;Eintrag&lt;/li&gt;
      &lt;li&gt;Eintrag&lt;/li&gt;
    &lt;/ul&gt;

---
## Geordnete Liste

<ol>
  <li>Erster Eintrag</li>
  <li>Zweiter Eintrag</li>
  <li>Dritter Eintrag</li>
</ol>

    &lt;ol&gt;
      &lt;li&gt;Erster Eintrag&lt;/li&gt;
      &lt;li&gt;Zweiter Eintrag&lt;/li&gt;
      &lt;li&gt;Dritter Eintrag&lt;/li&gt;
    &lt;/ol&gt;

---
## Definitionsliste

<dl>
  <dt>Bezeichnung 1. Eintrag</dt>
  <dd>Beschreibung zu erstem Eintrag.</dd>
  <dt>Bezeichnung 2. Eintrag</dt>
  <dd>Beschreibung zu zweitem Eintrag.</dd>
</dl>

    &lt;dl&gt;
      &lt;dt&gt;Bezeichnung 1. Eintrag&lt;/dt&gt;
      &lt;dd&gt;Beschreibung zu erstem Eintrag.&lt;/dd&gt;
      &lt;dt&gt;Bezeichnung 2. Eintrag&lt;/dt&gt;
      &lt;dd&gt;Beschreibung zu zweitem Eintrag.&lt;/dd&gt;
    &lt;/dl&gt;

---
## Tabellen

Sind Block-Elemente.

<table class="demo">
  <tr>
    <th>Spalte 1</th>
    <th>Spalte 2</th>
  </tr>
  <tr>
    <td>Zeile 1, Spalte 1</td>
    <td>Zeile 1, Spalte 2</td>
  </tr>
  <tr>
    <td>Zeile 2, Spalte 1</td>
    <td>Zeile 2, Spalte 2</td>
  </tr>
</table>

    &lt;table&gt;
      &lt;tr&gt;
        &lt;th&gt;Spalte 1&lt;/th&gt;
        &lt;th&gt;Spalte 2&lt;/th&gt;
      &lt;/tr&gt;
      &lt;tr&gt;
        &lt;td&gt;Zeile 1, Spalte 1&lt;/td&gt;
        &lt;td&gt;Zeile 1, Spalte 2&lt;/td&gt;
      &lt;/tr&gt;
      &lt;tr&gt;
        &lt;td&gt;Zeile 2, Spalte 1&lt;/td&gt;
        &lt;td&gt;Zeile 2, Spalte 2&lt;/td&gt;
      &lt;/tr&gt;
    &lt;/table&gt;

---
## Links

* Sind Inline-Elemente
* Links zu anderen Dokumenten:

    ```
    &lt;a href="http://www.campus02.at/index.asp?menuId=5"&gt;
      sichtbarer Linktext
    &lt;/a&gt;
    ```

* Sprungziel in einem Dokument:

    ```
    &lt;a name="ankername"&gt;Sprungziel-Text&lt;/a&gt;
    &lt;h1 id="ankername"&gt;Sprungziel-Text&lt;/h1&gt;
    ```

* Link zu einem Sprungziel im gleichen Dokument:

    ```
    &lt;a href="#ankername"&gt;sichtbarer Linktext&lt;/a&gt;
    ```

* Link zu einem Sprungziel in einem anderen Dokument:

    ```
    &lt;a href="http://www.campus02.at/index.asp#ankername"&gt;
      sichtbarer Linktext
    &lt;/a&gt;
    ```

---
# Exkurs: Verlinkung

* absolute URIs
* relative URIs
* absolute Pfade
* relative Pfade

---
## Absolute URIs

Die einfachste, aber auch am wenigsten flexibel anwendbare Variante. Sie geben
den Ort der Resource absolut an ohne die aktuelle URI zu berücksichtigen.

* `http://www.example.org/`
* `http://www.example.org/index.htm`
* `http://www.example.org/index.htm#toc`
* `https://www.example.org/cgi-bin/suche.cgi?ausdruck=Lorem`
* `ftp://www.example.org/documents/invoice.pdf`
* `http://www.example.org:8082/backend/admin.html`

---
## Relative URIs

Ermöglichen das Auffinden von Resouren, abhängig vom aktuell verwendeten Schema
(`http` oder `https`).

* `//static.example.org/jquery.js`
* `//www.example.org/style.css`

---
## Absolute Pfade

Referenzieren Resource absolut auf einer Authority (siehe URLs). Pfade beginnen
an der **Document-Root** des Webservers.

* `/`
* `/index.htm`
* `/index.htm#toc`
* `/cgi-bin/suche.cgi?ausdruck=Lorem`
* `/documents/invoice.pdf`
* `/backend/admin.html`

---
## Relative Pfade

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

---
# Zurück zu HTML

---
## Bilder

* Inline-Elemente
* Elemente ohne eigenen Inhalt

<img src="images/cat.jpg" width="800" height="600" alt="Turkish Angora Cat">

    &lt;img src="images/cat.jpg"
      width="800"
      height="600"
      alt="Turkish Angora Cat"&gt;

---
## Formulare

* Block-Elemente
* Definition des Formularbereiches mit **`&lt;form&gt;`**
* Pflichtattribut **`action`** definiert die Zieladresse der Daten
* Attribut **`method`** bestimmt wie die Daten übertragen werden **`(method="post | get")`**
* Interaktion mit dem Benutzer über Formularelemente

```
&lt;form action="/blog/article/save" method="post"&gt;
  ...
&lt;/form&gt;
```

---
## Formularelemente

Formulare können verschiedene Arten von Elementen zur Eingabe von daten
beinhalten. Jedes dieser Elemente muss über ein Attribut mit dem Namen
**`name`** verfügen, welches den Namen des Eingabelements definiert.

```
&lt;element name="vorname" /&gt;
```

---
## Eingabefelder, Radio-Buttons, Checkboxen, …

<input type="text" value="Hier Text eingeben ...">
<input type="checkbox" checked="checked">
<input type="radio" checked="checked">

```
&lt;input type="..." name="..." /&gt;
```

Attribut **`type`**: `text` | `password` | `radio` | `checkbox` | …

---
## Auswahlfelder

<select>
  <option>Bitte auswählen ...</option>
</select>

```
&lt;select name="..."&gt;
  &lt;option&gt;Wert 1&lt;/option&gt;
  &lt;option&gt;Wert 2&lt;/option&gt;
  &lt;option&gt;Wert 3&lt;/option&gt;
&lt;/select&gt;
```

Option in einem Auswahlfeld &lt;option&gt;

---
## Textfelder

<textarea cols="50" rows="10 cols="50" rows="10"">
Hier kann mehrzeiliger Text eingegeben werden ...
Dies ist die zweite Zeile ...
</textarea>

```
&lt;textarea name="..."&gt;
... Text...
... mehrzeilig ...
&lt/textarea&gt;
```

---
## Buttons

Kein `name` Attribut nötig, da meist keine Daten direkt am Button eingegeben werden.

<button>Button mit Text</button>
<input type="submit" value="Input-Submit mit Text">

```
&lt;button type="button | submit | reset"&gt;
&lt;input type="submit | reset"&gt;
```

---
## Frames

* Definition eines Framesets mittels **`&lt;frameset&gt;`**. Die Attribute **`cols`**
  und **`rows`** definieren die Spalten und Zeilen.
* Definition eines einzelen Frames mittels **`&lt;frame&gt;`**. Das Attribut **`src`**
  legt den URL zum Inhalte des Frames fest.
* Framesets können ineinander geschachtelt werden.
* Veraltet und haben Probleme (Bookmarks, Ausdrucke, neu laden, vor/zurück).

```
&lt;frameset cols="50%,50%"&gt;
  &lt;frame src="page.html" /&gt;
  &lt;frame src="http://example.com/main.html" /&gt;
&lt;/frameset&gt;
```

---
## Eingebettete Frames

Betten den Inhalt einer URL in einer Seite ein.

<iframe src="https://www.campus02.at/" class="embedded-website"></iframe>

```
&lt;iframe src="https://www.campus02.at/"&gt;&lt;/iframe&gt;
```

---
## Videos

<video width="640" height="360" autoplay="autoplay" loop="loop" muted="muted">
  <source src="video/bunny.mp4" type="video/mp4"/>
  <source src="video/bunny.webm" type="video/webm"/>
  <source src="video/bunny.ogv" type="video/ogg"/>
</video>

```
&lt;video width="640" height="360"
  muted="muted" autoplay="autoplay" loop="loop"&gt;
  &lt;source src="video/bunny.mp4" type="video/mp4"/&gt;
  &lt;source src="video/bunny.webm" type="video/webm"/&gt;
  &lt;source src="video/bunny.ogv" type="video/ogg"/&gt;
&lt;/video&gt;
```

[Demo-Videos](http://www.sample-videos.com/) zum Download.

---
## Audio

```
&lt;audio controls="controls"&gt;
  &lt;source src="foo.wav" type="audio/wav"&gt;
&lt;/audio&gt;
```

---
## Externe Plugins

* Flash
* Java Applets
* Silverlight
* ActiveX
* ...

```
&lt;object width="40" height="50" data="flash.swf"&gt;&lt;/object&gt;
```

---
# Übung

Wir erstellen gemeinsam eine Trouble-Ticket-Website, bestehend aus drei
HTML-Dokumenten:

* Einer Tabelle mit allen offenen Tickets (`tabelle.html`)
* Mindestens einer Detail-Seite zu einem Ticket (`2.html`)
* Einem Formular für neue Tickets (`formular.html`)

---
## Die Tabelle

`tabelle.html`

<iframe src="tabelle.html" class="embedded-website"></iframe>

---
## Die Detail-Seite

`2.html`

<iframe src="2.html" class="embedded-website"></iframe>

---
## Das Formular

`formular.html`

<iframe src="formular.html" class="embedded-website"></iframe>

POST-Request sollen vom Formular an die
[Demo-Anwendung](https://campus02.fladi.at/web/form-data) geschickt werden.

---
# Referenzen

* [HTML 4.01](http://www.w3.org/TR/html401/)
* [XHTML 1.0](http://www.w3.org/TR/xhtml1/)
* [HTML5](http://www.w3.org/TR/html5/)
* [SELFHTML](http://de.selfhtml.org/)
* [HTML Tutorial](http://www.w3schools.com/html/default.asp)

---
# Einzelarbeit

Erstellen Sie eine Website für einen Tee-Shop mit diesen Seiten:

* Startseite
* Produktübersicht
* Mehrere Detail-Seiten
* Bestellformular

Daten zu den Tee-Sorten finden Sie auf [Moodle](https://moodle.campus02.at/).

---
## Startseite

* Name des Shops
* Logo als Vektor-Grafik
* Begrüßungstext
* Ein Zitat (vielleicht zum Theme Tee?)
* Links zu Produktübersicht und Bestellformular

---
## Produktübersicht

* Tabelle der Tee-Sorten mit Name, Art, Abbild, Herkunft, Brühzeit und Preis/100g (min. 5 Tee-Sorten)
* Verlinkung jeder Teesorte auf eine Detail-Seite
* Internes Sprungziel am Anfang der Seite
* Link auf internes Sprungziel am Ende der Tabelle
* Link zurück zur Startseite

---
## Detail-Seiten

Für jede Tee-Sorte aus der Tabelle soll ein eigenes HTML-Dokument erstellt
werden, das neben den Daten aus der Tabellenzeile auch eine Produktvorschau in
Form von einer Abbilung enthält.

Die Bilder dazu finden Sie in der Datei auf [Moodle](https://moodle.campus02.at/).

Folgende Elemente sollen noch enthalten sein:

* Link zurück zur Produktübersicht
* Link zurück zur Startseite

---
## Bestellformular (1/2)

Verwenden Sie folgende URL als `action` Attribut am Formular:
`https://campus02.fladi.at/web/order?pkz=12345678`

* Ersetzen Sie `12345678` durch ihre Personen-Kennzahl.
* Sie müssen das Formular mit allen Feldern korrekt implementiert haben (Feld-Namen beachten!) damit eine Bestellung gespeichert wird.

Folgende Elemente sollen enthalten sein:

* Link zurück zur Produktübersicht
* Link zurück zur Startseite

---
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

---

