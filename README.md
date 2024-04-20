# Tarea LLM (Language Model Language)

El siguiente proyecto pretende desarrollar un código capaz de interactuar de diferentes formas con el LLM más famoso del momento. Realizarle preguntas, cargarle información adicional "contexto" 
para que responda según este nuevo conocimiento.

¿Pero antes de proseguir, que es un LLM?  
Se refiere a un Language Model Language, lo que quiere decir que es un sistema capaz de "entender" el lenguaje y responder de forma coherente según los datos que tiene, usualmente son usados
para generar texto de forma automática, corregirlo o responder, agilizar procesos de análisis de este mismo.

### Prerrequisitos

- [Python](https://www.python.org/downloads/): Lenguaje de programación con el que se va a trabajar, se recomienda usar la última versión estable.
- [Pip]: El gestor de dependencias de python, el cual debe ser de la última versión disponible para evitar conflictos.
- [Visual Studio Installer](https://visualstudio.microsoft.com/es/downloads/): Este programa nos permitirá descargar algunas librerías de C++, necesarias para las dependencias del proyecto.


### Empezando

Se clona el repositorio

~~~
git clone https://github.com/JordyBautista10/LLM-Class9
~~~

Con ayuda de la herramienta de Visual Studio tools, asegúrese de tener todos los módulos de la siguiente imagen para no tener problema con la librería Cromadb

![image](https://github.com/JordyBautista10/LLM-Class9/assets/123812969/de1c2211-1568-4847-ab76-a82c582360fb)

Ahora si se pueden descargar las librerías que usa el proyecto, con el siguiente comando:

~~~
pip install -r requirements.tx
~~~

Ya por último, debe contar con una llave API de OpenIA, la cual deberá reemplazar en cada uno de los programas para que  funcionen correctamente


### Como funciona

El proyecto cuenta con tres programas, cada uno con un proposito diferente ya que:
- SimpleQuestion: este programa es sencillo, pues se conecta al API de ChatGPT y le envia una unstruccion que esta dentro de una variable quemada en el codigo, si desea realiar otro tipo de preguntas,
puede canbiar el valor de la variable.
- SimpleRAG:
