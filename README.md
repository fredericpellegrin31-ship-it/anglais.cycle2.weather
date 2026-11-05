# ☀️ The Weather – Jeux d'anglais (Cycle 2)

Un petit ensemble de jeux interactifs pour apprendre à **dire le temps qu'il fait en anglais**.
Destiné aux élèves de **cycle 2** (CP – CE1 – CE2), il fonctionne directement dans un navigateur, sans installation.

## 🎯 Objectifs pédagogiques

- Découvrir et mémoriser le vocabulaire de la météo.
- Reconnaître à l'oral et à l'écrit les phrases « **It's + météo** ».
- S'entraîner à prononcer ces phrases à voix haute.

## 📚 Vocabulaire travaillé

| Image | Anglais | Français |
|---|---|---|
| `sunny.png` | It's sunny | Il fait beau / ensoleillé |
| `cloudy.png` | It's cloudy | Il y a des nuages |
| `foggy.png` | It's foggy | Il y a du brouillard |
| `raining.png` | It's raining | Il pleut |
| `snowing.png` | It's snowing | Il neige |
| `stormy.png` | It's stormy | Il y a de l'orage |
| `windy.png` | It's windy | Il y a du vent |

## 🎮 Les jeux

Le menu (`index.html`) propose cinq activités :

| Fichier | Titre | Principe |
|---|---|---|
| `jeu1.html` | **Je révise** | Imagier interactif : on clique sur une image pour voir et écouter la phrase. Une version imprimable est prévue. |
| `jeu4.html` | **Le safari de la météo** | Jeu de questions en 3D : l'élève entend un mot et clique sur la bonne image dans le décor. |
| `jeu5.html` | **Weather racing** | Jeu de course en 3D : l'élève choisit la bonne image pour faire avancer son véhicule. |
| `jeu11.html` | **Weather quiz** | Quiz d'association entre images et phrases, avec un écran de résultats. |
| `jeu12.html` | **Défi oral : What's the weather?** | L'élève dit la phrase à voix haute. Cette activité utilise la reconnaissance vocale du navigateur. |

Chaque jeu comporte un bouton **🏠 Menu Principal** pour revenir à l'accueil.

## 🗂️ Organisation des fichiers

Tous les fichiers doivent se trouver **dans le même dossier** :

```
index.html
jeu1.html
jeu4.html
jeu5.html
jeu11.html
jeu12.html
README.md

sunny.png   cloudy.png   foggy.png   raining.png
snowing.png stormy.png   windy.png

jeu1.png  jeu4.png  jeu5.png  jeu11.png  jeu12.png   (miniatures du menu)
```

- Les **images de la météo** sont utilisées par les jeux.
- Les **miniatures** `jeuN.png` s'affichent dans le menu. Tant qu'elles sont absentes, un bandeau de remplacement apparaît.
- Si une image météo est absente, le jeu affiche à la place le **mot écrit en anglais**.

## ▶️ Utilisation

1. Ouvrir `index.html` dans un navigateur (ordinateur, tablette).
2. Choisir un jeu.
3. Autoriser le son. Pour le défi oral, autoriser aussi le **microphone**.

> 💡 Pour le défi oral (`jeu12`), privilégier **Google Chrome** ou **Microsoft Edge**, qui prennent en charge la reconnaissance vocale. Il vaut mieux héberger les fichiers sur un site (HTTPS) que les ouvrir directement depuis le disque, ce qui peut bloquer le microphone.
>
> 🌐 Une connexion internet est nécessaire, car les jeux chargent des bibliothèques externes (Tailwind CSS, React, Three.js…).

## 🛠️ Personnalisation (enseignant)

Le vocabulaire est défini dans chaque fichier `jeuN.html`, dans le bloc `words: [ ... ]` du thème par défaut :

```js
{ id: 'raining', en: 'Raining', speech: "It's raining", image: 'raining.png' }
```

- `en` : mot ou phrase affiché.
- `speech` : texte lu à voix haute par la synthèse vocale.
- `image` : nom du fichier image.

Pour ajouter ou modifier un mot, il suffit d'ajouter ou de changer une ligne de ce type dans chacun des jeux.

Les jeux savent aussi charger un thème personnalisé enregistré dans le navigateur (clé `app_vocab_themes` du `localStorage`, appelé via `?themeId=...`). Sans thème enregistré, le thème « Weather » par défaut est utilisé.

## 📄 Licence et crédits

Jeux créés pour un usage pédagogique en classe de cycle 2. Les images de la météo sont celles fournies par l'enseignant : vérifier leurs droits avant toute diffusion publique.
