---
marp: true
theme: teaching
paginate: true
size: 4:3
---

<!-- _class: titre -->
# Utiliser Marp<br> pour ses<br> diaporamas <!-- fit-->
Cédric Eyssette (2019-2020)
cedric.eyssette@gmail.com

---
[Marp](https://marp.app/) est un outil qui permet de créer un diaporama à partir d'un fichier texte, écrit avec une syntaxe très simple.

Cela permet de se concentrer sur le contenu, sans avoir à gérer le positionnement, le redimensionnement des éléments et des polices de caractère, grâce à des modèles de diapositives déjà définis.

---
<!-- _class: fppppppppp-->
Pour écrire un diaporama avec Marp, il faut :
1. Connaître la syntaxe [Markown](https://github.com/YannHY/cours/blob/master/Markdown/Apprendre%20le%20Markdown.md) (c'est très simple),
2. Savoir convertir son fichier en PDF ou en fichier html avec [Marp for VS Code](https://marketplace.visualstudio.com/items?itemName=marp-team.marp-vscode) ou [Marp CLI](https://github.com/marp-team/marp-cli)
    - Une solution plus simple, mais pour le moment moins complète : [Marp web](https://web.marp.app/)

---
<style scoped>
    ol {list-style-type:none;}
</style>
Ce diaporama a été créé avec ce système et sert à en illustrer les fonctionnalités :

1. I – Organiser son diaporama
2. II – Construire son cours
3. III – Intégrer des exercices
4. IV – Gérer la mise en page

---
<!-- _class: partie -->
# I – Organiser <br>son diaporama <!-- fit-->
Première partie

---
Pour faire une partie, une sous-partie, ou une étape, il suffit d'utiliser les codes suivants : 
1. ```<!-- _class: partie --> ```
2. ```<!-- _class: souspartie -->```
3. ```<!-- _class: etape -->```

---
<!-- _class: fppppppp -->
Pour les parties, on utilise un titre de niveau 1 (```#```), pour les sous-parties, un titre de niveau 2 (```##```), et pour les étapes, un titre de niveau 3 (```###```).

Si on veut que le titre occupe le maximum de place sur la diapositive, on ajoute, après le titre : ```<!-- fit -->```. On peut utiliser ```<br>```pour forcer le passage à la ligne.

---
<!-- _class: souspartie -->
## A. Faire une sous&#8209;partie <br>(niveau 2) <!-- fit-->
<!-- Code html trait d'union insécable :  &#8209; -->

---
<!-- _class: etape -->
### 1/ Etape (niveau 3)
On utilise la classe ```etape```
si on souhaite la faire
apparaître en pleine page

---
### 2/ Étape (niveau 3)

Le titre d'une étape de niveau 3 peut être intégré dans une diapositive avec du contenu, si on le souhaite.

Dans ce cas, on n'utilise pas de code particulier, on définit simplement un titre de niveau 3 en markdown : ```### Titre```



---
<!-- _class: partie -->
# II – Construire <br>son cours <!-- fit -->
Deuxième partie

---
<!-- _class: souspartie -->
## Explications et questions

---
On écrit son texte normalement, sans code particulier, pour faire un paragraphe simple

Pour intégrer une question que l'on veut poser aux élèves, on utilise une puce : ```- ``` qui s'affichera ainsi :

- Question posée aux élèves : ………… ?

---
<!-- _class: puces -->
<style scoped>
/* La compilation via Github ne permet pas l'usage de la balise div, mais on peut l'utiliser en compilant sur son ordinateur */
ul {
    padding-left:1.8em;
    background-color:inherit;
}
ul li {
    padding-left:0.2em;
    list-style-type: disc;
}
ul ul li {
    list-style-type:circle;
}
ul li:before {
    content:none;
}
</style>
Pour utiliser les puces ordinaires, on encadre les puces avec la balise ```<div class="puces"></div>```

- puce ordinaire
  - puce ordinaire



---
<!-- _class: fmmmmmmm centrerquestion -->

Comme il y a beaucoup de contenu dans cette diapositive (c'est déconseillé 😄), on peut réduire la taille de la police de caractère avec la class `f`(pour “font”) et on ajoute une série de “m” pour avoir une police _moins_ grande, ou une série de “p” pour avoir une police _plus_ grande. Ici la classe utilisée est : ```fmmmmmmm```

**Trois remarques** :

1) On peut faire apparaître progressivement du contenu dans des listes ordonnées en écrivant ```1)```, ```2)```, … plutôt que ```1.```, ```2.```, ….
2) Cela ne marche bien sûr que pour l'export en HTML : le fichier PDF affichera la diapositive complète.
3) On peut utiliser cet affichage progressif également pour les “puces” ordinaires, qui sont utilisées, dans ce modèle, pour afficher des questions posées aux élèves. On écrit alors ```* ``` plutôt que ```-```.

* Est-ce suffisament clair ?

---
<!-- _class: souspartie -->
## Point méthode   

---
<!-- _class: pm -->
On peut annoncer un point méthode avec la classe ```pm``` : le sigle \[PM] s'affiche dans le coin en haut à droite.

----
<!-- _class: pointmethode -->
### Point méthode
Les points méthodes sont définis par la classe ```pointmethode```

---
<!-- _class: souspartie -->
## Définition

----
<!-- _class: definition fppppppp-->

### Définition
- Le but de cet encadré est de formuler explicitement la **définition** d'un terme, mais on pourrait bien sûr imaginer d'autres usages.
- Pour créer une diapositive de ce type, on utilise la classe ```definition```

---
<!-- _class: souspartie-->
## Citations

---
<!-- _class: etape fpp-->
### Citation longue 
Les citations longues s'affichent
en pleine page, sans image

On utilise la classe ```citationL```, et la syntaxe
Markdown pour les citations (```>```).

La syntaxe pour le gras (```**Auteur**```) est
utilisée ici pour les petites majuscules.

---
<!-- _class: citationL -->
>« Peu de créatures humaines accepteraient d'être changées en animaux inférieurs sur la promesse de la plus large ration de plaisirs de bêtes ; aucun être humain intelligent ne consentirait à être un imbécile, aucun homme instruit à être un ignorant, […] même s'ils avaient la conviction que l'imbécile, l'ignorant […] sont, avec leurs lots respectifs, plus complètement satisfaits qu'eux-mêmes avec le leur. [...] Un être pourvu de facultés supérieures demande plus pour être heureux, est probablement exposé à souffrir de façon plus aiguë, et offre certainement à la souffrance plus de points vulnérables qu'un être de type inférieur, mais en dépit de ces risques, il ne peut jamais souhaiter réellement tomber à un niveau d'existence qu'il sent inférieur. Nous pouvons donner de cette répugnance le nom qu'il nous plaira [...] mais si on veut l'appeler de son vrai nom, c'est un sens de la dignité que tous les êtres humains possèdent, sous une forme ou sous une autre, et qui correspond – de façon nullement rigoureuse d'ailleurs – au développement de leurs facultés supérieures. [...] Il vaut mieux être un homme insatisfait qu'un porc satisfait ; il vaut mieux être Socrate insatisfait qu'un imbécile satisfait. »
>>John Stuart **Mill**, _L'Utilitarisme_

---
<!-- _class: etape fppp-->
### Citation de taille moyenne
Les citations de taille moyenne intègrent
une image (auteur ou couverture du livre).

On utilise la classe ```citationM1``` ou ```citationM2```
selon la taille du texte, et la syntaxe
Markdown pour les images ```![](URL)```

---
<!-- _class: citationM1 -->
![](https://upload.wikimedia.org/wikipedia/commons/thumb/b/b7/Jean-Jacques_Rousseau_%28painted_portrait%29.jpg/860px-Jean-Jacques_Rousseau_%28painted_portrait%29.jpg)
>« [L]a pitié, disposition convenable à des êtres aussi faibles, et sujets à autant de maux que nous le sommes [est une] vertu d’autant plus universelle et d’autant plus utile à l’homme qu’elle précède en lui l’usage de toute réflexion, et si naturelle que les bêtes mêmes en donnent quelquefois des signes sensibles. […] [D]e cette seule qualité découlent toutes les vertus sociales […] la générosité, la clémence, l’humanité »
>>**Rousseau**, _Discours sur l’origine et les fondements de l’inégalité parmi les hommes_, I

---
<!-- _class: citationM2 -->
![](https://upload.wikimedia.org/wikipedia/commons/thumb/b/b7/Jean-Jacques_Rousseau_%28painted_portrait%29.jpg/860px-Jean-Jacques_Rousseau_%28painted_portrait%29.jpg)
>« [L]a pitié, disposition convenable à des êtres aussi faibles, et sujets à autant de maux que nous le sommes [est une] vertu d’autant plus universelle et d’autant plus utile à l’homme qu’elle précède en lui l’usage de toute réflexion, et si naturelle que les bêtes mêmes en donnent quelquefois des signes sensibles. […] [D]e cette seule qualité découlent toutes les vertus sociales […] la générosité, la clémence, l’humanité »
>>**Rousseau**, _Discours sur l’origine et les fondements de l’inégalité parmi les hommes_, I

---
<!-- _class: etape fpppppp-->
### Citation courte
On utilise la classe ```citationC```.

Pour l'image, on utilise la syntaxe
Mardown ```![bg left:40%](URL)```
pour mettre l'image à gauche
(on peut régler le pourcentage)

---
<!-- _class: citationC -->
![bg left:40%](https://upload.wikimedia.org/wikipedia/commons/e/ea/Spinoza.jpg)
>« Les hommes sont conscients de leurs désirs et ignorants des causes qui les déterminent ! »
>>**Spinoza**, *Lettre 58 à Schuller*


---
<!-- _class: souspartie -->
## Lectures et approfondissement

---
<!-- _class: entete lecture fppp-->
### Lectures

On utilise la classe ```entete``` pour faire apparaître le titre de niveau 3 en haut avec un fond grisé, et on ajoute ```lecture``` si on souhaite faire apparaître l'icône “livre”.
Une liste ordonnée peut être utile ici pour indiquer les lectures à faire : 
1. Première lecture possible
2. Deuxième lecture possible
3. ...


---
<!-- _class: entete approfondissement fppppppp-->
### Pour aller plus loin

On utilise à nouveau la classe ```entete```.

On ajoute ```approfondissement``` si on souhaite faire apparaître l'icône “escalade”.

---
<!-- _class: souspartie -->
## Usage du cinéma : affiche + résumé

---
<!-- _class: fppppppp -->
On utilise la classe ```cinema```.

Pour l'image (affiche ou photogramme), on utilise la syntaxe Markdown ```![](URL)```. Pour le résumé, on utilise la syntaxe pour les citations ```>```.

On peut également faire en sorte que l'image soit cliquable pour renvoyer vers une vidéo en ligne : ```[![](URL-image)](URL-vidéo-en-ligne)```

---
<!-- _class: cinema fmmmmmmmmmm-->

[![](https://raw.githubusercontent.com/eyssette/marp-slides/master/slides/images/scarface.png)](https://safeYouTube.net/w/kg3J)

> « Antonio “Tony” Montana (Al Pacino) […] est un petit malfrat cubain qui migre vers Miami dans l'espoir de faire fortune. Il trouve au départ un petit boulot dans une baraque à frites de Miami. Mais travailler pour quelques dollars ne correspond pas à l'idée qu'il se fait du « rêve américain ». Il se fait alors embaucher par un malfrat local puis par Frank Lopez, son patron]. […] Tony apprend vite le métier de mafioso de la drogue : il monte en grade […] Il a les dents beaucoup plus longues que ses collègues, il est mégalomane, ambitieux et d'une intelligence plus perverse. Il prend pour adage : _The World is Yours_ (Le monde est à toi) [...] Mais il commence à faire des erreurs dans ce monde qui ne pardonne pas, où l'on est vite remplacé. Il prend conscience que d'être arrivé au sommet de la mafia ne le rend pas aussi heureux qu'il l'avait espéré, qu'il n'est pas capable de rendre heureuses les personnes qu'il aime&nbsp;» (source : [wikipedia](https://fr.wikipedia.org/wiki/American_History_X))


---
<!-- _class: souspartie -->
## Images, schémas, photogrammes

Voir la partie IV pour la mise en page


---
<!-- _class: souspartie -->
## Tableaux récapitulatifs

---
<!-- _class: fpppppp-->
On utilise la syntaxe Markdown pour les tableaux. Il faudra généralement diminuer la taille de la police.

Si on veut faire apparaître progressivement le contenu du tableau (avec l'export HTML), on peut utiliser la syntaxe : ```<div data-marpit-fragment>Texte</div>``` dans chaque cellule.


---
<!-- _class: fmmmmmm -->
|| Pertinence |Limites|
|:-|:-:|:--:|
|**Relativisme culturel** | Paragraphe explicatif. Paragraphe explicatif. Paragraphe explicatif.|Paragraphe explicatif. Paragraphe explicatif. Paragraphe explicatif.|
| **Morale de la<br>sensibilité** | Paragraphe explicatif. Paragraphe explicatif. Paragraphe explicatif. |Paragraphe explicatif. Paragraphe explicatif. Paragraphe explicatif. |
| **Morale des<br> conséquences** | Paragraphe explicatif. Paragraphe explicatif. Paragraphe explicatif. |Paragraphe explicatif. Paragraphe explicatif. Paragraphe explicatif. |
|**Morale des<br> principes** | Paragraphe explicatif. Paragraphe explicatif. Paragraphe explicatif. |Paragraphe explicatif. Paragraphe explicatif. Paragraphe explicatif.|

---
<!-- _class: partie -->
# III – Intégrer <br>des exercices <!-- fit-->
Troisième partie

---
<!-- _class: souspartie -->
## Exercice type :<br> QCM

---
<!-- _class: fpppppppp -->
On utilise la classe ```qcm```. L'icône “question” est automatiquement intégrée.

Pour poser la question, on utilise une puce ```-```, et une liste ordonnée ```1.```, ```2.```… pour les propositions.

Pour la correction, on copie-colle la diapositive, et on indique la réponse en utilisant la syntaxe pour le gras : ```**réponse**```.

---
<!-- _class: qcm --> 
- Comment peut-on distinguer le bonheur du plaisir ?

1. Le bonheur est un état de satisfaction partiel qui provient d’un jugement sur la vie en général
2. Le bonheur est un état de satisfaction global, et non pas durable
3. Le bonheur est un état de satisfaction durable causé par un fait particulier
4. Le bonheur est un état de satisfaction global qui provient d’un jugement sur la vie en général

---
<!-- _class: qcm --> 
- Comment peut-on distinguer le bonheur du plaisir ?

1. Le bonheur est un état de satisfaction partiel qui provient d’un jugement sur la vie en général
2. Le bonheur est un état de satisfaction global, et non pas durable
3. Le bonheur est un état de satisfaction durable causé par un fait particulier
4. **Le bonheur est un état de satisfaction global qui provient d’un jugement sur la vie en général**

---
<!-- _class: souspartie -->
## Exercice type : tableau de distinctions

---
<!-- _class: fppp -->
On utilise la classe ```exercice tableau```, la syntaxe Markdown pour le tableau, et une liste ordonnée ```1.```, ```2.```, … pour les propositions de réponses.

Pour la correction, on crée une autre diapositive, on copie-colle le tableau, et on inscrit les propositions au bon endroit. On utilise la classe ```exercice tableau-r``` pour cette diapositive.

On peut décider de garder les numéros des propositions : il faut alors utiliser la syntaxe pour l'italique (```_1_```ou ```*1*```), afin de les faire apparaître en grisé.

---
<!-- _class: etape -->
### 1) Tableau simple 

---
<!-- _class: exercice tableau -->
| Le bonheur est un état de satisfaction … |Le plaisir est un état de satisfaction …|
|:--:|:--:|
|?|?|
|?|?|
|?|?|

1. qui provient d’un jugement général sur la vie
2. durable
3. global
4. éphémère
5. partiel
6. qui provient d’un fait particulier

---
<!-- _class: exercice tableau-r fpppp--> 
<!-- TODO : Utiliser du bleu (pour la couleur de la conceptualisation) -->
| Le bonheur est un état de satisfaction <br/>… |Le plaisir est un état de satisfaction <br/>…|
|:--:|:--:|
|*3* global|*5* partiel|
|*2* durable|*4* éphémère|
|*1* qui provient d’un <br>jugement général<br> sur la vie|*6* qui provient d’un<br> fait particulier|

---
<!-- _class: etape fpppp -->
### 2) Tableau avec propositions de réponse en deux colonnes

Si le tableau est complexe, on peut disposer les propositions de réponse en colonnes : on ajoute simplement la classe ```colonnes```

---
<!-- _class: exercice tableau colonnes -->
| La contrainte |L'obligation|
|:--:|:--:|
|?|?|
|?|?|
|?|?|

1. Exemple : la menace (« je dois lui donner mon argent ») ; l'arbre sur la route (« je dois faire demi-tour »)
2. Elle réside dans la conscience intérieure
3. Exemple : le médecin face à son patient (« je dois lui dire la vérité »)
4. Les autres options ne sont pas rationnellement envisageables (pas réalisables ou bien trop risquées ou coûteuses pour moi)
5. Elle réside dans un élément extérieur
6. Les autres options ne sont pas acceptables du point de vue de certaines valeurs ou normes sociales, juridiques, morales

---
<!-- _class: souspartie -->
## Exercice type : argumentation

---
<!-- _class:  fppppppppp-->
Le but de ce type d'exercice est soit de trouver la prémisse intermédiaire qui permet de parvenir à une conclusion, soit la conclusion que l'on peut déduire de deux prémisses.

Pour cette diapositive, on utilise la classe ```exercice argumentation```, et une liste ordonnée pour les deux prémisses et la conclusion.

---
<!-- _class: exercice argumentation fppppppp -->
1. Le désir est un état de manque
2. ………………………………
3. Désirer, c'est souffrir


---
<!-- _class: exercice argumentation -->
1. Le  bonheur est un idéal, non de la raison, mais de l'imagination
2. L'imagination produit des images vagues et non des concepts précis et déterminés
3. ………………………………

---
<!-- _class: souspartie -->
## Exercice type : Application des connaissances

---
<!-- _class: fppppp -->
Les exercices d'application sont des exercices de rédaction (un paragraphe).

Pour cette diapositive, on utilise la classe ```exercice application```, un titre de niveau 3 (```###```), une puce pour la question (```-```), et une liste ordonnée pour les propositions de sujet (```1.```, ```2.```, …).


---
<!-- _class: exercice application -->  

### Exercice : application des connaissances 
- Rédiger un paragraphe (150 mots minimum), qui répond à l'un de ces sujets, avec un argument qui mobilise le cours sur le stoïcisme :
1. Le désir nous rend-il aveugle ?
1. Est-il raisonnable de lutter contre le temps ?
1. Le bonheur dépend-il de nous ?
1. La réflexion est-elle un obstacle au bonheur ?
1. Le bonheur se trouve-t-il dans le plaisir ?
1. Le bonheur peut-il s’apprendre ?

---
<!-- _class: souspartie -->

## Exercice type : discussion


---
<!-- _class: entete discussion -->

### Discussion

<br>On utilise la classe ```entete``` et on ajoute ```discussion``` si on souhaite faire apparaître l'icône associée à ce type d'exercice. 

---
<!-- _class: souspartie -->
## Exercice type : travaux de groupe

---
<!-- _class: entete groupe -->
### Travail en groupe

<br>On utilise la classe ```entete``` et on ajoute ```groupe``` si on souhaite faire apparaître l'icône associée à ce type d'exercice. 

---
<!-- _class: partie -->
# IV – Mises <br>en page
Quatrième partie

---
<!-- _class: souspartie -->
## A. Avec une image

---
<!-- _class: etape fppppppp -->
### 1) Une image, sans texte
On utilise la classe ```i1t0```
(image : 1 / texte : 0)

On ajoute ```pp```si on veut utiliser
le mode pleine page

L'image se redimensionne automatiquement pour occuper le maximum de place sur la diapositive

---
<!-- _class: i1t0 pp -->
![](https://i.ibb.co/DbydYNJ/plan.png)
<!-- https://www.pastery.net/buhwpe/  -->

---
<!-- _class: i1t0 pp -->
![](https://www.decorarconarte.com/WebRoot/StoreES2/Shops/61552482/4775/FD5E/B35F/5A2B/2D91/C0A8/28B9/489F/37229_Rafael_ml.jpg)
<!-- https://www.pastery.net/buhwpe/  -->

---
<!-- _class: i1t0 -->
![](https://i.ibb.co/DbydYNJ/plan.png)
<!-- https://www.pastery.net/buhwpe/  -->

---
<!-- _class: i1t0 -->
![](https://www.decorarconarte.com/WebRoot/StoreES2/Shops/61552482/4775/FD5E/B35F/5A2B/2D91/C0A8/28B9/489F/37229_Rafael_ml.jpg)
<!-- https://www.pastery.net/buhwpe/  -->

---
<!-- _class: etape fmmmmm -->

### 2) Une image + un bloc de texte <!-- fit -->

On utilise la classe ```i1t1 vertical```  pour un alignement vertical, ou la classe ```i1t1 horizontal``` pour un alignement horizontal.

La disposition (en haut ou en bas, à gauche ou à droite)
dépend de l'ordre dans lequel vous avez placé l'image
et le texte dans votre fichier en Markdown.

On peut ajouter ```pp``` pour avoir un affichage en pleine page.

---
<!-- _class: i1t1 vertical -->
![](https://pbs.twimg.com/media/ETu0VirWoAgwlqs.jpg)

Un extrait de Minority Report [+](https://drive.google.com/file/d/10Rz6T-5OkkDlnwSzHse2SnyMd7ZiT-HF/view?usp=sharing)


---
<!-- _class: i1t1 vertical -->
<style scoped>
    section p:first-child {padding-bottom:5px;}
</style>
Platon : le mythe d'Aristophane 

![](https://vignette.wikia.nocookie.net/lettresantiques/images/7/78/Clivage-de-landrogyne.jpg/revision/latest?cb=20141118131404&path-prefix=fr)

---
<!-- _class: i1t1 vertical fmmmmmmmm-->

![](https://upload.wikimedia.org/wikipedia/commons/0/07/Le_Caravage_-_L%27incr%C3%A9dulit%C3%A9_de_Saint_Thomas.jpg)

- Comment peut-on chercher à prouver la vérité d'un jugement de fait ?


---
<!-- _class: i1t1 vertical -->

![](https://i.ibb.co/DbydYNJ/plan.png)

Plan du cours

---
<!-- _class: i1t1 vertical pp -->

Plan du cours

![](https://i.ibb.co/DbydYNJ/plan.png)

---

<!-- _class: i1t1 vertical pp -->

![](https://www.decorarconarte.com/WebRoot/StoreES2/Shops/61552482/4775/FD5E/B35F/5A2B/2D91/C0A8/28B9/489F/37229_Rafael_ml.jpg)

Platon et Aristote

---

En cas d'alignement vertical, le bloc de texte est conçu pour ne pas être très grand (une ou deux lignes).

Si on souhaite avoir une image plus petite, on peut le faire en transformant le style de mise en page seulement pour cette diapositive :

``` <style scoped> section img {height:510px;} </style>```

---
<!-- _class: i1t1 vertical pp fmmmm-->
<style scoped>
    section img {height:510px;}
</style>

![](https://www.tate.org.uk/art/images/work/T/T07/T07573_9.jpg)

- Pourquoi cet objet ne semble-t-il pas, à première vue, être une œuvre d’art ? Qu’attendons-nous d’une œuvre d’art ?
- Quel est, à votre avis, le sens du geste de Duchamp ? Que cherche-t-il à faire ?

---
<!-- _class: i1t1 horizontal -->
![](https://www.decorarconarte.com/WebRoot/StoreES2/Shops/61552482/4775/FD5E/B35F/5A2B/2D91/C0A8/28B9/489F/37229_Rafael_ml.jpg)

Platon et Aristote : détail de la fresque _L'école d'Athènes_  

---
<!-- _class: i1t1 horizontal fppppppp -->
![](https://cdn.pixabay.com/photo/2015/04/06/19/56/boy-709943_1280.jpg)

- Manger du chocolat, est-ce le bonheur ?

---
<!-- _class: i1t1 horizontal pp contain-->

Par défaut, l'image est zoomée pour correspondre au cadre prédéfini.<br>
Si on souhaite que l'image soit redimensionnée automatiquement pour qu'on puisse la voir dans son intégralité, on ajoute la classe ```contain```

![](https://www.decorarconarte.com/WebRoot/StoreES2/Shops/61552482/4775/FD5E/B35F/5A2B/2D91/C0A8/28B9/489F/37229_Rafael_ml.jpg)



---
<!-- _class: etape fpp-->
### 3) Une image + deux <br>blocs de texte

On utilise la classe ```i1t2```, un titre de 
niveau 3 (```### Titre```), et un bloc de texte,
qui se positionne automatiquement à droite
ou à gauche  selon l'ordre par rapport à
l'image dans le fichier Markdown.

On peut ajouter ```pp```pour un
affichage en pleine page.

---
<!-- _class: i1t2 -->
### Raphaël, _L'École d'Athènes_

L'École d'Athènes est une fresque du peintre italien Raphaël, qui présente les figures majeures de la pensée antique.

![](https://www.decorarconarte.com/WebRoot/StoreES2/Shops/61552482/4775/FD5E/B35F/5A2B/2D91/C0A8/28B9/489F/37229_Rafael_ml.jpg)



---
<!-- _class: i1t2 fm-->
### Raphaël, _L'École d'Athènes_

![](https://www.decorarconarte.com/WebRoot/StoreES2/Shops/61552482/4775/FD5E/B35F/5A2B/2D91/C0A8/28B9/489F/37229_Rafael_ml.jpg)

L'École d'Athènes est une fresque du peintre italien Raphaël, qui présente les figures majeures de la pensée antique.

---
<!-- _class: i1t2 pp -->

### Raphaël, _L'École d'Athènes_

L'École d'Athènes est une fresque du peintre italien Raphaël, qui présente les figures majeures de la pensée antique.

![](https://www.decorarconarte.com/WebRoot/StoreES2/Shops/61552482/4775/FD5E/B35F/5A2B/2D91/C0A8/28B9/489F/37229_Rafael_ml.jpg)


---
<!-- _class: souspartie -->
## B. Avec deux images

---
<!-- _class: etape -->
### 1) Deux images : alignement horizontal
On utilise la classe ```i2t0``` (aucun texte) ou ```i2t1``` (titre en haut).
Par défaut l'alignement est horizontal.

On ajoute ```pp```si on veut un
affichage en pleine page.

---
<!-- _class: i2t0 -->

### Platon et Aristote

![](https://upload.wikimedia.org/wikipedia/commons/1/1b/Raffael_067.jpg)

![](https://upload.wikimedia.org/wikipedia/commons/e/e3/Raffael_061.jpg)

---
<!-- _class : i2t1 rapprocher contain fmmmmm-->

- Que peut-on dire à propos de la question du déterminisme biologique en l’état actuel de nos connaissances ?

![](https://static.fnac-static.com/multimedia/images_produits/ZoomPE/4/5/4/9782738115454/tsp20130828140529/Existe-t-il-des-genes-du-comportement.jpg)

![](https://images-na.ssl-images-amazon.com/images/I/51Anet6cFzL._SX328_BO1,204,203,200_.jpg)


---
<!-- _class: etape -->
### 1) Deux images : alignement vertical
On utilise la classe : ```i2t0```,
et on ajoute ```vertical```si on veut un alignement vertical des deux images.

On ajoute ```pp``` pour
l'affichage en pleine page.

---
<!-- _class: fppp -->
On peut décaler la zone affichée de l'image en changeant le style de la diapositive.

<br>Par exemple :  

```<style scoped> p:nth-child(1) img {object-position:0px -40px} </style>```

---
<!-- _class: i2t0 vertical pp -->
<style scoped>
    p:nth-child(1) img {object-position:0px -40px}
</style>

![](https://static.usbeketrica.com/images/thumb_840xh/5b51b6806d0e2.jpg)

![](https://pbs.twimg.com/media/ETu0VirWoAgwlqs.jpg)

---
<!-- _class: souspartie -->
## C. Avec trois images

---
<!-- _class: fppp -->
On utilise la classe ```i3t0``` et la syntaxe ```![bg contain](URL)``` pour les trois images.

On ajoute la classe ```pp``` pour un affichage en pleine page.

Pour un alignement vertical, on utilise la même syntaxe, sauf pour la première image, où l'on met : ```![bg contain vertical](URL)```.

On peut supprimer le mot clé ```contain``` : l'image sera alors zoomée pour correspondre automatiquement au cadre prédéfini.

---
<!-- _class: i3t0 -->

![bg contain](https://fr.web.img5.acsta.net/medias/nmedia/18/83/23/81/19672460.jpg)
![bg contain](https://cenicienta.fr/wp-content/uploads/2018/02/pocahontas.jpg)
![bg contain](https://www.filmspourenfants.net/wp-content/uploads/2018/01/avatar-a-376x500.jpg)

---
<!-- _class: i3t0 vertical pp -->

![bg contain vertical](https://s.yimg.com/uu/api/res/1.2/PQRflV1fICGi5BDeo0gMGg--~B/aD0yNDA7dz00MjU7YXBwaWQ9eXRhY2h5b24-/https://www.blogcdn.com/massively.joystiq.com/media/2008/12/smeagol_1-sms-1208.jpg)
![bg contain](https://i.imgur.com/AEiMmrN.jpg)
![bg](https://i.ytimg.com/vi/UYpRSs7pzJo/maxresdefault.jpg)


---
<!-- _class: souspartie -->
## D. Avec quatre images

---
On utilise la classe ```i4t0```.

On ajoute ```pp```pour un affichage en pleine page.

---
<!-- _class: i4t0 pp -->
<style scoped>
    p:nth-child(2) img {object-position:0px -20px}
</style>

![](https://upload.wikimedia.org/wikipedia/commons/thumb/a/ae/StillLifeWithASkull.jpg/1564px-StillLifeWithASkull.jpg)

![](https://upload.wikimedia.org/wikipedia/commons/d/d2/Georges_de_La_Tour_-_The_Penitent_Magdalen_-_WGA12339.jpg)

![](https://upload.wikimedia.org/wikipedia/commons/3/35/Pieter_van_Steenwyck_001.jpg)

![](https://upload.wikimedia.org/wikipedia/commons/thumb/3/31/Edwaert_Collier_-_Vanitas_-_Still_Life_with_Books_and_Manuscripts_and_a_Skull_-_Google_Art_Project.jpg/1474px-Edwaert_Collier_-_Vanitas_-_Still_Life_with_Books_and_Manuscripts_and_a_Skull_-_Google_Art_Project.jpg)


---
<!-- _class: souspartie -->
## E. Mises en page complexes

---

Pour contrôler précisément la disposition de chaque élément sur une diapositive, on peut utiliser une grille.

On utilise la classe ```grille```. On peut tout d'abord s'aider avec un quadrillage, que l'on fait apparaître, temporairement, avec la classe ```quadrillage```.

On dispose alors les éléments avec la propriété CSS ```grid-area```.

---
<!-- _class: grille quadrillage -->
<style scoped>
section *:nth-child(1) {font-size:inherit;grid-area: 1 / 1 / 1 / -1; }
section *:nth-child(2) {font-size:inherit;grid-area: 1 / 1 / -1 / -1; display:none!important;}
section *:nth-child(3) {font-size:inherit;grid-area: 1 / 1 / -1 / -1; display:none!important;}
section *:nth-child(4) {font-size:inherit;grid-area: 1 / 1 / -1 / -1 ;display:none!important;}
section *:nth-child(5) {font-size:inherit;grid-area: 1 / 1 / -1 / -1 ;display:none!important;}
</style>


---
<!-- _class: grille  -->
<style scoped>
section *:nth-child(1) {font-size:inherit;grid-area: 7 / 6 / 25 / -6 }
section *:nth-child(2) {font-size:inherit;grid-area: 32 / 6 / -25 / -6; }
section *:nth-child(3) {font-size:29px;grid-area: 32 / 22 / -8 / -6  ;}
section *:nth-child(4) {font-size:inherit;grid-area: 2 / 2 / -2 / -2 ;display:none!important;}
section *:nth-child(5) {font-size:inherit;grid-area: 2 / 2 / -2 / -2 ;display:none!important;}
</style>

Cette idée que l'harmonie se définit objectivement par des rapports numériques, par des proportions définies, correspond à la **conception pythagoricienne du Beau**.

![](https://upload.wikimedia.org/wikipedia/commons/1/1a/Kapitolinischer_Pythagoras_adjusted.jpg)

- Lire le texte de la diapositive suivante (Carole Talon-Hugon, _L’antiquité grecque_ (2014), chapitre II : « Qu’est-ce que le beau ? »), et répondre aux questions suivantes :
- Pourquoi Pythagore affirme-t-il que le principe de toutes choses est dans le nombre ?
- Quelles ont été les applications de cette idée en architecture, en peinture et dans la sculpture ?
 

---

Ce thème pour le logiciel [Marp](https://marp.app/) s'intitule _teaching_. Vous pouvez l'utiliser pour vos diapositives, le modifier. Il est [publié sur Github](https://github.com/eyssette/teaching-theme-for-marp).

Merci de me faire part de vos usages, de vos remarques et de vos suggestions d'amélioration !

- Email : cedric.eyssette@gmail.com
