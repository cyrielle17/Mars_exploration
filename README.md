# ARES-VII // Mount Sharp Boxwork EVA Navigator

Système d'aide à la navigation et **visière HUD en réalité augmentée** pour une mission d'exploration humaine assistée par mini-rover sur les flancs du **Mont Sharp (*Aeolis Mons*)**, dans le **cratère Gale** (`-4.74° S, 137.85° E`).

**[Tester le simulateur interactif en ligne (GitHub Pages)](https://cyrielle17.github.io/Mars_exploration/)**

---

## Objectif de la mission
Reconstituer l'histoire des dernières circulations d'eaux souterraines sur Mars en explorant les formations géologiques en **boxwork** (réseaux polygonaux de crêtes minéralisées observés par *Curiosity*), tout en garantissant la sécurité d'un astronaute en scaphandre **xEMU** accompagné d'un **mini-rover éclaireur**.

## Fonctionnalités de l'interface (`index.html`)
* **Double vue synchronisée :** Bascule instantanée entre la **Visière Casque HUD (POV première personne)** et la **Carte Orbitale Tactique (*Mars Trek GIS*)**, couplées à un **profil d'élévation topographique** en temps réel.
* **5 couches de données NASA activables :**
  1. **MRO HiRISE & MOLA :** Détection des escarpements critiques ($\theta > 20^\circ$).
  2. **Odyssey THEMIS (IR) :** Repérage des cuvettes de sable meuble ($I < 120$) pour éviter l'enlisement.
  3. **MRO CRISM :** Surbrillance spectrale des veines riches en sulfates hydratés et oxydes de fer.
  4. **Curiosity RAD & MAVEN :** Calcul du débit de dose effectif et de l'effet d'abri offert par les parois rocheuses.
  5. **Perseverance MEDA :** Suivi du vent, de l'opacité $\tau$ (bascule automatique en *Vision Synthétique* si $\tau > 0,8$) et activation du dépoussiérage électrostatique (**EDS**).
* **Simulateur physique en direct :** Calcul de la vitesse de marche sous pesanteur martienne ($g = 3,72\text{ m/s}^2$), suivi de la réserve d'$\text{O}_2$ ($650\text{ g}$), impact énergétique du mini-rover porteur ($-22\,\%$) et comparaison entre le **tracé sécurisé ($1\,350\text{ m}$)** et un **raccourci direct risqué**.

## Structure du dépôt
* `index.html` — Application web interactive complète (moteur physique, grille terrain et rendu HUD).
* `docs/mission_brief.md` — Dossier scientifique, équations physiques et plan de route en 5 waypoints.
* `docs/assets/` — Captures orbitales *NASA Mars Trek* et vues au sol *Curiosity*.
