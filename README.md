# Manon Training App

App de suivi pour le programme de préparation de Manon (poids de corps + cardio). Elle utilise la **même base de données Supabase** que les apps de Jox, Loan et Fifi — pas besoin de recréer un compte ou un projet.

## Particularité par rapport aux autres apps

Le programme de Manon n'a pas de charges (kg) : c'est du poids de corps (tractions, dips, pompes, gainage, handstand...) et du cardio, avec 2 séances fixes qui reviennent chaque semaine (pas de programme qui change de semaine en semaine). La progression se fait en augmentant les reps/le temps tenu et en réduisant la récupération entre les séries.

Du coup, la colonne "Charge (kg)" est remplacée par une ou plusieurs cases par exercice :
- une case par série/tour prescrit (reps réalisées, ou secondes tenues pour les exercices statiques)
- et, quand la récup est un levier de progression indiqué dans le programme (tractions, dips, pompes, handstand, gainage, corde à sauter, L-Sit), une case finale **"Récup (s)"** pour noter la récupération réellement utilisée.

Le tableau de bord affiche un graphique de progression pour chaque exercice (total de reps/secondes réalisées) et, séparément, un graphique de la récupération utilisée dans le temps.

## 1. Base de données

✅ Déjà faite — cette app utilise le même projet Supabase que Jox/Loan/Fifi, avec la colonne `athlete` qui sépare les données de chacun.

## 2. Configurer l'appli

✅ Déjà fait — `index.html` contient l'URL et la clé Supabase (les mêmes que pour les autres), et un code d'accès (`6284` par défaut, modifiable en cherchant `APP_PIN` dans le fichier).

## 3. Déployer sur Vercel (gratuit) — sans rien installer

Même procédure que pour les autres athlètes :

1. Crée un nouveau repo GitHub (ex: `manon-training-app`).
2. Upload les 2 fichiers (`index.html`, `README.md`) via "uploading an existing file" sur la page du repo.
3. Va sur [vercel.com/new](https://vercel.com/new), importe ce nouveau repo, déploie avec les réglages par défaut.
4. Récupère l'URL propre du projet (ex: `https://manon-training-app.vercel.app`, pas l'URL avec un hash aléatoire) dans la section "Domains" du projet.

## 4. Utilisation

Envoie l'URL + le code `6284` à Manon. Toi, tu ouvres la même URL sur ton ordinateur avec le même code pour suivre ses séances et sa progression.
