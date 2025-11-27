# Exercices de reqêtes SQL

## Exercice 1 : Obtenir la liste des 10 villes les plus peuplées en 2012

```sql
    SELECT
	    ville_nom Ville,
        ville_population_2012 Population_2012
    FROM
	    villes_france_free
    ORDER BY
        ville_population_2012 DESC
    limit 10;
```

## Exercice 2 : Obtenir la liste des 50 villes ayant la plus faible superficie

```sql
    SELECT
        ville_nom Ville,
        ville_surface Superficie
    FROM
        villes_france_free
    ORDER BY
        ville_surface ASC
    limit 50;
```

## Exercice 3 : Obtenir la liste des départements d’outres-mer, c’est-à-dire ceux dont le numéro de département commencent par “97”

```sql
    SELECT
        departement_nom Departement,
        departement_code Code
    FROM
        departement
    WHERE departement_code >= 97
    ORDER BY departement_nom ASC;
```

## Exercice 4 : Obtenir le nom des 10 villes les plus peuplées en 2012, ainsi que le nom du département associé

```sql
     SELECT
	    ville_nom Ville,
        ville_population_2012 Population_2012,
        d.departement_nom Département
    FROM
	    villes_france_free v
    JOIN departement d ON v.ville_departement = d.departement_code
    ORDER BY
        ville_population_2012 DESC
    limit 10;
```

## Exercice 5 : Obtenir la liste du nom de chaque département, associé à son code et du nombre de commune au sein de ces département, en triant afin d’obtenir en priorité les départements qui possèdent le plus de communes

```sql

```

## Exercice 6 : Obtenir la liste des 10 plus grands départements, en terme de superficie

```sql

```

## Exercice 7 : Compter le nombre de villes dont le nom commence par “Saint”

```sql

```

## Exercice 8 : Obtenir la liste des villes qui ont un nom existants plusieurs fois, et trier afin d’obtenir en premier celles dont le n est le plus souvent utilisé par plusieurs communes

```sql

```

## Exercice 9 : Obtenir en une seule requête SQL la liste des villes dont la superficie est supérieur à la superficie moyenne

```sql

```

## Exercice 10 : Obtenir la liste des départements qui possèdent plus de 2 millions d’habitants

```sql

```

## Exercice 11 : Remplacez les tirets par un espace vide, pour toutes les villes commençant par “SAINT-” (dans la colonne qui contient les noms en majuscule)

```sql

```
