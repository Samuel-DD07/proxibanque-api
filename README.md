# Proxibanque - API REST de Gestion Bancaire

API REST developpee avec Spring Boot permettant de modeliser et gerer les agences, conseillers, clients et comptes d'un reseau bancaire. Ce projet a ete developpe dans un cadre academique (EPITA).

## Fonctionnalites principales

- **Gestion des Agences** : Creation, modification et suppression des agences bancaires du reseau.
- **Gestion des Conseillers** : Affectation des conseillers clientele a des agences specifiques et gestion de leur portefeuille clients.
- **Gestion des Clients** : Suivi des informations personnelles et profils des clients.
- **Gestion des Comptes et Cartes** : Gestion des comptes courants et comptes d'epargne associes aux clients, avec affectation de cartes bancaires (Visa, Mastercard, etc.).

## Architecture et Technologies

- **Langage** : Java 21
- **Framework** : Spring Boot 3.5.7
- **Persistance** : Spring Data JPA / Hibernate
- **Base de donnees** : H2 Database (base de donnees en memoire ideale pour le developpement et les tests)
- **Gestionnaire de dependances** : Gradle (Wrapper fourni)
- **Librairie** : Lombok (reduction du boilerplate code pour les entites)

## Structure du projet

```text
src/main/java/fr/epita/assistants/proxibanque/
├── ProxibanqueApplication.java     # Point d'entree principal de l'application Spring Boot
├── controller/                    # Controleurs REST exposant les endpoints de l'API
├── entity/                        # Modeles JPA (Agence, Conseiller, Client, Compte, CarteBancaire, etc.)
├── repository/                    # Interfaces Spring Data Repository pour l'acces aux donnees
└── service/                       # Services implémentant la logique metier de l'application
```

## Lancement local

### Prerequis
- JDK 21 installe.

### Compilation et execution
Pour lancer l'application en mode developpement, utilisez la commande suivante a la racine du projet :

```bash
./gradlew bootRun
```

L'application demarrera par defaut a l'adresse : http://localhost:8080

### Acces a la console H2
La console d'administration de la base de donnees en memoire est accessible a l'adresse :
http://localhost:8080/h2-console
- **JDBC URL** : jdbc:h2:mem:proxibanque
- **Username** : sa
- **Password** : (vide)
