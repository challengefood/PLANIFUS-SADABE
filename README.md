# SADABE PLANIFIUS

**SADABE PLANIFIUS** est une application web open source de planification mensuelle des activités de SADABE.

Elle permet de voir les activités qui devraient être faites pendant un mois, de connaître le responsable principal, d'ajouter les membres de l'équipe affectés à chaque activité, et de filtrer le dashboard par personne, projet, partenaire et statut.

## Fonctionnalités

- Dashboard mensuel des activités
- Filtre par mois, projet, partenaire, personne et statut
- Calcul automatique de l'urgence : urgent, en retard, bientôt, normal, clôturé
- Gestion des projets : SOS Lemurs, Darwin Initiatives, Seacology, Rainforest Trust, avec possibilité d'ajouter d'autres projets
- Gestion des partenaires : TGBS (MBG), MfM, UWE, Regen, UNI, ENS, avec possibilité d'ajouter d'autres partenaires
- Gestion des membres de l'équipe SADABE et de leurs postes
- Ajout d'un responsable principal par activité
- Ajout de plusieurs membres affectés à une activité avec un rôle spécifique
- Import Excel, CSV ou Word
- Export Excel du planning filtré ou de toute la base
- Sauvegarde de la base SQLite
- Logo SADABE intégré

## Installation locale

### 1. Installer Python

Installer Python 3.10 ou supérieur.

### 2. Installer les dépendances

Dans le dossier du projet :

```bash
pip install -r requirements.txt
```

### 3. Lancer l'application

```bash
streamlit run app.py
```

L'application s'ouvrira dans le navigateur.

## Installation rapide Windows

Double-cliquer sur :

```text
lancer_windows.bat
```

## Installation rapide Mac / Linux

Dans le terminal :

```bash
chmod +x lancer_mac_linux.sh
./lancer_mac_linux.sh
```

## Déploiement sur GitHub + Streamlit Cloud

1. Créer un dépôt GitHub public.
2. Envoyer tous les fichiers du dossier `SADABE_PLANIFIUS` dans le dépôt.
3. Aller sur Streamlit Community Cloud.
4. Créer une nouvelle application depuis GitHub.
5. Sélectionner :

```text
Branch: main
Main file path: app.py
```

6. Cliquer sur **Deploy**.

## Import de fichiers

Un modèle Excel est fourni dans :

```text
sample_data/modele_import_sadabe_planifius.xlsx
```

Colonnes recommandées pour les activités :

- Activité
- Description
- Projet
- Partenaire
- Mois prévu (YYYY-MM)
- Jour prévu
- Date limite
- Priorité
- Statut
- Responsable principal
- Membres équipe
- Lieu
- Résultat attendu
- Notes

Les membres d'équipe peuvent être séparés par `;` ou `,`.

Exemple :

```text
Membre 1; Membre 2; Membre 3
```

## Base de données

Par défaut, l'application crée une base SQLite locale :

```text
sadabe_planifius.db
```

Pour Streamlit Cloud, pensez à exporter régulièrement la base SQLite depuis la page **Import / Export**, car le stockage peut être réinitialisé lors de certains redéploiements.

## Structure du projet

```text
SADABE_PLANIFIUS/
├── app.py
├── requirements.txt
├── README.md
├── LICENSE
├── assets/
│   ├── logo_sadabe.png
│   ├── tsinjoarivo_valley_1.jpeg
│   ├── tsinjoarivo_valley_2.jpeg
│   └── community_meeting.jpeg
├── sample_data/
│   ├── modele_import_sadabe_planifius.xlsx
│   └── exemple_activites_sadabe.csv
├── .streamlit/
│   └── config.toml
├── lancer_windows.bat
└── lancer_mac_linux.sh
```

## Licence

MIT License. Le logiciel est open source et peut être adapté aux besoins de SADABE.
