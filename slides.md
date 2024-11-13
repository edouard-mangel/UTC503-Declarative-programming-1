---
# theme id, package name, or local path
# Learn more: https://sli.dev/guide/theme-addon.html#use-theme
theme: seriph
# addons, can be a list of package names or local paths
# Learn more: https://sli.dev/guide/theme-addon.html#use-addon
addons: []
# title of your slide, will inferred from the first header if not specified
title: Introduction à la programmation déclarative
# titleTemplate for the webpage, `%s` will be replaced by the slides deck's title
titleTemplate: "%s - CNAM UTC503"
# information for your slides, can be a Markdown string
info: false
# author field for exported PDF or PPTX
author: Edouard MANGEL
# keywords field for exported PDF, comma-delimited
keywords: CNAM UTC503, Déclarative Programming, F#
layout: cover
background: "../images/background-1.png"
---

<style>
.slidev-layout.cover h1 {
    text-shadow: -1px 0 black, 0 2px black, 2px 0 black, 0 -2px black;
}

.slidev-layout.cover p {
    font-size: 2rem;
    text-shadow: -2px 0 black, 0 2px black, 2px 0 black, 0 -2px black;
    line-height: 2rem;
}

.slidev-layout h1+p {
    opacity: 0.8;
}
</style>

# Introduction à la programmation déclarative
En quoi la programmation déclarative facilite la compréhension et la testabilité du code ?

---
layout: fact
---

<u>**Définition :**</u>

## La **programmation déclarative** est un paradigme de programmation qui consiste à créer des applications sur la base de composants logiciels indépendants du contexte et ne comportant aucun état interne.

---
layout: section
---

# Les différences entre la programmation impérative et déclarative

---
layout: center
---

# Programmation Impérative
On ordonne à l'ordinateur **comment** effectuer une tâche, en lui donnant une série d'instructions.

<v-clicks>

Chaque **instruction** est exécutée dans un ordre précis, modifiant l'état du programme. 

Les boucles, les conditions et les variables sont des éléments clés de la programmation impérative.

Les langages impératifs les plus connus sont C, C++, C#, Java, Python, etc.

</v-clicks>


---
layout: center
---

# Qu'est-ce qu'une instruction ?

<v-clicks>

C'est une commande qui indique à l'ordinateur **comment** effectuer une tâche.

Par exemple: 

- Affecter une valeur à une variable
- Exécuter une opération arithmétique
- Modifier l'état d'une structure de données

</v-clicks>


---
layout: center
---

# Qu'est-ce qu'une expression ? 

<v-clicks>

C'est une combinaison de valeurs, de variables, d'opérateurs et de fonctions qui produit un résultat.

Par exemple:
- 5 + 3 : retourne la valeur 8.
- x * 10 : retourne le produit de x multiplié par 10, selon la valeur de x.
- myFunction(y) : retourne la valeur produite par myFunction appliquée à y.

</v-clicks>


---
layout: two-cols-header
--- 

# Exemples :

On cherche à filtrer une liste d'étudiants pour ne garder que ceux qui ont plus de 18 ans, et en extraire leur nom.

En utilisant une approche **impérative** (C#), on doit écrire un code qui spécifie **comment** effectuer cette tâche.

En utilisant une approche **déclarative** (SQL ou F#), on spécifie **quoi** doit être fait, sans se soucier de la manière dont cela est réalisé.

::left::

<v-clicks>

**Impérative (C#)**:
```csharp
var students = new List<Student> {
    new Student { Name = "Alice", Age = 20 },
    new Student { Name = "Bob", Age = 17 }
};
var result = new List<string>();
foreach (var student in students) {
    if (student.Age > 18) {
        result.Add(student.Name);
    }
}
```

</v-clicks>

::right::

<v-clicks>

**Déclarative (SQL)**:
```sql
SELECT name FROM students WHERE age > 18;
```
</v-clicks>

<v-click>

**Déclarative (F#)**:

```fsharp
students |> List.filter (fun s -> s.Age > 18) |> List.map (fun s -> s.Name)
```

</v-click>


---

# Le Concept Clé

Dans la programmation fonctionnelle, le code est écrit sous forme **d'expressions**, et non de séquences **d’instructions**.

---
layout: two-cols-header
---

# Programmation Fonctionnelle en Pratique
Les avantages de la programmation fonctionnelle se révèlent dans des situations réelles, en apportant des solutions aux problèmes suivants :

::left::
- Dépendances cachées et effets de bord imprévisibles
- Modèles répétitifs limitant la créativité
- Difficulté à raisonner sur l’ordre d’exécution
- Abstractions limitées, ne précisant pas uniquement les objectifs

---
layout: two-cols
---

# Problèmes Résolus par la Programmation Fonctionnelle
Voici quelques problèmes courants résolus par un style fonctionnel :

::left::
- Flux asynchrones complexes
- Concurrence sur plusieurs cœurs de processeur
- Différences de comportement entre tests unitaires et exécution réelle

::right::
> La programmation fonctionnelle peut structurer votre code de manière à résoudre ces problèmes efficacement.

---
layout: fact
---
# Conclusion
Adopter un style fonctionnel permet de créer un code plus prévisible, modulable et adapté aux environnements complexes du monde réel.

---

