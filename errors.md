# Erreurs

Les erreurs de validations seront retournées sous le format suivant:

```javascript
{
  error: {
    code: 1,
    message: "validation_error",
    details: "Validation error(s)",
    validationErrors: [
      {
        message: "required",
        members: [
          "Amount"
        ]
      },
      {
        message: "required",
        members: [
          "ChargeType"
        ]
      }
    ]
  }
}
```
