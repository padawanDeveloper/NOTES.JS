Primera Tarea
=============
1. Hacer el video tutorial **JavaScript30**
 * Utilizamos elemento _window_ con el evento _keydown_ con el cual invocamos la funcion _playSound_ 
 * Utilizamos _document.queryselector_ el cual nos devuelve los elementos audio y .key
 * Creamos arreglos para almacenar los elementos
 * Al presionar la tecla invocada se le agrega a cada key la calse **css** 'playing'

2. Agregar pistas para combinarlas con los sonidos de instrumentos.
 * Se identifica primero que tipo es con la clase _data-type_ la cual es corroborada con **getAttribute** 
 * Creamos un arreglo para los **audios**  _bases_ y para _instrumentos_
 * Filtramos con _if_
 * Se corrobora si la base se esta reproduciendo, para dar _pausa_ o _reproducir_