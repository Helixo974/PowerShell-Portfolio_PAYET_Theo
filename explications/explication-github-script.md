1️⃣ Pagination GitHub
(100 mots min)

Expliquez avec vos propres mots :
• Pourquoi la pagination est nécessaire dans l'API GitHub ?

La pagination est nécessaire dans l’API GitHub parce que l’API ne renvoie pas tous les repositories en une seule fois. Car par default elle va limiter le nombre de résultats par requête entre 30 par défaut et jusqu’à 100 maximum. Cela permettra d’éviter des réponses trop lourdes et de protéger les serveurs contre la surcharge. Ce qui fais que si un utilisateur a plus de 100 repositories il faut faire plusieurs requêtes en utilisant les paramètres per_page et page pour récupérer toutes les pages une par une. Sans cette pagination le script ne récupérerait qu’une partie des repos et l’analyse serait incomplète.

• Comment fonctionne-t-elle techniquement ?

La pagination fonctionne en divisant les résultats en plusieurs pages numérotées. On utilise per_page pour définir le nombre d’éléments par requête (max 100) et page pour choisir la page à récupérer. Le script commence à la page 1 puis incrémente le numéro et refait des appels API jusqu’à ce qu’il n’y ait plus de résultats. Cela permet de récupérer tous les repositories sans dépasser les limites de GitHub.

• Quels paramètres utilise-t-on ( per_page , page ) ?

On va utiliser deux paramètres principaux: le per_page qui va définir le nombre d’éléments retournés par requête (au maximum 100) ensuite le paramètre page va indiquer le numéro de la page à récupérer. En combinant ces 2 paramètres on peut parcourir toutes les pages et récupérer toutes les repositories.


2️⃣ updated_at vs pushed_at
(50 mots min)

• Que représente updated_at ?

Le champ updated_at correspond à la dernière modification effectuée sur le repository que ce soit un changement de description soit de paramètres soit de README ou d’autres éléments non liés directement au code.

• Que représente pushed_at ?

Le champ pushed_at indique la date du dernier push de code effectué sur le repository. Il va reflèter une modification réelle du contenu du projet.

• Pourquoi utilise-t-on pushed_at pour mesurer l'activité réelle ?

On utilise pushed_at car il nous montre la dernière modification du code. Contrairement à updated_at il permettra d’évaluer l’activité réelle du développement du projet.

