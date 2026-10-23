# Tracker de Séries

Un tableau tout simple pour suivre ses séries d'exercices, **semaine par
semaine et matière par matière**. Fait à l'EPFL, pour l'EPFL, mais utile
partout où il y a des séries.

| état | couleur |
|---|---|
| à venir | gris léger |
| en cours | bleu |
| à corriger | vert clair |
| fait | vert |
| vacances | gris, ou vert sauge pointillé (au choix dans ⚙) |

## Utilisation

- **Clic** sur une case : état suivant. **Clic droit** : état précédent.
- **⚙** : nom du semestre, matières, nombre de semaines de cours, date de
  début. Avec la date de début, la semaine en cours est surlignée.
- **Vacances et jours fériés** (dans ⚙) : une semaine entièrement couverte,
  du lundi au vendredi, s'intercale comme une bande continue sur toutes les
  matières. Elle ne compte pas parmi les semaines de cours (14 + 1 de
  vacances = 15 rangées) et la série suivante garde son numéro. Pour un férié isolé, **Maj + clic** sur la case
  concernée marque cette seule série comme sautée.
- **+ nouveau semestre** reprend les matières du semestre affiché ; les
  semestres passés restent accessibles dans le menu déroulant.
- Thème **clair / sombre / auto** dans l'en-tête.
- **?** affiche l'aide dans la page.

### L'installer comme une application

Dans Chrome, Edge ou Brave : menu → *Installer l'application*. Sur iPhone :
Safari → *Partager* → *Sur l'écran d'accueil*. Elle s'ouvre alors dans sa
propre fenêtre.

## Vos données

Tout est enregistré **dans votre navigateur** (`localStorage`), sur votre
appareil. Rien n'est envoyé nulle part : pas de compte, pas de serveur, pas de
traceur.

La contrepartie : effacer les données de navigation efface aussi le tableau,
et deux navigateurs (ou deux appareils) ont chacun le leur. Le bouton
**Exporter** télécharge une sauvegarde JSON ; **Importer** la recharge, ici ou
ailleurs.

## Technique

Un seul fichier `index.html`, sans dépendance ni étape de compilation. Pour
l'héberger, n'importe quel serveur statique convient (GitHub Pages par
exemple). Pour le modifier, les couleurs sont regroupées en variables CSS en
tête de fichier (`--s0` à `--s3` pour les états).

## Licence

[MIT](LICENSE) : libre de l'utiliser, de le modifier et de le partager.
