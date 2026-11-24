# Fiche détaillée — AURELIS Operations Intelligence

Document préparé le 17 octobre 2026 pour solliciter un avis externe sur l'amélioration du dashboard. Les sections 15 à 21 détaillent la disposition des pages, le système visuel, les formats et les visualisations.

## 1. Présentation et positionnement

**Nom :** AURELIS Operations Intelligence, également présenté dans le projet comme AURELIS Global Supply — Interactive Operations Dashboard.

**Auteur indiqué :** Armel Asopjio.

**Nature :** application interactive de pilotage des opérations et d'aide à la décision, développée en R Shiny. Elle réunit des tableaux de bord de direction, le suivi commercial, les achats, les livraisons, les stocks, les créances clients, la préparation de devis et un laboratoire d'analyse statistique.

**Version examinée :** projet local dont la documentation et le manifeste décrivent une mise à jour Analysis Lab datée du 15 octobre 2026.

**Statut :** démonstration fonctionnelle utilisant des données synthétiques. Les montants et entreprises affichés ne constituent pas des résultats réels d'entreprise. Le niveau de préparation à un déploiement en production reste à évaluer.

**Proposition de valeur :** relier performance financière, relations commerciales et exécution opérationnelle afin de passer d'un indicateur global à un client, une commande, un fournisseur ou une action à examiner.

## 2. Utilisateurs et décisions visés

| Public | Besoins couverts |
|---|---|
| Direction générale | Vue consolidée, rentabilité, concentration du portefeuille, exposition clients et surveillance des opérations |
| Managers | Performance des équipes, charge des acheteurs, retards et priorités opérationnelles |
| Acheteurs et approvisionnement | Comparaison des fournisseurs, historique des commandes, coûts et délais |
| Commercial et gestion de clientèle | Performance client, historique de relation, devis et documents à partager |
| Finance et recouvrement | Facturation, soldes impayés, ancienneté des créances et relevés clients |
| Logistique et magasin | Disponibilité des articles, réceptions attendues, reliquats et risque de livraison |
| Analystes | Exploration de fichiers, qualité des données, tests, prévisions, régressions et scénarios |

Ces publics sont déduits des fonctions présentes. Le nombre réel d'utilisateurs, leurs usages quotidiens et leurs attentes n'ont pas été documentés dans cette analyse.

## 3. Organisation et navigation

L'application possède une barre latérale regroupant les espaces de travail, ainsi qu'une barre supérieure avec filtres année/mois, rafraîchissement, accès aux rapports et exports, commande de navigation et changement de thème.

Les principaux ensembles sont :

- **Command Center :** vue exécutive, centre des KPI, atlas mondial et observatoire d'activité.
- **Commercial Intelligence :** ventes, rentabilité, performance clients, relevés, commandes et activité des acheteurs.
- **Supply Chain Control :** commandes/livraisons, stocks, fournisseurs et créances.
- **Workspace & Studio :** espace utilisateur, devis et intelligence produit.
- **Data & Relationships :** annuaire, relations, données de démonstration et documentation des processus.
- **Analysis Lab et Probability Studio :** exploration et analyse quantitative.

Le raccourci Ctrl+K ou Cmd+K ouvre une palette permettant de rechercher et rejoindre un espace. Les intitulés de l'interface sont principalement en anglais.

## 4. Description des espaces fonctionnels

### 4.1 Executive Overview — synthèse de direction

La page d'accueil affiche quatre indicateurs principaux : chiffre d'affaires reconnu, bénéfice brut, créances restantes et nombre de commandes d'achat suivies.

Elle comporte une courbe du chiffre d'affaires et du bénéfice brut, un tableau de performance clients et un résumé décisionnel calculé. Le tableau présente chiffre d'affaires, bénéfice brut, marge, part du chiffre d'affaires, nombre de lignes de facturation et encours. Sélectionner un client ouvre son espace de performance.

Le résumé attire l'attention sur la marge brute pondérée, la part du chiffre d'affaires des cinq premiers clients et le solde des créances échues. Il propose un accès au suivi des créances. Des vues complémentaires présentent les principaux clients, le bénéfice par représentant, la contribution des pays et une comparaison annuelle.

### 4.2 KPI Command Center

Espace de suivi transversal : tendances des indicateurs de management, état des KPI opérationnels, contribution des clients et charge/valeur des commandes par acheteur.

**Question métier :** quels indicateurs et équipes nécessitent une attention particulière sur la période choisie ?

### 4.3 Global Network Atlas

Carte interactive des clients, fournisseurs et représentants. Navigation géographique du continent vers le pays, la région, la ville et la relation individuelle. Des panneaux présentent la relation sélectionnée, les répartitions géographiques et les connexions commerciales. Des commandes permettent de réinitialiser la carte, focaliser une sélection et ouvrir un espace associé.

### 4.4 Executive Activity Observatory

Espace orienté direction pour consulter les actions enregistrées, les sessions actives et les engagements de livraison à venir, avec des éléments de gouvernance des accès. Le code prévoit une restriction de cet observatoire au profil CEO.

La présence de ces vues dans une démonstration ne prouve pas l'existence d'un dispositif complet d'audit et d'authentification en production.

### 4.5 Sales & Profitability

Suivi du chiffre d'affaires, des coûts, du bénéfice brut, de la marge pondérée et du nombre de transactions. Analyse mensuelle, comparaison des représentants, contribution des pays et détail des résultats. Une vue compare la marge à une cible.

### 4.6 Customer Performance

Fiche de relation client réunissant historique commercial, commandes distinctes, temps d'exécution prévu, taux de réalisation des quantités, statut de livraison, contribution des fournisseurs et couverture par les acheteurs.

Elle comprend une vue annuelle de la collaboration, un positionnement dans le portefeuille et des éléments destinés à un document client. Un export PDF de présentation de la relation est proposé.

### 4.7 Client Statements

Consultation d'un compte client : total facturé, montant restant dû, pourcentage payé, nombre de factures, ancienneté des soldes, chronologie et relevé détaillé. Export CSV du relevé.

### 4.8 POs & Buyers et Buyer Activity

Analyse du volume et de la valeur des commandes par mois et par acheteur. Tableaux de synthèse et journal détaillé des commandes. L'activité des acheteurs peut être explorée du niveau annuel au mois, à la semaine et au jour, avec classement, répartition des clients et journal d'activité.

### 4.9 Orders & Delivery

Suivi des statuts de livraison, charge par date, matrice de risque, calendrier, exposition ouverte par client et statut, planning priorisé et historique détaillé des commandes. Des exports sont proposés sur cette page.

### 4.10 Inventory & Warehouse

Deux dimensions sont présentées : disponibilité en magasin et approvisionnements/réceptions attendus.

