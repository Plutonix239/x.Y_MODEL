# x.Y_MODEL
Application d'intelligence artificielle permettant de générer automatiquement un rapport d'investissement à partir de données structurées sur une entreprise

## 🌟 Objectif

Concevoir une application d'intelligence artificielle permettant de générer automatiquement un rapport d'investissement (Investment Memorandum) à partir de données structurées sur une entreprise. L'architecture repose sur un modèle inspiré d'un réseau neuronal alvéolaire, où chaque module (ou "alvéole") effectue une tâche spécifique.

## 🔧 Architecture du projet

```
 x.Y_MODEL/
 │
 └︎ main.py                      # Point d'entrée principal

 ├︎ config/
 │   └︎ settings.py              # Paramètres globaux

 ├︎ data/
 │   ├︎ input/                   # Données sources
 │   ├︎ output/                  # Résultats générés
 │   └︎ schemas.py              # Schémas de données

 ├︎ core/
 │   ├︎ orchestrator.py          # Coordination des modules
 │   ├︎ runner.py                # Gestionnaire d'exécution
 │   └︎ utils.py                 # Fonctions utilitaires

 ├︎ controller/
 │   └︎ manager.py               # Ajout/suppression/modification de modules

 ├︎ modules/
 │   ├︎ executive_summary.py     # Alvéoles thématiques
 │   ├︎ market_analysis.py
 │   └︎ etc.

 ├︎ models/
 │   ├︎ gpt_interface.py         # Connexion aux LLM
 │   └︎ prompts/
 │       ├︎ executive_summary.txt
 │       └︎ market_analysis.txt

 ├︎ view/
 │   ├︎ report_builder.py        # Génération du rapport final
 │   └︎ preview.py              # Aperçu HTML interactif

 ├︎ logs/
 │   └︎ run_20240619.log         # Historique d'exécution

 ├︎ tests/
 │   ├︎ test_modules.py
 │   └︎ test_orchestrator.py

 └︎ sources/
     └︎ aurore.pdf               # Documentation fournie
```

## 🚀 Fonctionnement

* L'utilisateur fournit des données (secteur, métriques, etc.)
* `orchestrator.py` décompose la tâche et appelle chaque module spécialisé
* Les alvéoles utilisent `gpt_interface.py` + `prompts` pour produire du contenu
* Les résultats sont regroupés via `report_builder.py` pour générer un PDF
* L'affichage HTML est assuré par `preview.py`

## 💡 Technologies

* Python 3.10+
* GPT (OpenAI) ou Mixtral via Hugging Face API
* Markdown + Pandoc + LaTeX pour les rapports
* Architecture IA modulaire inspirée du vivant
* VS Code + LaTeX Workshop + Pandoc

## 🔹 Auteur

**Jonathan Cador**
Projet réalisé dans le cadre d'un stage en 2025
