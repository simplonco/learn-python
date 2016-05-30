# Python

Python est un langage de programmation très facile à prendre en main.
Les fichiers contenant le code ont pour extension `.py`. Il suffit donc de
taper `python programme.py` par exemple dans une invite de commandes pour
éxecuter votre code.

Une invite de commandes peut s'ouvrir de deux manières : clic droit puis
`ouvrir une invite de commandes` ou windows + r et taper `cmd`.

# Opérations arithmétiques

Effectuer des calculs est intuitif :

```python
print('Calculs :')
print(3 + 2)
print((3 + 2) * 6)
print(11 / 5)
print(11 % 5) # modulo
print(2 ** 2) # puissance
```

# Variables

Les variables permettent d'enregistrer des données.

```python
argent = 100
print("J'ai", argent, "euros")

argent -= 50
argent = argent / 2
print("J'ai perdu de l'argent, il me reste", argent, "euros")

nom = "Antoine"
print("Je m'appelle", nom)
```

On peut lire du texte entré par l'utilisateur, lancez ce code et tapez votre
nom :

```python
nom = input('Entrez votre nom : ')
print("Bonjour", nom, "!")
```

# Répétitions

Effectuer des répétitions est possible avec la boucle `for`. Cet exemple repète
ainsi 5 fois l'instruction `print("Bonjour", nom, "!")` :

```python
nom = input('Entrez votre nom : ')
for i in range(5):
    print("Bonjour", nom, "!")
```

La variable `i` contient le numéro de la répétition, celui-ci commence à 0. On
peut s'en rendre compte et s'en servir ainsi :

```python
for i in range(10):
    print(i)
```

## Exercices

* Adapter le code précédent pour afficher tous les nombres de 1 à 100.
* Afficher un rectangle de taille 4x5 composé de "x".
* Afficher tous les nombres de à 100 à 1.
* Afficher un triangle composé de 10 "o" au total.

# Conditions

Les conditions permettent d'exécuter une partie du code selon certaines valeurs.

```python
nom = input('Entrez votre nom : ')
mot_de_passe = input('Mot de passe : ')

if nom == "Alice" and mot_de_passe == "password1234":
    print("Bienvenue Alice !")
else:
    print("Accès refusé")
```

On peut utiliser des comparaisons :

```python
taille = 120

if taille < 130:
    print("La taille minimale pour l'attraction est de 150cm !")
elif taille > 210:
    print("Vous êtes trop grand, vous ne pouvez pas rentrer !")
else:
    print("Vous pouvez y aller.")
```

# Tableaux

Les tableaux permettent de contenir plusieurs données d'un coup. Par exemple
une liste de noms :

```python
noms = ['Maxime', 'Aline', 'Pierre', 'Nina']
print(noms[0])
print(noms[2])
print("Il y a", len(noms), "noms enregistrés")

nouveau = input()
noms.append(nouveau) # ajoute un élément au tableau
print(noms) # affiche la liste en entier
```

On peut utiliser une boucle pour parcourir un tableau :

```python
classement = ['framboise', 'yaourt', 'noix de coco', 'fraise']
for i in range(len(classement)):
    print("Le gateau", classement[i], "a la place numéro", i+1)
```

Si on a pas besoin du  `i`, on peut tout simplement écrire :

```python
liste = ['framboise', 'noix', 'bûche de noël', 'fromage blanc']
print('Liste de gateaux :')
for gateau in liste:
    print("-", gateau)
```

## Exercice

* Écrire un programme qui demande 5 prénoms, les stocke dans un tableau, puis
les affiche.

# Chaînes de caractères

Les chaînes de caractères sont très similaires aux tableaux.

```python
texte = "j'ai faim"
for lettre in texte:
    print(i)
```

Comme pour les tableaux, on peut utiliser des conditions sur les chaînes :

```python
texte = "j'ai plus faim qu'avant"
for lettre in texte:
    if lettre == 'a':
        print('Il y a un "a" ici !')
```

Ou bien, pour vérifier la présence d'un élément :

```python
texte = "j'ai encore plus faim"
if 'encore' in texte:
    print("C'est bientôt l'heure de manger, pas de soucis !")
```

Une chaîne de caractères peut être découpée, donnant un tableau :

```python
texte = "Bonjour, je suis là !"
texte = texte.split()
for mot in texte:
    print(mot)
```

# Dictionnaires

Les dictionnaires sont similaires aux tableaux : ils permettent de stocker
plusieurs valeurs. On associe une valeur à une clé.

```python
dico = {"nom": "Marchand", "prénom": "Joseph", "ville": "Paris"}
print('Monsieur', dico['nom'], 'habite à', dico['ville'])
dico['age'] = 20 # ajout de clé
dico['nom'] = 'Martin' # remplacement
print(dico['prénom'], dico['nom'], 'a', dico['age'], 'ans')
```

On peut combiner ces différents types de données, par exemple un tableau
contenant des dictionnaires :

```python
courses = [
    {'nom': 'bananes', 'quantité': 5, 'type': 'fruit'},
    {'nom': 'abricots', 'quantité': 10, 'type': 'fruit'},
    {'nom': 'bonbons', 'quantité': 2, 'type': 'confiseries'},
    {'nom': 'steaks', 'quantité': 2, 'type': 'viande'},
    {'nom': "bouteilles d'eau", 'quantité': 4, 'type': 'boissons'},
]

for produit in courses:
    print('Il faut acheter', produit['quantité'], produit['nom'])
```

## Exercice

* Compléter ce code pour afficher les films diffusés après 12h :

```python
horaires = [
    {'film': 'Seul sur Mars', 'heure': 9},
    {'film': 'Astérix et Obélix Mission Cléopâtre', 'heure': 10},
    {'film': 'Star Wars VII', 'heure': 15},
    {'film': 'Time Lapse', 'heure': 18},
    {'film': 'Fatal', 'heure': 20},
    {'film': 'Limitless', 'heure': 20},
]
```
