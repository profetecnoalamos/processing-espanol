# PROCESSING ESPAÑOL

Documentación para aprender Processing en español.

## Descargar

Processing está disponible para Linux, Mac y Windows. 
Seleccione uno para descargar el software a continuación y se desacrgará un archivo `.zip`:

* [Mac]() La versión de Mac OS X es un archivo `.zip`. Haga doble clic en él y arrastre el ícono de **Processsing** a la carpeta `Aplicaciones`. Si está utilizando la máquina de otra persona y no puede modificar la carpeta Aplicaciones, simplemente arrastre la aplicación al escritorio. Luego haga doble clic en el icono Procesamiento para comenzar.
* [Linux 64 bits]() La versión de Linux es un archivo .tar.gz, que debería ser familiar para la mayoría de los usuarios de Linux. Descargue el archivo a su directorio de inicio, luego abra una ventana de terminal y escriba:

        tar xvfz processing-xxxx.tgz

    (Reemplace xxxxcon el resto del nombre del archivo, que es el número de versión). Esto creará una carpeta con un nombre processing-2.0o algo similar. Luego cambie a ese directorio:

        cd processing-xxxx

    y ejecutarlo:

        ./processing 

* [Windows 64 bits]() En Windows, tendrá también un archivo `.zip`. Haga doble clic en él y arrastre la carpeta hacia una ubicación en su disco duro. Podría ser *Archivos de programa* o simplemente al *Escritorio*, pero lo importante es que la carpeta de Processing se descomprima. Luego haga doble clic en processing.exe para comenzar.
* [Windows 32 bits]() Si tiene un PC de 32 bits con windows también puede descargar Processing (necesitamos descomprimirlo igualmente).

## Tu primer programa

Ahora está ejecutando el entorno de desarrollo **Processing**. 

* El **área grande** es el **`Editor de texto`** y hay una fila de botones en la parte superior, esta es la **`Barra de herramientas`**. 

* Debajo del `Editor de texto` está el **`Área de mensajes`**, y debajo está la **`Consola`**. 

    * El **`Área de mensajes`** se usa para mensajes de una línea.
    * La **`Consola`** se usa para más detalles técnicos.

En el editor, escribe lo siguiente:

    ellipse(50, 50, 80, 80);

Esta línea de código significa *"dibuja una elipse, con el centro 50 píxeles por encima de la izquierda y 50 píxeles por debajo de la parte superior, con un ancho y una altura de 80 píxeles"*. Haga clic en el botón **Ejecutar** (botón triangular en la barra de herramientas).

Si ha escrito todo correctamente, verá un círculo en su pantalla. Si no lo escribió correctamente, el área de mensajes se volverá roja y se quejará de un error. Si esto sucede, asegúrese de haber copiado exactamente el código de ejemplo: los números deben estar entre paréntesis y tener comas entre cada uno de ellos, y la línea debe terminar con un punto y coma.

Una de las cosas más difíciles de empezar a programar es que tienes que ser muy específico con la **sintaxis**. El software Processing no siempre es lo suficientemente inteligente como para saber lo que quiere decir, y puede ser bastante quisquilloso con la ubicación de la puntuación. Te acostumbrarás con un poco de práctica.

A continuación, pasaremos a un boceto que es un poco más emocionante. Elimine el texto del último ejemplo e intente esto:

    void setup() {
        //función setup --> se trata de las configuraciones iniciales
        size(480, 120); //tamaño de pantalla
    }

    void draw() {
        ellipse(mouseX, mouseY, 80, 80); //dibuja un circulo de 80x80 con centro en el mouse

        if (mousePressed) {
        //Si presiona el ratón lo rellena de negro y sino de blanco
            fill(0);
        } else {
            fill(255);
        }
    }