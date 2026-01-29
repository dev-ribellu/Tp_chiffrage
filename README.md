# 🔐 Chiffré & Déchiffré

Application web de chiffrement et déchiffrement de messages utilisant l'algorithme de César avec une clé personnalisée.

## 📋 Description

Ce projet permet de chiffrer et déchiffrer des messages textuels en utilisant une variante de l'algorithme de César. La clé de chiffrement est convertie en une valeur numérique basée sur les codes ASCII de ses caractères.

## ✨ Fonctionnalités

- **Chiffrement de messages** : Convertit votre texte en clair en texte chiffré
- **Déchiffrement de messages** : Récupère le message original à partir du texte chiffré
- **Clé personnalisée** : Utilisez n'importe quelle chaîne de caractères comme clé
- **Interface style "hacker"** : Design inspiré de Matrix avec effets néon verts
- **Validation des entrées** : Vérification que tous les champs sont remplis

## 🚀 Installation

1. Clonez ou téléchargez ce dépôt
2. Assurez-vous d'avoir les fichiers suivants :
   - `index.html` - Page principale
   - `style.css` - Feuille de style

3. Ouvrez `index.html` dans votre navigateur web

## 💻 Utilisation

### Chiffrement

1. Entrez votre message dans le champ "Entrez votre message à chiffrer"
2. Saisissez une clé de chiffrement dans le champ "Entrez la clef"
3. Cliquez sur "Chiffrer le message"
4. Le message chiffré s'affiche en dessous

### Déchiffrement

1. Entrez le message chiffré dans le champ "Entrez votre message à déchiffrer"
2. Saisissez la même clé utilisée pour le chiffrement
3. Cliquez sur "Déchiffrer le message"
4. Le message original s'affiche en dessous

## 🔧 Algorithme

### Calcul de la clé

La clé est convertie en valeur numérique :
```javascript
somme = (sum des codes ASCII de la clé) % 26
```

### Chiffrement

Pour chaque caractère alphabétique :
- **Majuscules (A-Z)** : `((code - 65 + somme) % 26) + 65`
- **Minuscules (a-z)** : `((code - 97 + somme) % 26) + 97`
- Les caractères non-alphabétiques restent inchangés

### Déchiffrement

Pour chaque caractère alphabétique :
- **Majuscules (A-Z)** : `((code - 65 - somme + 26) % 26) + 65`
- **Minuscules (a-z)** : `((code - 97 - somme + 26) % 26) + 97`

## 📁 Structure du projet

```
chiffré&déchiffré/
│
├── index.html          # Page principale avec la logique JavaScript
├── style.css           # Feuille de style (thème hacker)
└── README.md           # Ce fichier
```

## 🎨 Personnalisation

### Modifier le thème

Éditez `style.css` pour changer :
- La couleur principale : `#00ff41` (vert néon)
- La couleur de fond : `#0d0208` (noir profond)
- Les effets d'animation et de glow

### Modifier l'algorithme

Dans `index.html`, vous pouvez modifier :
- La fonction `avoir_Somme()` pour changer le calcul de la clé
- Les fonctions `encrypt()` et `decrypt()` pour un autre algorithme

## ⚠️ Limitations

- **Sécurité** : Cet algorithme est à usage éducatif uniquement. Il n'est PAS sécurisé pour des données sensibles.
- **Caractères** : Seuls les caractères alphabétiques (A-Z, a-z) sont chiffrés
- **Clé faible** : L'utilisation du modulo 26 limite la complexité de la clé

## 🛠️ Technologies utilisées

- HTML5
- CSS3 (avec animations et effets)
- JavaScript vanilla (ES6+)

## 📝 Exemple d'utilisation

```
Message original : "Hello World"
Clé : "secret"
Message chiffré : "Lipps Asvph"

Pour déchiffrer :
Message chiffré : "Lipps Asvph"
Clé : "secret"
Message déchiffré : "Hello World"
```



## 📄 Licence

Ce projet est libre d'utilisation à des fins éducatives.

## 👤 Auteur

Créé dans le cadre d'un projet éducatif de cryptographie.

---

