# Projet : Générateur d'Articles Dynamique avec Changement de Couleur de Fond

## Description

Ce projet est une page HTML simple qui permet à l'utilisateur de créer des articles dynamiquement en remplissant un formulaire. Le formulaire comporte trois champs : **Titre**, **Adresse** et **Description**. Une fois le formulaire soumis, un nouvel article est ajouté sous le formulaire. Il y a également un bouton permettant de changer la couleur de fond de la page à **violet**.

## Fonctionnalités

- **Formulaire dynamique** : L'utilisateur peut saisir un titre, une adresse et une description. Lors de la soumission, un article est créé et ajouté à la page sans recharger celle-ci.
- **Changement de couleur de fond** : Un bouton permet de modifier la couleur de fond de la page en **violet**.

## Structure du projet

Le projet contient un fichier HTML avec des éléments de base tels que des champs de texte et un bouton, ainsi qu'un peu de JavaScript pour rendre le contenu interactif. Le script permet d'ajouter des articles à la page et d'appliquer un changement de couleur de fond à l'aide de la méthode `style.backgroundColor`.

### Fichier `index.html`

```html
<!DOCTYPE html>
<html lang="fr">

<head>
    <meta charset="UTF-8">
    <title>finalement</title>
</head>

<body>

    <!-- Formulaire pour ajouter un article -->
    <form id="articleForm">
        <input type="text" id="title" placeholder="Titre" required>
        <input type="text" id="address" placeholder="Adresse" required>
        <textarea id="description" placeholder="Description" required></textarea>
        <button type="submit">Submit</button>
    </form>

    <!-- Conteneur pour afficher les articles -->
    <div id="articlesContainer"></div>

    <h2>The backgroundColor Property</h2>

    <!-- Bouton pour changer la couleur de fond -->
    <button type="button" onclick="myFunction()">Changer la couleur de fond</button>

    <script>
        // Fonction pour gérer la soumission du formulaire
        document.getElementById('articleForm').addEventListener('submit', function(event) {
            event.preventDefault(); // Empêcher le rechargement de la page

            // Récupérer les données du formulaire
            const titre = document.getElementById('title').value;
            const adresse = document.getElementById('address').value;
            const description = document.getElementById('description').value;

            // Créer un article HTML
            const article = document.createElement('article');
            article.innerHTML = `<h3>${titre}</h3><p>${adresse}</p><p>${description}</p>`;

            // Ajouter l'article au conteneur d'articles
            document.getElementById('articlesContainer').appendChild(article);
        });

        // Fonction pour changer la couleur de fond en violet
        function myFunction() {
            document.body.style.backgroundColor = "purple";
        }
    </script>

</body>

</html>


Comment utiliser
Clonez le repository :

bash
Copier le code
git clone https://github.com/votre-utilisateur/votre-repository.git
Ouvrir le fichier HTML dans un navigateur :

Naviguez vers le fichier index.html dans le dossier cloné.
Ouvrez le fichier dans un navigateur pour voir le formulaire en action et tester la fonctionnalité du changement de couleur de fond.
Ajouter des articles :

Remplissez le formulaire avec un titre, une adresse et une description.
Cliquez sur le bouton Submit pour ajouter un nouvel article sous le formulaire.
Changer la couleur de fond :

Cliquez sur le bouton Changer la couleur de fond pour modifier la couleur de la page en violet.
Technologies utilisées
HTML : Structure de base de la page.
JavaScript : Logique interactive pour gérer la soumission du formulaire et modifier l'apparence de la page.
CSS : Aucune utilisation de CSS dans ce projet, tout se fait avec HTML et JavaScript pour la partie visuelle.
Contribuer
Si vous souhaitez améliorer ce projet, vous pouvez :

Forker ce projet.
Créer une branche pour ajouter une fonctionnalité ou corriger un bug.
Soumettre une Pull Request avec vos changements.
................................................................................

### Explication du fichier `README.md` :
- **Titre du projet** : "Générateur d'Articles Dynamique avec Changement de Couleur de Fond" pour décrire ce que fait le projet.
- **Description** : Présentation des principales fonctionnalités du projet : formulaire pour créer des articles et bouton pour changer la couleur de fond.


- **Comment utiliser** : Instructions pour cloner le projet, l'ouvrir dans un navigateur, et tester ses fonctionnalités.
- **Technologies utilisées** : Information sur les technologies employées (HTML et JavaScript).
- **Auteurs** : TheDarkPassenger..

------------------------------------------------------------------------------------------------------------

#END
