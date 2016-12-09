:data-transition-duration: 2000
:skip-help: true
:css: css/campus02.css

.. title: Bootstrap

.. _Boostrap: http://getbootstrap.com/

.. role:: html(code)
  :language: html

----

Bootstrap 3
-----------

`Boostrap`_ ist ein CSS-Framework das grundlegend UI-Bestandteile für HTML bereitstellt.

----

Verwendung
----------

.. html::

  <link rel="stylesheet" href="bootstrap.min.css">
  <link rel="stylesheet" href="bootstrap-theme.min.css">
  <script src="bootstrap.min.js"></script>

----

Bestellformular (1/2)
---------------------

Verwenden Sie folgende URL als `action` Attribut am Formular:
`<https://campus02.fladi.at/web/order?pkz=12345678>`_

* Ersetzen Sie `12345678` durch ihre Personen-Kennzahl.
* Sie müssen das Formular mit allen Feldern korrekt implementiert haben (Feld-Namen beachten!) damit eine Bestellung gespeichert wird.

----

Bestellformular (2/2)
---------------------

Folgende Felder sollen enthalten sein:

* Name des Käufers [`customer`]
* Produktauswahl als Dropdown [`product`]
* Bestätigung Geschenkoption als Checkbox [`gift`]
* Dateiupload für Bild als Motiv auf Verpackung [`image`]
* Mehrzeiliges Textfeld für Anmerkungen [`comment`]
* Bestell-Button zum Absenden

Die Namen in **[]** sind für die `name` Attribute der Formular-Felder zu verwenden.
