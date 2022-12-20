---
title: "*Pourquoi NETFLIX, c'est MOCHE ?* : Précisions sur la vidéo"
date: 2021-02-13

categories:
  - Divagations
tags:
  - Netflix
  - DRM
---

Avant toute chose, allez voir la vidéo d'[**INTHEPANDA**](https://www.youtube.com/channel/UCKpRJZK14ZH7ffHtXMwPcTg), puisque cet article est un complément de cette dernière.

{% include video id="WMMw8GORDX4" provider="youtube" %}

**WARNING : CECI N'EST PAS UNE REMISE EN QUESTION DE LA VIDÉO !! J'ADORE LE CONTENU DE CE VIDÉASTE, JE VOULAIS SEULEMENT APPORTER MA PART SUR QUELQUES IMPRÉCISIONS.**

La vidéo est regardée ? OK, on commence.

# Netflix, DRM et les navigateurs

[Netflix](https://fr.wikipedia.org/wiki/Netflix) est un service de [vidéo à la demande](https://fr.wikipedia.org/wiki/Vid%C3%A9o_%C3%A0_la_demande). Comme son nom l'indique, la plateforme permet de regarder des vidéos (films, séries, etc.) à la demande de l'utilisateur, depuis une [multitude d'appareils](https://devices.netflix.com/fr/). La question est : que nous envoie Netflix quand on lance un contenu ?

>Ba une vidéo, nan ?

Alors, oui et non. Oui car stricto sensu, ce que vous recevez à la fin est un flux vidéo lu par votre appareil. Pourtant, ce flux n'est pas un fichier vidéo conventionnel.

Un fichier vidéo est, comme n'importe quel fichier numérique, un assemblage de [bits](https://fr.wikipedia.org/wiki/Bit), de 0 et de 1. Comme ces bits peuvent être agencés de n'importe quelle façon, des standards sont apparus pour simplifier la lecture de fichier. Ces standards, vous en connaissez certains puisqu'ils sont identifiés par [l'extension de fichier](https://fr.wikipedia.org/wiki/Extension_de_nom_de_fichier) : .pdf, .jpeg, .mp3; dans le cas des fichiers vidéos, les plus courants sont les .mp4 et les .mkv. Grâce à l'extension d'un fichier, l'ordinateur sait de quelle manière lire la suite de 0 et de 1 qui lui est transmis. Quand vous regardez une vidéo sur internet, l'ordinateur distant (appelé serveur) nous envoi donc un de ces fichiers vidéos pour que notre ordinateur puisse la lire.

Dans le cas de Netflix donc (oui, ne pas oublier le sujet principal), on pourrait croire que l'ordinateur reçoit un simple .mp4 et le tour est joué. Le problème est que tout fichier envoyé sur votre ordinateur peut être enregistré, et il est entendable que Netflix ne souhaite pas que tout son contenu soit enregistré par les utilisateurs. Pour le résoudre, Netflix a eu recours à deux stratagèmes : la technologie [DASH](https://fr.wikipedia.org/wiki/Dynamic_Adaptive_Streaming_over_HTTP) et un système de [DRM](https://fr.wikipedia.org/wiki/Gestion_des_droits_num%C3%A9riques).

Sans devenir trop technique, DASH est une technologie permettant de découper votre vidéo en plein de petits morceaux. Au lieu d'envoyer un énorme fichier vidéo de deux heures, on vous envoie de multiples séquences, pouvant varier en longueur et en taille de fichier, et même changer la résolution (c'est comme cela qu'un film peut commencer en basse qualité et finir en 1080p une fois que la connexion s'est stabilisée). Grâce à cette technique, le service peut changer l'audio, les sous-titres, la résolution; vous pouvez avancer ou reculer dans la vidéo, et cela sans avoir à re-télécharger entièrement la vidéo. Pour Netflix, cela permet des économies (pas besoin de renvoyer un gros fichier si l'utilisateur a déjà regardé la moitié du film), mais aussi de limiter (un peu) le piratage, remettre bout-à-bout des morceaux étant plus contraignant que juste attendre que la vidéo soit entièrement chargée.

