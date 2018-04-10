Primera Tarea
=============
1. Hacer el video 1 tutorial **JavaScript30**
 * Utilizamos elemento _window_ con el evento _keydown_ con el cual invocamos la funcion _playSound_ 
 * Utilizamos _document.queryselector_ el cual nos devuelve los elementos audio y .key
 * Creamos arreglos para almacenar los elementos
 * Al presionar la tecla invocada se le agrega a cada key la calse **css** 'playing'

2. Agregar pistas para combinarlas con los sonidos de instrumentos.
 * Se identifica primero que tipo es con la clase _data-type_ la cual es corroborada con **getAttribute** 
 * Creamos un arreglo para los **audios**  _bases_ y para _instrumentos_
 * Filtramos con _if_
 * Se corrobora si la base se esta reproduciendo, para dar _pausa_ o _reproducir_

Segunda Tarea
=============
1. Hacer el video 2 tutorial **JavaScript30**
  * Creamos variables para las **horas** , **minutos** y **segundos**
  * Se crea una funcion para calcular _horas_ , _minutos_ y _segundos_
  * Se crean variables para calcular el _angulo_ de rotacion para cada _barra_  
  * __secondHand.style.transform = `rotate(${secondsDegrees}deg)`__ cada vez que se actualice se le asigna en el css cuando encuentra transfom

2. Crear reloj digital con css y html
  * Se creo un branch en el repo con lo avanzado con problema

Tercera Tarea
=============
1. Hacer el video 3 tutorial **JavaScript30**
  * :root{} variable que almacena las propiedades a las cuales se accederan con el JS
  * Realizado.

2. IaaS/PaaS/SaaS
  * __Infrastructure as a service__: Es un servicio que se ofrece mucho para poder ser usado en la nube ideal para programadores o gente que quiere armar el server casi a medida en la nube,  _Gartner define IaaS como_: “una oferta automatizada y estandarizada, donde recursos de computo, complementados con opciones de almacenamiento y capacidades de red, son propiedad del proveedor y son ofrecidos al consumidor para que los consuma cuando quiera”. 
  * __Platform as a Service__: Permite a los usuarios crear aplicaciones de software utilizando herramientas suministradas por el proveedor. Los servicios PaaS pueden consistir en funcionalidades _preconfiguradas_ a las que los clientes puedan suscribirse, eligiendo las funciones que deseen incluir para resolver sus necesidades y descartando aquellas que no necesiten.(BD, cantidad de usuarios a los que se desea llegar, almacenamiento, etc...).
  * __Software as a Service__: Se describe cualquier servicio cloud en el que los _consumidores_ (usuarios) puedan acceder a aplicaciones de software a través de internet. Esas aplicaciones están alojadas "en la nube" y pueden utilizarse para una amplia variedad de tareas, tanto para particulares como para organizaciones. Google, Twitter, Facebook y Flickr son ejemplos de SaaS, en los cuales los usuarios pueden acceder a los servicios a través de cualquier dispositivo que pueda conectarse a internet.

| IaaS          | SaaS          | PaaS  |
| :-------------|:-------------| :-----|
|Escalabilidad  |Se paga sólo por lo que se utiliza|No necesitan invertir en infraestructura física|
|Sin necesidad de invertir en hardware| No tiene costes adicionales de hardware|Hace posible que incluso usuarios "no expertos" puedan realizar desarrollos|
|Modelo de tarificación similar al de los suministros públicos como la luz o el gas| El uso del servicio es escalable |Flexibilidad|
|Independencia de la localización|Las actualizaciones son automáticas|Adaptabilidad|
|Seguridad física en los centros de datos|Compatibilidad entre dispositivos|Seguridad|
|No hay puntos únicos de fallo|Accesible desde cualquier lugar|Permite la colaboración entre equipos situados en varios lugares distintos|

