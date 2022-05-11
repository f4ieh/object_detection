# Data-Scientest-Github ~ MAIN
FootBall Helmet Detection
Object-Tracking 
Représenter ces résultats (avec un graphique)
Calculer le nombre d'objets par image
Calculer le nombre de casques par image
Calculer le nombdre d'objets différents des casques par image
Methode
a. remplacer le code des objets par leur nom
b. faire du get_dummies sur la colonne qui contient le nom des objets
c. faire un groupby sur l'identifiant de la photo (sum sur les indicatrices)
Nombre d'objets total (par différente classe d'objet)
(value_counts sur la colonne type d'objet)
18 h 21
Calculer par exemple la taille moyenne des casques (surface)
Position moyenne des casques x_moy et y_moy -> distribution, scatter
Position moyenne des autres objets
(modifié)
Nouveau


Paul - DataScientest  18 h 37
import pandas as pd
import numpy as np
import matplotlib.pyplot as plt
import seaborn as sns
%matplotlib inline

n_lines = 10000

df = pd.DataFrame(
    {
        "x_moy": np.random.normal(size=n_lines),
        "y_moy": np.random.normal(size=n_lines)
    }
)

df.head()

with plt.style.context("dark_background"):
    plt.figure(figsize=(20, 20))
    
    plt.scatter(
        x=df["x_moy"],
        y=df["y_moy"],
        c="green",
        alpha=.1
    )
