# Service Moyenne

Ce projet est un service PHP permettant de calculer les moyennes des notes des étudiants pour différents cours. Il interagit avec des services externes pour récupérer les informations nécessaires.

## Fonctionnalités

Le service prend en charge les cas suivants :

1. **Moyennes pour tous les étudiants et tous les cours**  
   - Retourne les moyennes des notes pour chaque étudiant et chaque cours.
   - **URL** : `https://api-service-moyenne.onrender.com/getMoyenne.php`
   - **Paramètres** : Aucun.

2. **Moyennes pour un cours spécifique**  
   - Retourne les moyennes des notes pour un cours donné.
   - **URL** : `https://api-service-moyenne.onrender.com/getMoyenne.php`
   - **Paramètres** : `code_cours`.

3. **Moyenne d’un étudiant dans un cours**  
   - Retourne la moyenne des notes pour un étudiant spécifique dans un cours donné.
   - **URL** : `https://api-service-moyenne.onrender.com/getMoyenne.php`
   - **Paramètres** : `etudiant_id`, `code_cours`.

4. **Moyennes pour tous les cours d’un étudiant**  
   - Retourne les moyennes des notes pour tous les cours d’un étudiant donné.
   - **URL** : `https://api-service-moyenne.onrender.com/getMoyenne.php``
   - **Paramètres** : `etudiant_id`.

## Structure des Réponses

Les réponses sont au format JSON. Exemple pour une requête réussie :

```json
{
  "success": true,
  "moyennes": [
    {
      "etudiant_id": "123",
      "nom": "John Doe",
      "code_cours": "MATH101",
      "cours": "Mathématiques",
      "moyenne": 15.5
    }
  ]
}
