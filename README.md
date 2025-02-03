Analyse des Données de Laboratoire sur les Infections Virales
Ce répertoire contient un projet d'analyse des données de laboratoire liées aux infections virales, utilisant des techniques statistiques avancées comme l'Analyse des Correspondances Multiples (ACM) et les arbres de décision en R.

Contenu du Répertoire
Le répertoire contient plusieurs fichiers et scripts pour charger, analyser et visualiser les données cliniques liées aux infections virales, y compris des arbovirus.

TBL_ARBO.xlsx : Fichier Excel contenant les données des résultats de tests sérologiques et moléculaires, ainsi que d'autres informations pertinentes sur les patients et les échantillons.

Ce fichier doit être chargé dans le script R pour effectuer les analyses.
Script d'Analyse (analyse_labo.Rmd) : Script R Markdown qui exécute les opérations suivantes :

Chargement des bibliothèques nécessaires.
Importation et préparation des données : Le fichier Excel est chargé, et des recodages de variables sont effectués pour faciliter l'analyse.
Recodage des variables : Transformation des variables en facteurs ou en types appropriés (dates, caractères, facteurs).
Recodage des résultats sérologiques : Pour certains virus, les résultats sont codés de manière spécifique.
Visualisation des données : Des graphiques sont générés pour examiner la distribution des variables sélectionnées.
Analyse des Correspondances Multiples (ACM) : L'ACM est effectuée sur des sous-ensembles de données spécifiques pour explorer les relations entre différentes variables qualitatives.
Arbres de décision : Des arbres de décision sont générés pour examiner les relations entre certaines variables, comme les résultats ARN de différents virus.
Arbre de Décision et Visualisation : Le script génère des arbres de décision pour explorer les relations entre différentes variables, telles que la présence de l'ARN du virus, et les visualise sous forme graphique.

Dépendances
Pour exécuter ce script, vous devez installer les bibliothèques R suivantes :

readxl : Pour importer des données depuis des fichiers Excel.
FactoMineR : Pour effectuer des analyses de correspondances multiples (ACM).
factoextra : Pour la visualisation des résultats ACM.
corrplot : Pour afficher des matrices de corrélation.
rpart : Pour créer des arbres de décision.
rpart.plot : Pour visualiser les arbres de décision.
Vous pouvez installer ces packages en exécutant les commandes suivantes dans R :

r
Copier
Modifier
install.packages("readxl")
install.packages("FactoMineR")
install.packages("factoextra")
install.packages("corrplot")
install.packages("rpart")
install.packages("rpart.plot")
Étapes de l'Analyse
Chargement et préparation des données :

Le fichier TBL_ARBO.xlsx est chargé et les variables sont recodées pour garantir une interprétation correcte. Les variables sont converties en facteurs ou caractères selon leur nature, et les dates sont traitées correctement.
Recodage des résultats sérologiques et viraux :

Les résultats sérologiques sont recodés pour chaque virus étudié (par exemple, Ebola, Marburg, Lassa), afin de différencier les statuts "positif", "négatif", et autres catégories spécifiques.
Visualisation des données :

Des graphiques de distribution sont créés pour certaines variables, telles que les résultats ARN et IgM, ainsi que les informations géographiques (région, site) et démographiques (sexe, âge).
Analyse des correspondances multiples (ACM) :

L'ACM est réalisée sur les données d'ARN pour explorer les relations entre les différents virus. Des graphiques sont générés pour visualiser les résultats de l'ACM, et les axes principaux sont analysés pour identifier des patterns.
Arbres de décision :

Des arbres de décision sont générés pour analyser les relations entre certaines variables, telles que l'ARN du virus RVF et le virus WN ou Chikungunya. Les arbres permettent d'identifier les relations complexes et les facteurs prédictifs.
Résultats attendus
Une fois le script exécuté, vous obtiendrez les résultats suivants :

Graphiques de distribution pour examiner la répartition des résultats sérologiques et ARN.
Résultats de l'ACM pour explorer les relations entre les variables cliniques et virales.
Arbres de décision pour déterminer les relations prédictives entre les résultats des tests sérologiques et ARN des différents virus.
Conclusion et Interprétation
L'analyse des correspondances multiples permet d'identifier des relations entre les variables qualitatives (ARN de virus, statut sérologique, sexe, etc.).
Les arbres de décision aident à comprendre quelles variables influencent les résultats des tests ARN pour les virus étudiés.
Contributeurs
Serigne Fallou Mbacke NGOM : Développeur principal et auteur du projet.
