## Projet_ML_S3
L’apnée est un sport de plus en plus populaire. De nombreuses compétitions existent autour
du monde.
Une plongée réussie en compétition est la réussite de la profondeur annoncée. Des juges
sont présents et donnent un carton selon la réussite de la plongée :
*blanc : l’apnéiste a été à la profondeur annoncée et a effectué le protocole de sortie
*jaune: l’apnéiste a tourné avant (la profondeur annoncée n’est pas atteinte) et a
effectué son protocole de sortie
*rouge: l’apnéiste n’a pas effectué le protocole de sortie (syncope, défaut de
protocole, discipline non respectée). La plongée n’est pas validée.
Quels sont les facteurs qui peuvent influencer une plongée (en compétition)? Pour quelles
raisons un apnéiste ne valide pas sa plongée?
C’est ce que nous allez devoir essayer de répondre dans ce projet.

https://www.youtube.com/live/W6Hkdo4h2W0

Les résultats des compétitions venant de l’organisation d’AIDA peuvent être extrait du site
web de l'organisation (https://www.aidainternational.org/Events/EventCalendar )

Le fichier contient le résultat des plongées de 1984 à aujourd'hui(2024).
La description des colonnes est celle-ci. Les colonnes suivantes correspondent aux
caractéristiques :
- Start : l’indice de départ de l’apnéiste dans la journée de compétition (peu
intéressant)
- Diver : le nom de l’apnéiste
- Nationality : le pays de l’apnéiste
- Gender : le genre de l’apnéiste H/F
- Discipline : la discipline concurrue (FIM: immersion libre, CNF: brasse, CWT: poids
constant libre souvent en monopalme, CWT-B: en by-palmes)
- Line : ligne de départ, très peu renseignée (peu intéressant)
- Official Top : l’heure officielle de son départ (peu intéressant?)
- AP : la profondeur annoncée, l’apnéiste doit annoncer la profondeur qu’il veut
effecter et l’effectuer pour valider un carton blanc
- Day : jour de la compétition
- Title Event : titre de la compétition
- Event Type : le type de l’événement