- Stock physique, quantités allouées, disponibles et en commande.
- Statut du stock, seuil de réapprovisionnement, couverture et valeur par entrepôt.
- Matrice de priorité de réapprovisionnement et détail des articles.
- Valeur ouverte par fournisseur, quantités attendues par client, articles en attente et profil des échéances.

Certains intitulés mentionnent le « temps réel », mais la version étudiée repose sur des fichiers et leur rafraîchissement. La fraîcheur réelle dépend donc des sources.

### 4.11 Suppliers & Procurement

Atelier de sélection des fournisseurs, annuaire de produits/services vendeurs, comparaison de coûts et délais, synthèse des livraisons et de l'exposition, valeur des commandes ouvertes et recherche dans l'historique des commandes.

### 4.12 Accounts Receivable

Suivi des soldes par tranche d'ancienneté, tendances factures/encours, répartition par responsable, exposition client et grand livre détaillé des créances.

L'ancienneté repose notamment sur les champs disponibles dans l'instantané source, dont `Days_Past_Due`. Ce n'est pas une consultation bancaire en direct.

### 4.13 My Workspace

Identification du propriétaire de l'espace, visibilité sur les sessions et activités, gestion de brouillons de devis personnels ou partagés. Des profils CEO, Manager, Analyst et Buyer sont présents dans la logique d'accès.

Les brouillons sont stockés dans un environnement mémoire du processus R, avec numéro de version. Leur conservation durable après redémarrage et leur partage entre plusieurs processus ne sont pas assurés par ce mécanisme. Une partie du journal d'activité est écrite dans un fichier CSV.

### 4.14 Quotation Studio & Finance Engine

Processus structuré de préparation des devis :

1. Identité du devis et sélection du client.
2. Reprise d'une commande historique et consultation des habitudes de paiement.
3. Saisie/modification des lignes et coûts fournisseurs, import CSV, ajout, duplication et suppression de lignes.
4. Prise en compte des frais spécifiques et du coût rendu.
5. Simulation des charges de financement et échéanciers.
6. Politique commerciale et provision pour aléas.
7. Calcul du prix final et revue des scénarios.
8. Prévisualisation et export du devis PDF et du classeur de calcul Excel.

Le module propose également création, sauvegarde et réouverture de brouillons, ainsi que l'ajout de produits depuis le catalogue.

### 4.15 Product Intelligence

Exploration du catalogue, recommandations de produits, proposition prioritaire, comparaison des coûts et délais et préparation d'un brief de réponse à une demande client.

La présence du terme « intelligence » ou « recommandation » ne signifie pas qu'un modèle d'IA générative externe est connecté.

### 4.16 Directory & Relationships

Annuaire des contacts et relations, fiche de relation, historique mensuel, flux acheteur–client–vendeur, contreparties importantes et historique des interactions de commande. Un formulaire permet d'enregistrer un nouveau client ; sa durabilité doit être évaluée séparément avant un usage réel.

### 4.17 Demo Data & Process

Présentation des sources synthétiques, commandes de rafraîchissement, diagnostics de schéma/import, état des connexions et documentation des processus. Des notes peuvent être enregistrées pour la session.

Les références à Access et QuickBooks décrivent des perspectives d'intégration ou du contexte historique ; la version documentée ne fournit pas de connexion opérationnelle à ces systèmes.

## 5. Analysis Lab — laboratoire analytique

### Sources, exploration et préparation

Découverte des fichiers pris en charge dans `data/`, y compris les sous-dossiers. Formats : CSV, TSV, Excel avec choix de feuille, RDS tabulaire et JSON tabulaire. Import d'un fichier local jusqu'à 100 Mo, limité à la session, sans écraser les sources.

Les contrôles comprennent recherche globale, sélection des colonnes visibles, recherche par colonne, tri multiple, pagination côté serveur et inspection d'une ligne. Les filtres s'adaptent au type des colonnes : plages numériques, dates, catégories ou recherche textuelle pour forte cardinalité. Les filtres structurés se combinent avec AND. Une option conserve les valeurs manquantes et une autre retire les doublons.

L'export CSV respecte les colonnes sélectionnées et les recherches du tableau, sur l'ensemble des résultats correspondants. Les textes susceptibles d'être interprétés comme formules de tableur sont préfixés pour limiter leur exécution automatique.

### Profile

Distribution, boîte à moustaches, graphique quantile–quantile normal et statistiques descriptives : moyenne, dispersion, quantiles, asymétrie, kurtosis et intervalle de confiance de la moyenne. Contrôles des valeurs manquantes, doublons exacts et observations atypiques.

### Hypothesis tests

Tests t à un échantillon, t de Welch, Mann–Whitney, ANOVA de Welch, Kruskal–Wallis et Shapiro–Wilk. Réglage du seuil alpha, des alternatives applicables et du niveau de confiance ; tailles d'effet pour les tests t.

Les hypothèses d'indépendance doivent être vérifiées, notamment pour plusieurs lignes d'une même commande. Aucune correction automatique des comparaisons multiples ni conclusion causale n'est annoncée.

### Trends & forecast

Agrégation par semaine, mois, trimestre ou année, en total ou moyenne. Prévision linéaire de référence avec intervalles de prédiction, horizon de 1 à 12 périodes. Au moins six périodes calendaires consécutives sont nécessaires. Les périodes absentes ne sont pas inventées.

Cette méthode ne constitue pas un modèle saisonnier validé en production. La saisonnalité, l'autocorrélation et les périodes incomplètes peuvent affecter sa précision.

### Drivers

Corrélations de Pearson/Spearman, régression linéaire multiple jusqu'à huit prédicteurs, coefficients et diagnostics des résidus. Les associations ne démontrent pas une causalité. Les identifiants et identités arithmétiques entre chiffre d'affaires, coût et bénéfice peuvent produire des résultats trompeurs.

### Scenarios

Rééchantillonnage empirique avec variation de moyenne, dispersion et graine reproductible. Choix de 1 000, 5 000 ou 10 000 simulations et comparaison de cas de base, favorable et défavorable. Il s'agit d'une analyse de sensibilité d'observations individuelles, pas d'une prévision de trésorerie ni d'une VaR de portefeuille.

### Financial metrics

Indicateurs calculés à partir des champs reconnus : revenus, coûts, bénéfice, exposition sur factures et réalisation des quantités. Calculateur d'investissement à partir de flux annuels constants saisis par l'utilisateur et actualisés en fin d'année.

Les métriques nécessitant un bilan ou une trésorerie détaillée, comme la liquidité, le ROE et la durée de trésorerie disponible, ne sont pas fournies sans les données nécessaires.

### Chart builder

