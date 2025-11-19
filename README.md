# 🤖 Bot Altissia - Automatisation d'exercices

Bot Python + Playwright pour automatiser les exercices Altissia de type "Type the right answer".

## 📦 Installation

```bash
# 1. Installer les dépendances Python
pip install -r requirements.txt

# 2. Installer les navigateurs Playwright
playwright install chromium

# 3. Configurer vos identifiants
cp .env.example .env
# Puis éditer .env avec vos identifiants Altissia
```

## ⚙️ Configuration

Créez un fichier `.env` à la racine du projet avec vos identifiants :

```env
ALTISSIA_USERNAME=votre_email@example.com
ALTISSIA_PASSWORD=votre_mot_de_passe
ALTISSIA_URL=https://www.altissia.com/
```

## 🚀 Utilisation

```bash
python main.py
```

Le bot va :
1. Se connecter à Altissia
2. Afficher la liste des exercices disponibles
3. Vous permettre de choisir un exercice
4. Résoudre automatiquement toutes les questions

## 🧩 Fonctionnement

Pour chaque question de type "fill in the blank" :
1. Clique sur "Valider" sans répondre → révèle la bonne réponse
2. Récupère la solution affichée
3. Remplit le champ avec la réponse
4. Valide la réponse
5. Clique sur "Continuer"
6. Passe à la question suivante

## 📁 Structure du projet

```
bot/
├── main.py              # Script principal
├── automations.py       # Fonctions d'automatisation
├── utils.py            # Utilitaires et helpers
├── requirements.txt    # Dépendances Python
├── .env               # Configuration (à créer)
└── README.md          # Ce fichier
```

## 🛠️ Sélecteurs HTML utilisés

- **Champ de réponse** : `input.c-iJOJc`
- **Bouton Valider** : `button:has-text("Valider")`
- **Réponse correcte** : `span.c-gUxMKR-bkfbUO-isCorrect-true`
- **Bouton Continuer** : `button.c-jUtMbh:has-text("Continuer")`

## ⚠️ Note

Ce bot est conçu à des fins éducatives. Utilisez-le de manière responsable.
