# Membres

Par défaut lorsqu'un membre vous est retourné, l'ensemble de ces valeurs seront retournées systématiquement.

| Attribut | Description |
| :--- | :--- |
| _id_ | Identifiant unique du membre. Cet identifiant est utilisé pour toutes les méthodes qui requièrent les données d'un membre en particulier. |
| _properties_ | Cette propriété contient l'ensemble des informations du membre. Par défaut, cette propriété contient toujours la valeur `email`. |
| _creatonTime_ | Date de création du membre sous format `UTC`. |

```javascript
{
  "id": "{MEMBER_ID}",
  "properties": {
    "email": "{MEMBER_EMAIL}"
    // ...
  },
  "creationTime": "{MEMBER_CREATION_TIME}"
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
