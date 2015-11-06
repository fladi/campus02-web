---

author: Dr. Xiaoshan Liu, DI Michael Fladischer
title: Web Grundlagen

---

# HTML

*HyperText Markup Language*

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
## Eingabefelder, Radio-Buttons, Checkboxen, …

<input type="text" value="Hier Text eingeben ...">
<input type="checkbox" checked="checked">
<input type="radio" checked="checked">

```
&lt;input type="..."&gt;
```

Attribut **`type`**: `text` | `password` | `radio` | `checkbox` | …

---
## Auswahlfelder

<select>
  <option>Bitte auswählen ...</option>
</select>

```
&lt;select&gt;
  &lt;option&gt;
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
&lt;textarea&gt;
```

---
# Buttons

<button>Button mit Text</button>
<input type="submit" value="Input-Submit mit Text">

```
&lt;button  type="button | submit | reset"&gt;
&lt;input type="submit | reset"&gt;
```

---

