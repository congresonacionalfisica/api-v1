---
title: CNF API

language_tabs: # must be one of https://git.io/vQNgJ
  - shell

toc_footers:
  - <a href='http://cnf.smf.mx/' target="_blank">Congreso Nacional de Física</a>
  - <a href='https://www.smf.mx' target="_blank">Sociedad Mexicana de Física</a>

includes:
  - errors

search: false
---

# Introducción

Bienvenido a la API del Congreso Nacional de Física. Tú podrás usar nuestra API para acceder a los CNF API endpoints, donde podrás obtener información sobre los trabajos aprobados para su presentación en nuestro siguiente evento. Únicamente se encuentra habilitado el método `GET`.

Puedes ver ejemplos de las peticiones en el área negra de la derecha.

Plataforma creada y administrada por la Sociedad Mexicana de Física. Hecho en México.

# Autentificación

```shell
# La CNF API es abierta, por lo tanto no necesita ninguna autorización
curl "http://cnf.smf.mx/api/v1/"
```

CNF API se encuentra en modo de desarrollo por lo tanto actualmente no requiere ningun tipo de token para poder consultar la información.

# Archivos CNF

## Obtener todos los archivos

```shell
curl "http://cnf.smf.mx/api/v1/archivos/"
```


> Devuelve una lista de objetos JSON:

```json
[
  {
    "url": "http://cnf.smf.mx/archivos/40/",
    "titulo": "DESARROLLO DE UN SISTEMA DE CULTIVO AGRICOLA AUTOMATIZADO MEDIANTE MONITOREO DE VARIBLES HMI A TRAVES DE LA IRRIGACION",
    "abstract": "Diseño, desarrollo e implementación de un sistema de control automático, en conjunto de su respectiva HMI para satisfacer las necesidades de cultivo inteligente para la producción en masa a través de control y monitoreo de variables.",
    "area": "Ciencias de la Tierra",
    "autor": [
          {
            "first_name": "Jose Yahir ",
            "last_name": "Manuel Ruiz",
            "estudios": "Maestría",
            "institucion": null
          },
          {
            "first_name": "Maria Graciela ",
            "last_name": "Hernndez y Orduña",
            "estudios": "Doctorado",
            "institucion": null
          }
      ],
    "presentacion_asignada": "Poster"
  },
  {
    "url": "http://cnf.smf.mx/archivos/68/",
    "titulo": "La importancia del Códice “Cruz-Badiano”, las plantas medicinales nativas de México, y su estudio de contenidos radiológicos.",
    "abstract": "En este trabajo se presenta el Códice Cruz-Badiano (1552) y su importancia a nivel internacional en el desarrollo del uso de las plantas medicinales nativas de México para la cura de diversas enfermedades y la producción de productos farmacéuticos, así como de esencias y saborizantes como es el caso de la Vainilla (Vanilla planifolia Andrews) (planta de origen mexicano). También se presentan algunas de las ilustraciones pintadas por los Tlacuilos (artistas nativos Mexicas), además de algunos espectros gamma, de los estudios realizados de los contenidos radiológicos en las plantas medicinales del Códice, y empleadas comúnmente hasta la fecha.",
    "area": "Física de Radiaciones",
    "autor": [
          {
            "first_name": "Guillermo Cirano",
            "last_name": "Espinosa García",
            "estudios": "Doctorado",
            "institucion": "Universidad Nacional Autónoma de México"
          },
          {
            "first_name": "José Ignacio",
            "last_name": "Golzarri y Moreno",
            "estudios": "Licenciatura",
            "institucion": "Universidad Nacional Autónoma de México"
          },
          {
            "first_name": "Allan Canek",
            "last_name": "Chavarría Sánchez",
            "estudios": "Doctorado",
            "institucion": "Universidad Nacional Autónoma de México"
          }
      ],
    "presentacion_asignada": "Poster"
  },
  {
    "url": "http://cnf.smf.mx/archivos/620/",
    "titulo": "ESTUDIO COMPARATIVO ESTACIONAL EN UN MONITOREO ANUAL DE LAS VARIACIONES DE LA TEMPERATURA Y  LA  HUMEDAD EN UNA ZONA AL SUR DE MORELIA MICHOACÁN. ",
    "abstract": "En un trabajo previo [1] se presento un estudio de las variaciones de la temperatura y la humedad en un área del sur de Morelia Michoacán. Donde se reportaron solamente dos periodos de tiempo correspondientes a las estaciones de primavera y verano. En este trabajo se presentan los estudios correspondientes para los periodos estacionales de otoño y invierno para poder disponer de un monitoreo anual de las variaciones de la temperatura y humedad. Se presenta un análisis temporal, de espectros de Fourier, de mapas de retorno y de correlaciones, para cada periodo estacional. En base a estos análisis se propone un modelo semi-empírico para predecir las variaciones en el periodo anual analizado.  \r\n1 C. H. Mendoza Pérez et al., LX Congreso Nacional de Física (2017).Trabajo M1A003.",
    "area": "Ciencias de la Tierra",
    "autor": [
          {
            "first_name": "Misael ",
            "last_name": "Vieyra Ríos",
            "estudios": "Maestría",
            "institucion": "Universidad Michoacana de San Nicolás de Hidalgo"
          },
          {
            "first_name": "José ",
            "last_name": "Vega Cabrera",
            "estudios": "Maestría",
            "institucion": "Universidad Michoacana de San Nicolás de Hidalgo"
          },
          {
            "first_name": "Gabriel ",
            "last_name": "Arroyo Correa",
            "estudios": "Maestría",
            "institucion": "Universidad Michoacana de San Nicolás de Hidalgo"
          },
          {
            "first_name": "Carlos Heriberto ",
            "last_name": "Mendoza Pérez",
            "estudios": "Licenciatura",
            "institucion": "Universidad Michoacana de San Nicolás de Hidalgo"
          }
      ],
    "presentacion_asignada": "Poster"
  }
]
```

