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





