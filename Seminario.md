# Algunas ideas del borrador
## **Recuperación de Información basada en Imágenes (Image Information Retrieval)**


La Recuperación de imágenes es el campo que se encarga de buscar y obtener imágenes digitales de una base de datos. Debido a la cantidad creciente de imágenes digitales alrededor del mundo, desde 1970 este campo ha estado bien activo. Un sistema de recuperación efectivo y rápido de imágenes necesita operar sobre una colección de imágenes y devolver las imágenes relevantes basadas en la consulta, la cual se realiza lo más cercana posible a la percepción humana. Los investigadores de este campo poco a poco, han ido mejorando e implementando varios tipos de sistemas de recuperación de imágenes, de los sistemas basados en **palabras claves**, pasando por los sistemas basados en el contenido (características) de una imagen, y finalmente llegando a los sistemas de recuperación semánticos, con el objetivo de reducir el vacío semántico que existe entre la representación de características de bajo nivel (color, textura, forma, etc) y la semántica de alto nivel en las imágenes.

Tipos de mecanismos de recuperación de imágenes:

- Keyword Based Image Retrieval

    Antes de que las imágenes sean almacenadas en la base de datos, son examinadas manualmente y se les asigna una palabra clave (**keyword**) para describir su contenido. Estos **keywords** son almacenados como parte de los atributos asociados a la imagen. En el proceso de hacer una consulta, el sistema aceptará del usuario una o varias **keywords** que serán el criterio de búsqueda. Luego se realiza un proceso para encontrar las imágenes que cumplen con el criterio de búsqueda.

- CBIR (Content-based Image Retrival)

    Está basado principalmente en el contenido visual de las imágenes como el color, la textura y la forma. Las aplicaciones CBIR se convirtieron en parte de una vida práctica y se utiliza en varios comerciales, archivos gubernamentales e instituciones académicas como bibliotecas. CBIR es una alternativa al text-based image retrieval y se convierte en el área de investigación actual del image retrieval.

    ![./imgs/cbir.png](./imgs/cbir.png)

    Los principales componentes de un sistema CBIR son los siguientes:

    Interfaz gráfica de usuario que permite al usuario seleccionar la consulta que puede estar en uno de los siguientes formas:

    Un ejemplo de imagen: recuperación de imágenes basadas en contenido. Los sistemas permiten al usuario especificar una imagen de ejemplo y busca las imágenes que son más similates a esta, presentando en orden decreciente su puntuación de similitud.

    Motor de consulta / búsqueda: es una colección de algoritmos
    responsables de buscar imágenes en la base de datos que es similar a la consulta del usuario

    Base de datos de imágenes: es un repositorio de imágenes.

    Extracción de características: es el proceso de extraer las características visuales (color, forma y textura) de las imágenes.

    Base de datos de características: es un repositorio  de  características de las imágenes.

- Semantic Based Image Retrieval

    Ni una, ni la combinación de varias características visuales o de bajo nivel (color, textura, forma, relación espacial) pueden capturar completamente los conceptos de alto nivel de las imágenes. Además, debido a que el rendimiento de la recuperación de imágenes basado en características de bajo nivel no es satisfactorio, hay una necesidad de que la investigación vaya dirigida hacia la recuperación de imágenes basada en el significado semántico, tratando de utilizar el concepto cognitivo del ser humano para traducir esas características de bajo nivel a conceptos semánticos de alto nivel (vacío semántico). Este acercamiento permite a los usuarios acceder a imágenes a través de consultas por texto, la cual es más intuitiva, fácil y preferida por los usuarios para expresar su deseo. Como mencionamos previamente en el CBIR, las imágenes pasan por un proceso de extracción de características de bajo nivel que se almacena junto con las imágenes, ahora aquí, se hace necesario traducir esas características de bajo nivel a conceptos de alto nivel que no es capaz de comprender una máquina. Esta traducción usualmente se lleva a cabo utilizando herramientas de aprendizaje supervisado o no-supervisado, para asociar las características de bajo nivel con conceptos de alto nivel, los cuáles serán apuntados con palabras, durante el proceso de anotación de imágenes.

    Como podemos ver la recuperación de imágenes basada en la semántica utiliza técnicas de los 2 mecanismos que surgieron previamente, la extracción de características de bajo nivel utilizada en CBIR y la anotación de imágenes utilizada en el mecanismo basado en palabras claves, para almacenar en la imagen palabras (**keywords**) que se obtengan del proceso de conversión de características de bajo nivel a conceptos de alto nivel propio de este nuevo mecanismo.


