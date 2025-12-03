# Travail Pratique 3: Gestion d'inventaire avec une classe Produit

## Contexte
On vous demande de modéliser une classe Produit pour pouvoir gérer un inventaire.

Ce travail doit être fait en équipe de 2 ou 3. Tout travail solo ne sera pas corrigé et se verra attribué la note de 0.


## Requis à implémenter

1) Créer une class ```Produit``` qui contient les attributs suivants :
    - ``code``
      - le code du produit ex: P001
    - ``nom``
      - le nom du produit
    - ``categorie``
      - la catégorie du produit ex: "ALIMENTAIRE", "VETEMENT", etc
    - ``prix``
      - prix unitaire du produit
    - ``quantite``
      - quantité en stock
2) Ajouter un constructeur ``__init__`` qui permet d'initialiser tous les attributs de la classe ``Produit``
   - Tous les attributs doivent être passés en paramètre du constructeur.
   - Mettre des valeurs par défaut raisonnables aux arguments (ex. prix = 0.0, quantite = 0) si nécessaire.
3) Créer les différentes méthodes setter et getter pour chaque attribut de la classe.
   - les setters de ``prix`` et ``quantite`` doivent refuser les valeurs négatives 
      - si une valeur négative est reçue, laisser l’ancienne valeur ou mettre 0).
4) Ajouter une méthode d’instance nommée ``valeur_stock()`` qui retourne la valeur totale du stock pour ce produit, c’est-à-dire :
      ``valeur_stock = prix * quantite``
5) Ajouter une méthode spéciale ``__str__`` qui retourne une chaîne de caractères formatée contenant toutes les informations d’un produit
   - par exemple : ``Code: P001 | Nom: Lait 2% | Catégorie: ALIMENTAIRE | Prix: 3.29$ | Quantité: 20 | Valeur stock: 65.80$``
6) Instancier dans une liste nommée inventaire au moins 6 objets ``Produit``.
   - Les informations doivent être écrites directement dans le code (hard codées dans l'appel du constructeur), sans saisie au clavier.
   - Utiliser au moins 3 catégories différentes.
7) Créer une fonction (pas une méthode) nommée ``produit_plus_cher`` qui prend en paramètre la liste inventaire et retourne le ou les produits ayant le prix unitaire le plus élevé.
   - Dans le programme principal, appeler cette fonction et afficher les informations du produit retourné.
8) Demander à l’utilisateur de saisir une catégorie au clavier, puis :
   - Afficher tous les produits de l'inventaire qui appartiennent à cette catégorie.
   - La comparaison doit être insensible à la casse
     - ex. "alimentaire", "ALIMENTAIRE", "Alimentaire" doivent être acceptés comme la même catégorie.
   - Si aucun produit ne correspond, afficher un message approprié.
9) Créer une fonction (pas une méthode) nommée ``appliquer_promotion`` qui :
   - Prend en paramètre la liste inventaire, une catégorie et un pourcentage de réduction (ex. 10 pour 10%).
   - Diminue le ``prix`` de tous les produits de cette catégorie selon le pourcentage donné.
     - Exemple : prix = 100, réduction 10% → nouveau prix = 90.
   - Dans le programme principal :
     - Afficher les produits d’une catégorie avant la promotion.
     - Appeler la fonction ``appliquer_promotion``.
     - Afficher à nouveau les produits de cette catégorie après la promotion.
10) Trier les produits de l’inventaire par valeur de stock décroissante (du stock le plus élevé au plus faible), puis :
    - Afficher la liste triée en utilisant la méthode ``__str__`` pour chaque produit.
    - Indiquer clairement à l’écran que l’affichage est ``trié par valeur de stock décroissante``.
                               
## Barème
1) Classe ``Produit`` + attributs (3 pts)
2) Constructeur ``__init__`` (3 pts)
3) Setters & getters (6 pts)
4) Méthode ``valeur_stock`` (3 pts)
5) Méthode ``__str__`` (3 pts)
6) Liste inventaire avec au moins 6 produits (4 pts)
7) Fonction ``produit_plus_cher(inventaire)`` (5 pts)
8) Recherche par catégorie (saisie clavier, insensible à la casse) (5 pts)
9) Fonction ``appliquer_promotion(inventaire, categorie, pourcentage)`` (4 pts)
10) Tri par valeur de stock décroissante  (4 pts)

## Critères d'évaluation
- Fonctionnalité du code
  - Fonctionnement
  - Respect des requis
- Respecte des normes et conventions (PEP-008)
- Beauté du code
  - Facilité à comprendre le code
  - efficience
  - présence de commentaires

