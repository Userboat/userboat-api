# Factures & paiements

Par défaut lorsqu'une facture vous est retournée, l'ensemble de ces valeurs seront retournées systématiquement.

| Attribut | Description |
| :--- | :--- |
| _id_ | Identifiant unique de la facture. Cet identifiant est utilisé pour toutes les méthodes qui requièrent les données d'une facture. |
| _status_ | C'est le status courant de la facture. `10` représente `Non-payée`, `20` représente `Payée`. |
| _charges_ | Cette propriété l'ensemble des paiements effectués pour la facture. |
| _paidTime_ | Date du paiement complèt de la facture sous format `UTC`. |
| _creationTime_ | Date de création de la facture sous format `UTC`. |

```javascript
{
  id: "57793ecd-61ea-45d5-b50a-8c49d5123f74",
  status: 10,
  charges: [
    // ...
  ],
  paidTime: "2017-05-23T17:54:24.837642Z",
  creationTime: "2017-05-23T17:54:24.837642Z"
}
```

{% method %}
### /api/v1/invoices - __`GET`__

Récupère les détails d'une facture existante.

| Paramètre | Description |
| :--- | :--- |
| _id_ | Identifiant unique de la facture. |

{% sample lang="bash" %}
```bash 
curl https://app.userboat.com/api/invoices/{ID} \
   -H "Content-Type: application/json"
   -H "Authorization: Bearer {ACCESS_TOKEN}"
```

{% common %}
L'objet retourné est celui de la facture, comme décrit ci-haut.

{% endmethod %}

{% method %}
### /api/v1/invoices - __`DELETE`__

Supprime une facture.

| Paramètre | Description |
| :--- | :--- |
| _id_ | Identifiant unique de la facture. |

{% sample lang="bash" %}
```bash 
curl https://app.userboat.com/api/invoices/{ID} \
   -H "Content-Type: application/json"
   -H "Authorization: Bearer {ACCESS_TOKEN}"
```

{% common %}
L'objet retourné sera vide en cas de succès.

{% endmethod %}