Este endpoint devuelve todos los archivos.

### HTTP Request

`GET http://cnf.smf.mx/api/v1/archivos`

### Parámetros opcionales

Parámetro | Opción | Descripción
--------- | ------- | -----------
area | 1 | Astrofísica
 | 2 | Ciencias de la Tierra
  | 3 | Dinámica de Fluidos 
   | 4 | Enseñanza 
    | 5 | Estado Sólido 
     | 6 | Física Atómica y Molecular 
      | 7 | Física de Plasmas
       | 8 | Física de Radiaciones
        | 9 | Física Estadística y Termodinámica 
         | 10 | Física Médica 
          | 11 | Física Nuclear 
           | 12 | Gravitación y Física Matemática 
             | 13 | Historia y Filosofía de la Física 
              | 14 | Información Cuántica 
               | 15 | Instrumentación 
                | 16 | Nanociencias y Nanotecnología 
                 | 17 | Óptica 
                  | 18 | Partículas y Campos 
                   | 19 | Rayos Cósmicos
                   | 19 | Otro
    presentacion | poster | El archivo se presenta en mural
    | platica | El archivo se presenta en oral
    titulo | <code>String</code> | Título del archivo
    autor | <code>String</code> | Nombre de alguno de los autores del archivo

<aside class="notice">
Nota — Algunos autores tiene el valor <code>null</code> en el campo <code>institución</code>
</aside>

<aside class="success">
Recuerda — En caso de no encontrar un archivo que cumpla con los parámetros establecidos regresará una lista vacía.
</aside>

## Obtener un archivo específico

```shell
curl "http://cnf.smf.mx/api/v1/archivos/866/"
```

> El comando anterior regresa el siguiente JSON:

```json
{
  "url": "http://cnf.smf.mx/archivos/866/",
  "titulo": "Dinámica poblacional de la interacción del árbol de la especie \\textit{Vachellia cornigera}  y hormigas de la especie \\textit{Pseudomyrmex ferrugineus} mediante un modelo de Lotka-Volterra",
  "abstract": "El mutualismo es la interacción biológica interespecífica mutuamente benéfica. Lo estudiamos en los árboles de la especie \\textit{Vachellia cornigera} que acogen y alimentan a colonias de hormigas de la especie \\textit{Pseudomyrmex ferrugineus}, las que defienden a los árboles de la depredación de otros organismos. En este trabajo modelamos el mutualismo mediante las ecuaciones diferenciales presa-depredador de Lotka-Volterra. Las poblaciones son consideradas biomasa que se conserva dentro de los alrededores del árbol. Se proponen parámetros de interacción dependientes de factores abióticos que se plantean como funciones de la tasa metabólica de los organismos. Agradecemos a los proyectos LANCAD-UNAM-DGTIC-276 y UNAM-DGAPA-PAPIIT IN116617.",
  "area": "Ciencias de la Tierra",
  "autor": [
      {
        "first_name": "Saúl Iván ",
        "last_name": "Hernández Hernández",
        "estudios": "Doctorado",
        "institucion": "UMDI-Juriquilla, Fac. de Ciencias UNAM"
      },
      {
        "first_name": "Aldo",
        "last_name": "Ledesma Durán",
        "estudios": "Doctorado",
        "institucion": "CFATA, UNAM campus Juriquilla"
      },
      {
        "first_name": "Iván",
        "last_name": "Santamaría Holek",
        "estudios": "Doctorado",
        "institucion": "UMDI-Juriquilla, Fac. de Ciencias UNAM"
      },
      {
        "first_name": "Benjamín ",
        "last_name": "Tenopala Carmona",
        "estudios": "Licenciatura",
        "institucion": "UMDI-Juriquilla, Fac. de Ciencias UNAM"
      },
      {
        "first_name": "Cassandra",
        "last_name": "Cruz Martínez",
        "estudios": "Licenciatura",
        "institucion": "Universidad Autónoma de Querétaro"
      }
  ],
  "presentacion_asignada": "Poster"
}
```

Este endpoint devuelve un archivo específico.

<aside class="warning">En caso de que el ID del archivo no exista se devolverá un <code>Error 404</code>.</aside>

### HTTP Request

`GET http://cnf.smf.mx/api/v1/archivos/<ID>`

### Parámetros de la URL

Parámetro | Descripción
--------- | -----------
ID | El ID del archivo a devolver
