# WU_IPARCUS
# 1
_Nous avons infiltré un groupe de mafieux qui font de la revente de produit issu du marché noir._
_Ces mafieux sont fan de golf... Notre espion a eu rendez vous avec les leaders de ce groupe mafieux._
_Combien sont-ils ? (sans compter notre espion biensur...)_
_De quelle couleur est le pantalon flashy de notre espion ? (en majuscule)_

_Le flag sera donné sous la forme : 00_COULEUR_
_exemple : 07_JAUNE_


Nous avons un fichier nommé ``khaleesi.pcapng`` et nous voulons en extraire une ou des images.

Pour se faire nous allons utiliser la commande : ``sudo foremost -T  Khaleesi.pcapng``
<br> 
Sur une des photos les plus nettes extraites on retrouve 3 hommes jouant au golf sur un extrait de vidéo surveillance. <br><br><br>
<img src="https://github.com/mrk59/WU_IPARCUS/blob/main/WU_IPARCUS/images/khaleesi_golf.png"> <br>

Notre espion porte un pantalon bleu flashy.
``flag : 02_BLEU``
# 2 
_Nous avons infiltré un groupe de mafieux qui font de la revente de produit issu du marché noir._
_Ces mafieux sont fan de golf... Notre espion a eu rendez vous avec les deux leaders de ce groupe mafieux._

_Quel est le nom du golf ou la rencontre à eu lieu ? (sans tiret ou espace, en majuscule)_
<br><br><br>
La photo n'étant pas assez nette pour tenter de GEOINT l'image il va falloir retrouver l'addresse ip de la caméra qui a prit ces images.<br>
Pour se faire on va continuer d'utiliser tshark avec : ``tshark -r Khaleesi.pcapng -T fields -e ip.addr | sort -u > ips.txt`` <br>
Une fois le tri fait dans ips.txt il liste 4 ip, celle qui nous interessera sera : ``217.38.38.154``<br>
On se rend sur ``https://whatismyipaddress.com/fr/mon-ip``<br><br>
![](https://github.com/mrk59/WU_IPARCUS/blob/main/WU_IPARCUS/images/addr_golf.png)
``flag : TANDRIDGOLFCLUB``
# 3
_Nous avons infiltré un groupe de mafieux qui font de la revente de produit issu du marché noir._
_Ces mafieux sont fan de golf... Notre espion a eu rendez vous avec les deux leaders de ce groupe mafieux._

_A quelle heure a eut lieu le rendez vous ? (sous la forme, AAAA-MM-JJ_HH)_ <br><br>

Sur l'image de vidéo surveillance on appercoit la date et l'heure à laquelle la rencontre a eu lieu. <br>
<img src="https://github.com/mrk59/WU_IPARCUS/blob/main/WU_IPARCUS/images/date_rencontre.png">

``flag : 2023-03-06_10``
# 4
_Nous avons infiltré un groupe de mafieux qui font de la revente de produit issu du marché noir._
_Ces mafieux sont fan de golf... Notre espion a eu rendez vous avec les deux leaders de ce groupe mafieux._

_L'un des mafieux semble se vanter d'avoir son nom juste au dessus de la cheminée depuis 2011, trouver son prénom et nom complet ? (PRENOMSNOM en majuscule sans espace)_

En se balandant sur le site du golf ``http://www.tandridgegolfclub.com`` on le voit sur l'onglet ``The club house``



<img src="https://github.com/mrk59/WU_IPARCUS/blob/main/WU_IPARCUS/images/cheminée_flag.jpg">

# 5 
_Ce premier rendez vous s'étant bien passé, les 2 mafieux et notre espion doivent se retrouver à la fin de la semaine dans un bar / restaurant non loin de la entre 17h et 19h pour déguster un de leur très nombreux cocktails._

_Comment s'appel se bar ? (sur le logo du bar, en majuscule, sans espace)_
_Combien y a t il de cocktail dans ce bar ?_

_Le flag se donnera sous la forme : NOMDUBAR_000 (exemple : IPARCUS_123)_

# 6 
Les mafieux sont très attachés à ce bar, en raison de son affiliation... Nous devons retrouver l'affiliation pour pouvoir démenteler la globalité de ce groupe mafieux.

A qui appartient / appartenait ce blason ? (nom complet en majuscule, séparé par des underscore)

``flag : GEORGE_LOUIS_DE_HANOVRE``
