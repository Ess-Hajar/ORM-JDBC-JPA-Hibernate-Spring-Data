

<h2 style="color : skyblue">Introduction</h2>
<p>
Dans l'univers dynamique du développement d'applications, la gestion efficace de la persistance des données demeure un élément essentiel. Face à ce défi, une palette de technologies, allant de l'ORM (Object-Relational Mapping) au JDBC (Java Database Connectivity), en passant par des cadres renommés tels que JPA (Java Persistence API), Hibernate et Spring Data, a émergé pour redéfinir la manière dont les développeurs interagissent avec les bases de données. Ces avancées offrent des solutions robustes et flexibles pour assurer la persistance des données.
<br>

Cette étude approfondie se focalise sur l'exploration de ces concepts fondamentaux, mettant en lumière leur rôle central dans le développement d'applications Java. Nous scrutons les différentes strates de l'architecture de persistance, de l'accès aux bases de données avec JDBC à l'utilisation de JPA pour simplifier la gestion des objets persistants. Par ailleurs, nous plongeons dans l'univers de Hibernate, un framework ORM de renom facilitant la liaison entre les objets Java et les bases de données relationnelles.
<br>

Enfin, notre parcours nous conduit à Spring Data, un composant puissant du framework Spring, simplifiant davantage la gestion des données en fournissant une interface cohérente et flexible pour la persistance. Notre objectif est de mettre en exergue les avantages, les fonctionnalités clés et les scénarios d'utilisation de ces technologies, tout en illustrant leur implémentation concrète.
</p>
<h2 style="color: skyblue">Énoncé</h2>
<ol>
  <li>Installer IntelliJ Ultimate.</li>
  <li>Créer un projet Spring Initializer en incluant les dépendances JPA, H2, Spring Web et Lombok.</li>
  <li>Créer une entité JPA "Patient" avec les attributs suivants :</li>
  <ul>
    <li>Un identifiant de type Long.</li>
    <li>Un nom de type String.</li>
    <li>Une date de naissance de type Date.</li>
    <li>Un statut "malade" de type boolean.</li>
    <li>Un score de type int.</li>
  </ul>
  <li>Configurer l'unité de persistance dans le fichier application.properties.</li>
  <li>Élaborer une interface JPA Repository basée sur Spring Data.</li>
  <li>Tester diverses opérations de gestion, notamment :</li>
  <ul>
    <li>Ajouter des patients.</li>
    <li>Consulter la liste complète des patients.</li>
    <li>Rechercher un patient par son identifiant.</li>
    <li>Mettre à jour les informations d'un patient.</li>
    <li>Supprimer un patient.</li>
  </ul>
  <li>Effectuer la migration de la base de données H2 vers MySQL.</li>
</ol>
<h2 style="color: skyblue">Réalisation du TP</h2>
<ol>
  <li>
    <strong>Installation d'IntelliJ IDEA Ultimate</strong>
    <p>La première phase de cette démarche pratique implique l'installation d'IntelliJ IDEA Ultimate, un environnement de développement intégré (IDE) puissant qui servira de plateforme pour le développement de notre application.</p>
  </li>

  <li>
    <strong>Création d'un projet Spring Initializer avec Maven</strong>
    <p>En ajoutant les dépendances suivantes :</p>
    <ul>
      <li>Spring Data JPA</li>
      <li>H2 Database (base de données en mémoire)</li>
      <li>Spring Web (pour les contrôleurs web)</li>
      <li>Lombok (pour la génération automatique de code)</li>
      <li>MySQL Driver</li>
      <li>Thymeleaf</li>
    </ul>
  </li>

  <li>
    <strong>Création de l'entité JPA Patient</strong>
    <p>Voici les caractéristiques de cette entité :</p>
    <ul>
      <li>Un identifiant de type Long</li>
      <li>Un nom de type String</li>
      <li>Une date de naissance de type Date</li>
      <li>Un statut "malade" de type boolean</li>
      <li>Un score de type int</li>
    </ul>
  </li>
</ol>
 <img src="captures/entity.png" alt="entity">

  <li>Configuration de l'unité de persistance dans le fichier application.properties pour utiliser H2 Databease</li>

<p> Ces paramètres de configuration déterminent l'URL de la base de données (H2 en mémoire), activent la console H2 pour une gestion interactive, et spécifient le port (8082) d'accès à l'application. Ces ajustements garantissent une utilisation optimale de la base de données H2 en mémoire pour notre application.</p>

  <img src="captures/app_properties_h2.png" alt="Properties">

  <li>Création de l'interface JPA Repository basée sur Spring Data</li>

<p>
L'interface 'PatientRepository' étend 'JpaRepository' afin de faciliter l'accès aux données de l'entité 'Patient'. Elle propose des méthodes permettant de rechercher des patients en fonction de divers critères tels que le statut de maladie, le score, la date de naissance et le nom. De plus, elle intègre une requête personnalisée pour des recherches spécifiques.</p>

  <img src="captures/repository.png" alt="JPA Repository">

<li>Tests des Opérations de Gestion</li>
<ul>
    <li>Le point d'entrée de l'application Spring Boot</li>
<img src="captures/demarrage.png">
    <li>Ajouter des patients</li>
<img src="captures/ajout.png">
    <li>Consulter tous les patients</li>
<img src="captures/affichage.png">
<li>Chercher des patients selon des critéres</li>
<img src="captures/critere.png">
    <li>Chercher un patient par Id</li>
<img src="captures/recherche_id.png">
    <li>Mettre à jour un patient</li>
<img src="captures/modifier.png">
    <li>Supprimer un patient</li>
<img src="captures/supprimer.png">
<li> les données dans H2 Database</li>
<img src="captures/h2_console_login.png">
<img src="captures/h2_console.png">
</ul>

<li>Migration de H2 Database vers MySQL</li>
<ul>
<img src="captures/app_properties_mysql.png">
<li> les données dans My SQL</li>
<img src="captures/mysql_table.png">
</ul>


<h2 style="color: Skyblue">Conclusion</h2>
<p>
En conclusion, ce travail pratique nous a plongés dans le monde complexe de la gestion de la persistance des données avec des outils essentiels comme l'ORM, le JDBC, le JPA, Hibernate et Spring Data. On a vu comment ces outils rendent la vie plus facile aux développeurs pour créer des applications Java solides.
<br>

Choisir les bons outils pour gérer les données selon les besoins spécifiques d'un projet est crucial. Apprendre et appliquer ces concepts devient une compétence précieuse pour les développeurs qui cherchent à rendre leurs applications efficaces, performantes et fiables.
<br>

En résumé, cette exploration élargit notre compréhension des technologies de gestion de données, ouvrant la porte à des projets plus avancés et à une meilleure expertise en développement d'applications Java. Cela souligne aussi l'importance capitale de ces outils dans le monde du développement logiciel moderne, où bien gérer les données est une clé du succès des projets.
</p>
