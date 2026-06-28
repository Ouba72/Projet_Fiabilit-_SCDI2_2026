# Étude probabiliste et économique du dimensionnement d'une digue de protection

## Présentation

Ce projet a été réalisé dans le cadre du cours **Pratique de la fiabilité** à l'ISUP (Université Paris Cité).

L'objectif est de déterminer la hauteur optimale d'une digue protégeant une installation industrielle située en bordure d'une rivière. Le problème est étudié selon trois approches complémentaires :

1. exploitation des données historiques de crues ;
2. modélisation probabiliste du risque de surverse ;
3. optimisation économique prenant en compte les coûts de construction, de maintenance et les dommages potentiels.

L'ensemble des analyses est réalisé sous **Python** dans un notebook Jupyter.

---

## Objectifs

Le projet vise à :

* analyser les données historiques de débit et de hauteur de crue ;
* modéliser les incertitudes hydrauliques à l'aide de lois de probabilité ;
* estimer la probabilité de surverse par simulation de Monte Carlo ;
* construire un modèle économique intégrant les coûts d'investissement et les coûts de dommages ;
* déterminer la hauteur de digue minimisant le coût économique moyen.

---

## Structure du projet

```text
.
├── Projet_Fiabilté_Mohamadou_Diao_Baldé.ipynb   # Notebook principal
├── Sujet-Projet-Pratique-Fiabilité.pdf          # Énoncé du projet
├── Rapport.pdf                                  # Rapport (optionnel)
└── README.md
```

---

## Méthodes utilisées

* Analyse exploratoire des données
* Ajustement de lois de probabilité
* Simulation de Monte Carlo
* Modèle hydraulique simplifié
* Modélisation économique des coûts
* Optimisation par recherche du minimum

---

## Principaux résultats

Le modèle économique conduit à une hauteur de digue optimale de :

* **Hauteur optimale :** **3.10 m**
* **Coût économique moyen :** **647 k€/an**

Cette hauteur constitue le meilleur compromis entre :

* le coût de construction et de maintenance de la digue ;
* les coûts attendus liés aux éventuelles inondations.

La simulation Monte Carlo montre également que la probabilité annuelle de surverse devient très faible pour cette hauteur :

| Hauteur de digue | Probabilité de surverse |
| ---------------: | ----------------------: |
|            0.0 m |                1.0920 % |
|            2.0 m |                0.0715 % |
|       **3.10 m** |            **0.0175 %** |
|            4.0 m |                0.0035 % |

---

## Technologies utilisées

* Python 3
* Jupyter Notebook
* NumPy
* SciPy
* Pandas
* Matplotlib

---

## Exécution

Installer les dépendances :

```bash
pip install numpy scipy pandas matplotlib jupyter
```

Puis lancer le notebook :

```bash
jupyter notebook
```

---

## Auteur

**Mohamadou Diao Baldé**

Master ISUP – Science des Données, Calcul Intensif et Décision (SCDI)

Université Paris Cité

---

## Remarque

Ce projet est réalisé dans un objectif pédagogique dans le cadre du cours *Pratique de la fiabilité*. Les données, le modèle hydraulique et le modèle économique sont issus de l'énoncé du projet et servent uniquement d'illustration des méthodes probabilistes appliquées à la gestion des risques.