Barres, courbes, nuages de points et boîtes à moustaches ; transformations z-score et logarithme des valeurs positives. Les barres/courbes agrègent des moyennes ; les barres retiennent les 30 premières catégories. Limites présentes : 30 catégories pour les boîtes et 30 000 lignes pour le nuage de points.

Création d'une mesure de session `Calculated_Metric` avec une expression arithmétique contrôlée. Le moteur n'évalue pas du code R arbitraire.

### Probability Studio

Modèles normal, Student, F, log-normal, exponentiel, gamma, Poisson et empirique. Calculs de probabilités cumulées, queues gauche/droite, intervalles et quantiles, avec graphiques et comparaisons de groupes.

## 6. Périmètre des filtres et des calculs

- Les pages métier et la vue exécutive utilisent les filtres année/mois de l'en-tête.
- Analysis Lab utilise sa propre source et ses propres filtres. Les filtres de l'en-tête ne réduisent pas silencieusement les fichiers importés.
- Les filtres structurés du Lab s'appliquent aux analyses ; les recherches propres au tableau concernent le tableau et son export CSV.
- Le retrait des observations atypiques concerne les analyses statistiques, pas les données sources, les totaux des ratios financiers ni le constructeur de graphiques.
- Probability Studio conserve ses contrôles et le périmètre temporel de l'en-tête.

Ces différences de périmètre constituent un point important à examiner pour la compréhension des chiffres et la cohérence de navigation.

## 7. Données disponibles

Comptages réalisés sur les CSV présents dans le projet lors de la rédaction :

| Source | Lignes | Contenu principal |
|---|---:|---|
| Revenue | 1 896 | Dates, clients, factures, commandes, chiffre d'affaires, coûts, bénéfice, pays, représentants |
| Accounts Receivable | 1 896 | Factures, échéances, soldes, conditions et ancienneté |
| Daily PO | 2 025 | Commandes, clients, acheteurs, dates et valeur |
| Inventory | 10 255 | Lignes de commande, quantités, réceptions, reliquats et livraisons |
| Warehouse | 800 | Articles, entrepôts, stocks, seuils, demande et valorisation |
| Customers | 180 | Entreprises, segments, conditions et responsables |
| Customer Reference | 180 | Référentiel clients et délais de paiement |
| Suppliers | 85 | Fournisseurs, pays et indice de fiabilité |
| Products | 800 | Articles, catégories, coûts et fournisseurs préférés |
| Seller Catalog | 2 517 | Produits/services fournisseurs, coûts, délais, MOQ et devises |
| Contacts | 607 | Contacts, fonctions et rattachements |
| Directory | 710 | Relations, coordonnées et types de contact |
| Geography | 279 | Entités, coordonnées et hiérarchie géographique |
| Terms Reference | 7 | Répartition des échéanciers de paiement |
| Activity Log | 147 | Événements enregistrés ; volume évolutif |

Deux autres CSV, `Aurelis_User_Clients.csv` et `client_inquiry_records.csv`, sont présents ; aucun enregistrement n'a été retourné par leur lecture lors de cet inventaire.

Le manifeste annonce les années 2018 à 2026. Un commentaire historique en tête d'`app.R` mentionne une plage différente ; les dates réellement présentes doivent être la référence pour préciser la couverture de chaque source.

**Attention à la granularité :** une ligne de facture, une commande distincte, une ligne d'article et un contact représentent des objets différents. Les jointures et agrégations doivent éviter les doubles comptes. La quantité de commandes et le nombre de lignes d'inventaire ne sont pas directement comparables.

## 8. Design et expérience utilisateur

Le style actuel privilégie un fond sombre proche de l'obsidienne, des panneaux gris foncé, des accents menthe et bleu, des bordures discrètes et peu d'effets décoratifs. Une variante claire de l'espace de travail est disponible, avec préférence mémorisée dans le navigateur ; la navigation reste sombre.

La typographie utilise notamment Segoe UI/system sans-serif, une hiérarchie compacte et des chiffres tabulaires. Les tableaux sont denses et les graphiques interactifs utilisent Plotly. Les styles prévoient adaptation responsive et réduction des animations.

La capture de la page d'accueil montre un bandeau de quatre KPI, un graphique principal à gauche, le résumé décisionnel à droite et le tableau clients en dessous. Les montants peuvent être longs et l'application comporte de nombreuses destinations dans la barre latérale.

**Éléments à faire évaluer :** lisibilité des petites tailles de texte, densité de navigation, hiérarchie des priorités, comportement mobile, distinction entre filtres globaux et locaux, compréhension des unités et possibilité d'agir après avoir identifié un problème. La conformité d'accessibilité n'a pas été auditée ici.

## 9. Architecture et exploitation

- **Exécution :** R, Shiny et bs4Dash.
- **Données et calculs :** dplyr, tidyr, lubridate, readxl et fonctions statistiques R.
- **Affichage :** ggplot2, Plotly, DT, CSS et JavaScript.
- **Dépendances complémentaires :** certains exports ou formats nécessitent des packages optionnels, notamment openxlsx, pagedown ou jsonlite.
- **Lancement local :** `shiny::runApp(".")` depuis le projet.
- **Rafraîchissement :** manuel et cycle de rafraîchissement documenté à 300 secondes ; ce mécanisme ne transforme pas les fichiers en sources temps réel.
- **Organisation :** `app.R` centralise encore une grande partie de l'application, sur environ 900 Ko ; des modules distincts existent dans `R/` pour le laboratoire, son moteur et la vue exécutive.
- **Tests présents :** validations du moteur, contrôles réactifs Shiny, chargement de l'application, doublons d'identifiants et scripts de vérification navigateur.

L'existence de ces tests a été vérifiée dans les fichiers. Ils n'ont pas été exécutés pour rédiger cette fiche. Aucune mesure de charge, de latence ou de capacité multiutilisateur n'a été réalisée.

## 10. Limites et points à distinguer des fonctions présentes

1. **Données synthétiques :** la pertinence métier sur de vraies données reste à valider.
2. **IA :** les briefs documentés reposent sur des calculs et règles explicites. Aucun envoi à un modèle génératif externe n'est décrit.
3. **Authentification :** présence de profils de démonstration et d'un mécanisme conditionnel de connexion par configuration ; les sélecteurs de propriétaire/profil ne suffisent pas à établir une identité sécurisée. La documentation prévoit une intégration d'authentification d'entreprise pour la production.
4. **Collaboration :** sessions et brouillons locaux existent ; une collaboration durable et distribuée demanderait un stockage et une architecture adaptés.
5. **Intégrations :** les connexions opérationnelles à Access, QuickBooks ou d'autres bases externes restent à réaliser pour cette version.
6. **Prévision et statistiques :** méthodes utiles à l'exploration, avec hypothèses et limites explicites ; validation métier et temporelle nécessaire avant décision automatisée.
7. **Rapports :** les possibilités d'export varient selon les pages. Le Lab fournit du CSV et l'export d'images Plotly ; aucun rapport analytique PDF/Excel complet n'y est promis.
8. **Production :** sauvegardes, reprise après incident, concurrence d'écriture, supervision, contrôle d'accès aux données et gestion des dépendances restent des sujets d'évaluation.

