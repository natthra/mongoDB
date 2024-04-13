# Busquedas en colecciones de una base de datos

## Busquedas

### __*Selecciona todos los documentos de una cloeccion*__

```
db.libros.find()
db.libros.find({})
```
---
__Seleccionar todos los documentos de la coleccion libros donde el precio sea igual a 25__
```
db.libros.find({precio:25})
```

__Seleccionar todos aquellos documentos donde su precio sea mayor a 25__
```
db.libros.find({Precio: {$gt25}})
```









