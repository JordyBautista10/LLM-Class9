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
- PineCone: Tener una cuenta, pues se hará uno de una base de datos vectorial.


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

El proyecto cuenta con tres programas, cada uno con un propósito diferente, ya que:
- SimpleQuestion: Este programa es sencillo, pues se conecta al API de ChatGPT y le envía una instrucción que está dentro de una variable quemada en el código, si desea realizar otro tipo de preguntas,
puede cambiar el valor de la variable. El uso de este programa es prácticamente el mismo que si el usuario le estuviera preguntando a la IA a través de navegador. Para este proyecto se le preguntó
'¿Cuál es el núcleo de la teoría de la ciencia de Popper?' y esta fue la respuesta:

![image](https://github.com/JordyBautista10/LLM-Class9/assets/123812969/1c44e76c-2a94-4780-9e6b-2289499c4e57)

- SimpleRAG: Por otro lado, el funcionamiento de este programa introduce un aspecto interesante, pues, se le esta cargando un contexto, una iformacion previa, con la cual el modelo puede proporcionar mejores respuestas ya que conoce de que tema de esta hablando, con esto respondera acerca de la informacioni proporcionada, en este proyecto se le cargo como contexto el contenido de la pagina: https://lilianweng.github.io/posts/2023-06-23-agent/

![image](https://github.com/JordyBautista10/LLM-Class9/assets/123812969/360a12f2-79cf-4a82-86d5-f3dd2f82282a)

Con la información anterior, se le realiza la siguiente pregunta '¿Qué es la descomposición de tareas?', si el modelo no tuviera el contexto apropiado, la respuesta sería tremendamente ambigua, sin embargo,
gracias a que ahora el modelo tiene el contexto, la respuesta siguiente es conforme al texto.

![image](https://github.com/JordyBautista10/LLM-Class9/assets/123812969/49b862f1-935c-4cbf-b256-7317826f83fb)

- PineConeRAG: La diferencia con respecto al anterior, es que ahora, podemos proporcionarle información directamente nosotros, con ayuda la de base de datos vectorial PineCone, esto se hace
por medio de distintas funciones, que dividen el texto de un archivo de texto que tengamos en el disco del equipo y subirá estas partes a la base de datos, donde esta información será cargada al modelo
con el fin de responder a la información que le suministramos nosotros. Este último programa es el que ofrece mayor flexibilidad, pues la información puede ser cualquier texto que queramos. Como
ejemplo en este proyecto, se carga la información del txt llamado 'Conocimiento' el cual contiene el libro de Frankenstein, por lo que se le pueden hacer preguntas al respecto.

![image](https://github.com/JordyBautista10/LLM-Class9/assets/123812969/a24d0627-a514-4c10-baf3-00ab0c8b1315)

