# Membres

Par défaut lorsqu'un membre vous est retourné, l'ensemble de ces valeurs seront retournées systématiquement.

| Attribut | Description |
| :--- | :--- |
| _id_ | Identifiant unique du membre. Cet identifiant est utilisé pour toutes les méthodes qui requièrent les données d'un membre en particulier. |
| _properties_ | Cette propriété contient l'ensemble des informations du membre. Par défaut, cette propriété contient toujours la valeur `email`. |
| _groupIds_ | Cette propriété contient l'ensemble des informations du membre. Par défaut, cette propriété contient toujours la valeur `email`. |
| _paymentOptions_ | Méthode(s) de paiement utilisé par le membre. |
| _invoices_ | Facture(s) liées au membre. |
| _creatonTime_ | Date de création du membre sous format `UTC`. |

```javascript
{
  id: "{MEMBER_ID}",
  properties: {
    email: "{MEMBER_EMAIL}"
    // ...
  },
  groupIds: ["{GROUP_ID}"],
  creationTime: "{MEMBER_CREATION_TIME}",
  subscriptions: {
    // ...
  },
  invoices: {
    // ...
  }
}
```

{% method %}
### /api/members - __`GET`__

Récupère les détails d'un membre existant.

| Paramètre | Description |
| :--- | :--- |
| _id_ | Identifiant unique du membre. |

{% sample lang="bash" %}
```bash 
curl https://app.userboat.com/api/members/{ID} \
   -H "Content-Type: application/json"
   -H "Authorization: Bearer {ACCESS_TOKEN}"
```

{% common %}
L'objet retourné est celui du membre, comme décrit ci-haut.

{% endmethod %}

{% method %}
### /api/members - __`POST`__

Crée un membre.

| Paramètre | Description |
| :--- | :--- |
| _properties_ | Série de propriétés dans le but modifier les informations du membre. |
| _groupIds_ | Liste contenant les identifiants des groupes auxquels il faut associer le membre. |

{% sample lang="bash" %}
```bash 
curl https://app.userboat.com/api/members/{ID} \
   -H "Content-Type: application/json"
   -H "Authorization: Bearer {ACCESS_TOKEN}"
   -d '{"properties": { "email":"COURRIEL" } }'
   -d '{"groupIds": [ "ID_GROUP1", "ID_GROUP2" ] }'
```

{% common %}
L'objet retourné est celui du membre, comme décrit ci-haut.

{% endmethod %}

{% method %}
### /api/members - __`PUT`__

Met à jour les détails d'un membre existant.

| Paramètre | Description |
| :--- | :--- |
| _id_ | Identifiant unique du membre. |
| _properties_ | Série de propriétés dans le but modifier les informations du membre. |

{% sample lang="bash" %}
```bash 
curl https://app.userboat.com/api/members/{ID} \
   -H "Content-Type: application/json"
   -H "Authorization: Bearer {ACCESS_TOKEN}"
   -d '{"email":"NOUVEAU_COURRIEL"}'
```

{% common %}
L'objet retourné est celui du membre, comme décrit ci-haut.

{% endmethod %}

{% method %}
### /api/members - __`DELETE`__

Supprime un membre.

| Paramètre | Description |
| :--- | :--- |
| _id_ | Identifiant unique du membre. |

{% sample lang="bash" %}
```bash 
curl https://app.userboat.com/api/members/{ID} \
   -H "Content-Type: application/json"
   -H "Authorization: Bearer {ACCESS_TOKEN}"
```

{% common %}
L'objet retourné sera vide en cas de succès.

{% endmethod %}
