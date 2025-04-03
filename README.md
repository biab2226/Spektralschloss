# Spektralschloss
Überblick, Designdateien und Bauanleitung für das Fablab-Projekt "Spektralschloss" im WiSe '24 vom J. Wesner, F. Werner und B. Abb0ud

## Einleitung
Das Spektralschloss wurde im Rahmen des Fablab-Moduls an der Berliner Hochschule für Technik im WiSe 2024 entwickelt. Der Zweck 
des Spektralschlosses ist eine photonische Neuinterpretation des jahrtausendealten Prinzips von mechanischen Schlössern durch die Verwendung
von selbstgebauten lichtbrechenden Elementen als Schlüssel, in diesem Fall eine Anordnung von mehreren Prismenebenen aus PMMA oder Akrylglas anstelle
der typischen Schlüsselzacken.

# Bau des Schlosses
Der Bau des Schlosses erfolgt in zwei Hauptschritten: Dem Bau des Prismenschlüssels und dem 3D-Druck und Zusammenbauen des Schlosses und der Elektronik.

## Prismenschlüssel
Materialien & Werkzeug:
-CO2-Laser
-6mm PMMA / Akrylglas
-Ceriumoxid-Politur & Substrat
-3mm Pressholzplatte
-Photopolymerisierendes Kunstharz
-UV-Lichtquelle (direktes Sonnenlicht, NUV oder UVA Laser, NUV LED)
-Reagenzglas

Mit dem CO2-Laser werden verschiedene Prismenformen aus der PMMA-Platte geschnitten. Anschließend werden die Facetten mit der Ceriumoxid-Politur auf einer
flachen Oberfläche poliert, bis transmittiertes und gebrochenenes Licht keine starke Streuung mehr aufweist.
Aus der Pressholzplatte werden nun runde Scheiben, die als Abstandhalter zwischen den Prismen dienen, mittels des CO2-Lasers ausgeschnitten.
Die Ebenen werden mit einer geringen Menge des photopolyerisierenden Kunstharzes verklebt. Zum Aushärten wird dabei die UV-Lichtquelle verwendet.
Dies erlaubt eine einfache und präzise Justage der Prismen auf die gewünschte Position, der die Fixierung durch das UV-Licht folgt.

Der "Prismenstapel" kann nun in das Reagenzglas geladen und mit dem Kunstharz befestigt werden.

## Spektralschloss
Materialien & Werkzeug:
-Arduino Uno
-Breadboard und Kabel
-5x rote (650nm) Diodenlasermodule mit Treiber (3-5V) der Laserklasse 1M oder weniger
-Heißkleber oder photopolymerisierendes Kunstharz
-Druckknopf
-10x Fotowiderstände mit ADC und Triggerlevel-Einstellung
-LED oder anderer Indikator für eine erfolgreiche Öffnung des Schlosses

Die .stl-Datei wird gesliced und gedruckt. Die Laserdioden werden in die vertikalen Löcher geklebt und parallel geschaltet. Der Druckknopf wird in Serie mit den Laserdioden
verbunden und aktiviert diese, wenn jener gepresst wird. Der Druckknopf wird am Ende des Speaktralschlosses angeklebt. Schließlich werden die Fotowiderstände
mit dem Arduino verkabelt, konfiguriert und an verschiedenen
Positionen der Schlossebene so installiert, dass bei einer erfolgreichen Öffnung sowohl einige Fotowiderstände das Triggerlevel erreichen und andere nicht.
Somit wird ein Knacken des Schlosses mit einer starken Lichtquelle verhindert.