Cuarta Tarea
=============
1. Hacer el video 4 tutorial **JavaScript30**
  * const fisteen = inventors.filter(function(inventor){
      if(inventor.year >= 1500 && inventor.year < 1600){
        return true;
      }
    });
    es lo mismo que lo de arriba pero con etra escritura.
    const fifteen = inventors.filter(inventor =>(inventor.year >= 1500 && inventor.year < 1600))

  * const fullName= inventors.map(inventor => inventor.first + inventor.last);
    Otra forma para concatenar.
    const fullName= inventors.map(inventor => `${inventor.first} ${inventor.last}`);

  * const ordered = inventors.sort(function(a, b){
      if(a.year > b.year){
        return 1;
      }else{
        return -1;
      }
    });
    Es lo mismo de arriba si retorna true asigna 1 si no retorna el -1. ordena alfabeticamente y ascendente
    const ordered = inventors.sort((a, b) => a.year > b.year ? 1 : -1);

  * el _split_ los separa y forma un objeto con nombre y apellido(que es lo que contiene y estan separados por la ,);
    const alpha = people.sort(function(lastOne, nextOne){
      const [aLast, aFirst] = lastOne.split(', ');
      const [bLast, bFirst] = nextOne.split(', ');
      return aLast > bLast ? 1 : -1;
    });
2. Crear conexion ssh desde el mac a gitHub

  * ssh-keygen -t rsa -b 4096 -C _"your_email@example.com"_ Agregamos el email a la conexion
  * Enter a file in which to save the key (/Users/you/.ssh/id_rsa): [Press enter] dabamos enter para que lo guarde por defecto
  * Enter passphrase (empty for no passphrase): [Type a passphrase]
    Enter same passphrase again: [Type passphrase again] ingresa la clave y repite
  * eval "$(ssh-agent -s)" agrega el ssh
  * ssh-add -K ~/.ssh/id_rsa 
  * pbcopy < ~/.ssh/id_rsa.pub se copia el contenido de id_rsa.pub

3. Hacer el video 5 tutorial **JavaScript30**

