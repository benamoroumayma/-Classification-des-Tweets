
# Classification et clustering des tweets en Python.

# Introduction :
Twitter est un service de réseautage social et de microblogage sur lequel les utilisateurs publient et interagissent les uns avec les autres par le biais de messages appelés «tweets». Il est classé au 6e rang des sites et applications de réseautage social les plus populaires par Dream Grow en avril 2020 avec une moyenne de 330 millions d'utilisateurs mensuels actifs.
Grâce à l'analyse des sentiments, les parties intéressées peuvent comprendre de quoi parlent les utilisateurs et, à partir des informations, prendre les décisions appropriées. Cet article se concentre sur la classification des tweets en 4 grandes catégories: économique, social, culturel et de la santé, puis sur la réalisation d'une analyse de cluster KMeans sur les groupes.
# Base de données:
Les données utilisées sont extraites de Twitter à l'aide de Tweepy , une bibliothèque python permettant d'accéder à l'API Twitter.
# Prétraitement:
## Nettoyage des tweets:
Les tweets contiennent des objets inutiles tels que des hashtags, des mentions, des liens et des signes de ponctuation qui peuvent affecter les performances d'un algorithme et doivent donc être supprimés. Tous les textes sont convertis en minuscules pour éviter que les algorithmes n'interprètent les mêmes mots avec des cas différents comme différents.
## Tokenisation, lemmatisation et suppression des mots vides:
Les mots vides sont des mots couramment utilisés dont la présence dans une phrase a moins de poids que d'autres mots. Ils incluent des mots comme «et», «ou», «a» et.c.
La tokenisation est le processus de division d'une chaîne en une liste de jetons. Une phrase peut être réduite en mots et un mot peut être réduit en lettres à l'aide des tokenizers appropriés.
La lemmatisation réduit un mot à sa forme racine. Par exemple, la forme de racine des « roches » est « roche ».
Les langues utilisées dans les tweets sont principalement l'anglais et le swahili. Ce dernier n'a aucun support donc nous ne travaillerons qu'avec le premier. Cela rend l'analyse paralysée d'une certaine manière étant donné que les textes swahili seront ignorés.
# Classification des tweets:
##KMeans Clustering:
Le calcul de la distance en k-moyennes pèse chaque dimension de manière égale et il faut donc veiller à ce que l'unité de dimension ne déforme pas la proximité relative des observations. La méthode courante consiste à standardiser chaque dimension individuellement.
# Similitude Jaccard :
 La similarité Jaccard ou l'intersection sur l'union est définie comme la taille de l'intersection divisée par la taille de l'union de deux ensembles.
La similarité Jaccard prend uniquement un ensemble unique de mots pour chaque phrase ou document, tandis que la similitude cosinus prend la longueur totale des vecteurs. La similitude Jaccard est bonne pour les cas où la duplication n'a pas d'importance, la similitude cosinus est bonne pour les cas où la duplication est importante. Dans notre cas, le contexte compte plus que la duplication, donc la similarité Jaccard est la technique idéale à utiliser.
# Conclusion :
Le traitement du langage naturel est un vaste domaine et il y a tellement plus à faire sur les données pour obtenir des informations plus précises et utiles. Cela vaut la peine d'être exploré!



 
 [![Binder](https://mybinder.org/badge_logo.svg)](https://mybinder.org/v2/gh/benamoroumayma/-Classification-des-Tweets.git/main)
