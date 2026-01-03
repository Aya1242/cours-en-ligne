# Modèle de données

## Table `users`
| Champ       | Type        | Description            |
|-------------|-------------|------------------------|
| id          | UUID        | Identifiant unique     |
| email       | STRING      | Email (unique)         |
| password    | STRING      | Hash du mot de passe   |
| name        | STRING      | Nom complet            |
| role        | ENUM        | 'student' ou 'teacher' |
| created_at  | DATETIME    | Date de création       |

## Table `courses`
| Champ        | Type        | Description               |
|--------------|-------------|---------------------------|
| id           | UUID        | Identifiant unique        |
| title        | STRING      | Nom du cours              |
| code         | STRING      | Ex: BDD-L3GIP             |
| semester     | STRING      | Ex: S5                    |
| teacher_id   | UUID        | Référence à users.id      |
| created_at   | DATETIME    |                           |

## Table `documents`
| Champ        | Type        | Description                     |
|--------------|-------------|---------------------------------|
| id           | UUID        | Identifiant unique              |
| course_id    | UUID        | Référence à courses.id          |
| filename     | STRING      | Nom original (ex: cours.pdf)    |
| filepath     | STRING      | Chemin (ex: /uploads/cours.pdf) |
| uploaded_at  | DATETIME    |                                 |