## 11. Parcours utiles pour une évaluation externe

- **Direction :** ouvrir l'Overview, choisir une période, identifier une exposition, ouvrir le client puis examiner ses créances.
- **Acheteur :** sélectionner un client/produit, comparer les fournisseurs, consulter les coûts et délais puis préparer un devis.
- **Logistique :** repérer une commande à risque, consulter les quantités reçues et les reliquats, puis examiner le fournisseur et l'échéance.
- **Finance :** sélectionner les créances échues, identifier les clients prioritaires et produire un relevé.
- **Analyste :** importer un fichier, contrôler sa qualité, filtrer les observations, comparer des groupes, étudier une tendance et exporter les résultats.

Pour chaque parcours, demander si l'utilisateur comprend la situation, identifie la prochaine action et peut la réaliser ou la transmettre à un responsable.

## 12. Informations encore nécessaires pour un avis contextualisé

Secteur et pays de déploiement ; taille de l'entreprise ; utilisateurs simultanés ; trois décisions les plus fréquentes ; difficultés actuelles ; volumes futurs ; fréquence de mise à jour attendue ; systèmes à connecter ; devises et langues ; hébergement ; exigences de sécurité ; budget et temps disponibles.

Ces éléments ne doivent pas être inventés par l'IA évaluatrice. Elle peut formuler des hypothèses clairement identifiées et poser les questions les plus déterminantes.

## 13. Consigne prête à transmettre à d'autres IA

> Je développe AURELIS Operations Intelligence. La fiche ci-dessus décrit les fonctions et limites observées de mon dashboard R Shiny. Je souhaite un avis critique, concret et adapté à son état actuel.
>
> Analyse le produit selon l'utilité métier, l'UX/UI, la navigation, la cohérence des KPI, la qualité des données, les statistiques, les devis, la collaboration, la sécurité, les performances et la maintenabilité.
>
> Commence par identifier les points forts et les cinq problèmes qui limiteraient le plus son adoption ou la qualité des décisions. Distingue ce qui est établi par la fiche de tes hypothèses et des points nécessitant un test. Si tu n'as pas de capture, ne prétends pas avoir évalué le rendu visuel.
>
> Propose ensuite au maximum quinze améliorations, classées par priorité. Pour chaque proposition, précise : problème rencontré, utilisateur concerné, changement concret, bénéfice attendu, effort faible/moyen/élevé, dépendances et critère mesurable de réussite. Indique si la fonction existe déjà et doit être améliorée, ou si elle serait nouvelle.
>
> Donne un exemple de page d'accueil améliorée et deux parcours métier plus efficaces. Réutilise les fonctions existantes avant de proposer de nouveaux modules. Explique les compromis et les fonctions que tu simplifierais ou regrouperais.
>
> Termine par une feuille de route à 30, 60 et 90 jours, avec une séparation entre gains rapides, consolidation technique et évolutions majeures. Reste compatible avec R Shiny lorsque c'est pertinent ; justifie toute proposition de changement de technologie. N'ajoute de l'IA générative que si elle résout un besoin précis, avec ses données nécessaires et un moyen de vérifier ses résultats.
>
> Pose enfin les cinq questions dont les réponses changeraient le plus tes recommandations. Évite les conseils génériques et les fonctions déjà présentes dans la fiche.

## 14. Pièces à joindre pour améliorer les avis

Joindre cette fiche et, idéalement, les captures déjà disponibles :

- `exports/overview-final.png` : vue exécutive sombre.
- `exports/overview-light.png` : variante claire.
- `exports/overview-mobile.png` : affichage mobile.
- `exports/analysis-lab-desktop.png` : laboratoire analytique.

Pour une revue technique, ajouter les fichiers concernés et les tests. Pour une revue des formules métier, joindre un extrait synthétique représentatif et la définition attendue des KPI.

**Base de rédaction :** lecture de `README.md`, `Aurelis_Dataset_Manifest.json`, portions ciblées d'`app.R`, modules `R/`, styles `www/workspace.css`, inventaire des CSV et inspection de la capture `overview-final.png`. Cette fiche décrit l'existant observé ; elle ne remplace pas un essai interactif complet de chaque fonction.

## 15. Disposition générale de l'interface

### Structure de l'écran sur ordinateur

L'écran comprend une navigation verticale à gauche, un en-tête horizontal fixe et une zone centrale qui défile verticalement. Le logo AURELIS est situé en haut de la navigation. Le pied de page comporte une signature d'auteur.

La feuille de style du workspace définit une navigation de **220 px** lorsque l'écran mesure au moins 992 px et que la barre latérale est déployée. L'en-tête mesure **57 px**. Le contenu est décalé pour tenir compte de ces éléments. Le logo est contraint à environ 175 px de large dans les dernières règles du thème.

Dans l'en-tête : commande du menu latéral, accès « Go to… », sélection année, sélection mois, Refresh, Report / Export, éléments d'information/plein écran selon le rendu et bouton Light mode / Dark mode.

Les pages se lisent principalement du haut vers le bas : titre/contexte, filtres, indicateurs, synthèses graphiques, tableaux détaillés, puis actions de rapport ou d'export. Des espaces comme Quotation Studio suivent un formulaire séquentiel plus long.

### Convention utilisée pour décrire les grilles

La plupart des écrans métier utilisent la grille Bootstrap/bs4Dash à **12 colonnes**. Dans les descriptions suivantes :

- `12` signifie une zone sur toute la largeur disponible.
- `6 | 6` signifie deux zones de même largeur.
- `8 | 4` signifie environ deux tiers à gauche et un tiers à droite.
- `7 | 5` signifie environ 58 % à gauche et 42 % à droite.
- `3 | 3 | 3 | 3` signifie quatre indicateurs sur une rangée.

Ces proportions décrivent la déclaration de l'interface sur grand écran. Les gouttières, marges et ajustements responsive réduisent la largeur réellement disponible. Les hauteurs indiquées correspondent aux **zones de graphiques déclarées**, auxquelles s'ajoutent le titre et les marges de la carte.

### Schéma de la page d'accueil