Quinta Tarea
=============
1. Hacer el video 6 tutorial **JavaScript30**

  * Filtramos las ciudades y creamos otra variable que almacene las coisidencias
    return cities.filter(place => {
      // aquí tenemos que averiguar si la ciudad o el estado coinciden con lo que se buscó
      const regex = new RegExp(wordToMatch, 'gi');
      return place.city.match(regex) || place.state.match(regex)
  * Toma el contenido en el input search
    _const searchInput = document.querySelector('.search');_
    _const suggestions = document.querySelector('.suggestions');_
  * Cuando detecta movimiento ejecuta la funcion displayMatches
    _searchInput.addEventListener('change', displayMatches);_
    _searchInput.addEventListener('keyup', displayMatches);_

Sexta Tarea
=============
1. Hacer el video 7 tutorial **JavaScript30**

  * El método some () comprueba si alguno de los elementos en una matriz pasa una prueba (proporcionada como una función).
  * El método some () ejecuta la función una vez para cada elemento presente en la matriz:

1.1 Si encuentra un elemento de matriz donde la función devuelve un valor verdadero , some () devuelve verdadero (y no verifica los valores restantes)
1.2 De lo contrario, devuelve falso
  * El método slice () devuelve los elementos seleccionados en una matriz, como un nuevo objeto de matriz.

  * El método slice () selecciona los elementos comenzando en el argumento de inicio dado , y termina en, pero no incluye , el argumento final dado .

  __Nota:__ La matriz original no se cambiará.

2. Hacer el video 8 tutorial **JavaScript30**

  * Tutorial completo 
  * __El método beginPath ()__ inicia una ruta o restablece la ruta actual.
_Consejo: Use moveTo (), lineTo (), quadricCurveTo (), bezierCurveTo (), arcTo (), y arc (), para crear rutas._
_Consejo: use el método stroke () para dibujar la ruta en el lienzo._

3. Hacer el video 9 tutorial **JavaScript30**
  * Tutorial completado
  * Es casi todo lo aprendido con anterioridad y se enseña nuevos metodos de consola.(esta comentado en el codigo lo nuevo)

4. Hacer el video 10 tutorial **JavaScript30**
  * Video completo
  * Hay cosas que se pueden mejorar,se podria crear un arrego con los checked para saver exactamente cuale estan presionados antes de seleccionar varios

Septima Tarea
=============
1. Hacer el video 11 tutorial **JavaScript30**
  * Video completado, manejo de la barra de progreso controlando la duracion.

2. Hacer video 12 tutorial **JavaScript30**
  * Video completado, evento visto keyup (detecta las teclas que se precionan)

3. Hacer video 13 tutorial **JavaScript30**
  * Tutorial completado, La propiedad offsetTop devuelve la posición superior (en píxeles) relativa a la parte superior del elemento offsetParent.

El valor devuelto incluye:

la posición superior y el margen del elemento
el relleno superior, la barra de desplazamiento y el borde del elemento offsetParent
**Nota:** El elemento offsetParent es el ancestro más cercano que tiene una posición que no sea estática.

**Consejo:** Para devolver la posición izquierda de un elemento, use la propiedad offsetLeft .

4. Hacer video 14 tutorial **JavaScript30**

Octava Tarea
=============
1. Hacer el video 15 tutorial **JavaScript30**
  * La propiedad Element.innerHTML cambia o devuelve la sintaxis HTML describiendo los descendientes del elemento.
  * Agrega un checkBox y le asigna un id 
  * input type="checkbox" data-index=${i} id="item${i}" ${plate.done ? 'checked' : ''} 

2. Hacer el video 16 tutorial **JavaScript30**
  * Tutorial hecho 

¿Que es Versionado Semántico 2.0.0-rc.2?
=============  

Es un set simple de reglas y requerimientos que dictan cómo asignar y cómo aumentar los números de versión. Para que este sistema funcione, tienes que declarar primero un **API pública**. Esto puede consistir en documentación o ser explicitado en el código mismo. De cualquier forma, es importante que esta API sea clara y precisa. Una vez que identificaste tu **API pública**, comunicas cambios a ella con aumentos específicos al número de versión. Considera un formato de versión del tipo _X.Y.Z_ (Major.Minor.Patch) Los arreglos de bugs que no cambian el API incrementan el patch, los cambios y adiciones que no rompen la compatibilidad de las dependencias anteriores incrementan el minor, y los cambios que rompen la compatibilidad incrementan el major.

MUST, MUST NOT, SHOULD, SOULD NOT y MAY.
============= 
1. __DEBE__ declarar una API pública, debería ser precisa y completa.
-
2. __DEBE__ tomar la forma X.Y.Z donde X, Y, y Z, (X es la versión “major”, Y es la versión “minor”, y Z es la versión “patch”) el  incremento de estos son de a 1.
-
3. Cada liberacion de _version_ es unica y los contenidos de esa versión __NO DEBEN__ ser modificadas.
-
4. La _versión_ __major__ en cero (__0__.y.z) es para desarrollo inicial. Cualquier cosa puede cambiar en cualquier momento. El API pública no debiera ser considerada estable.
-
5. La _versión_ __1.0.0__ define el _API pública_.
-
6. La _versión_ patch Z (x.y.Z | x > 0) DEBE incrementarse cuando se introducen solo arreglos compatibles con la versión anterior.
-
7. La versión __minor__ Y (x.Y.z | x > 0) DEBE ser incrementada si se introduce nueva funcionalidad compatible con la versión anterior. Se __DEBE__ incrementar si cualquier funcionalidad de la _API_ es marcada como deprecada. __PUEDE__ ser incrementada si se agrega funcionalidad o arreglos considerables al código privado.
-
8. La versión major X (X.y.z | X > 0) DEBE ser incrementada si cualquier cambio no compatible con la versión anterior es introducida a la API pública. PUEDE incluir cambios de niver minor y/o patch. Las versiones patch y minor DEBEN ser reseteadas a 0 cuando se incrementa la versión major.











