# Travailler avec les données : Python et la bibliothèque Pandas

| ![ Sketchnote par [(@sketchthedocs)](https://sketchthedocs.dev) ](../../sketchnotes/07-WorkWithPython.png) |
| :-------------------------------------------------------------------------------------------------------: |
|                 Travailler avec Python - _Sketchnote par [@nitya](https://twitter.com/nitya)_                 |

[![Vidéo d'introduction](../../../../translated_images/fr/video-ds-python.245247dc811db8e4.webp)](https://youtu.be/dZjWOGbsN4Y)

Bien que les bases de données offrent des moyens très efficaces de stocker des données et de les interroger en utilisant des langages de requête, la méthode la plus flexible de traitement des données est d'écrire votre propre programme pour manipuler les données. Dans de nombreux cas, effectuer une requête en base de données serait une méthode plus efficace. Cependant, dans certains cas où un traitement de données plus complexe est nécessaire, cela ne peut pas être fait facilement avec SQL.
Le traitement des données peut être programmé dans n'importe quel langage de programmation, mais certains langages sont plus haut niveau en ce qui concerne le travail avec les données. Les data scientists préfèrent généralement l'un des langages suivants :

* **[Python](https://www.python.org/)**, un langage de programmation à usage général, considéré souvent comme l'une des meilleures options pour les débutants grâce à sa simplicité. Python possède de nombreuses bibliothèques supplémentaires qui peuvent vous aider à résoudre de nombreux problèmes pratiques, comme extraire vos données d'une archive ZIP, ou convertir une image en niveaux de gris. En plus de la science des données, Python est souvent utilisé pour le développement web.
* **[R](https://www.r-project.org/)** est une boîte à outils traditionnelle développée pour le traitement statistique des données. Elle contient également un vaste dépôt de bibliothèques (CRAN), ce qui en fait un bon choix pour le traitement des données. Cependant, R n’est pas un langage de programmation à usage général, et est rarement utilisé en dehors du domaine de la science des données.
* **[Julia](https://julialang.org/)** est un autre langage développé spécifiquement pour la science des données. Il est destiné à offrir de meilleures performances que Python, ce qui en fait un excellent outil pour l'expérimentation scientifique.

Dans cette leçon, nous nous concentrerons sur l'utilisation de Python pour un traitement simple des données. Nous supposerons une familiarité de base avec ce langage. Si vous souhaitez un tour plus approfondi de Python, vous pouvez vous référer à l'une des ressources suivantes :

* [Apprenez Python de manière ludique avec Turtle Graphics et les fractales](https://github.com/shwars/pycourse) - Cours d'introduction rapide à la programmation Python sur GitHub
* [Faites vos premiers pas avec Python](https://docs.microsoft.com/en-us/learn/paths/python-first-steps/?WT.mc_id=academic-77958-bethanycheum) Parcours d’apprentissage sur [Microsoft Learn](http://learn.microsoft.com/?WT.mc_id=academic-77958-bethanycheum)

Les données peuvent se présenter sous plusieurs formes. Dans cette leçon, nous examinerons trois formes de données : **les données tabulaires**, **le texte** et **les images**.

Nous nous concentrerons sur quelques exemples de traitement des données, au lieu de vous donner une vue d'ensemble complète de toutes les bibliothèques associées. Cela vous permettra de saisir l'idée principale de ce qui est possible, et de comprendre où trouver des solutions à vos problèmes lorsque vous en aurez besoin.

> **Conseil le plus utile**. Lorsque vous devez effectuer une certaine opération sur des données que vous ne savez pas comment faire, essayez de la rechercher sur internet. [Stackoverflow](https://stackoverflow.com/) contient généralement beaucoup d'exemples de code utiles en Python pour de nombreuses tâches typiques.



## [Quiz avant la conférence](https://ff-quizzes.netlify.app/en/ds/quiz/12)

## Données tabulaires et Dataframes

Vous avez déjà rencontré des données tabulaires lorsque nous avons parlé des bases de données relationnelles. Lorsque vous avez beaucoup de données contenues dans plusieurs tables liées, il est effectivement judicieux d'utiliser SQL pour travailler avec elles. Cependant, il y a beaucoup de cas où nous disposons d'une table de données et devons obtenir une **compréhension** ou des **informations** sur ces données, telles que la distribution, la corrélation entre les valeurs, etc. En science des données, il y a beaucoup de cas où nous devons effectuer certaines transformations sur les données originales, suivies de visualisation. Ces deux étapes peuvent être facilement réalisées avec Python.

Il existe deux bibliothèques très utiles en Python qui peuvent vous aider avec les données tabulaires :
* **[Pandas](https://pandas.pydata.org/)** vous permet de manipuler les **Dataframes**, qui sont analogues aux tables relationnelles. Vous pouvez avoir des colonnes nommées et effectuer différentes opérations sur les lignes, les colonnes et les Dataframes en général.
* **[Numpy](https://numpy.org/)** est une bibliothèque pour travailler avec les **tenseurs**, c'est-à-dire des **tableaux** multidimensionnels. Un tableau a des valeurs du même type sous-jacent, il est plus simple qu’un DataFrame, mais offre plus d'opérations mathématiques et crée moins de surcharge.

Il y a également quelques autres bibliothèques que vous devriez connaître :
* **[Matplotlib](https://matplotlib.org/)** est une bibliothèque utilisée pour la visualisation des données et le traçage de graphes
* **[SciPy](https://www.scipy.org/)** est une bibliothèque avec des fonctions scientifiques supplémentaires. Nous avons déjà rencontré cette bibliothèque en parlant de probabilité et de statistiques

Voici un extrait de code que vous utilisez typiquement pour importer ces bibliothèques au début de votre programme Python :
```python
import numpy as np
import pandas as pd
import matplotlib.pyplot as plt
from scipy import ... # vous devez spécifier les sous-paquets exacts dont vous avez besoin
``` 

Pandas est centré autour de quelques concepts de base.

### Series

**Series** est une séquence de valeurs, similaire à une liste ou à un tableau numpy. La principale différence est que la série a aussi un **index**, et lorsque nous opérons sur les séries (ex., les additionner), l'index est pris en compte. L'index peut être aussi simple que le numéro entier de ligne (c'est l'index utilisé par défaut lors de la création d'une série à partir d'une liste ou d'un tableau), ou il peut avoir une structure complexe, comme un intervalle de dates.

> **Note** : Il y a un peu de code introductif sur Pandas dans le carnet associé [`notebook.ipynb`](notebook.ipynb). Nous ne présentons ici que quelques exemples, et vous êtes bien sûr invités à consulter le carnet complet.

Considérons un exemple : nous voulons analyser les ventes de notre glacier. Générons une série de nombres de ventes (nombre d’articles vendus chaque jour) pour une période donnée :

```python
start_date = "Jan 1, 2020"
end_date = "Mar 31, 2020"
idx = pd.date_range(start_date,end_date)
print(f"Length of index is {len(idx)}")
items_sold = pd.Series(np.random.randint(25,50,size=len(idx)),index=idx)
items_sold.plot()
```
![Graphique de séries temporelles](../../../../translated_images/fr/timeseries-1.80de678ab1cf727e.webp)

Supposons maintenant que chaque semaine nous organisons une fête pour des amis, et prenons 10 paquets de glace supplémentaires pour la fête. Nous pouvons créer une autre série, indexée par semaine, pour le démontrer :
```python
additional_items = pd.Series(10,index=pd.date_range(start_date,end_date,freq="W"))
```
Quand nous additionnons deux séries ensemble, nous obtenons le nombre total :
```python
total_items = items_sold.add(additional_items,fill_value=0)
total_items.plot()
```
![Graphique de séries temporelles](../../../../translated_images/fr/timeseries-2.aae51d575c55181c.webp)

> **Note** que nous n'utilisons pas la syntaxe simple `total_items+additional_items`. Si nous le faisions, nous obtiendrions beaucoup de valeurs `NaN` (*Not a Number*) dans la série résultante. C’est parce qu’il manque des valeurs pour certains points de l’index dans la série `additional_items`, et ajouter `NaN` à quoi que ce soit donne `NaN`. Nous devons donc spécifier le paramètre `fill_value` lors de l’addition.

Avec les séries temporelles, nous pouvons également **rééchantillonner** la série avec des intervalles de temps différents. Par exemple, supposons que nous voulons calculer la moyenne mensuelle des volumes de vente. Nous pouvons utiliser le code suivant :
```python
monthly = total_items.resample("1M").mean()
ax = monthly.plot(kind='bar')
```
![Moyennes mensuelles des séries temporelles](../../../../translated_images/fr/timeseries-3.f3147cbc8c624881.webp)

### DataFrame

Un DataFrame est essentiellement une collection de séries ayant le même index. Nous pouvons combiner plusieurs séries ensemble dans un DataFrame :
```python
a = pd.Series(range(1,10))
b = pd.Series(["I","like","to","play","games","and","will","not","change"],index=range(0,9))
df = pd.DataFrame([a,b])
```
Cela créera une table horizontale comme celle-ci :
|     | 0   | 1    | 2   | 3   | 4      | 5   | 6      | 7    | 8    |
| --- | --- | ---- | --- | --- | ------ | --- | ------ | ---- | ---- |
| 0   | 1   | 2    | 3   | 4   | 5      | 6   | 7      | 8    | 9    |
| 1   | I   | like | to  | use | Python | and | Pandas | very | much |

Nous pouvons aussi utiliser des Series comme colonnes, et spécifier les noms des colonnes avec un dictionnaire :
```python
df = pd.DataFrame({ 'A' : a, 'B' : b })
```
Cela nous donnera une table comme celle-ci :

|     | A   | B      |
| --- | --- | ------ |
| 0   | 1   | I      |
| 1   | 2   | like   |
| 2   | 3   | to     |
| 3   | 4   | use    |
| 4   | 5   | Python |
| 5   | 6   | and    |
| 6   | 7   | Pandas |
| 7   | 8   | very   |
| 8   | 9   | much   |

**Note** que nous pouvons aussi obtenir cette disposition en transposant la table précédente, par exemple en écrivant 
```python
df = pd.DataFrame([a,b]).T.rename(columns={ 0 : 'A', 1 : 'B' })
```
Ici, `.T` signifie l'opération de transposition du DataFrame, c’est-à-dire le changement de lignes en colonnes, et l’opération `rename` nous permet de renommer les colonnes pour correspondre à l'exemple précédent.

Voici quelques-unes des opérations les plus importantes que nous pouvons effectuer sur les DataFrames :

**Sélection de colonne**. Nous pouvons sélectionner des colonnes individuelles en écrivant `df['A']` - cette opération retourne une Series. Nous pouvons aussi sélectionner un sous-ensemble de colonnes dans un autre DataFrame en écrivant `df[['B','A']]` - cela retourne un autre DataFrame.

**Filtrer** seulement certaines lignes selon des critères. Par exemple, pour ne retenir que les lignes dont la colonne `A` est supérieure à 5, on peut écrire `df[df['A']>5]`.

> **Note** : Le filtrage fonctionne ainsi. L'expression `df['A']<5` retourne une série booléenne, indiquant si l'expression est `True` ou `False` pour chaque élément de la série originale `df['A']`. Quand une série booléenne est utilisée comme index, elle retourne un sous-ensemble de lignes dans le DataFrame. Il n’est donc pas possible d'utiliser une expression booléenne Python arbitraire, par exemple écrire `df[df['A']>5 and df['A']<7]` serait incorrect. À la place, vous devez utiliser l'opération spéciale `&` sur les séries booléennes, en écrivant `df[(df['A']>5) & (df['A']<7)]` (*les parenthèses sont importantes ici*).

**Créer de nouvelles colonnes calculables**. Nous pouvons facilement créer de nouvelles colonnes calculables dans notre DataFrame en utilisant des expressions intuitives comme celle-ci :
```python
df['DivA'] = df['A']-df['A'].mean() 
``` 
Cet exemple calcule la divergence de A par rapport à sa valeur moyenne. Ce qui se passe réellement ici, c'est que nous calculons une série, puis affectons cette série à la gauche, créant une nouvelle colonne. Nous ne pouvons donc pas utiliser d'opérations qui ne sont pas compatibles avec les séries, par exemple, le code ci-dessous est erroné :
```python
# Code incorrect -> df['ADescr'] = "Low" si df['A'] < 5 sinon "Hi"
df['LenB'] = len(df['B']) # <- Résultat incorrect
``` 
Le dernier exemple, bien que syntaxiquement correct, donne un résultat erroné, car il assigne la longueur de la série `B` à toutes les valeurs de la colonne, et non la longueur des éléments individuels comme nous le voulions.

Si nous devons calculer des expressions complexes comme celle-ci, nous pouvons utiliser la fonction `apply`. Le dernier exemple peut s'écrire ainsi :
```python
df['LenB'] = df['B'].apply(lambda x : len(x))
# ou
df['LenB'] = df['B'].apply(len)
```

Après les opérations ci-dessus, nous obtiendrons le DataFrame suivant :

|     | A   | B      | DivA | LenB |
| --- | --- | ------ | ---- | ---- |
| 0   | 1   | I      | -4.0 | 1    |
| 1   | 2   | like   | -3.0 | 4    |
| 2   | 3   | to     | -2.0 | 2    |
| 3   | 4   | use    | -1.0 | 3    |
| 4   | 5   | Python | 0.0  | 6    |
| 5   | 6   | and    | 1.0  | 3    |
| 6   | 7   | Pandas | 2.0  | 6    |
| 7   | 8   | very   | 3.0  | 4    |
| 8   | 9   | much   | 4.0  | 4    |

**Sélectionner des lignes selon leur position** peut se faire avec la construction `iloc`. Par exemple, pour sélectionner les 5 premières lignes du DataFrame :
```python
df.iloc[:5]
```

**Groupement** est souvent utilisé pour obtenir un résultat semblable aux *tableaux croisés dynamiques* dans Excel. Supposons que nous voulions calculer la valeur moyenne de la colonne `A` pour chaque valeur de `LenB`. Nous pouvons alors grouper notre DataFrame par `LenB` et appeler `mean` :
```python
df.groupby(by='LenB')[['A','DivA']].mean()
```
Si nous devons calculer la moyenne et le nombre d’éléments dans le groupe, nous pouvons utiliser la fonction plus complexe `aggregate` :
```python
df.groupby(by='LenB') \
 .aggregate({ 'DivA' : len, 'A' : lambda x: x.mean() }) \
 .rename(columns={ 'DivA' : 'Count', 'A' : 'Mean'})
```
Cela nous donne le tableau suivant :

| LenB | Count | Mean     |
| ---- | ----- | -------- |
| 1    | 1     | 1.000000 |
| 2    | 1     | 3.000000 |
| 3    | 2     | 5.000000 |
| 4    | 3     | 6.333333 |
| 6    | 2     | 6.000000 |

### Récupérer les données


Nous avons vu à quel point il est facile de construire des Series et des DataFrames à partir d'objets Python. Cependant, les données proviennent généralement sous forme de fichier texte ou de tableau Excel. Heureusement, Pandas nous offre un moyen simple de charger des données depuis le disque. Par exemple, lire un fichier CSV est aussi simple que cela :
```python
df = pd.read_csv('file.csv')
```
Nous verrons plus d'exemples de chargement de données, y compris leur récupération depuis des sites web externes, dans la section "Challenge"


### Impression et Tracé

Un Data Scientist doit souvent explorer les données, il est donc important de pouvoir les visualiser. Lorsque le DataFrame est volumineux, souvent on veut juste s'assurer que tout est correct en affichant les premières lignes. Cela peut être fait en appelant `df.head()`. Si vous l'exécutez depuis Jupyter Notebook, cela affichera le DataFrame sous une forme tabulaire agréable.

Nous avons également vu l'utilisation de la fonction `plot` pour visualiser certaines colonnes. Bien que `plot` soit très utile pour de nombreuses tâches et supporte différents types de graphiques via le paramètre `kind=`, vous pouvez toujours utiliser la bibliothèque brute `matplotlib` pour tracer quelque chose de plus complexe. Nous aborderons la visualisation des données en détail dans des leçons distinctes.

Cette vue d'ensemble couvre les concepts les plus importants de Pandas, cependant, la bibliothèque est très riche, et il n'y a pas de limite à ce que vous pouvez faire avec ! Appliquons maintenant ces connaissances pour résoudre un problème spécifique.

## 🚀 Challenge 1 : Analyse de la propagation du COVID

Le premier problème sur lequel nous allons nous concentrer est la modélisation de la propagation épidémique du COVID-19. Pour ce faire, nous utiliserons les données sur le nombre d'individus infectés dans différents pays, fournies par le [Center for Systems Science and Engineering](https://systems.jhu.edu/) (CSSE) de [l'Université Johns Hopkins](https://jhu.edu/). Le jeu de données est disponible dans [ce dépôt GitHub](https://github.com/CSSEGISandData/COVID-19).

Comme nous voulons montrer comment traiter les données, nous vous invitons à ouvrir [`notebook-covidspread.ipynb`](notebook-covidspread.ipynb) et à le lire de haut en bas. Vous pouvez aussi exécuter les cellules, et réaliser certains défis que nous avons laissés pour vous à la fin.

![Propagation du COVID](../../../../translated_images/fr/covidspread.f3d131c4f1d260ab.webp)

> Si vous ne savez pas comment exécuter du code dans Jupyter Notebook, jetez un œil à [cet article](https://soshnikov.com/education/how-to-execute-notebooks-from-github/).

## Travailler avec des données non structurées

Bien que les données soient très souvent sous forme tabulaire, dans certains cas il est nécessaire de traiter des données moins structurées, par exemple, du texte ou des images. Dans ce cas, pour appliquer les techniques de traitement des données vues ci-dessus, nous devons d'une manière ou d'une autre **extraire** des données structurées. Voici quelques exemples :

* Extraire des mots-clés du texte, et voir la fréquence d'apparition de ces mots-clés
* Utiliser des réseaux neuronaux pour extraire des informations sur les objets dans une image
* Obtenir des informations sur les émotions des personnes via un flux vidéo de caméra

## 🚀 Challenge 2 : Analyse des articles COVID

Dans ce challenge, nous continuerons sur le sujet de la pandémie de COVID, en nous concentrant sur le traitement d'articles scientifiques à ce sujet. Il existe un [jeu de données CORD-19](https://www.kaggle.com/allen-institute-for-ai/CORD-19-research-challenge) avec plus de 7000 (au moment de la rédaction) articles sur le COVID, disponible avec les métadonnées et les résumés (et pour environ la moitié d'entre eux, le texte complet est aussi fourni).

Un exemple complet d'analyse de ce jeu de données en utilisant le service cognitif [Text Analytics for Health](https://docs.microsoft.com/azure/cognitive-services/text-analytics/how-tos/text-analytics-for-health/?WT.mc_id=academic-77958-bethanycheum) est décrit [dans cet article de blog](https://soshnikov.com/science/analyzing-medical-papers-with-azure-and-text-analytics-for-health/). Nous discuterons d'une version simplifiée de cette analyse.

> **NOTE** : Nous ne fournissons pas une copie du jeu de données dans ce dépôt. Vous devrez d'abord télécharger le fichier [`metadata.csv`](https://www.kaggle.com/allen-institute-for-ai/CORD-19-research-challenge?select=metadata.csv) depuis [ce jeu de données sur Kaggle](https://www.kaggle.com/allen-institute-for-ai/CORD-19-research-challenge). Une inscription à Kaggle peut être requise. Vous pouvez également télécharger le jeu de données sans inscription [depuis ici](https://ai2-semanticscholar-cord-19.s3-us-west-2.amazonaws.com/historical_releases.html), mais cela inclura tous les textes complets en plus du fichier de métadonnées.

Ouvrez [`notebook-papers.ipynb`](notebook-papers.ipynb) et lisez-le de haut en bas. Vous pouvez aussi exécuter les cellules et relever les défis que nous avons laissés pour vous à la fin.

![Traitement médical du Covid](../../../../translated_images/fr/covidtreat.b2ba59f57ca45fbc.webp)

## Traitement des données d’images

Récemment, des modèles d'IA très puissants ont été développés pour nous permettre de comprendre les images. De nombreuses tâches peuvent être résolues en utilisant des réseaux neuronaux pré-entraînés ou des services cloud. Voici quelques exemples :

* **Classification d'images**, qui peut vous aider à classer l'image dans l'une des catégories prédéfinies. Vous pouvez facilement entraîner vos propres classificateurs d'images en utilisant des services tels que [Custom Vision](https://azure.microsoft.com/services/cognitive-services/custom-vision-service/?WT.mc_id=academic-77958-bethanycheum)
* **Détection d'objets** pour détecter différents objets dans l'image. Des services comme [computer vision](https://azure.microsoft.com/services/cognitive-services/computer-vision/?WT.mc_id=academic-77958-bethanycheum) peuvent détecter plusieurs objets courants, et vous pouvez entraîner un modèle [Custom Vision](https://azure.microsoft.com/services/cognitive-services/custom-vision-service/?WT.mc_id=academic-77958-bethanycheum) pour détecter certains objets spécifiques d’intérêt.
* **Détection des visages**, y compris la détection de l'âge, du genre et des émotions. Cela peut être réalisé via [Face API](https://azure.microsoft.com/services/cognitive-services/face/?WT.mc_id=academic-77958-bethanycheum).

Tous ces services cloud peuvent être appelés en utilisant des [SDK Python](https://docs.microsoft.com/samples/azure-samples/cognitive-services-python-sdk-samples/cognitive-services-python-sdk-samples/?WT.mc_id=academic-77958-bethanycheum), et peuvent donc être facilement intégrés dans votre flux de travail d'exploration des données.

Voici quelques exemples d'exploration des données à partir de sources d'images :
* Dans l'article de blog [Comment apprendre la Data Science sans coder](https://soshnikov.com/azure/how-to-learn-data-science-without-coding/) nous explorons les photos Instagram, en essayant de comprendre ce qui fait que les gens aiment plus une photo. Nous extrayons d'abord autant d'informations que possible des images en utilisant [computer vision](https://azure.microsoft.com/services/cognitive-services/computer-vision/?WT.mc_id=academic-77958-bethanycheum), puis utilisons [Azure Machine Learning AutoML](https://docs.microsoft.com/azure/machine-learning/concept-automated-ml/?WT.mc_id=academic-77958-bethanycheum) pour construire un modèle interprétable.
* Dans [Facial Studies Workshop](https://github.com/CloudAdvocacy/FaceStudies) nous utilisons [Face API](https://azure.microsoft.com/services/cognitive-services/face/?WT.mc_id=academic-77958-bethanycheum) pour extraire les émotions des personnes sur des photographies d'événements, afin d'essayer de comprendre ce qui rend les gens heureux.

## Conclusion

Que vous ayez déjà des données structurées ou non structurées, en utilisant Python vous pouvez effectuer toutes les étapes liées au traitement et à la compréhension des données. C'est probablement la manière la plus flexible de traiter les données, et c’est la raison pour laquelle la majorité des data scientists utilisent Python comme outil principal. Apprendre Python en profondeur est probablement une bonne idée si vous êtes sérieux dans votre parcours en data science !

## [Quiz post-conférence](https://ff-quizzes.netlify.app/en/ds/quiz/13)

## Révision & Auto-apprentissage

**Livres**
* [Wes McKinney. Python for Data Analysis : Manipulation de données avec Pandas, NumPy et IPython](https://www.amazon.com/gp/product/1491957662)

**Ressources en ligne**
* Tutoriel officiel [10 minutes to Pandas](https://pandas.pydata.org/pandas-docs/stable/user_guide/10min.html)
* [Documentation sur la visualisation avec Pandas](https://pandas.pydata.org/pandas-docs/stable/user_guide/visualization.html)

**Apprendre Python**
* [Apprendre Python de manière ludique avec Turtle Graphics et Fractales](https://github.com/shwars/pycourse)
* [Faites vos premiers pas avec Python](https://docs.microsoft.com/learn/paths/python-first-steps/?WT.mc_id=academic-77958-bethanycheum) Parcours d'apprentissage sur [Microsoft Learn](http://learn.microsoft.com/?WT.mc_id=academic-77958-bethanycheum)

## Devoir

[Effectuer une étude de données plus détaillée pour les défis ci-dessus](assignment.md)

## Crédits

Cette leçon a été réalisée avec ♥️ par [Dmitry Soshnikov](http://soshnikov.com)

---

<!-- CO-OP TRANSLATOR DISCLAIMER START -->
**Avertissement** :
Ce document a été traduit à l'aide du service de traduction automatique [Co-op Translator](https://github.com/Azure/co-op-translator). Bien que nous nous efforçions d'assurer l'exactitude, veuillez noter que les traductions automatisées peuvent contenir des erreurs ou des inexactitudes. Le document original dans sa langue native doit être considéré comme la source faisant autorité. Pour les informations critiques, il est recommandé de recourir à une traduction professionnelle réalisée par un humain. Nous ne saurions être tenus responsables des malentendus ou erreurs d'interprétation découlant de l'utilisation de cette traduction.
<!-- CO-OP TRANSLATOR DISCLAIMER END -->