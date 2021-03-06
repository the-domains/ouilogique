---
inFeed: true
hasPage: false
inNav: false
isBasedOnUrl: 'http://ouilogique.com/programmer_un_attiny_avec_un_arduino_uno/'
inLanguage: null
starred: false
keywords: []
description: ACCUEIL RECHERCHE    Programmer un ATtiny25V avec un Arduino UNO comme programmateur  Matériel requis  Un ordinateur sur OS X Yosemite (10.10) Un Arduino UNO Un
datePublished: '2016-02-03T09:44:12.665Z'
dateModified: '2016-02-03T09:32:30.372Z'
author: []
title: Programmer un ATtiny25V avec un Arduino UNO comme programmateur
authors: []
publisher:
  name: ouilogique.com
  domain: ouilogique.com
  url: null
  favicon: null
sourcePath: _posts/2016-02-03-programmer-un-attiny25v-avec-un-arduino-uno-comme-programmat.md
published: true
_context: 'http://schema.org'
_type: Article

---
ACCUEIL RECHERCHE Programmer un ATtiny25V avec un Arduino UNO comme programmateur Matériel requis Un ordinateur sur OS X Yosemite (10.10) Un Arduino UNO Un ATtiny25V Un breadboard 4 LED 4 résistances de 220 Ω Sources Source principale http://www.didel.com/diduino/ProgrammerUnAtTiny.pdf Autres sources http://arduino.cc/en/Tutorial/ArduinoISP http://www.atmel.com/images/atmel-2586-avr-8-bit-microcontroller-attiny25-attiny45-attiny85\_datasheet.pdf À voir aussi http://arduino.cc/en/Main/Standalone http://arduino.cc/en/Tutorial/ArduinoToBreadboard http://codeandlife.com/2012/03/21/using-arduino-uno-as-isp/ Préambule Le but de ce document est de présenter la programmation d'un microcontrôleur ATtiny25V à l'aide d'un Arduino UNO. Ce mode de programmation s'appelle en anglais AVR ISP (in-system programmer). L'IDE Arduino utilisé pendant les tests était la version 1.5.8 bêta Java 6\. Préparation matérielle Câbler la plaque d'essai selon le schéma ci-dessous. Les trois premières LED, verte, rouge et orange, servent à afficher le statut lors de la programmation : pin 9: Heartbeat - shows the programmer is running pin 8: Error - Lights up if something goes wrong (use red if that makes sense) pin 7: Programming - In communication with the slave et la quatrième LED, bleue, sert à vérifier que l'ATtiny a effectivement été programmé avec le programme tinyblinky.ino. À noter que les LED sont optionnelles. Préparation logicielle Télécharger les librairies (Core Libraries) de la famille ATtiny de https://code.google.com/p/arduino-tiny/ en prenant garde de choisir la version correspondante à l'IDE Arduino qui va être utilisé par la suite. Décompresser le fichier zip et déplacer le répertoire tiny dans ~/Documents/Arduino/hardware/. Copier le fichier tiny/avr/Prospective Boards.txt vers tiny/avr/boards.txt. Le fichier boards.txt peut optionnellement être modifié, par exemple pour enlever des définitions de microcontrôleurs inutiles. Ce fichier complète celui de l'IDE qui se trouve à /Applications/Arduino.app/Contents/Resources/Java/hardware/arduino/avr/boards.txt et qui peut lui aussi être édité. Redémarrer l'IDE. Le menu Outils/Type de carte doit afficher la liste des ATtiny installés ci-dessus. Configurer l'Arduino UNO comme un programmateur Ouvrir le croquis ArduinoISP.ino qui se trouve dans le menu Fichier/Exemples en onzième position. Vérifier que la cible est l'Arduino UNO : Outils/Type de carte/Arduino UNO Outils/Port : Sélectionner le port du UNO Outils/Programmateur/AVRISP mkII Téléverser le croquis ArduinoISP.ino sur le UNO. Charger le bootloader dans l'ATtiny Normalement cette étape n'est pas nécessaire quand on programme en mode ISP. Le bootloader est justement là pour palier l'absence de programmateur. Comme je n'ai pas encore vérifié cette info, je laisse ce texte pour l'instant. De toute façon une chose est sûre : ça fonctionne comme ça. Cette opération est nécessaire pour les microcontrôleurs qui n'ont jamais été programmés. Elle ne doit être effectuée qu'une fois. Changer la cible pour programmer l'ATtiny25V : Outils/Type de carte/ATtiny25 @ 1 MHz Outils/Port : Sélectionner le port du UNO Outils/Programmateur/Arduino as ISP Charger le bootloader : Outils/Graver la séquence d'initialisation D'après Didel, ce n'est pas vraiment un bootloader qui est chargé, mais une configuration des fusibles qui est réalisée. Programmer l'ATtiny Vérifier que la cible est effectivement l'ATtiny comme à l'étape précédente. Téléverser le croquis suivant : /\* tinyblinky.ino Programme pour tester la programmation en mode ISP d'un ATtiny25V Fait clignoter une LED sur PB4, pin 3 \*/ \#include \#define LedPin PORTB4 \#define LedToggle PORTB ^= ( 1<\><\></\></\>