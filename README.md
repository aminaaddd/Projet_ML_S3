## Projet_ML_S3
L’apnée est un sport de plus en plus populaire. De nombreuses compétitions existent autour du monde.
Une plongée réussie en compétition est la réussite de la profondeur annoncée. Des juges sont présents et donnent un carton selon la réussite de la plongée :
- blanc : l’apnéiste a été à la profondeur annoncée et a effectué le protocole de sortie
- jaune: l’apnéiste a tourné avant (la profondeur annoncée n’est pas atteinte) et a effectué son protocole de sortie
- rouge: l’apnéiste n’a pas effectué le protocole de sortie (syncope, défaut de protocole, discipline non respectée). La plongée n’est pas validée.

Quels sont les facteurs qui peuvent influencer une plongée (en compétition)? Pour quelles raisons un apnéiste ne valide pas sa plongée?
C’est ce que nous allez devoir essayer de répondre dans ce projet.

https://www.youtube.com/live/W6Hkdo4h2W0

Les résultats des compétitions venant de l’organisation d’AIDA peuvent être extrait du site
web de l'organisation (https://www.aidainternational.org/Events/EventCalendar )

Le fichier contient le résultat des plongées de 1984 à aujourd'hui(2024).
La description des colonnes est celle-ci. Les colonnes suivantes correspondent aux caractéristiques :
- Start : l’indice de départ de l’apnéiste dans la journée de compétition (peu intéressant)
- Diver : le nom de l’apnéiste
- Nationality : le pays de l’apnéiste
- Gender : le genre de l’apnéiste H/F
- Discipline : la discipline concurrue (FIM: immersion libre, CNF: brasse, CWT: poids constant libre souvent en monopalme, CWT-B: en by-palmes)
- Line : ligne de départ, très peu renseignée (peu intéressant)
- Official Top : l’heure officielle de son départ (peu intéressant?)
- AP : la profondeur annoncée, l’apnéiste doit annoncer la profondeur qu’il veut effecter et l’effectuer pour valider un carton blanc
- Day : jour de la compétition
- Title Event : titre de la compétition
- Event Type : le type de l’événement

Les informations obtenues après la plongée (ce ne sont donc pas des caractéristiques mais la sortie):
- RP : la profondeur réalisée
- Card : le carton du juge, un blanc, la profonceur a été atteinte et le protocole de sortie réalisé, jaune, la profondeur n’a pas été atteinte ou le tag n’a pas été récupéré, le protocole de sortie bien effectuée, rouge: erreur sur le protocole de sortie
- Points : différence entre AP et RP et des points de pénalité le cas échéant
- Remarks : commentaire de la plongée

## Exploration des données
Des erreurs de log , de collecte ou d’extraction de données peuvent être présentes.
L’exploration des données va vous permettre d’analyser ces données. Dans le cas d’incohérence, des choix de transformation, suppression, remplacement peuvent être fait.

## Clustering
On souhaite expliquer pour quelles raisons un apnéiste obtient un carton rouge (la discipline, la profondeur annoncée, le manque d’expérience ?). Un carton rouge signifie que l’apnéiste n’a pas respecté le protocole de plongée ou de sortie qui assure que sa plongée s’est bien effectuée (la description est dans la colonne ‘remark’ mais elle est très peu normalisée). 
Pour cela, on va vouloir identifier les clusters qui permettront de définir le profil de la plongée échouée en utilisant les différentes caractéristiques obtenues par l’historique des plongées effectuées dans les compétitions.

## Classification
Prédire si le résultat d’une plongée va être un carton blanc, jaune, rouge selon les caractéristiques.
