# Proyecto MATRICULATOR

Propuesta técnica RA1 sobre lenguajes de programación para una aplicación de reconocimiento de matrículas en aparcamientos.

## Enlaces y entregables

- [Web del proyecto en Netlify](https://proyecto-matriculator.netlify.app/)
- [Versión en ChatGPT Sites](https://matriculator-ra1-ian.rainer-agoge.chatgpt.site)
- [Informe completo](Proyecto%20MATRICULATOR.pdf)
- [Notebook de pseudocódigo](pseudocodigo.ipynb)
- [Demostración de formatos](demo_lenguajes.ipynb)
- [Código de la web](index.html)
- [CSV de Google Trends](data/)

La versión de Netlify se publicó mediante una subida manual de los archivos de la web; los cambios futuros en GitHub requieren volver a desplegarla.

La web es estática: se puede abrir `index.html` en un navegador. Debe mantenerse la carpeta `data/` junto a ese archivo para descargar los CSV. La demostración de formatos utiliza bibliotecas incluidas en Python y datos sintéticos. El notebook de pseudocódigo describe el proceso; no es Python ejecutable.

## Aplicación propuesta

Cuando llega un vehículo, la cámara comprobaría la iluminación y encendería una luz auxiliar si hiciera falta. Después se capturaría y prepararía la imagen. Un primer modelo localizaría y reconocería la matrícula, con OCR para leer los caracteres; un segundo modelo propondría el tipo de placa y su país de procedencia.

La aplicación mostraría la lectura, fecha, tipo, país propuesto y estado. Una persona revisaría las lecturas dudosas y las decisiones que afectasen al conductor. Un formato plausible no demuestra que una matrícula sea auténtica o que el vehículo esté autorizado a entrar.

La tarea solicita una propuesta hipotética, sin exigir entrenar un modelo. El equipo también trabajó en una aplicación funcional como ampliación; su código no está incorporado en este repositorio.

## Organización y reparto de tareas

| Integrante | Función principal | Tareas realizadas |
|---|---|---|
| Carmelo José Beato Garcia | Organización y gestión | Organizar las tareas y el avance del trabajo, revisar los conceptos y requisitos, coordinar los entregables y elaborar la parte general del informe. |
| Oihan Cabada | Programación y desarrollo web | Crear la página web, programar la aplicación y redactar las partes del informe relacionadas con el desarrollo y la programación. |

Dividimos el trabajo en dos áreas principales: organización y documentación, y desarrollo técnico. Carmelo se centró en organizar lo que íbamos haciendo y preparar los contenidos y entregables. Oihan se centró en crear la página web y programar la aplicación, además de elaborar la documentación correspondiente a su parte.

## Temporalización del trabajo

Disponíamos de 8 horas para realizar el proyecto, pero finalmente dedicamos unas 12 horas. La siguiente tabla recoge una estimación del tiempo empleado en cada parte:

| Tarea | Tiempo previsto | Tiempo real |
|---|---:|---:|
| Leer el enunciado, organizar el trabajo y definir Matriculator | 0,5 h | 1 h |
| Comparar lenguajes y elaborar la matriz de decisión | 1 h | 1,5 h |
| Recopilar datos de Google Trends y analizar los resultados | 1 h | 1 h |
| Elaborar los diagramas, explicar el funcionamiento y preparar el notebook de pseudocódigo | 1 h | 1,5 h |
| Explicar los formatos de datos y preparar el notebook de demostración | 1 h | 1 h |
| Crear la página web e incorporar el contenido y los gráficos | 1,5 h | 2 h |
| Desarrollar y probar la aplicación funcional | 1,5 h | 2,5 h |
| Revisar el informe y corregir diferencias entre los materiales | 0,5 h | 1,5 h |
| **Total** | **8 h** | **12 h** |

### Desviaciones y revisión de la planificación

El principal problema fue que al principio no entendimos bien algunas partes del enunciado. Esto hizo que dedicáramos tiempo a desarrollar una aplicación funcional, aunque la actividad pedía principalmente una propuesta técnica. También tuvimos que rehacer algunas explicaciones y diagramas para ajustarlos a lo solicitado y mantener la coherencia entre el informe y la página web.

Al detectar estas dificultades, tuvimos que ampliar la planificación inicial de 8 a 12 horas, destinando más tiempo al desarrollo, las correcciones y la revisión final.

### Reflexión del equipo

Hemos aprendido que antes de empezar a programar debemos revisar los requisitos y distinguir qué entregables son obligatorios y cuáles son mejoras adicionales. Para futuros trabajos, prepararíamos una lista de comprobación desde el principio y reservaríamos más tiempo para revisar el conjunto. Esto nos ayudaría a evitar repetir tareas y a cumplir mejor el plazo previsto.

## Preguntas adicionales

### ¿Es una IA débil o fuerte?

Matriculator sería una IA débil, porque estaría diseñada para realizar una tarea concreta: localizar y leer matrículas en imágenes. No tendría inteligencia general ni podría realizar cualquier tipo de tarea.

### ¿Usamos un modelo preentrenado o lo entrenamos desde cero?

Utilizaríamos dos modelos preentrenados y los adaptaríamos con imágenes etiquetadas: uno para localizar y reconocer la matrícula y otro para identificar su tipo y procedencia. Elegimos esta opción porque entrenarlos desde cero requeriría más imágenes, tiempo y recursos.

Una vez puesto el sistema en marcha, una persona revisaría las lecturas dudosas y corregiría los errores. Esos ejemplos revisados servirían para actualizar los datos de entrenamiento y realizar reentrenamientos periódicos. Antes de incorporar una nueva versión, comprobaríamos su funcionamiento con imágenes de prueba que no se hubieran utilizado para entrenarla.

## Evidencias de uso de IA generativa

Utilizamos ChatGPT como apoyo para resolver dudas, organizar contenidos, revisar el informe y trabajar sobre la web. Los prompts siguientes documentan las peticiones; no demuestran por sí solos que una función estuviera implementada o verificada.

### Prompts y peticiones de Carmelo

Se incluyen fragmentos de las conversaciones del proyecto.

| Parte del trabajo | Prompt o fragmento utilizado | Finalidad |
|---|---|---|
| Comparación de lenguajes | «actualiza la matriz de eleccion con los siguientes criterios» | Aportar nuestras valoraciones y adaptar la matriz. |
| Página web | «actualiza el site con dicha informacion» | Incorporar los contenidos revisados. |
| Control de iluminación | «añadir un paso en los cuales si la camara detecta que la luminosidad es insuficiente, enciende una luz» | Añadir la condición de poca luz. |
| Flujo de funcionamiento | «Flujo general: Describe el funcionamiento esperado de la aplicación mediante entre 6 y 10 etapas» | Adaptar el enunciado al flujo de Matriculator. |
| Revisión del informe | «vamos con la parte del informe, dime en que pagina esta y que cosas pongo» | Localizar y corregir apartados. |
| Actualización de datos | «actualiza el csv de youtube con este que abarca mas tiempo» | Ampliar el periodo de datos. |
| Comprobación de requisitos | «que me falta» | Comparar el trabajo con el enunciado. |
| Notebook de formatos | «el otro inventatelo en base a lo que hemos hecho en el informe» | Crear ejemplos sintéticos para demo_lenguajes.ipynb. |

### Prompts de Oihan

Prompts aportados por el equipo el 6 de octubre de 2026. Debajo de cada uno explicamos cómo sus respuestas sirvieron de base para el trabajo final y qué revisiones o ampliaciones realizamos. Esta explicación relaciona las peticiones con los entregables; no reproduce literalmente las respuestas originales.

#### Prompt 1. Idea general del proyecto

> Estoy trabajando en un proyecto llamado Matriculator para una empresa de aparcamientos. La idea consiste en analizar imágenes captadas por cámaras mediante inteligencia artificial para detectar matrículas de vehículos y determinar si son matrículas reales o no.

**Resultado y aplicación en el trabajo final.** La respuesta a este prompt sirvió de base para definir el problema y el objetivo de Matriculator. A partir de ella desarrollamos el apartado de la aplicación elegida del informe y la sección «Qué problema resuelve» de la web: entrada de imágenes, detección de la matrícula, lectura y presentación del resultado. Durante la elaboración concretamos el uso en entradas y salidas de aparcamientos y añadimos la iluminación auxiliar y la revisión humana. También delimitamos la propuesta: comprobar el formato de una matrícula no demuestra por sí solo que sea auténtica.

#### Prompt 2. Comparación de lenguajes de programación

> Analiza qué lenguajes de programación serían más adecuados para desarrollar Matriculator, un sistema de detección de matrículas mediante imágenes y visión artificial. Compara Python, JavaScript con Node.js, R, C++, PHP y Java, teniendo en cuenta la facilidad de aprendizaje, legibilidad y mantenimiento, integración con webs, API y bases de datos, análisis estadístico, bibliotecas de inteligencia artificial, modelos preentrenados, rendimiento, despliegue, documentación, comunidad y compatibilidad.

**Resultado y aplicación en el trabajo final.** La respuesta nos proporcionó una base para comparar Python, JavaScript/Node.js, R, C++, PHP y Java según las necesidades de Matriculator. Esa comparación se refleja en las ventajas e inconvenientes del informe y en la tabla de lenguajes de la web. Nos ayudó a distinguir las herramientas adecuadas para la interfaz y los servicios web de las destinadas al reconocimiento de imágenes. Justificamos la elección de Python por sus bibliotecas, los modelos disponibles y la familiaridad del equipo, considerando C++ como alternativa de mayor rendimiento y desarrollo más complejo.

#### Prompt 3. Google Trends

> Investiga mediante Google Trends el interés a nivel mundial por los lenguajes de programación seleccionados para Matriculator. Compara las búsquedas tanto en la web como en YouTube, utiliza el periodo histórico más amplio disponible y exporta los datos y gráficos en archivos CSV e imágenes para guardarlos en la carpeta data del proyecto.

**Resultado y aplicación en el trabajo final.** Este prompt orientó la comparación del interés de búsqueda y su incorporación al proyecto. El resultado final se puede consultar en la sección Google Trends de la web y en los archivos de la carpeta [data/](data/): la página utiliza una serie de 2004 a 2026 y otra identificada por el equipo como YouTube, de 2008 a 2026. Añadimos medias, máximos, últimos valores y conclusiones sobre la evolución y la elección de Python. Aunque el prompt pedía también imágenes, la entrega genera los gráficos mediante código a partir de los datos, como exige la tarea. Los CSV no conservan todos los filtros originales y no presentamos esos filtros como verificados.

#### Prompt 4. Pseudocódigo en Jupyter Notebook

> Crea un archivo pseudocodigo.ipynb con entre 20 y 50 líneas de pseudocódigo utilizando el lenguaje de inteligencia artificial elegido para Matriculator. Representa el funcionamiento básico del sistema: recibir una imagen, procesarla, detectar una posible matrícula, analizar el resultado y devolver si la matrícula parece válida o no.

**Resultado y aplicación en el trabajo final.** La respuesta sirvió de base para describir el proceso de recepción y validación de la imagen, preparación, detección, OCR, comprobación de formato y confianza, revisión humana y presentación del resultado. Este contenido se recoge en el informe y en [pseudocodigo.ipynb](pseudocodigo.ipynb). El notebook conserva el pseudocódigo aportado por el equipo en una celda Markdown, porque describe la lógica sin constituir un programa ejecutable. La web incorpora además un resumen ampliado con iluminación auxiliar y clasificación de tipo y país. Así, el prompt contribuyó a explicar la estructura del programa y sus controles de error.

Los prompts se conservan como evidencia de las solicitudes originales. La propuesta final limita la validación a la lectura y al formato plausible, sin garantizar autenticidad. En la web, los gráficos se generan con los datos y no se sustituyen por capturas.

### Repreguntas, cambios y correcciones

No utilizamos siempre la primera respuesta de ChatGPT. Fuimos aportando información y solicitando cambios para ajustar las propuestas a nuestro proyecto.

Aclaramos que nuestra propuesta contemplaba dos entrenamientos iniciales: uno para reconocer matrículas y otro para identificar su procedencia, además de un reentrenamiento posterior con supervisión humana.

También indicamos que Google Trends ya estaba incluido en la web cuando ChatGPT lo señaló como pendiente al revisar únicamente el PDF. Le proporcionamos el enlace para que tuviera en cuenta ese contenido.

Pedimos ampliar el periodo del CSV de YouTube, desarrollar mejor las conclusiones y unificar la matriz, porque Python aparecía con 48 puntos en la web y 49 en el informe. La web actual utiliza 49 puntos. Solicitamos incorporar los diagramas, la luz auxiliar y los enlaces a los entregables.

### Justificación de la herramienta y decisiones humanas

Utilizamos ChatGPT porque nos permitía plantear dudas en lenguaje sencillo, aportar documentos y recibir propuestas que podíamos revisar y modificar. Nos ayudó a estructurar explicaciones, comparar nuestro trabajo con los requisitos y preparar cambios concretos.

Las decisiones sobre el proyecto las tomamos nosotros. Aportamos los criterios de comparación, mantuvimos Python como lenguaje principal e indicamos funciones como la iluminación auxiliar y la revisión humana.

### Reflexión conjunta

La IA nos ayudó a avanzar en la redacción y a detectar diferencias entre los materiales. Sin embargo, no sustituyó la lectura del enunciado ni evitó que interpretáramos mal algunas partes. Tuvimos que rehacer contenido y dedicar 12 horas en lugar de las 8 previstas.

Aprendimos que debemos comprobar las respuestas con los documentos originales y explicar con precisión lo que queremos. También vimos que una propuesta bien redactada puede contener errores o no coincidir con nuestra idea.

## Fuentes y referencias

### Materiales utilizados

- Enunciado de la actividad «Trabajo grupal sobre lenguajes de programación para Inteligencia Artificial», proporcionado por el profesorado.
- [Google Trends](https://trends.google.com/): exportaciones aportadas por el equipo, guardadas en `data/`. La web utiliza `mundial-2004.csv` y `youtube-2008-2026.csv`. Sus fechas de exportación indicadas son 23 de septiembre y 5 de octubre de 2026, respectivamente.
- ChatGPT: herramienta de apoyo cuyo uso se documenta arriba; sus respuestas no sustituyen las fuentes técnicas.

### Referencias técnicas propuestas por ChatGPT, pendientes de revisión por el equipo

No las presentamos como documentación ya consultada por los integrantes. No se asigna una fecha de consulta que no esté acreditada.

| Documento | Entidad | Enlace | Estado |
|---|---|---|---|
| OpenCV-Python Tutorials | OpenCV | https://docs.opencv.org/4.13.0/d6/d00/tutorial_py_root.html | Pendiente de revisión |
| Transfer Learning for Computer Vision | PyTorch | https://docs.pytorch.org/tutorials/beginner/transfer_learning_tutorial | Pendiente de revisión |
| csv — CSV File Reading and Writing | Python Software Foundation | https://docs.python.org/3/library/csv.html | Pendiente de revisión |
| json — JSON encoder and decoder | Python Software Foundation | https://docs.python.org/3/library/json.html | Pendiente de revisión |
| HTML DOM API | MDN Web Docs | https://developer.mozilla.org/en-US/docs/Web/API/HTML_DOM_API | Pendiente de revisión |

## Comprobaciones pendientes para la entrega

- Revisar las referencias técnicas y anotar las fechas reales de consulta; corregir en la web la fecha de consulta no acreditada.
