# Crear una api básica

El Gobierno Nacional puso a disposición de la ciudadanía de la República Argentina un dataset
que actualiza diariamente con los casos diarios de SARS-COV-2, popularmente conocido
como coronavirus.
Los datos están disponibles en:
http://datos.salud.gob.ar/dataset/covid-19-casos-registrados-en-la-republica-argentina

El ejercicio consta de construir una API REST con los siguientes endpoints:

## Casos Totales

### GET /covid/total
Debe soportar los siguientes filtros:
1) Rango de Fechas (año/mes/día)
2) Rango de Edad
3) Género
4) Provincia

## Muertes

### GET /covid/deaths
Debe soportar los mismos filtros que el endpoint anterior.

## Carga

### GET /covid/update
Devuelve los siguientes datos:
1) Cuándo se realizó la última
2) Cuántos nuevos registros se agregaron

### POST /covid/update
Dispara el proceso de carga de datos.

El ejercicio debe estar desarrollado en .NET 5 en adelante. Lo más importante es la simplicidad y elegancia
que la complejidad y robustez.
No hace falta crear usuarios ni autenticación.
El dataset tiene millones de registros, pero podés trabajar con los últimos 1000 registros y en
cada update ir acumulándolos. No es necesario que la API esté preparada para manejar
millones de registros.
Sí deben persistir los datos de alguna forma, pero pueden bajarse a disco de la forma que te
resulte más sencilla (ya sea en un JSON, CSV, sqlite, rdbms, etc). Tené presente que el CSV
del dataset tiene mucha más data de la que necesitás.
