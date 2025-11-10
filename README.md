# 🧮 Simulation du Modèle de Ruine de Cramér-Lundberg

Un projet Python illustrant la modélisation du **risque actuariel** à travers le modèle de ruine classique de **Cramér-Lundberg**.  
Ce projet a pour objectif d’estimer la **probabilité de ruine** d’une compagnie d’assurance par simulation Monte Carlo et de visualiser l’évolution du capital assurantiel dans le temps.

---

## 📘 Description du modèle

Le modèle de Cramér-Lundberg décrit l’évolution du capital d’une compagnie d’assurance :
\[
U(t) = u + c \cdot t - \sum_{i=1}^{N(t)} X_i
\]

où :
- \( u \) : capital initial,  
- \( c \) : taux de primes (revenus constants),  
- \( N(t) \) : processus de Poisson d’intensité \( \lambda \) (arrivées des sinistres),  
- \( X_i \) : montants de sinistres i.i.d. suivant une loi donnée (exponentielle, Pareto, lognormale...).

Le but est d’estimer la **probabilité de ruine avant un horizon \( T \)** :
\[
\psi(u) = \mathbb{P}(U(t) < 0 \text{ pour un } t \leq T)
\]

---

## 🚀 Fonctionnalités principales

- **Simulation du capital** \(U(t)\) jusqu’à la ruine ou l’horizon \(T\)
- **Estimation Monte Carlo** de la probabilité de ruine
- **Visualisation des trajectoires** du capital et des résultats
- **Comparaison des lois de sinistres** : Exponentielle, Pareto, Lognormale
- **Extensions prêtes** :
  - Réassurance *quota-share* (proportionnelle)
  - Réassurance *stop-loss* (non proportionnelle)
  - Étude de la sensibilité du capital initial \(u\)

---

## 🧩 Structure du projet

