---
last_modified_at: 2019-10-18T03:15:47+02:00
date: 2019-10-17
title: "Vererbung"
categories:
  - Informatik
tags:
  - extends

comments: true
# read_time: false
# related: false
# share: false
# toc: true
# toc_label: "Unique Title"
# toc_icon: "heart"
# toc_sticky: true
# excerpt_separator: "<!--more-->"
# link: https://github.com
# classes: wide
# search: false
# header:
  # image: /assets/images/page-header-image.png
  # og_image: /assets/images/page-header-og-image.png
# header:
  # overlay_image: /assets/images/unsplash-image-1.jpg
  # og_image: /assets/images/page-header-og-image.png
  # caption: "Photo credit: [**Unsplash**](https://unsplash.com)"
  # actions:
  #   - label: "Learn More"
  #     url: "https://unsplash.com"
# header:
  # teaser: /assets/images/page-header-teaser.png
  # og_image: /assets/images/page-header-og-image.png
# header:
  # video:
    # id: XsxDH4HcOWA
    # provider: youtube
# sidebar:
  # - title: "Title"
  #   image: http://placehold.it/350x250
  #   image_alt: "image"
  #   text: "Some text here."
  #   nav: sidebar-sample
  # - title: Another sidebar nav
  #   nav: sidebar-sample

---

**Was bezeichnen wir als Modellierung?**

- Abstraktes Wissen über Gegenstände mit Hilfe von Klassen auszudrücken.



**Worauf kommt es bei der Abstraktion ganz besonders an?**

- Bei der Auswahl der Eigenschaften den Zweck des Programms nie aus den Augen zu verlieren.



**Angenommen, wir wollen für ein Programm eine Klasse namens Auto entwerfen. Welche Eigenschaften hältst du hierbei für wichtig?**

- Kann so nicht entschieden werden



**Was bewirkt der this-Bezeichner?**
Er ermöglicht es, Variablen, die als Parameter übergeben wurden, den
gleichen Namen zu geben, wie Attributen der Klasse.



**Oberklasse:**
Eine Oberklasse vererbt all ihre Attribute und Metho-
den an ihre Unterklasse.

**Unterklasse:**
Eine Unterklasse erbt alle Attribute und Methoden
ihrer Oberklasse



**Vorteile der Vererbung:**

- bessere Wartbarkeit
- weniger Fehlerquellen
- keine Code-Duplizierung
- übersichtlichere Klassendiagramme



**Was bedeutet Vererbung in der objektorientierten Programmierung?**

- eine Klasse überträgt all ihre Eigenschaften an eine andere Klasse



**Welche der folgenden Aussagen zu Ober- und Unterklassen sind richtig?**

- eine Oberklasse überträgt ihre Eigenschaften an eine Unterklasse
- Oberklassen und Unterklassen beschreiben eine IST-Beziehung



**Betrachte die Vorteile der Vererbung. Welche der folgenden Aussagen sind richtig?**

- Klassen können mit der Vererbung so miteinander ’verknüpft’ werden, dass bei der Änderung einer Klasse andere Klassen gleich mit verändert werden
- Mit Hilfe der Vererbung erstellte Programme können leicht erweitert werden



**Welche Verwendung des Befehls extends ist korrekt?**

- public class A extends B



**Welche Aussagen bezüglich des Ausdrucks super sind richtig?**

- Um in einer Unterklasse eine Methode der Oberklasse aufzurufen, wird der Ausdruck super verwendet



**Worauf muss bei Konstruktoren in einer Unterklasse geachtet werden?**

- Möglicherweise muss der geerbte Konstruktor der Oberklasse erweitert werden, damit alle Attribute initialisiert werden können



**Wann wird von einer polymorphen Variable gesprochen?**

- Wenn ein Objekt einer Unterklasse an eine Variable vom Typ seiner Oberklasse zugewiesen wird.
