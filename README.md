# Projet d'etude de donnees

Ce depot fournit une base reproductible et une méthode pour explorer un jeu de donnees des prix de l'électricité avec Python et Jupyter.

## Objectif

- **Appliquer des méthodes EPF/PEPF sur la prévision des prix spot de l'électricité**
- **Jeu de donnees : Prix sur le marché EPEX Spot en France entre 2011 et 2016**

## Structure

```text
.
|-- notebooks/
|   `-- electricityforecasting_perrin.ipynb
|-- .gitignore
|-- .python-version
|-- README.md
`-- requirements.txt
```

## Environnement

La version Python cible est indiquee dans `.python-version`. Les dependances
directes et leurs versions sont epinglees dans `requirements.txt`.

### Windows (PowerShell)

```powershell
py -3.11 -m venv .venv
.\.venv\Scripts\Activate.ps1
python -m pip install --upgrade pip
python -m pip install -r requirements.txt
python -m ipykernel install --user --name etude-donnees --display-name "Python (etude-donnees)"
```

Dans VS Code, ouvrez le dossier du projet, installez les extensions Python et
Jupyter si necessaire, puis selectionnez l'environnement `.venv` comme noyau
du notebook.

### macOS / Linux

```bash
python3.11 -m venv .venv
source .venv/bin/activate
python -m pip install --upgrade pip
python -m pip install -r requirements.txt
python -m ipykernel install --user --name etude-donnees --display-name "Python (etude-donnees)"
```

Pour telecharger les donnees depuis Kaggle, configurez l'authentification
localement avec la variable d'environnement `KAGGLE_API_TOKEN` ou le fichier
`~/.kaggle/kaggle.json`. Ne placez jamais votre jeton dans le notebook ni dans
le depot.

Pour reconstruire l'environnement plus tard, recreez l'environnement virtuel et
rejouez l'installation depuis `requirements.txt`. Pour mettre a jour une
dependance, modifiez sa version epinglee puis validez et documentez le
changement.

## Lancer l'analyse

Ouvrez `notebooks/electricityforecasting_perrin.ipynb` dans VS Code ou lancez Jupyter depuis
la racine du projet :

```bash
python -m jupyter lab
```

Executez les cellules dans l'ordre. Le notebook est un point de depart a
completer avec les controles, analyses et conclusions propres au projet.
