# Biblio

Groupe : D.R.H

Application PHP en ligne de commande qui gère une bibliothèque (livres, membres, emprunts). Projet réalisé en équipe dans le cadre du TP Git / GitHub (GINF2).

## Contrat d'interface

- **Livre** (A) : propriétés privées isbn, titre, auteur, disponible. Constructeur (string $isbn, string $titre, string $auteur) qui lève InvalidArgumentException si l'ISBN n'a pas 10 ou 13 chiffres. Méthodes : getIsbn(), getTitre(), getAuteur(), estDisponible(): bool, emprunter() et rendre() (Exception si l'état est déjà celui demandé), __toString(): string.
- **Bibliotheque** (B) : ajouter(Livre $l): void (exception si l'ISBN existe déjà), trouver(string $isbn): ?Livre, tous(): array, compter(): int, rechercher(string $mot): array (titre ou auteur, sans tenir compte de la casse).
- **Membre** (C) : Membre(int $id, string $nom), getId(), getNom(), emprunter(Livre $l) (3 livres maximum), rendre(Livre $l), getEmprunts(): array. Plus index.php : menu interactif.

## Lancer les tests

    php tests/run.php
