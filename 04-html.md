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

HTML dient der Strukturierung von Texten (Tags)

Trennung von Aufbau (HTML) und Darstellung (CSS)

Weiterentwicklung durch das [World Wide Web Consortium (W3C)](http://www.w3.org/)

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

<i>Leonato.</i> I learn in this letter that <strong>Don Peter</strong> of
<strong>Arragon</strong> comes this night to <strong>Messina</strong>.

<i>Messenger.</i> He is very near by this: he was not three leagues off when I
left him.

<i>Leonato.</i> How many gentlemen have you lost in this action?

<i>Messenger.</i> But few of any sort, and none of name.

---
## Text mit Auszeichnung ohne Darstellung

**&lt;i&gt;**Leonato.**&lt;/i&gt;** I learn in this letter that **&lt;strong&gt;**Don
Peter**&lt;/strong&gt;** of **&lt;strong&gt;**Arragon**&lt;/strong&gt;** comes this night
to **&lt;strong&gt;**Messina**&lt;/strong&gt;**.

**&lt;i&gt;**Messenger.**&lt;/i&gt;** He is very near by this: he was not three leagues
off when I left him.

**&lt;i&gt;**Leonato.**&lt;/i&gt;** How many gentlemen have you lost in this action?

**&lt;i&gt;**Messenger.**&lt;/i&gt;** But few of any sort, and none of name.

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
        &lt;meta charset="utf-8“&gt;
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

* Ist immer von einem Element umgeben
* Einige Zeichen müssen maskiert werden – Verwendung einer Zeichenreferenz (z.B.  &lt;, &gt;, ")

---

