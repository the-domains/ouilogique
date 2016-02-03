---
inFeed: true
hasPage: true
inNav: false
inLanguage: null
starred: true
keywords: []
description: ''
datePublished: '2016-02-03T09:44:12.645Z'
dateModified: '2016-02-03T09:33:51.691Z'
title: "Programmer un MSP430 en\_mode ISP"
author: []
authors: []
publisher:
  name: null
  domain: null
  url: null
  favicon: null
sourcePath: _posts/2016-02-03-programmer-un-msp430-en-mode-isp.md
published: true
url: programmer-un-msp430-en-mode-isp/index.html
_type: Article

---
# Programmer un MSP430 en mode ISP

Lors du[quatrième MOOC sur les µcontrôleurs de l'EPFL][0], Pierre-Yves Rochat nous a présenté comment utiliser une carte Launchpad pour programmer un MSP430 sur un breadboard. Cette façon de programmer est souvent appelée[ISP (in-system programmer) ou programmation in situ][1]en français.

Le document original peut être téléchargé ici :

[http://pyr.ch/coursera/ExperiencesAvecLaunchpad.pdf][2]

Voilà le proto sur breadboard :
![](https://the-grid-user-content.s3-us-west-2.amazonaws.com/333c6357-f942-4daf-8a26-8afa445bb83f.JPG)

Voilà le résultat final :
![](https://the-grid-user-content.s3-us-west-2.amazonaws.com/824c1cce-80fc-4693-adf6-a3d1ee2e1f8f.jpg)
![](https://the-grid-user-content.s3-us-west-2.amazonaws.com/38901a9e-13e1-4412-8dbb-dab022ab1774.jpg)
![](https://the-grid-user-content.s3-us-west-2.amazonaws.com/7e0160d8-a10d-4603-b983-2ad12a4a6dc8.jpg)

## Leçons apprises

* Programmer un MSP sur breadboard (un MSP430G2231 dans cette application).
* Utiliser une découpeuse laser.
* [Les plaques à souder Perma-Proto d'Adafruit][3]sont très pratiques.
* Que les LED RGB translucides sont très nettement moins lumineuses que les transparentes. J'utilise une LED translucide dans ce projet, mais j'ai un gadget similaire avec une LED transparente et la différence est frappante. J'aurais aussi dû être moins conservatif sur la question de la consommation et utiliser des résistances plus faibles.
* Qu'une LED éclaire beaucoup plus sur le dessus que sur les côtés.
* Qu'il est horriblement long et compliqué de réaliser un projet, même aussi simple que celui-là quand on a pas de matériel. J'étais tributaire des horaires d'ouverture du[FabLab Chêne 20][4]et ça a été la course permanente pour réaliser ce montage. Notez que j'ai réalisé deux autres versions : une qui ne sera jamais utilisée et une autre que j'ai offerte à Noël, mais qui ne contient pas le montage électronique, c'est donc un simple photophore pour y placer une bougie et il a une forme différente de celui que je présente ici.

[0]: https://www.coursera.org/course/microcontroleurs
[1]: http://fr.wikipedia.org/wiki/Programmation_in-situ
[2]: http://pyr.ch/coursera/ExperiencesAvecLaunchpad.pdf
[3]: http://www.adafruit.com/blog/2011/11/18/adafruit-perma-proto-half-sized-breadboard-pcb-3-pack/
[4]: http://www.fablab-chene20.ch/