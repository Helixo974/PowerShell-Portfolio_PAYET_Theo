Expliquez avec vos propres mots :
• Pourquoi la pagination est nécessaire dans l'API GitHub ?

La pagination est nécessaire dans l’API GitHub parce que l’API ne renvoie pas tous les repositories en une seule fois. Car par default elle va limiter le nombre de résultats par requête entre 30 par défaut et jusqu’à 100 maximum. Cela permettra d’éviter des réponses trop lourdes et de protéger les serveurs contre la surcharge. Ce qui fais que si un utilisateur a plus de 100 repositories il faut faire plusieurs requêtes en utilisant les paramètres per_page et page pour récupérer toutes les pages une par une. Sans cette pagination le script ne récupérerait qu’une partie des repos et l’analyse serait incomplète.
