# Authentification

__Il est obligatoire de s'authentifier afin de pouvoir communiquer avec l'API__

L'authentification à l'API est effectuée via JSON Web Token. Authentifiez votre compte lors de l'utilisation de l'API en incluant votre `accessToken` dans les `headers`de votre requête. Ne partagez jamais ce token avec quiconque.

Toutes les demandes d'API doivent être effectuées sur HTTPS. Les appels effectués sur HTTP simple échoueront. Les demandes API sans authentification échoueront également.

{% method %}
### /api/auth/jwt 
__`POST`__

{% sample lang="js" %}
Here is how to print a message to `stdout` using JavaScript.

```js
console.log('My first method');
```

{% sample lang="go" %}
Here is how to print a message to `stdout` using Go.

```go
fmt.Println("My first method")
```

{% common %}
Whatever language you are using, the result will be the same.



{% endmethod %}
