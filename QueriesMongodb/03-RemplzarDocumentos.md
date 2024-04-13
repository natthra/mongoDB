# Reemplazar Documentos

### Sustituir un documento completo
```m
db.libros.replaceOne({_id:2}, {titulo: 'De la tierra a la luna', autor: 'Julio Verne', editorial:Terra, precio:100})
```


### Borrar documentos
__Dos metodos__

1. deleteOne
1. deleteMany

### Eliminar todo el documento con un id 2
```m
db.libros.deleteOne({_id:2})
```

### Eliminar todos los documentos donde la cantidad sea mayor a 150
```m
db.libros.deleteMany({cantidad: {gt$:150}})
```
# Expresiones regulares
### Seleccionar todos los documentos que contengan en el titulo una T
```m
db.libros.find({titulo: /t/})
```

### Seleccionar todos los documentos que contengan en el titulo la palabra json
```m
db.libros.find({titulo: /JSON/})
```
### Seleccionar todos los documentos que contengan en el titulo la palabra tos
```m
db.libros.find({titulo: /tos$/})
```

# Operador $regex

### Seleccionar todos los documentos que contengan la palabra para
```m
db.libros.find({titulo:{$regex:'para'}})
```

```m
db.libros.find({titulo:{$regex:/para/}})
```

### Seleccionar todos los documentos donde contenga el titulo JSON pero que sea case sensitive
```m
db.libros.find({editorial: {$regex:/Planeta/, options: i}}, {_id:0, titulo:1, editorial::1})
```

### Operador $exist
_Permite buscar la existencia de la columna_
```m
db.Libros.find({titulo:{$exists:true}})
```

# Expleciones regulares

## Tabla tipos de datos de mongoDB
| Type | Numbre | Alias |
|-|-|-|
|  |  | |

## Opreador $set
Sirve para cambiar el valor de un campo de la coleccion
```m
 db.Libros.updateOne({titulo: 'Java como programar'}, {$set:{titulo:'Java como programar desde 0'}})
```

### Actualizar el valor de la cantidad a y el precio a 10 donde el id = 9
```m
db.Libros.updateOne({_id:9}, {$set:{cantidad:50, precio:10}})
```

### Actualizar todos los doumentos donde el precio sea mayor a  10 por el precio a 150
```m
db.Libros.updateMany({precio:{$gt:10}}, {$set:{precio: 150}})
```

## Operador sort
Ordena los documentos de la coleccion

### Ordenar todos los documentos de forma ascendente por la editorial y mostrar solamente el titulo, precio y editorial
__Acendente__
```m
db.Libros.find({},{titulo:1, precio:1, editorial:1, _id:0}).sort({editorial:1})
```
__Descendente__
```m
db.Libros.find({},{titulo:1, precio:1, editorial:1, _id:0}).sort({editorial:1})
```