```text
┌──────────────┬────────────────────────────────────────────────────┐
│ Logo         │ Menu · Recherche · Année · Mois · Refresh · Export │
│              ├────────────────────────────────────────────────────┤
│ Navigation   │ Titre / sous-titre          Badge + Explore data   │
│ par groupes  ├────────────┬────────────┬────────────┬─────────────┤
│              │ Revenue    │ Gross      │ Outstanding│ Purchase    │
│              │            │ profit     │ receivables│ orders      │
│              ├────────────────────────────────┬───────────────────┤
│              │ Courbes revenu / bénéfice      │ Decision brief    │
│              │ largeur 8/12                   │ largeur 4/12      │
│              ├────────────────────────────────┴───────────────────┤
│              │ Tableau de performance clients — pleine largeur   │
│              ├────────────────────────────────────────────────────┤
│              │ More performance views — section dépliable        │
└──────────────┴────────────────────────────────────────────────────┘
```

## 16. Disposition détaillée des pages métier

L'ordre ci-dessous décrit les blocs du haut vers le bas et, pour chaque rangée, de gauche à droite. Les cartes restent soumises aux conditions d'accès et à la disponibilité des données.

### Executive Overview

1. En-tête : surtitre AURELIS / BUSINESS OPERATIONS, titre Operating overview, courte description ; badge de données synthétiques et bouton Explore data à droite.
2. Bandeau commun de quatre KPI sur quatre cellules séparées par des traits verticaux. Chaque cellule contient libellé, montant/nombre en grand et précision de périmètre.
3. Grille `8 | 4` : courbes Revenue & gross profit, zone graphique 285 px ; Decision brief avec trois rubriques numérotées, conclusion calculée, explication et bouton Review receivables.
4. Tableau clients `12`, avec légende de lecture, recherche et sélection d'une ligne. Pagination à huit lignes dans ce tableau.
5. Accordéon More performance views : `7 | 5`, classement des clients et anneau du bénéfice par représentant, 310 px chacun ; carte géographique du revenu, 320 px ; comparaison annuelle, 300 px, et barre de rapport.

### KPI Command Center

1. Deux rangées `3 | 3 | 3 | 3` : revenu, marge, valeur des commandes, créances ; puis réalisation des quantités, taux de reliquat, clients actifs, acheteurs actifs.
2. Rangée `8 | 4` : tendance de management, 390 px ; tableau de santé opérationnelle et note de définition.
3. Rangée `6 | 6` : contribution des clients et charge/valeur par acheteur, 390 px chacun.
4. Barre de rapport sur `12`.

### Global Network Atlas

1. Carte de contrôles Global Operating Lens sur `12`, avec filtres géographiques et métier, indicateurs de contexte et actions de réinitialisation/focalisation/navigation.
2. Rangée `8 | 4` : carte mondiale interactive de 610 px ; relation sélectionnée avec fiche, historique graphique de 250 px et tableau de contacts.
3. Geographic Business Breakdown sur `12`, graphique hiérarchique de 470 px.
4. Location Drilldown sur `12`, tableau de localisation.
5. Relationship Connections sur `12`, visualisation des relations de 390 px.

### Executive Activity Observatory

1. Bandeau pleine largeur : surtitre avec icône œil, titre descriptif, explication, badge du profil et trois compteurs de sessions, événements et engagements futurs.
2. Trois cartes `4 | 4 | 4` : activité passée, sessions en cours, engagements à venir, chacune avec un tableau.
3. Rangée `7 | 5` : graphique d'activité par employé/profil, 330 px ; gouvernance des accès sous forme de contenu explicatif.

### Buyer Activity

1. Carte de filtres pleine largeur permettant le drill-down temporel et par acheteur, avec bouton de remise à zéro.
2. Rangée `7 | 5` : activité quotidienne, 380 px ; classement des acheteurs, 380 px.
3. Rangée `5 | 7` : répartition de la clientèle sélectionnée, 390 px ; journal tabulaire d'activité.

### POs & Buyers

1. Filtres et commandes de remise à zéro sur `12`, suivis d'indicateurs synthétiques de commandes.
2. Rangée `7 | 5` : matrice de volume par acheteur/mois, 380 px ; valeur mensuelle par acheteur, 380 px.
3. Rangée `6 | 6` : tendance de valeur des commandes, 300 px ; tableau récapitulatif des acheteurs.
4. Journal détaillé des commandes sur `12` et actions associées.

### Sales & Profitability

1. Carte de filtres pleine largeur, puis quatre indicateurs de revenu, bénéfice brut, marge et transactions.
2. Évolution mensuelle revenu/coût/bénéfice sur `12`, 370 px.
3. Rangée `7 | 5` : revenu et bénéfice par représentant, 410 px ; jauge de marge et cible, 335 px.
4. Rangée `8 | 4` : contribution géographique ; synthèse du pays sélectionné.
5. Tableau détaillé de rentabilité sur `12`.

### Customer Performance

1. Sélection et filtres client sur `12`.
2. Carte de résumé de relation et préparation du PDF client sur `12`.
3. Customer Service KPI Board sur `12`, puis indicateurs de valeur historique, commandes distinctes, temps prévu et réalisation des quantités.
4. Rangée `7 | 5` : faits marquants de la relation ; jauge de positionnement dans le portefeuille, 300 px.
5. Rangée `8 | 4` : tendance mensuelle, 360 px ; anneau des statuts de réalisation, 360 px.
6. Histoire annuelle de collaboration sur `12`, 390 px.
7. Rangée `6 | 6` : contribution fournisseurs et couverture acheteurs, 390 px chacun.
8. Tableau de l'historique commandes/livraisons/fournisseurs sur `12`.

### Accounts Receivable

1. Filtres et indicateurs d'exposition en partie haute.
2. Rangée `5 | 7` : anneau des soldes par ancienneté, 400 px ; tendance facturation/encours, 400 px.
3. Répartition des soldes par responsable et ancienneté sur `12`, 390 px.
4. Bloc Customer Exposure sur `12`.
5. Grand livre complet sur `12`.

### Client Statements

1. Carte de sélection client et export CSV sur `12`.
2. Quatre KPI `3 | 3 | 3 | 3` : facturé, solde, pourcentage payé, nombre de factures.
3. Rangée `5 | 7` : anneau d'ancienneté des créances et chronologie des factures, 300 px chacun.
4. Relevé détaillé sur `12`.

### Orders & Delivery

1. Filtres et synthèses opérationnelles en partie haute.
2. Rangée `4 | 8` : anneau des statuts et charge par date exacte, 360 px chacun.
3. Rangée `7 | 5` : matrice de risque de livraison, 480 px ; calendrier de charge, 430 px.
4. Exposition par client/statut sur `12`, 450 px.
5. Planning priorisé et commandes d'export sur `12`.
6. Historique détaillé des commandes clients sur `12`.

### Inventory & Warehouse

Une note de qualité/provenance précède les onglets. Son texte dépend de la disponibilité reconnue des données ; les intitulés historiques de connexion doivent être interprétés avec le statut de démonstration décrit plus haut.

