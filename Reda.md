# Votre Objectif

Dans ce checkpoint, on vous demande d’écrire un algorithme qui lit une phrase, caractère par caractère.  
La phrase se termine obligatoirement par un point (`.`).

L’objectif est de déterminer :

- La longueur de la phrase (le nombre total de caractères).
- Le nombre de mots dans la phrase (en supposant que les mots sont séparés par un seul espace).
- Le nombre de voyelles dans la phrase.

---

# Instructions

- Chaque caractère doit être traité séparément.
- Le dernier caractère de la phrase est toujours un point (`.`).
- Vous devez utiliser **trois variables compteurs** :
  - Un compteur pour le nombre de caractères.
  - Un compteur pour le nombre de mots.
  - Un compteur pour le nombre de voyelles.

---

# Remarques

- Les voyelles à considérer sont : `a, e, i, o, u` (majuscule et minuscule si nécessaire).
- Les mots sont séparés par **un seul espace**.
- Le traitement s’arrête dès que le point est rencontré.

# Solution

Tout d’abord, on commence par initialiser :

- Trois variables compteurs de type **entier (integer)**.
- Une variable de type **string** pour stocker la phrase.
- Une variable de type **caractère (char)** pour lire chaque caractère.

Ensuite, l’utilisateur doit entrer la phrase souhaitée.  
On initialise tous les compteurs à `0`.

Comme on ne connaît pas à l’avance le nombre de caractères, on utilise une **boucle `while`**.  
La condition de la boucle est que le caractère lu soit différent du point (`.`), qui représente le dernier caractère de la phrase.

À chaque itération :

- On incrémente le compteur de longueur (nombre de caractères).
- On utilise une structure `if` pour vérifier les conditions suivantes :

  1. Si le caractère est un **espace**, cela indique un nouveau mot → on incrémente le compteur de mots.
  2. Si le caractère est l’une des **voyelles** (`a, e, i, o, u , y`), alors on incrémente le compteur de voyelles.

Le traitement s’arrête lorsque le point est rencontré.