Compétition qui existe depuis 1957, la Coupe d'afrique des nations a pour objectif de rassembler tout le continent africain autour d'une passion commune : le foot-ball. Créée par une initiative commune de l'Afrique du Sud, l'Egypte, Le soudan et l'Ethiopie, la première édition ne se jouera qu'avec 03 équipes. En effet, l'Afrique du Sud encore sous Apartheid est écartée pour cause de racisme, car ne voulant pas inclure des joueurs noirs dans leur sélection.

Cependant, les années suivantes la CAN est devenue plus inclusive. Désormais ce sont 24 équipes qui sont qualifiées aux éliminatoires tous les 2 ans pour participer à la compétition continentale, faire découvrir la diversité culture du continent et tisser des liens de fraternité entre patries.


## Sommaire : 
1. [Collecte des données](#données)
2. [Présentation des pays du continent africain](#paysSurnom)
3. [Les Buts marqués entre l'édition 1992 et l'édition 2021](#Goalscorers)
4. [Les sélectionneurs ](#coach)
5. [Conclusion](#conclusion)


## 1. Collecte des données <a name="données"></a>

Les données utilisées pour cette analyse du football africain sont issues de sources diverses dont Wikipédia, les archives de la RSSf(source:African Nations Cup 1992 (rsssf.org)) , la chaine l'Equipe, entres autres.
J'ai fait le choix de recueillir les données sur les sélections qualifiées à partir de l'année 1992, correspondant à la première édition organisée par le Sénégal.

>Remarque : les informations issues de Wikipédia ont été croisées d'autres sources d'informations pour s'assurer de leur fiabilité. Elles ont été recueillies et formatées manuellement au format csv.
>Le traitement sur l'outil Open Refine est une étape de vérification et de validation du jeu de données créé.
>
Le jeu de donnée se présente comme suit :
>- un fichier [selectioneurs.tsv](https://github.com/innojib/AFCON/blob/main/selectionneur-csv.tsv)
>- un fichier [VF_buteurs1998_2021.csv](https://github.com/innojib/AFCON/blob/main/VF_Buteurs1998_2021AFCON.csv)
>- un fichier [drapeauEmbleme.csv](https://github.com/innojib/AFCON/blob/main/DrapeauSurnom.csv)
>- un fihier [AFCON1992_2021.csv](https://github.com/innojib/AFCON/blob/main/AFCON1992to2021_data.csv)


>-Les images des drapeaux des pays africains sont exportées depuis Wikidata avec la reqête suivante:

``` sparql
#defaultView:ImageGrid
SELECT DISTINCT ?paysLabel ?drapeau
WHERE {
  ?country wdt:P31/wdt:P279* wd:Q6256;  # Instance de pays 
           wdt:P30 wd:Q15;               # Localisation Afrique
           rdfs:label ?paysLabel;
           wdt:P298 ?isoCode.            # ISO code pour ne pas avoir de doublons

  OPTIONAL { ?country wdt:P41 ?drapeau. }   # Drapeau

  FILTER(LANG(?paysLabel) = "fr")     # Filter by French labels
  FILTER(?isoCode != "null")             
}
ORDER BY ?paysLabel
```
>
## 2.Les pays du continent africain <a name="pays africains"></a>
>Le continent africain compte 54 pays. Chaque pays a un emblème, qui le plus souvent est un animal, qui le symbolise.
>
>-Ci-dessous la liste de tous les pays du continents africains, leur surnoms ainsi que des faits intéressants à leur propos.
>
<div class="flourish-embed flourish-cards" data-src="visualisation/16598308"><script src="https://public.flourish.studio/resources/embed.js"></script></div>

>
## 3.Les Buts marqués Par pays Entre l'édition 1992 et l'édition 2021 <a name="buts marqué de 1992 à 2021"></a>
> Story : les principaux buteurs des éditions précédentes

<div class="flourish-embed" data-src="story/2162474"><script src="https://public.flourish.studio/resources/embed.js"></script></div>

Cette visualisation a pour objectif d'illustrer les performances réalisées par les différentes équipes ayant au moins participées à une édition de la CAN.  

>- Il est important de noter pour la slide 2 que certains pays dont l'Egypte, ont un avantage net sur les autres sélections quant aux nombres de buts comptabilisés. Ceci s'explique par le nombre d'éditions auxquelles ils ont participé avant l'intégration des autres pays à la Confédération Africaine de Football (CAF).
>- 


>-Carte des buts totaux marqués par pays
<div style="min-height:699px"><script type="text/javascript" defer src="https://datawrapper.dwcdn.net/P1cH2/embed.js?v=3" charset="utf-8"></script><noscript><img src="https://datawrapper.dwcdn.net/P1cH2/full.png" alt="Cette carte indique le nombre de participation au tournoi de la Coupe d'Afrique des nations" /></noscript></div>



## 4.Les sélectionneurs <a name="sélectionneurs"></a>
Les sélectionneurs sont très importants pour faire thiompher une équipe. Et à partir de cette visualisation, on remarque que de nombreux sélectionneurs sont issus du continent.

Néanmoins, il y a également l'Europe et les Amériques qui sont représentées notamment par la France et le Portugal. La sollicitation de ces deux pays peut être interprétée par leur renommée dans le monde du Football.

<iframe title="Représentation des sélectionneurs par leur nationalité" aria-label="Carte" id="datawrapper-chart-6zOh4" src="https://datawrapper.dwcdn.net/6zOh4/2/" scrolling="no" frameborder="0" style="border: none;" width="900" height="506" data-external="1"></iframe>