**Onglet Warehouse Availability :** filtres pleine largeur ; synthèses de stock ; `4 | 8` pour anneau des statuts et comparaison des quantités, 350 px chacun ; `7 | 5` pour matrice de réapprovisionnement et valeur par entrepôt, 420 px chacun ; tableau des articles et export sur `12`.

**Onglet approvisionnements/reliquats :** filtres et synthèses ; `6 | 6` pour valeur ouverte par fournisseur et quantités attendues par client, 390 px chacun ; `7 | 5` pour articles en attente et anneau des échéances, 420 px chacun ; tableau détaillé sur `12`.

### Suppliers & Procurement

1. Supplier Selection Workbench sur `12` : contrôles, puis comparaison graphique à gauche `5/12`, 390 px, et tableau comparatif à droite `7/12`.
2. Annuaire des produits/services vendeurs sur `12`, avec tableau et actions de sélection.
3. Rangée `6 | 6` : valeur des commandes ouvertes par fournisseur, 380 px ; tableau de livraison/exposition.
4. Recherche détaillée des commandes sur `12`.

### My Workspace

1. Carte principale `12` : bannière de démonstration, rangée de quatre zones pour propriétaire, profil, option de brouillons partagés et statut ; puis trois cartes de statut pour sessions, brouillons et rafraîchissement.
2. Rangée `7 | 5` : bibliothèque des brouillons, sélection, boutons ouvrir/supprimer et tableau ; sessions concurrentes et note sur l'identification.
3. Activité récente sur `12` sous forme de tableau.

### Quotation Studio

La page utilise une succession de cartes numérotées, plutôt qu'un assistant à étapes masquant les sections suivantes.

1. Identité et client sur `12` : barre de création/duplication/sauvegarde, accès rapide aux brouillons, champs d'identité, coordonnées et conditions.
2. Rangée `7 | 5` : historique de commandes et clonage à gauche ; historique de paiement, échéances et exposition à droite.
3. Lignes et coûts fournisseurs sur `12` : import CSV, commandes d'ajout/duplication/suppression, catalogue et tableau de lignes modifiables.
4. Frais spécifiques sur `12`, organisés en champs numériques.
5. Moteur de financement sur `12`, avec hypothèses et scénarios.
6. Politique commerciale sur `12`, incluant provision et commande d'application de la recommandation.
7. Calcul final sur `12` : tableau de scénarios et graphique en cascade de 470 px.
8. Prévisualisation/export sur `12` : PDF et classeur ; trois zones de notes `4 | 4 | 4` pour périmètre, conditions et notes internes. Les notes internes sont signalées comme non imprimées.

### Product Intelligence

1. Bandeau `12` : titre, description, badge de données synthétiques et compteurs de catalogue/fournisseurs.
2. Deux colonnes `4 | 8` : à gauche, formulaire de recherche avec budget, catégorie, disponibilité et nombre de recommandations, puis recommandation prioritaire ; à droite, tableau classé avec bouton d'ajout au devis, puis paysage coût/délai de 330 px.
3. Rangée `7 | 5` : explorateur de catalogue et ajout au devis ; formulaire de demande client, texte libre et résultat du brief.

### Directory & Relationships

1. Filtres et export, puis quatre indicateurs : enregistrements, relations distinctes, commandes et valeur.
2. Rangée `5 | 7` : profil de la relation ; activité mensuelle, 340 px.
3. Rangée `7 | 5` : flux acheteur–client–vendeur et principales contreparties, 430 px chacun.
4. Rangée `7 | 5` : catalogue fournisseurs ; formulaire de nouveau client.
5. Historique des interactions sur `12`, puis annuaire complet sur `12`.

### Demo Data & Process

1. Quatre indicateurs d'état des sources et connexions.
2. Rafraîchissement synthétique sur `12`.
3. Rangée `5 | 7` : tests de connexion ; tableau des datasets chargés.
4. Diagnostics d'import/schéma sur `12`.
5. Contrat des datasets sur `12`.
6. Capture/documentation des processus sur `12`, avec zone de texte de 150 px et sauvegarde de session.
7. Résumé des sources sur `12`.

## 17. Disposition des espaces statistiques

### Structure permanente d'Analysis Lab

La largeur maximale du workspace est fixée à 1 800 px. Les contrôles communs précèdent les onglets dans cet ordre :

1. Surtitre, titre Analysis Lab, badge R engine et description ; boutons Refresh files et Export CSV alignés à droite.
2. Barre de source : sélection du fichier, sélection de feuille si applicable, recherche globale, état de la source et nombre de lignes/contexte.
3. Bloc d'import dépliable : fichier sur `5/12`, séparateur CSV sur `3/12`, retour aux fichiers sources et précision de portée sur `4/12`.
4. Barre de filtres : choix des colonnes à filtrer, conservation des manquants, retrait des doublons et Reset.
5. Contrôles dynamiques correspondant aux filtres choisis, puis texte de périmètre.
6. Contrôles analytiques partagés : mesure, politique d'observations atypiques et niveau de confiance.
7. Barre d'onglets, puis contenu de l'onglet actif.

| Onglet | Disposition et représentations |
|---|---|
| Data Explorer | Choix des colonnes et aide au tri ; tableau sur toute la largeur ; fiche de ligne sélectionnée ; schéma/qualité dans un bloc dépliable |
| Profile | Brief calculé ; distribution à gauche `7/12`, 310 px, statistiques à droite `5/12` ; puis boîte et Q-Q en `6 | 6`, 250 px chacun |
| Hypothesis tests | Rangée de méthode, référence, alternative et alpha ; sélection des groupes ; résultat explicatif ; tableau comparatif ; note méthodologique |
| Trends & forecast | Date, granularité, agrégation et horizon ; note de validité ; graphique observé/prévision de 370 px ; détail tabulaire des périodes |
| Drivers | Sélection des prédicteurs et corrélation ; `6 | 6` pour matrice de corrélation, 350 px, et coefficients ; `6 | 6` pour résidus/prédictions et Q-Q des résidus, 260 px chacun |
| Scenarios | Curseurs de moyenne/dispersion, itérations et graine ; synthèse ; distribution simulée de 310 px ; tableau base/favorable/défavorable ; avertissement de portée |
| Financial metrics | Résultats financiers compatibles avec la source ; carte d'investissement avec quatre contrôles, résultat et hypothèses |
| Chart builder | Choix des axes, type et transformation ; graphique de 390 px ; carte de formule avec expression, bouton et statut |
| Probability studio | Carte explicative et bouton ouvrant le studio distinct ; ne constitue pas un second studio embarqué |

### Probability Studio distinct

