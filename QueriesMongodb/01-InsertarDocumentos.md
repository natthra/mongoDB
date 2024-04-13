# Insertar Documentos
### Insertar unicos docuemtos
---
__*Ejemplo: creacion de documento basico*__ 
```
`dbLocal> db.Alumnos.insertOne(
    {
    NOMBRE: "Apolo"
    })`
```

__*Ejemplo: Creacion de documento un poco mas complejo*__
```
db.Alumnios.insertOne( 
    { 
        Nombre: "Rosa", 
        Edad: 22, 
        Apellidos: "Cabeza de vaca", 
        Aficiones: ["Paracaidismo", "Lectura", "Futbol"]
    })
```

__*Ejemplo: Insersion de documentos con subdocumentos*__
```
db.Alumnos.insertOne(
    {
    Nombre: "Raul",
    Edad: 67,
    cv: {
            "Informatica" : "Bueno",
            "Marketing" : "Bajo",
            "Contabilidad" : "Medio"
        }
    })
```

__*Insertar documento con ID personalizado*__
```
db.Alumnos.insertOne({_id: 1, "Nombre" : "Arcadia" })
```

### __*Insertar Varios Documentos*__
---
```
 db.Alumnos.insertMany(
... [
... {
... _id:2,
... Nombre: "Diana"
... },
... {
... _id:3,
... Nombre: "Flor",
... Edad: 43
... },
... {
...     _id:4,
...     Nombre: "Francisco Jesus Uriel",
...     Edad: 34,
...     Aficiones: "El agua bendita",
...     Desgracia: "La ex"
... }
... ]);
```

| Operador | Descripcion |
| -- | -- |
| $eq | Igual |
| $gt | Mayor que |
| $gte | Mayor o Igual |
| in | Buscar un elemento en un array |
| $lt | Menor que |
| $lte | Menor o igual |
| $ne | Todos los elementos que no sean iguales |
| $nin | Ninguno de los valores del arreglo |s





