# Authentification

__Il est obligatoire de s'authentifier afin de pouvoir communiquer avec l'API__

L'authentification à l'API est effectuée via JSON Web Token. Authentifiez votre compte lors de l'utilisation de l'API en incluant votre `accessToken` dans les `headers`de votre requête. Ne partagez jamais ce token avec quiconque.

Toutes les demandes d'API doivent être effectuées sur HTTPS. Les appels effectués sur HTTP simple échoueront. Les demandes API sans authentification échoueront également.

{% method %}
### /api/auth/jwt - `POST`

Il faut passer les paramètres `usernameOrEmailAddress` et `password` à cette méthode afin de recevoir votre token. Il faudra stocker ce token de votre côté, car celui-ci est requis pour chaque appel subséquent.

{% sample lang="bash" %}
```bash 
curl http://app.userboat.com/api/auth/jwt \
   -H "Content-Type: application/json"
   -d '{"usernameOrEmailAddress":"VOTRE_EMAIL","password":"VOTRE_PASSWORD"}'
```

{% common %}
```javascript
{
  "accessToken": "VOTRE_CLEF",
  "encryptedAccessToken": null,
  "expireInSeconds": 86400,
  "userId": 0
}
```
{% endmethod %}