1. Carte de configuration sur `12` pour source, mesure, distribution et paramètres.
2. Rangée `4 | 8` : résultat de probabilité à gauche ; courbe cumulative à droite, 340 px.
3. Profil d'échantillon sur `12`.
4. Rangée `7 | 5` : distribution observée et modèle ajusté ; contrôle des quantiles, 380 px chacun.
5. Rangée `7 | 5` : distributions des groupes, 390 px ; résultats des tests.
6. Tableau de synthèse des groupes et intervalles de confiance sur `12`.

## 18. Styles, couleurs et formats de composants

### Palette du workspace

| Usage | Sombre | Clair |
|---|---|---|
| Fond de contenu | `#101318` | `#F5F6F8` |
| Surface des panneaux | `#161A20` | `#FFFFFF` |
| Surface secondaire | `#1C222A` | `#EDF1F5` |
| Bordures | `#2A3039` | `#DCE2E9` |
| Texte principal | `#E6E9EF` | `#243244` |
| Texte secondaire | `#A0AABA` | `#58697D` |
| Accent principal | Menthe `#7DD3B0` | Accents verts adaptés sur certains composants |
| Série secondaire | Bleu `#8CB4EC` | Palette de séries conservée, textes adaptés |

La navigation et l'en-tête utilisent un fond `#13171D`. Les graphiques du Lab disposent aussi de tons ambre `#D8BB81` et mauve `#B4A2E8`. Les pages historiques utilisent des variables de marque et des couleurs de statut supplémentaires ; toute la palette n'est donc pas limitée à ces quatre couleurs.

### Typographie et hiérarchie

| Élément | Format défini dans le CSS du workspace |
|---|---|
| Police de base | Segoe UI Variable, Segoe UI, system-ui, sans-serif |
| Texte de base | 13 px |
| Grand titre du workspace | 27 px, graisse 600, interligne 1,2 ; adaptation mobile à 24 px dans une règle responsive |
| Surtitre | 10 px, capitales, espacement des lettres de 0,12 em |
| Titres de cartes | Environ 12–13 px, graisse 600 |
| Libellés de formulaires | 11 px, graisse 500 |
| Boutons et champs | 12 px |
| Libellé d'un KPI | 11 px |
| Valeur KPI de l'Overview | Taille adaptative de 19 à 32 px selon largeur ; chiffres tabulaires |
| Précision sous un KPI | 10 px |
| Légendes/aides | Environ 10–11 px |
| Texte des graphiques du Lab | 11 px, Segoe UI |

### Panneaux et espacement

Les cartes ont une bordure fine de 1 px et un rayon de 7 px. Les effets de relief, transparence décorative et mouvements au survol sont neutralisés sur les cartes visées par la feuille de style. Les titres sont séparés du contenu par une ligne horizontale.

Les panneaux du Lab utilisent typiquement 16 px de padding interne, 13 × 16 px dans leur en-tête et 18 px de marge inférieure. Le bandeau KPI de l'Overview utilise 20 px de padding vertical et 22 px de padding horizontal par cellule sur grand écran.

### Boutons, champs et états

- Bouton principal : fond menthe, texte vert très foncé, rayon de 5 px.
- Boutons secondaires : surfaces sombres, texte clair et bordure discrète.
- Hauteur minimale générale des boutons : 32 px ; padding courant 7 × 12 px.
- Champs : fond `#12171D`, bordure `#343D49`, texte clair et rayon de 5 px.
- Focus : bordure menthe et contour perceptible sur les champs ciblés.
- Sélecteurs Selectize : choix recherchables, listes déroulantes et puces pour sélections multiples.
- Onglet actif : fond transparent, texte éclairci et soulignement menthe de 2 px.
- Badges : petite capsule rectangulaire arrondie, bordure et fond teintés, texte de 10 px.
- Notes méthodologiques : encart de fond bleuté sombre, bord gauche coloré et texte de 12 px.
- Chargement : plusieurs graphiques/tableaux historiques sont entourés d'un indicateur d'attente coloré.
- Notifications : messages, avertissements ou erreurs lors des actions de devis, imports et inscriptions.

### Tableaux

Le composant DT présente des en-têtes en capitales, police de 10 px, avec léger espacement de lettres et fond distinct. Les cellules sont en 12 px, chiffres tabulaires et padding d'environ 9 × 12 px. Des séparateurs horizontaux structurent les lignes.

Le survol éclaire la ligne ; une ligne sélectionnée prend une teinte verte. Les options de recherche, pagination, largeur défilante et sélection varient selon le tableau. La pagination côté serveur est explicitement présente dans le Lab et le tableau clients de l'Overview ; elle ne doit pas être supposée identique pour chaque tableau historique.

## 19. Formats des valeurs, dates et documents

| Type | Présentation observée / convention |
|---|---|
| Montants de synthèse | Symbole `$`, séparateurs de milliers ; pas de décimales sur les KPI principaux et le tableau clients de l'Overview |
| Montants détaillés | Plusieurs tableaux et infobulles utilisent deux décimales, par exemple `$1,234.56` |
| Axes monétaires | Formats complets ou abrégés selon le graphique ; l'Overview utilise une échelle compacte de type `$5.0M` et mentionne USD |
| Marges et parts | Pourcentages ; une décimale notamment dans le tableau clients et le brief de l'Overview |
| Comptages | Nombres de commandes, transactions, clients, articles ou lignes ; l'unité doit être lue dans le libellé |
| Délais | Jours ou mois selon le module : livraison, exécution, ancienneté ou financement |
| Dates sources | Reconnaissance documentée du format ISO `YYYY-MM-DD` et des dates Excel dans le Lab |
| Dates de graphique | Plusieurs infobulles affichent mois/année ou mois/jour/année, avec abréviations anglaises |
| Horodatage d'activité | `YYYY-MM-DD HH:MM:SS` dans le journal généré par le code |
| Identifiants | Numéros de PO, facture, article et devis présentés comme références métier |

La présentation reste principalement anglophone, avec virgule pour les milliers et point décimal dans plusieurs sorties. Le symbole dollar ne suffit pas à démontrer une conversion entre devises : le catalogue possède un champ Currency, mais cette fiche n'établit pas une consolidation multidevise avec taux de change.

**Documents et sorties :** tableaux CSV ; images de graphiques via Plotly ; PDF de relation client ; devis PDF ; classeur de calcul du devis. Les documents n'ont pas tous fait l'objet d'une inspection visuelle dans cette revue : leur typographie, pagination et mise en page imprimée ne doivent pas être déduites des styles de l'écran.

## 20. Inventaire des visualisations et interactions