Pour autant, recoller les morceaux n'est pas si compliqué que ça pour n'importe quel développeur. La preuve en est, [Youtube](https://fr.wikipedia.org/wiki/YouTube) utilise DASH et il est extrêmement facile d'en télécharger un contenu. Comme Netflix tient plus à ses contenus que Youtube, ils ont décidé d'utiliser un système assez commun, appelé DRM.  
En gros, un DRM permet de rendre illisible un contenu pour tout usage non autorisé : un fichier (n'importe lequel) est lu par le système DRM, puis est traduit dans un format connu seulement par le DRM, ce qui le rend intraduisible par un système que le service n'a pas explicitement autorisé. Vous ne pouvez donc pas faire votre propre petit appareil, qui se connecte à Netflix et va regarder le contenu, puisque vous ne possédez pas la [boite noire](https://fr.wikipedia.org/wiki/Bo%C3%AEte_noire_(syst%C3%A8me)) permettant de lire ce dernier. Pourquoi parler de boite noire ? Car c'est ce qu'est tout système de DRM : un bout de code, dont le fonctionnement et la conception sont tenus secret. Ainsi, si vous pouvez visionner une série sur Netflix (ou Amazon Prime, etc) avec votre [navigateur](https://fr.wikipedia.org/wiki/Navigateur_web) préféré, c'est parce que ce dernier embarque un petit bout de code permettant de lire le fichier envoyé. Si votre navigateur ne le contient pas, pas de lecture possible.

>OK, mais le rapport avec la qualité de Netflix ?

Justement, j'y viens. **INTHEPANDA** parle dans sa vidéo d'un problème touchant le protocole [HTML5](https://fr.wikipedia.org/wiki/HTML5), empêchant la lecture de vidéo en [4K](https://fr.wikipedia.org/wiki/4K) sous [Chrome](https://fr.wikipedia.org/wiki/Google_Chrome) ou [Firefox](https://fr.wikipedia.org/wiki/Mozilla_Firefox). Alors disons-le, c'est faux. Encore une fois tout est à voir avec le système de DRM. Pour regarder une vidéo en 4K, il faut que votre matériel (physique!) supporte le système DRM utilisé par cette haute résolution; il faut que votre navigateur intègre la boite noire autorisée par Netflix (seulement [Edge](https://fr.wikipedia.org/wiki/Microsoft_Edge) et [Safari](https://fr.wikipedia.org/wiki/Safari_(navigateur_web))) ; il faut que vous soyez sous un système logiciel supporté (coucou les copains sous [Linux](https://fr.wikipedia.org/wiki/Linux)); il faut que votre câble supporte le protocole [HDCP 2.2](https://fr.wikipedia.org/wiki/High-bandwidth_Digital_Content_Protection) (c'est pas une blague, un vieux câble [HDMI](https://fr.wikipedia.org/wiki/High-Definition_Multimedia_Interface) pourrait ne pas fonctionner); enfin, si tous ces astres sont alignés et que vous avez enroulé un gnome dans du jambon, il faut avoir une connexion assez stable pour regarder le contenu en 4K jusqu'à la fin (mais ça, c'est indépendant de Netflix).

Et tout ça pour quoi ? Pour "ralentir" les pirates. Oui je mets des guillemets car, disons-le, ces systèmes ont été détournés depuis longtemps. Bien sûr, le "hack" n'est pas publique, gardé précieusement par quelques communautés pour empêcher Netflix de corriger la faille. Du coup, comme il est dit dans la vidéo, les pirates sont mieux lotis que les utilisateurs payants, comme c'est souvent le cas avec les systèmes DRM.

> Et le débit vidéo dans tout ça ?

Concernant le débit vidéo, pas besoin de chercher bien loin : Netflix a cherché le rendu le plus acceptable possible pour la majorité d'utilisateurs regardant sur leur ordinateur. Moins le débit qu'ils ont à délivrer est élevé, plus Netflix fait d'économies. De plus, les formats vidéos ne se valent pas tous, certains étant plus performants que d'autres, ce qui fait que pour une même qualité, la taille d'un fichier peut grandement varier, du simple au double !

# Blu-ray, DRM et conclusion

Plus loin dans la vidéo, notre vidéaste est confronté à un problème : lire un blu-ray (officiel) sur son ordinateur, ça a l'air compliqué. Alors, une explication :

![Un cadenas vomissant les DRM](https://www.eff.org/files/issues/og-drm-ugly.png)

Encore une fois, le problème est lié à un système de protection DRM. En effet, les blu-ray ne sont lisibles que par des lecteurs possédant la boite noire de traduction. Cette boite noire étant sous une licence d'utilisation payante, votre ordinateur ne peut pas la lire nativement. Il faut souvent passer par des logiciels payants, possédant les droits d'utilisations des licences blu-ray, ou alors utiliser une bonne vieille platine blu-ray; à moins que vous n'utilisiez des manières un peu moins légales (qui ne seront pas décrites ici).  
Le plus drôle dans tout ça étant que parfois la boite noire filtre sur internet et se retrouve "hacké". Les ayants-droits ont donc plusieurs fois dû changer cette boite noire, modifiant ainsi le format du blu-ray. Il faut donc mettre à jour les lecteurs pour supporter les nouveaux blu-rays. Vous sentez le problème venir ? Effectivement, si vous avez une vieille platine n'ayant jamais été mis à jour, vous pourriez ne pas réussir à lire un blu-ray trop récent.

Donc, pour pouvoir lire un blu-ray sur n'importe quel appareil sans trop de problème, il faudra donc le ["ripper"](https://fr.wikipedia.org/wiki/Rip_(informatique)), c'est-à-dire extraire le contenu du disque pour créer un fichier vidéo, lisible par tous et sans perte de qualité. Légalement, tant que vous ne le partagez pas sur les internets, vous pouvez faire vos propres fichiers vidéos. Ceux-ci seront sûrement d'une taille assez conséquente (plus de 20Go couramment), à moins que vous ne les [compressiez](https://fr.wikipedia.org/wiki/Compression_de_donn%C3%A9es) pour avoir un fichier de plus petite taille. Plus intéressant encore, vous pouvez fusionner plusieurs fichiers vidéos en un seul, permettant potentiellement d'avoir des sous-titres ou de l'audio en plus, ne figurant pas sur votre disque d'origine. Malheureusement, [pour par exemple réussir à voir un film dans sa qualité d'origine](https://www.thestarwarstrilogy.com/project-4k77/), il faudra parfois recourir au piratage, le support physique ou numérique légale ne répondant pas forcément à vos besoins.

Pour finir, je tiens à réitérer sur l'inutilité des DRM : les protections ne servent pas à grand-chose contre les pirates, ces derniers mettant peu de temps à passer outre; de multiples problèmes peuvent arriver aux utilisateurs légaux, les empêchant de profiter pleinement de l'œuvre (des jeux tournant moins bien, des livres ne pouvant être lu, etc); ces DRM rendent la postérité de ces œuvres incertaine, car il suffit que le service ou matériel offrant l'offre disparaisse ou perde les droits pour rendre le contenu inaccessible (coucou [Amazon](https://www.numerama.com/magazine/13484-kindle-amazon-efface-a-distance-des-centaines-de-livres-achetes-legalement-maj.html)). Pendant ce temps, des versions intactes, parfois restaurés ou augmentés circulent dans les réseaux pirates, versions souvent lisibles partout, même sur votre grille-pain connecté. Mais comme le disait [**Gabe Newell**](https://fr.wikipedia.org/wiki/Gabe_Newell) :

>La façon la plus facile d'arrêter le piratage n'est pas de mettre des protections élaborés, mais de proposer aux utilisateurs un service surpassant ce que les pirates ont à offrir.

et :

>Le piratage est presque systématiquement un problème d'accessibilité et non de prix.
