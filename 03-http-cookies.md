---

author: Dr. Xiaoshan Liu, DI Michael Fladischer
title: Web Grundlagen

---

# HTTP: Cookies

---
## Das Problem?

*HTTP ist zustandslos.*

![](figure/http-cookies-1.svg)

---
## Der Zusammenhang

Wie können dann einzelne HTTP-Verbindungen zu einer gemeinsamen Sitzung
zugeordnet werden?

![](figure/http-cookies-2.svg)

---
## Mögliche Ansätze

 * IP-Adressen?
 * Browser-Erkennung?
 * Eigenen Header mitschicken?

---
# Cookie == HTTP-Header

---
Der Webserver sendet das Cookie als einen eigenen Header:

    Set-Cookie: user=SusiSorglos

![](figure/http-cookies-3.svg)

*Zum Beispiel als Kennzeichnung der Sitzung nach erfolgreichem Login.*

---
Der Webbrowser liest das Cookie aus dem Header aus und legt es in einem lokalen
Speicher ab, der auch nach Abbau der HTTP-Verbindung erhalten bleibt.

![](figure/http-cookies-4.svg)

---
Der Webbrowser sendet nun bei jedem nachfolgenden Request das zuvor erhaltene
Cookie als Header zurück an den Webserver:

    Cookie: user=SusiSorglos

![](figure/http-cookies-5.svg)

Dieser kann nun anhand der Daten im Cookie die Zuordnung der Verbindung zu einer
Sitzung treffen.

---
## Aufbau

    set-cookie = "Set-Cookie:" cookie-str
    cookie-str = NAME "=" VALUE
                 *(";" cookie-av)
    cookie-av = "Domain" "=" value
              | "Max-Age" "=" value
              | "Expires" "=" value
              | "Path" "=" value
              | "Secure"
              | "HttpOnly"

---
## Sicherheit

Um zu verhindern, dass Cookies *gestohlen* werden, können sie mehreren Einschränkungen unterliegen:

 * Same-Origin-Policy
 * Secure
 * HttpOnly

---
## Same-Origin-Policy

 Relevant sind **Domain** und **Path**.

 Beim **Senden** matcht eine Domain auch für Subdomains (alle Level).
 *Ausnahme: Leerer Domain-Parameter matcht nur für den aktuellen Host.*

 Beim **Setzen** kann das Cookie bis auf die Ebene der Hauptdomain gesetzt werden.
 *Ausnahme: Third-Level-Domains wie gv.at, co.uk, ... (abhängig vom Webbrowser)*

---
## Secure

Das Cookie darf nur über sichere Kanäle (HTTPS) übertragen werden.

---
## HttpOnly

JavaScript hat keinen Zugriff auf das Cookie.

---
## Referenzen

* Alle HTTP RFCs
* [HTTP State Management Mechanism](http://tools.ietf.org/html/rfc6265)

---
