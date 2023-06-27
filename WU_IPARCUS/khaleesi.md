# WU_IPARCUS
# 1
Nous avons infiltré un groupe de mafieux qui font de la revente de produit issu du marché noir.
Ces mafieux sont fan de golf... Notre espion a eu rendez vous avec les leaders de ce groupe mafieux.
Combien sont-ils ? (sans compter notre espion biensur...)
De quelle couleur est le pantalon flashy de notre espion ? (en majuscule)

Le flag sera donné sous la forme : 00_COULEUR
exemple : 07_JAUNE


Nous avons un fichier nommé ``khaleesi.pcapng`` et nous voulons en extraire une ou des images.

Pour se faire nous allons utiliser la commande : ``sudo foremost -T  Khaleesi.pcapng``
<br> 
Sur une des photos les plus nettes extraites on retrouve 3 hommes jouant au golf sur un extrait de vidéo surveillance. <br><br><br>
<img src="https://github.com/mrk59/WU_IPARCUS/blob/main/WU_IPARCUS/images/khaleesi_golf.png"> <br>

Notre espion porte un pantalon bleu flashy.
``flag : 02_BLEU``
# 2 
Nous avons infiltré un groupe de mafieux qui font de la revente de produit issu du marché noir.
Ces mafieux sont fan de golf... Notre espion a eu rendez vous avec les deux leaders de ce groupe mafieux.

Quel est le nom du golf ou la rencontre à eu lieu ? (sans tiret ou espace, en majuscule)
<br><br><br>
La photo n'étant pas assez nette pour tenter de GEOINT l'image il va falloir retrouver l'addresse ip de la caméra qui a prit ces images.<br>
Pour se faire on va continuer d'utiliser tshark avec : ``tshark -r Khaleesi.pcapng -T fields -e ip.addr | sort -u > ips.txt`` <br>
Une fois le tri fait dans ips.txt il liste 4 ip, celle qui nous interessera sera : ``217.38.38.154``<br>
On se rend sur ``https://whatismyipaddress.com/fr/mon-ip``<br><br>
![](https://github.com/mrk59/WU_IPARCUS/blob/main/WU_IPARCUS/images/addr_golf.png)

# 3
