# ovh-api-bash
Script bash pour les commandes courantes en API OVH. 

# Le script est basé sur la présentation de l'API OVH en bash de Christophe Casalegno.
https://www.christophe-casalegno.com/jouons-un-peu-avec-lapi-ovhcloud-en-bash-sous-gnu-linux/
Je n'avais pas eu l'occasion de trouver une méthode simple & rapide pour les commandes courantes sur l'API OVH.

1 - # Générer votre secret key OVH dans un txt au format
CONSUMER_KEY="XXXXX"
APP_KEY="XXXXX"
APP_SECRET="XXXXX"

2 - # Regarder ce que vous pouvez faire avec l'API OVH disponible ici : https://api.ovh.com/ 

3 - # Lancer le script et utilisrz la commande "Help" pour vous aider.
Attention, l'API éxéctue des get/post/put/delete. En conséquence, soyez sur de vos actions.

HELP_TEXT='
List of commands and options:
-------------------------------
./script-dns check or api_check check authentification api

./script-dns domain_export - export all zone from NIC
./script-dns domain_check $domain

./script-dns domain_reset $domain - Supprime tout les enregistrements pour un domaine. Un domaine reset zone vide fera la même chose.
./domain-dns domain_redirect_racine $domain $url - Redirige racine vers url
./script-dns domain_redirect_www $domain $url redirige www vers url
./script-dns domain_redirect_del_add $domain $url - Supprime zone DNS puis ajoute  site racine + www + * vers $url
./script-dns domain_txt_proprio $domain - Ajoute un TXT pour definir qui est propritaire du domain
./script-dns domain_add_zone $domain - Ajoute la zone DNS pour préparer migration
./script-dns domain_import $domain

./script-dns api_whois - Historise le nb API
./script-dns domain_whois
./script-dns domain_check


Le script sera régulièrement mise à jour avec des nouvelles fonctions.
Baptiste,
