# Formation NumPy : les bases

Introduction à NumPy, avant Pandas.

## Contenu

```
formation-numpy/
├── 01_numpy_theorie.ipynb     # cours
├── 02_numpy_exercices.ipynb   # exercices
├── data/
│   └── Mall_Customers.csv     # données de l'exercice 3
├── pyproject.toml             # dépendances du projet : numpy, ipykernel
├── uv.lock                    # versions exactes, générées par uv (ne pas modifier)
├── .python-version            # version de Python utilisée par uv
└── README.md
```

Le dossier `data` doit rester à côté des notebooks.

## Prérequis

- Les bases de Python : listes, indices, boucles `for`, `print()`.
- Windows et VS Code avec les extensions **Python** et **Jupyter** (éditeur : Microsoft).

## Installation (PowerShell)

**1. Installer uv** (une seule fois par ordinateur), puis fermer et rouvrir le terminal :

```powershell
powershell -ExecutionPolicy ByPass -c "irm https://astral.sh/uv/install.ps1 | iex"
uv --version
```

**2. Dans le dossier de la formation** (celui qui contient `pyproject.toml`) :

```powershell
uv sync
```

Cette commande crée le dossier `.venv`, télécharge la bonne version de Python si nécessaire et installe les versions exactes notées dans `uv.lock`. Il n'est pas nécessaire d'activer l'environnement.

**3. Dans VS Code :** ouvrir `01_numpy_theorie.ipynb`, cliquer sur **Select Kernel** en haut à droite, puis **Python Environments** et choisir `.venv`.

**4. Vérifier :** exécuter la première cellule de code du notebook. Le chemin affiché doit se terminer par `.venv`.

## En cas de problème

| Symptôme | Solution |
|---|---|
| `uv n'est pas reconnu…` | Fermer et rouvrir le terminal (ou VS Code) après l'installation de uv. |
| `No pyproject.toml found` | Le terminal n'est pas dans le dossier de la formation : s'y placer avec `cd`, puis relancer `uv sync`. |
| `.venv` absent de la liste des kernels | `Ctrl + Maj + P`, puis **Developer: Reload Window**, puis **Select Kernel** à nouveau. |
| VS Code propose d'installer `ipykernel` | Refuser, relancer `uv sync`, puis resélectionner le kernel `.venv`. |
| `ModuleNotFoundError: No module named 'numpy'` | Mauvais kernel : resélectionner `.venv`. |
| `FileNotFoundError: data/Mall_Customers.csv` | Le dossier `data` n'est pas à côté du notebook. |
