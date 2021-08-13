# Crear una api básica

El Gobierno Nacional puso a disposición de la ciudadanía de la República Argentina un dataset
que actualiza diariamente con los casos diarios de SARS-COV-2, popularmente conocido
como coronavirus.
Los datos están disponibles en:
http://datos.salud.gob.ar/dataset/covid-19-casos-registrados-en-la-republica-argentina
De aquí tomar los datos para el ejercicio, el cual consta de construir una aplicación con las siguientes directivas:

# API (Backend)

## Casos Totales

### GET /covid/total
Debe soportar los siguientes filtros:
1) Rango de Fechas
2) Rango de Edad
3) Género
4) Provincia

## Carga

### POST /covid/update
Dispara el proceso de carga de un nuevo caso.
Se deben poder ingresar los mismos datos que en el GET:
1) Fecha
2) Edad
3) Género
4) Provincia

# UI (Frontend)

Crear una interfaz gráfica para mostrar los resultados de los endpoints. 
Se debe poder ingresar los filtros que soporta la API de la manera que te resulte más conveniente.

Podés utilizar el framework C# que quieras.

- El ejercicio debe estar desarrollado en .NET 5 en adelante, tanto API como UI (Blazor preferentemente). 
- Lo más importante es la simplicidad y elegancia que la complejidad y robustez.
- No hace falta crear usuarios ni autenticación.
- El dataset tiene millones de registros, pero podés trabajar con los últimos 1000 registros. 
- No es necesario que la API esté preparada para manejar millones de registros.
- Deben persistir los datos de alguna forma; pueden bajarse a disco de la forma que te
resulte más sencilla (ya sea en un JSON, CSV, sqlite, rdbms, etc). 
- Tené presente que el CSV del dataset tiene mucha más data de la que necesitás.
