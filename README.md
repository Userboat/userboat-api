# Userboat - API

L'API est organisée autour du concept `REST` et utilise des codes de réponse HTTP pour indiquer différentes erreurs. L'authentification se fait par [JSON Web token](https://jwt.io/). Le respect des verbes HTTP est très important, par exemple si vous tentez d'obtenir une ressource avec le verbe `POST`, le code erreur 404 (ressource non trouvée) vous sera retourné. Il est obligatoire de transiger avec nos services par HTTPS. Veuillez ne jamais exposer le `accessToken` qui vous sera retourné suite à votre authentification.
