---
title: Arbeiten mit einer fremden API - MediaWiki
author: Martin Kocur
documentclass: scrartcl
classoption:
  - a4paper
header-includes: |
    \usepackage{german} 
	\usepackage{xcolor}
    \usepackage[a4paper,left=2.5cm, right=2.5cm,top=2.5cm, bottom=3cm]{geometry}
    \usepackage{fancyhdr}
    \pagestyle{fancy}
    \fancyhf{}
    \rhead{Webtechnologien}
    \lhead{Übungsblatt}
    \fancypagestyle{plain}{
      \fancyhf{}
      \rhead{Webtechnologien}
      \lhead{Übungsblatt}}





---


# 07 | Arbeiten mit einer fremden API

## Aufgabe: Darstellen von Bildern mit Hilfe von Wikipedia und der MediaWiki API

Erstellen Sie in dieser Aufgabe eine einfache Anwendung, die lediglich aus einem Input-Feld besteht. In dieses Feld können Nutzer Städtenamen auf Englisch (z.B. Munich) eingeben, um daraufhin ein Bild der Stadt zu erhalten. Dieses Bild wird im Browser gerendert. Wird eine weitere Stadt eingegeben, so wird das nächste Bild angehängt.

Verwenden Sie die  [\textcolor{blue}{MediaWiki API}](https://www.mediawiki.org/wiki/API:Main_page), um die Bilder der Städte zu erhalten. Es ist völlig ausreichend, wenn Sie ein Bild der Hauptseite des Wikipedia-Artikels der dazugehörigen Stadt anzeigen.   Bauen Sie die Verbindung zur Wikipedia API über die in der Vorlesung  kennengelernte _Fetch API_ auf.

Die nachfolgenden Quellen sollen Ihnen dabei helfen, die Anwendung zu implementieren:

- Sie können mit Hilfe von einer *action=query* und zusätzlichen Parametern auf Inhalte von Wikipedia zugreifen. Mehr Informationen dazu finden Sie [\textcolor{blue}{hier}](https://www.mediawiki.org/w/api.php?action=help&modules=query).

- Über den Parameter _pageimages_ erhalten Sie Informationen zu Bildern und Fotos. Über _piprop_ können Sie Bilder in Originalgröße oder als Thumbnail abrufen. Mehr erfahren Sie [\textcolor{blue}{hier}](https://www.mediawiki.org/wiki/Extension:PageImages).

- [\textcolor{blue}{Hier}](https://en.wikipedia.org/w/api.php?action=query&titles=Berlin&format=json&indexpageids&prop=images&prop=pageimages&piprop=original) ist ein Beispiel einer URL, mit welcher Sie Information zur Stadt Berlin erhalten. 

- Hinweis: Binden Sie als letztes Element der URL **&origin=*** ein, damit sie über die Fetch API Zugriff auf die Wikipedia Inhalte haben. 

  



------

*Abgabekriterien:*

Laden Sie Ihre Antworten bis spätestens 29.06.2020 (23:59 Uhr) als zip-komprimierten Ordner auf GRIPS hoch.  Für dieses Übungsblatt haben Sie zwei Wochen Zeit. Benennen Sie die einzelnen Dateien pro Aufgabe sinnvoll und verwenden Sie geeignete Formate:

- Aufgabe: Ihr gesamtes Projekt


Der Name der Datei ergibt sich aus dem Präfix „Übung_WT_SS20“, der Nr. des Übungsblattes, ihrem Vor- und Nachnamen jeweils getrennt durch _ .

 

Beispiel: **Übung_WT_SS20_7_Max_Mustermann.zip**

