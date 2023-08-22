# Travaux pratiques GIT & GitHub

## Gestion d'un dépôt à plusieurs

Cet exercice doit être réalisé en équipe de 2.
Le mini programme sur lequel vous travaillerez est localisé dans le répertoire `src` du dépôt.

# Préparation du projet

1. Le 1er membre de l'équipe crée un dépôt nommé `tp-git-exemple` et y ajoute une branche `develop`. 

2. Le 2nd membre de l'équipe "Fork" le dépôt du 1er membre.

2. Les 2 membres de l'équipe clonent leur dépôt en local sur leur machine.

2. Les 2 membres de l'équipe prennent connaissance des tâches à effectuer (dans la partie "Travail à réaliser" de ce document).

# Démarche à adopter 

Pour chaque tâche à réaliser : 

- Créer un ticket sur github (dans l'onglet "issues" de votre fork)
- Créer une branche et 1 commit lorsque la tâche est terminée. 
- Votre code doit obligatoirement être documenté.

En d'autres termes :
- 1 tâche = 1 ticket = 1 branche = 1 commit

> Note: Créez tous les tickets AVANT de commencer à coder !

# Travail à réaliser

Rappel : faites obligatoirement un COMMIT et un PUSH après chaque tâche enumérée dans ce fichier.

1. Dans le dépôt, créer un répertoire `src`. Ouvrir le temrinal dans ce répertoire et y créer une application C# Console en tapant la commande `dotnet new console`

2. Créer un modèle `Car` représentant une voiture. Une voiture est caractérisée par une marque et un modèle.

3. Dans le fichier Program.cs, demander à l'utilisateur de saisir une marque et un modèle qui seront directement affichés dans la console.

4. Dans le fichier Program.cs, créez une instance de `Car` dans une variable nommée `myCar` et y renseigner la marque et modèle saisi par l'utilisateur. Afficher ensuite le modèle suivi du nom de la voiture dans la console. (à ce niveau, la marque et modèle s'affichent 2 fois dans le programme).

5. Créer une classe "CarContainer" dont le rôle est de gérer une liste de Carnes. Cette classe permet de trier les voitures soir par nom (CarContainer.SortByLastName()), soit par modèle (CarContainer.SortByFirstName()). Dans les 2 cas, le tri se fait par ordre croissant. La classe doit implémenter l'interface décrite ci-dessous : 

```csharp
interface ICarContainer
{
    List<Car> SortByLastName();
    List<Car> SortByFirstName();
}
```

6. Créez une instance de CarContainer dans le programme principal et modifiez le code du programme afin que l'instance de Car créée à l'étape 4 soit ajoutée dans CarContainer.

7. Modifier le programme principal afin que l'utilisateur puisse ajouter autant de voiture qu'il le souhaite dans CarContainer. Pour chaque voiture, l'utilisateur saisit la marque et le modèle

8. Les doublons ne sont pas permis, à l'ajout d'une voiture dans CarContainer, on doit vérifier que le coupe "marque + modèle" n'existe pas déjà dans la liste.

9. Modifier le programme principal afin que 3 voitures soit créées au démarrage du programme

10. Modifier le programme principal afin de proposer à l'utilisateur de sauvegarder la liste au format JSON lorsqu'il a terminé d'ajouter des voitures.

11. Dans le fichier README.md de votre dépôt, rédiger une petite documentation qui indique comment se servir du programme.

12. Lorsque le programme est terminé et fonctionnel, Ajouter une `release` qui sera étiquetée `v.1.0.0`.