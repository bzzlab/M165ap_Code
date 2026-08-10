### Übung 6.03: Fehlermeldung interpretieren

1. Führen Sie folgende Query aus und interpretieren Sie den Output und versuchen Sie eine Erklärung mit
eigenen Worten und ganzen Sätzen zu erarbeiten.

```
use mflix_labs
db.users.drop()

db.users.insertMany([
  {"_id": 2, "name": "Jon Snow", "email": "Jon.Snow@got.es"},
  {"_id": 3, "name": "Joffrey Baratheon", "email": "Joffrey.Baratheon@got.es"},
  {"_id": 5, "name": "Margaery Tyrell", "email": "Margaery.Tyrell@got.es"},
  {"_id": 6, "name": "Khal Drogo", "email": "Khal.Drogo@got.es"}
])

db.users.replaceOne(
  {"_id" : 5},
  {"name": "Margaery Baratheon", "email": "Margaery.Baratheon@got.es"}
)
db.users.find()


db.users.replaceOne(
  {"name" : "Margaery Baratheon"},
  {"_id": 9, "name": "Margaery Baratheon", "email": "Margaery.Baratheon@got.es"}
)
```