| Famille | Utilisation dans le dashboard | Lecture et interaction |
|---|---|---|
| Courbes temporelles | Revenu/bénéfice, tendances mensuelles, activité et comparaison annuelle | Axe horizontal temporel, valeurs verticales, légende et détails au survol |
| Barres horizontales | Classements clients, acheteurs, fournisseurs, articles et contreparties | Comparaison de catégories ; plusieurs graphiques proposent un clic de focalisation ou de navigation |
| Barres empilées | Valeur des commandes par acheteur et mois ; décomposition de soldes/statuts selon les vues | Contribution des séries à un total ; couleurs et légende distinguent les catégories |
| Graphiques combinés | Tendances KPI et activité acheteurs ; histoire annuelle client | Barres pour une mesure, courbe pour une autre, parfois deuxième axe à droite |
| Anneaux | Bénéfice par représentant, statuts de livraison, ancienneté des créances, états de stock et échéances | Parts d'un total ; trou central d'environ 55–58 % sur plusieurs vues et parfois texte central |
| Jauges | Marge par rapport à une cible, positionnement client | Valeur numérique et position dans une échelle ; repère/cible selon configuration |
| Heatmaps | Commandes acheteur/mois, calendrier de livraison, corrélations du Lab | Couleur représentant un volume, une charge ou un coefficient |
| Nuages de points / matrices | Risque de livraison, priorité de réapprovisionnement, paysage coût/délai | Position des observations sur deux axes ; attributs supplémentaires selon graphique |
| Carte à points géographiques | Global Network Atlas | Localisation des entités, sélection d'une relation et accès au détail |
| Carte choroplèthe | Revenu par pays dans les vues complémentaires de l'Overview | Pays colorés selon le revenu, échelle monétaire et sélection d'un pays |
| Sunburst | Répartition géographique hiérarchique dans l'Atlas | Anneaux hiérarchiques représentant les niveaux de regroupement |
| Vue de connexions | Relationship Connections de l'Atlas | Mise en relation d'entités et de leur activité, avec éléments cliquables selon la vue |
| Sankey | Flux acheteur–client–vendeur dans Directory & Relationships | Nœuds et liens dont la largeur encode la mesure choisie ; filtres dédiés |
| Cascade / waterfall | Décomposition du prix dans Quotation Studio | Construction progressive du prix à partir des coûts, charges et composantes commerciales |
| Histogramme / distribution | Profil analytique, distributions ajustées et simulations | Fréquences/densités et position des valeurs ; unités liées à la mesure choisie |
| Boîte à moustaches | Profil, groupes et Chart builder | Médiane, dispersion et valeurs atypiques |
| Q-Q | Normalité d'une mesure, ajustement de distribution et résidus | Comparaison des quantiles observés et théoriques |
| Courbe cumulative | Probability Studio | Probabilité cumulée et zone/repère correspondant au calcul choisi |
| Prévision avec intervalle | Trends & forecast | Observations historiques, prolongement linéaire et incertitude de prédiction |
| Résidus vs valeurs ajustées | Drivers | Diagnostic de structure résiduelle et d'adéquation du modèle |

**Précision technique utile :** l'identifiant `exec_country_treemap` contient le mot « treemap », mais son implémentation examinée construit une **carte choroplèthe**. Le nom d'une sortie ou le chargement d'un package ne suffit pas à identifier le graphique réellement affiché.

### Conventions graphiques du Lab

Les fonds des graphiques sont transparents pour s'intégrer aux panneaux. Les grilles sont discrètes ; les axes et textes utilisent des tons gris bleuté. Les marges par défaut du helper du Lab sont de 65 px à gauche, 24 px à droite, 55 px en bas et 20 px en haut, avec adaptations possibles par graphique.

La palette de séries commence par menthe, bleu, ambre et mauve. La barre Plotly permet notamment l'export en image ; les outils de sélection rectangulaire et lasso sont retirés par la configuration commune du Lab. Les pages historiques ont leurs propres configurations et peuvent différer.

### Interactions au-delà de la simple lecture

- Le survol d'un graphique affiche catégorie, période, montant, quantité ou pourcentage selon la vue.
- Plusieurs graphiques de classement et de pays déclenchent un filtre ou une navigation au clic ; cette propriété n'est pas universelle.
- La sélection d'une ligne du tableau clients de l'Overview ouvre la page client correspondante.
- Les tableaux de catalogue/recommandation permettent de choisir une ligne et de l'ajouter au devis via un bouton.
- Les commandes Reset permettent de sortir d'une sélection ou d'une focalisation.
- Les sections dépliables réduisent la densité initiale, notamment pour les vues complémentaires, imports et diagnostics.

## 21. Responsive, limites de la description visuelle et consigne complémentaire

### Comportements responsive définis

- À partir de 992 px : barre latérale déployée de 220 px lorsque le menu n'est pas réduit.
- Sous 1 100 px : retour à la ligne de la barre source du Lab, réorganisation des actions, réduction de certains espacements et remplacement du libellé de navigation rapide par une icône.
- Sous 768 px : bandeau KPI de l'Overview en grille de deux colonnes ; titre et actions empilés ; contrôles source/recherche sur toute la largeur ; toolbar d'exploration empilée ; filtres mobiles année/mois sur deux colonnes ; bouton de thème compact.
- Les colonnes Bootstrap se réorganisent selon les classes utilisées. Les tableaux peuvent nécessiter un défilement horizontal.
- La préférence système de réduction des animations supprime transitions/animations des éléments du workspace visés.

Ces règles décrivent le comportement prévu par le code. Elles ne garantissent pas que tous les graphiques, formulaires longs et tableaux soient confortables sur chaque appareil.

### Comment utiliser cette fiche pour une critique du design

Les dimensions, couleurs et dispositions ci-dessus proviennent du code et des styles du projet. La capture de l'Overview a été inspectée ; un contrôle visuel exhaustif des autres pages, états vides, erreurs, fenêtres modales et documents exportés n'a pas été effectué. La cascade CSS et les styles historiques peuvent modifier certains détails. Pour des recommandations au pixel près, joindre des captures actuelles des pages concernées.

Ajouter cette consigne à celle de la section 13 :

> Évalue aussi les dispositions détaillées, les proportions des colonnes, l'ordre des blocs, la densité d'information, les tailles de texte, les contrastes, les formats monétaires et les interactions des graphiques. Examine particulièrement les anneaux multiples, les doubles axes, la cohérence des couleurs entre pages, la différence entre somme et moyenne dans les graphiques et la lisibilité mobile.
>
> Pour chaque page que tu proposes de modifier, fournis une disposition explicite du haut vers le bas, avec proportions de colonnes, KPI conservés, graphiques remplacés ou regroupés, filtres et action principale. Précise le type de graphique recommandé, ses axes, l'unité, la règle d'agrégation et le comportement au clic. Distingue les améliorations justifiées par la structure décrite de celles qui nécessitent une capture ou un test utilisateur.
