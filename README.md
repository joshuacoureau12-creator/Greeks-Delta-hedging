# Greeks & Dynamic Delta-Hedging

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/joshuacoureau12-creator/greeks-delta-hedging/blob/main/greeks_hedging.ipynb)

Simulation et analyse d'une stratégie de **couverture en delta dynamique** sur une option
européenne, avec quantification du **P&L résiduel de couverture** en fonction de la fréquence
de rebalancement et de la qualité de calibration de la volatilité.

Ce projet complète mes autres travaux de pricing (Black-Scholes / Monte Carlo / arbres CRR,
surface de volatilité, optimisation de portefeuille) en abordant la dimension **gestion
dynamique du risque**, centrale dans un poste d'analyste quantitatif côté risque / validation
de modèle.

## Contenu

| Section | Description |
|---|---|
| 1. Greeks analytiques | Delta, Gamma, Vega, Theta, Rho — formules fermées Black-Scholes |
| 2. Greeks par différences finies | Vérification, approche réutilisable pour modèles sans formule fermée |
| 3. Simulation GBM | Trajectoires sous la mesure risque-neutre |
| 4. Delta-hedging dynamique | P&L de couverture vs fréquence de rebalancement |
| 5. Vol de hedge mal calibrée | Impact d'une erreur de calibration sur le P&L de couverture |
| 6. Conclusion + Q&A | Synthèse et questions d'entretien type |

## Résultats clés

- L'écart-type du P&L de couverture **décroît** avec la fréquence de rebalancement,
  illustration numérique de la convergence vers la réplication continue de Black-Scholes
  (limite du modèle binomial à pas fins — Shreve, *Stochastic Calculus for Finance I*, Ch.1).
- Une vol de hedge mal calibrée introduit un **biais systématique** de P&L, distinct de
  l'erreur de discrétisation — un point clé en validation de modèle.

## Lancer le projet

```bash
pip install -r requirements.txt
jupyter notebook greeks_hedging.ipynb
```

Ou directement sur Colab via le badge ci-dessus.

## Pistes d'extension

- Coûts de transaction et fréquence de rebalancement optimale
- Couverture Delta-Gamma à deux instruments
- Deep hedging (réseau de neurones vs réplication analytique)

## Stack

`numpy` · `scipy` · `pandas` · `matplotlib`
