# Étude probabiliste et économique du dimensionnement d'une digue de protection

> Projet réalisé dans le cadre du cours **Pratique de la fiabilité** (ISUP – Université Paris Cité).

## Présentation

Ce projet porte sur le dimensionnement d'une digue destinée à protéger une installation industrielle située en bordure d'une rivière contre le risque d'inondation.

L'objectif est de déterminer une hauteur de digue adaptée en tenant compte des incertitudes sur les phénomènes hydrauliques. Trois approches successives sont étudiées :

1. une approche basée sur les données historiques ;
2. une approche probabiliste utilisant un modèle hydraulique ;
3. une approche économique intégrant les coûts de protection et les dommages potentiels.

Le projet permet d'illustrer l'apport des méthodes de fiabilité dans la prise de décision en présence d'incertitudes.

---

# Objectifs

Les principaux objectifs sont :

* exploiter les données historiques de crues ;
* modéliser les principales sources d'incertitude ;
* estimer le risque de surverse par simulation de Monte Carlo ;
* construire un modèle économique du système ;
* déterminer la hauteur de digue offrant le meilleur compromis entre sécurité et coût.

---

# Contenu du projet

## Partie I — Exploitation des données historiques

La première partie repose uniquement sur les observations historiques des débits maximaux annuels et des hauteurs de crue.

L'objectif est de proposer une première hauteur de digue à partir des événements réellement observés.

### Résultat

Cette approche fournit une estimation simple de la hauteur de protection mais reste fortement dépendante des données disponibles.

### Limites

* ne tient pas compte des événements extrêmes non observés ;
* n'intègre pas explicitement les incertitudes ;
* ne permet pas d'évaluer quantitativement le risque futur.

---

## Partie II — Modèle hydraulique probabiliste

La deuxième partie introduit un modèle hydraulique reliant :

* le débit de la rivière,
* le coefficient de Strickler,
* la géométrie du cours d'eau,

à la hauteur d'eau maximale.

Les variables physiques sont modélisées par des lois de probabilité (Gumbel, Normale et Triangulaire), puis une simulation de Monte Carlo est utilisée pour estimer la probabilité de surverse.

### Résultat

Cette approche permet d'estimer directement la probabilité annuelle de surverse pour différentes hauteurs de digue.

Elle montre que cette probabilité décroît rapidement lorsque la hauteur de la digue augmente.

### Limites

* modèle hydraulique volontairement simplifié ;
* hypothèse d'indépendance entre les variables ;
* hypothèse de stationnarité des phénomènes hydrologiques.

---

## Partie III — Optimisation économique

La troisième partie complète le modèle précédent en intégrant les coûts :

* d'investissement ;
* de maintenance ;
* de dommages à la digue ;
* de dommages au site industriel.

L'objectif n'est plus uniquement de minimiser le risque de surverse mais de minimiser le coût économique moyen sur une période de 30 ans.

Une simulation Monte Carlo est utilisée afin d'estimer les dommages attendus pour chaque hauteur de digue.

### Résultats obtenus

L'optimisation conduit aux résultats suivants :

* **Hauteur optimale : 3.10 m**
* **Coût économique moyen : 647 k€/an**

Probabilités annuelles de surverse :

| Hauteur de digue |  Probabilité |
| ---------------: | -----------: |
|            0.0 m |     1.0920 % |
|            2.0 m |     0.0715 % |
|       **3.10 m** | **0.0175 %** |
|            4.0 m |     0.0035 % |

Ces résultats montrent qu'une digue plus haute réduit davantage le risque de surverse, mais que le coût supplémentaire de construction devient rapidement supérieur aux bénéfices économiques apportés.

La hauteur de **3.10 m** représente ainsi le meilleur compromis entre protection et coût.

---

# Technologies utilisées

* Python
* Jupyter Notebook
* NumPy
* SciPy
* Pandas
* Matplotlib

---

# Structure du dépôt

```text
.
├── Projet_Fiabilté_Mohamadou_Diao_Baldé.ipynb
├── Sujet-Projet-Pratique-Fiabilité.pdf
├── Rapport.pdf
└── README.md
```

---

# Installation

Installer les dépendances :

```bash
pip install numpy scipy pandas matplotlib jupyter
```

Puis lancer :

```bash
jupyter notebook
```

---

# Limites du projet

Plusieurs hypothèses simplificatrices ont été retenues afin de rendre le problème traitable :

* modèle hydraulique analytique simplifié ;
* variables d'entrée supposées indépendantes ;
* distributions de probabilité fixées a priori ;
* absence d'évolution climatique ou morphologique du cours d'eau ;
* optimisation réalisée sur un horizon de 30 ans.

Ces hypothèses permettent de mettre en œuvre les méthodes probabilistes tout en conservant un modèle facilement interprétable.

---

# Perspectives

Plusieurs améliorations pourraient être envisagées :

* utiliser un modèle hydraulique plus réaliste (par exemple HEC-RAS) ;
* prendre en compte la dépendance entre certaines variables hydrologiques ;
* intégrer les effets du changement climatique ;
* réaliser une analyse de sensibilité des paramètres ;
* utiliser des méthodes d'optimisation plus avancées.

---

# Auteur

**Mohamadou Diao Baldé**

Master2 ISUP — Science des Données

ISUP-Sorbonne Université
---

# Licence

Ce dépôt est publié à des fins pédagogiques. Les données et l'énoncé sont issus du cours **Pratique de la fiabilité** de l'ISUP.
