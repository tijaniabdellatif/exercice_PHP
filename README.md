# php-workshop
## Installation de PHP
1. Télécharger la dérnière version stable de php (`PHP 7.4`) sous format ZIP
2. Extrayer le contenu du fichier ZIP dans `C:\PHP7`.
3. Créer une copie du fichier C:\PHP7\php.ini-development et renommez la en C:\PHP7\php.ini.
4. Ouvrer le fichier C:\PHP7\php.ini nouvellement copié dans un éditeur de texte, tel que Visual Studio Code.
5. Modifier `memory_limit` de 128M à 1G (pour tenir compte des besoins en mémoire de `Composer` lorsqu'on aura besoin).
6. Rechercher `extension_dir` et décommenter la ligne (supprimez le point-virgule de tête, pour que la ligne ressemble à `extension_dir = "ext"`).
7. Pour ajouter C:\PHP7 à la variable d'environnement du chemin système de Windows 10
8. Dans une invite de commande (PowerShell ou un autre terminal), vérifiez que l'installation est réussie en tapant `php -v`

## Enoncé 1 : premier pas
Dans ce travail, nous apprendrons à utiliser le moteur de template intégré, le shell interactif de PHP, et à attribuer et utiliser des variables. À la fin, vous serez en mesure de le faire :

- Travailler avec le moteur de template intégré de PHP
- Exécuter un script PHP en ligne de commande
- Créer et attribuer des variables pour imprimer des messages simples sur le navigateur web
- Exécutez le serveur web intégré de PHP sur votre machine

1. Créez un fichier nommé `movies.php`.
2. Saisissez les données de la chaîne de requête dans le fichier pour stocker les détails des films, tels que les noms des films, les noms des acteurs/actrices et l'année de sortie.
3. Créez une structure HTML de base et affichez ensuite les chaînes de requête (`query string`) capturées.
4. Allez au terminal et exécutez la commande pour démarrer le serveur web intégré (Exécutez la commande suivante pour faire fonctionner le serveur web intégré de PHP : `php -S localhost:8085`).
5. Une fois le serveur web en marche, ouvrez la page PHP et ajoutez vos chaînes de requête à l'URL dans votre navigateur. La sortie attendue est illustrée dans la figure `enoncé1-sortie.png`.
- Documentez vous sur l'utilisation des variables prédéfies (`super globales`, `$_GET`) pour extraire les chaînes de requêtes (`query string`) que vous allez saisir dans l'`URL`.

## Enoncé 2 : type de données
À la fin de cet enoncé, vous pourrez :
- Utiliser les différents types de données dans PHP pour stocker et travailler avec les données
- Créer et utiliser des tableaux
- Mettre en œuvre le concept de tableaux multidimensionnels
- Travailler avec les opérateurs pour évaluer la valeur des opérations
- Effectuer un casting de pour convertir les variables d'un type à l'autre

Supposons que vous décidiez un jour de surveiller votre santé, mais que vous ne vouliez pas utiliser un outil tiers. Vous pourriez construire un outil simple pour prendre des mesures, notamment le nom, le poids et la taille. À partir de là, vous pouvez calculer votre `IMC`.

Dans cette activité, vous écrirez un script qui prendra des variables du script afin d'effectuer des calculs pour obtenir un résultat d'IMC. Vous définirez un certain nombre de valeurs par défaut, mais vous construirez également une option pour spécifier vos propres données via des chaînes de requête.

Voici les étapes à suivre pour réaliser l'activité :

1. Créer un fichier `tracker.php`.
2. Définir une chaîne `$name` pour stocker le nom de l'utilisateur.
3. Définir un entier `$weightKg` pour stocker le poids en kilogrammes.
4. Définir un entier `$heightCm` pour stocker la hauteur en centimètres.
5. Convertir la hauteur en mètres.
6. Calculer la valeur de la hauteur au carré.
7. Calculer l'IMC en divisant le poids de l'utilisateur par la valeur de la taille au carré.
8. Afficher un message à l'écran affichant le nom et le résultat de l'IMC.

## Enoncé 3 : structures de controle
Dans cette activité, nous pratiquerons le looping imbriqué et appliquerons des conditions pour limiter les itérations des boucles intérieures et extérieures. Nous disposerons d'un tableau associatif multidimensionnel dans lequel le nom du réalisateur sert de clé pour contenir un tableau de noms de films. Ainsi, chaque élément du tableau associatif contient un nom de réalisateur comme clé et le tableau des noms de films comme valeur. Nous allons introduire une boucle extérieure pour faire une boucle à travers les éléments du tableau associatif et imprimer le nom du réalisateur, utilisé comme clé. Une autre boucle interne doit boucler le tableau des noms de films de ce réalisateur - c'est la clé. Les arguments agissent comme des étapes d'itération de boucle pour maintenir où le premier argument définit combien de fois le nom d'un réalisateur doit être imprimé et le second argument définit combien de noms de films doivent être imprimés à partir du réalisateur donné.
- Le tableau multidimensionnel contient cinq réalisateurs.
- Les étapes à effectuer sont les suivantes :
1. Créer le fichier script `activity-movies.php`, qui prend deux arguments, tous deux numériques : le premier argument sera utilisé pour le nombre de réalisateurs, et le second sera utilisé pour le nombre de films.
2. Ajouter `un tableau imbriqué` contenant une `liste` de cinq réalisateurs, chaque entrée contenant une liste de cinq titres de films.
3. En exécutant le script, imprimez la liste des réalisateurs et des titres de films, comme l'exigent les arguments d'entrée.
4. Si les arguments d'entrée ne sont pas passés, considérez alors la valeur par défaut de 5 pour les deux.
- Voici quelques exemples de résultats obtenus en exécutant le script php activity-movies.php:

Les films de Steven Spielberg :

> The Post

> Le pont des espions

Les films de Christopher Nolan :

> Dunkerque

> Quai

Les films de Martin Scorsese :

> Le Loup de Wall Street

> Hugo

## Enoncé 4 : les fonction (callables)
Vous travaillez sur une application web d'une calculatrice. Imaginons qu'on vous donne tout le code de l'interface utilisateur, mais on vous demande de créer la fonction qui effectuera les calculs. Vous devez créer une fonction unique qui soit réutilisable pour tous les calculs nécessaires dans l'application.

Les étapes suivantes vous aideront à réaliser l'activité :

1. Créez une fonction qui calculera et retournera le factoriel du nombre d'entrée.
2. Créez une fonction qui retournera la somme des nombres d'entrée (un nombre variable de paramètres).
3. Créez une fonction qui évaluera `$number` entré, qui doit être un nombre entier et qui retournera si le nombre est un nombre premier ou non. Le type de retour de cette fonction est un booléen (bool).
4. Créer une fonction `performOperation` de base qui traitera les opérations mathématiques prédéfinies. Le premier paramètre de la fonction `performOperation` doit être une chaîne de caractères, soit "factorielle", soit "somme", soit "nombre premier". Les arguments restants sont transmis à la fonction mathématique appelée en tant qu'arguments.

## Enoncé 5 : Programmation Orienté Objet (POO)

Dans cette exercice, nous mettrons en œuvre les concepts de la POO pour créer des classes d'étudiants et de professeurs avec des constructeurs, des attributs et des méthodes de membres paramétrés. Nous instancierons les deux classes et établirons une relation entre les objets. Un professeur peut avoir un certain nombre d'étudiants inscrits dans sa classe. La liste des étudiants doit être imprimée en utilisant une méthode membre de l'objet Professeur.

Les étapes à effectuer sont les suivantes :

1. Créer un répertoire pour y mettre tout le contenu de nos activités. Il doit s'agir de notre répertoire de travail (vous pouvez vous connecter au répertoire).
2. Créez un fichier script appelé `main.php`.
3. Créez des classes de `professeurs` et d'`étudiants` dans des répertoires séparés avec les fonctionnalités suivantes : 
- Les deux utilisent leur propre `espace de noms` pour charger les classes automatiquement.
- Les deux prennent le nom comme premier `argument` dans le `constructeur` ; la classe Professeur accepte le second argument comme `liste d'étudiants` - la liste sera filtrée pour les instances de Student uniquement.
- Les deux auront la propriété de titre, qui, par défaut, pour la classe Professeur est Prof. et pour la classe Étudiant est Student.

4. Créez une fonction qui imprimera le titre du professeur, son nom, le nombre d'étudiants et la liste des étudiants.
5. Créez une instance de Professeur, en fournissant un nom et une liste d'étudiants - des instances d'Étudiant avec un nom dans le constructeur.
6. Ajoutez un nombre aléatoire d'instances de `Etudiant` à l'instance `Professeur`.
7. Changez le titre du `professeur` en `Dr`.
8. Imprimez la sortie en invoquant la fonction avec l'instance Professor.

## Enoncé 6 : utiliser un HTTP de manière sécurisé
Il vous est demandé de mettre en place un `formulaire de contact de support` sur un nouveau site web de marque. Le formulaire sera disponible uniquement pour les utilisateurs authentifiés, sur la page Profil, et la partie authentification est également à votre charge. Il y aura deux types d'utilisateurs : le niveau standard et le niveau VIP. Les utilisateurs standard pourront demander de l'aide une fois par jour, tandis que les utilisateurs VIP n'auront aucune limite. Le formulaire contiendra les champs suivants : le nom et l'adresse électronique à laquelle les réponses doivent être envoyées et le message. Les données du formulaire devront être `sanitisées et validées` avant d'être enregistrées. Les règles sont les suivantes : tous les champs obligatoires doivent être remplis, utiliser une adresse électronique valide et le message ne doit pas comporter moins de 40 caractères.

Voici les étapes à suivre pour réaliser l'activité :

1. Écrivez le code pour récupérer les données de l'utilisateur pour l'utilisateur qui est connecté.
2. Implémentez la méthode `\Handlers\Login::handle()` pour valider les données de l'utilisateur.
3. Créer un formulaire de connexion.
4. Créez la page de profil. Ici, vous devriez construire le fichier `src/templates/profile.php` à partir de zéro. Tout d'abord, ajoutez les salutations et un bouton de déconnexion.
5. Ajoutez une zone de support et divisez-la en deux parties horizontales égales.
6. Créez un formulaire de contact avec les spécifications suivantes : deux entrées de type texte, pour le nom et le courriel, et une entrée de zone de texte pour le message. Chacune d'entre elles aura un élément `label` associé et, en cas d'erreurs, celles-ci devront être imprimées sous l'entrée avec des données erronées.
Note : Vous pouvez travailler avec les composants de bootstrap. Vous pouvez vous référer à la documentation du cadre Bootstrap et utiliser le composant d'alerte.

7. Écrivez le code pour éviter qu'un utilisateur de niveau standard n'envoie plus d'un formulaire par jour. Là encore, vous pouvez utiliser les composants d'alertes du cadre Bootstrap.
8. `Sécurisez` le formulaire en générant et en utilisant un jeton `CSRF`.
9. Sur le bouton d'envoi, nous pouvons ajouter d'autres données de formulaire, afin de savoir avec certitude quel formulaire nous devons traiter dans les scripts PHP ; cela est très utile lorsque plusieurs formulaires sont ajoutés sur une seule page HTML, et que chacun envoie des données à la même URL.
10. Écrivez le code pour afficher l'historique de la liste des messages. Vous pouvez choisir le composant de la carte et imprimer tous les détails du message. Chaque entrée de l'historique stockée contiendra les données du formulaire (c'est-à-dire la clé du formulaire) et l'heure à laquelle le formulaire a été envoyé (c'est-à-dire la clé `timeAdded`).
11. Écrivez le code pour valider le formulaire envoyé, puis écrivez le code pour rafraîchir la page si la validation est réussie.
12. Saisissez le code pour envoyer les données suivantes au modèle : le nom d'utilisateur (la salutation), les erreurs éventuelles du formulaire, le jeton `CSRF` du formulaire et l'historique des formulaires envoyés.
13. Ajoutez la logique de validation du formulaire dans une méthode séparée.
14. Vérifiez s'il y a eu plusieurs envois dans le cas d'utilisateurs de niveau standard.
15. Écrivez le code pour afficher un message d'erreur si l'utilisateur tente de soumettre un champ de nom vide.
16. Mettre en œuvre la validation du courrier électronique à l'aide de la fonction `filter_var()` avec la validation `FILTER_VALIDATE_EMAIL`.
17. Pour le champ du message, écrivez le code pour vous assurer que le message comporte au moins 40 caractères.
18. Rassemblez les données du formulaire sanitisées et stockez-les dans la variable `$form`, qui est ensuite renvoyée avec la variable `$errors`.
19. Nous pouvons maintenant tester notre implémentation complète. 


## Biref projet : Application de gestion des contacts

### Contexte
Vous êtes tenu de créer un site web où les utilisateurs peuvent créer un compte et se connecter ensuite pour gérer une liste privée de contacts. Le site web utilisera des bases de données pour stocker les données de connexion des utilisateurs, ainsi que pour stocker les contacts de chaque utilisateur.

En plus des fonctionnalités de la base de données, vous devrez utiliser d'autres fonctionnalités afin de créer le site web (par exemple, les conditions, les déclarations de contrôle, les fonctions, la programmation orientée objet et la validation des formulaires, en utilisant HTTP).

Les pages requises sont les suivantes :

- Page d'accueil 
- Pages de connexion et d'inscription
- Page de profil
- Liste de contacts et ajout/modification de la page du formulaire de contact
### Mise en page et briefing

La mise en page est telle qu'elle est présentée :

#### La page d'accueil (voir `home_page.png`)

Une barre de navigation horizontale se trouve en haut de la page, avec le titre du site à gauche et le bouton de connexion à droite. Après une connexion réussie, le bouton `Connexion` est remplacé par le nom d'utilisateur, qui renvoie à la page `Profil`, au lien de la page `Contacts` et au lien Déconnexion.

Le contenu est un message avec deux liens d'appel à l'action : `S'inscrire`  et `Se connecter`.

#### La page de connexion (voir `login_page.png`) :

La connexion est basée sur le nom d'utilisateur et le mot de passe, le contenu est donc un simple formulaire de connexion, avec des champs pour le nom d'utilisateur et le mot de passe, et un bouton de connexion. La dernière phrase est un lien d'appel à l'action pour l'inscription.

Après s'être connecté, l'utilisateur est redirigé vers la page Profil.

#### La page d'inscription (voir `sine-up_page.png`)

Le contenu est le formulaire d'inscription, avec les entrées suivantes :

- Nom d'utilisateur
- Mot de passe
- Vérification du mot de passe
Le nom d'utilisateur doit comporter au moins trois caractères, et être uniquement alphanumérique. Le mot de passe doit comporter au moins six caractères et doit être vérifié par un second mot de passe saisi lors de l'inscription. Toute erreur de formulaire doit être affichée sous l'entrée d'où proviennent les données, voir `form_validation_error.png` :


Les comptes enregistrés doivent également conserver la date d'inscription. Après l'inscription, l'utilisateur est redirigé vers la page Profil.

#### La page de profil (voir `profile_page.png`) :


Elle contient un message d'accueil, les données du profil et l'heure de connexion à la session. Alors que le nom d'utilisateur et la date d'inscription sont stockés dans la base de données, l'heure de connexion à la session peut être stockée dans la session en cours.

#### La page Contacts (voir `contact_page.png`) :


Le contenu est divisé en deux : la liste des contacts et le formulaire d'ajout/de modification des contacts (voir `Contacts_list(CRUD).png`).

La liste de contacts énumère les enregistrements de contacts, chaque enregistrement ayant les liens `Modifier` et `Supprimer`. Si la liste est vide, alors affichez le message approprié au lieu de rendre la table vide.

#### Le formulaire de contact aura les noms de champs suivants :

- Nom : obligatoire ; au moins deux caractères
- Téléphone : facultatif ; ne doit autoriser que le +-() 666988756
- Courriel : obligatoire ; doit être validé
- Adresse : facultative ; 255 caractères maximum


Les messages d'erreur concernant des données non valides doivent être placés sous les entrées d'où émanent les données.

En accédant à la page Contacts, le formulaire est prêt à être utilisé pour créer de nouveaux contacts. Une fois que le bouton "Modifier" d'un contact est enfoncé, les coordonnées du contact sont remplies dans le formulaire ; l'envoi du formulaire met à jour le contact existant.

Lorsqu'un utilisateur authentifié accède à la page d'accueil, à la page de connexion ou à la page d'inscription, il est redirigé vers la page de profil.

Le titre de la page par défaut est Liste de contacts.

### Déroulement
Voici les étapes à suivre pour réaliser l'activité :

1. Créer les nouveaux modèles de page - les pages d'inscription et de liste de contacts.
2. Créer les gestionnaires de demande pour les pages d'inscription et de contact.
3. Ajouter le composant Base de données, où l'objet PDO sera invoqué pour fonctionner avec le serveur MySQL.
4. Ajouter le composant Auth, qui s'occupera d'autres tâches d'authentification couramment utilisées (par exemple, vérifier si l'utilisateur est connecté).
5. Créer la classe User, en tant que modèle de ligne de table (dans le répertoire src/models/), qui regroupera certaines fonctionnalités connexes (comme la vérification du mot de passe d'entrée par rapport au hachage du mot de passe existant).
6. Ajuster le gestionnaire de connexion afin d'utiliser la base de données comme source de données pour les utilisateurs.
7. Ajuster le gestionnaire de profil pour qu'il ne récupère que l'utilisateur dans la base de données et l'envoie au modèle.