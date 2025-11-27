# Exercice bonus

## Exercice 1 : Obtenir l’utilisateur ayant le prénom “Muriel” et le mot de passe “test11”, sachant que l’encodage du mot de passe est effectué avec l’algorithme Sha1.

```sql
    SELECT
        *
    FROM
        client
    WHERE
        client.password = SHA1("test11");
```

## Exercice 2 : Obtenir la liste de tous les produits qui sont présent sur plusieurs commandes.

```sql
    SELECT
        commande_ligne.nom Produit
    FROM
        commande_ligne
    GROUP BY
        commande_ligne.nom
    HAVING
        count(commande_ligne.nom) > 1;
```

## Exercice 3 : Obtenir la liste de tous les produits qui sont présent sur plusieurs commandes et y ajouter une colonne qui liste les identifiants des commandes associées.

```sql
    SELECT
        GROUP_CONCAT(cl.commande_id) Identifiant_commande,
        cl.nom Produit
    FROM
        commande_ligne cl
    JOIN
        commande c
            ON c.id = cl.commande_id
    GROUP BY
        cl.nom
    HAVING
        count(cl.nom) > 1;
```

## Exercice 4 : Enregistrer le prix total à l’intérieur de chaque ligne des commandes, en fonction du prix unitaire et de la quantité

```sql
UPDATE
	commande_ligne
        SET prix_total = commande_ligne.quantite * commande_ligne.prix_unitaire;
```

## Exercice 5 : Obtenir le montant total pour chaque commande et y voir facilement la date associée à cette commande ainsi que le prénom et nom du client associé

```sql

```

## Exercice 6 : (difficulté très haute) Enregistrer le montant total de chaque commande dans le champ intitulé “cache_prix_total”

```sql

```

## Exercice 7 : Obtenir le montant global de toutes les commandes, pour chaque mois

```sql

```

## Exercice 8 : Obtenir la liste des 10 clients qui ont effectué le plus grand montant de commandes, et obtenir ce montant total pour chaque client.

```sql

```

## Exercice 9 : Obtenir le montant total des commandes pour chaque date

```sql

```

## Exercice 10 : Ajouter une colonne intitulée “category” à la table contenant les commandes. Cette colonne contiendra une valeur numérique

```sql

```

## Exercice 11 : Enregistrer la valeur de la catégorie, en suivant les règles suivantes :

- “1” pour les commandes de moins de 200€
- “2” pour les commandes entre 200€ et 500€
- “3” pour les commandes entre 500€ et 1.000€
- “4” pour les commandes supérieures à 1.000€

```sql

```

## Exercice 12 : Créer une table intitulée “commande_category” qui contiendra le descriptif de ces catégories

```sql

```

## Exercice 13 : Insérer les ## Exercice : 4 descriptifs de chaque catégorie au sein de la table précédemment créée

```sql

```

## Exercice 14 : Supprimer toutes les commandes (et les lignes des commandes) inférieur au 1er février 2019. Cela doit être effectué en 2 requêtes maximum

```sql

```
