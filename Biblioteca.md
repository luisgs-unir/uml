# Biblioteca

Diseñar el diagrama de clases que represente el funcionamiento de una **Biblioteca**. En la biblioteca debe llevar un registro de todos los libros que posee así como de todos sus socios. 

La información que precisa conocer de un **libro** es la siguiente: su signatura (será su identificador, no podrá haber dos libros que posean la misma signatura), título y autor. Además será preciso conocer el estado en el que se encuentra el libro, que podrá ser prestado o disponible. En caso de que su estado sea prestado, será también será necesario conocer quién es el socio que lo tiene. Cuando se crea un libro, su estado deberá ser disponible y por consiguiente no tendrá la información relativa a ningún socio. 

La información que se precisa conocer de un **socio** es la siguiente: su código (será su identificador, no podrá haber dos socios que posean el mismo código), nombre, dirección así como todos los libros que tiene en préstamo. Cuando se crea un socio, carecerá de libros en préstamo. 

La biblioteca, **además de tener funcionalidades que permitan registrar los socios y los libros, también precisará de las siguientes**: 

- **Realizar un préstamo**: será necesario indicar la signatura del libro y código del socio que desea solicitarlo. Esta funcionalidad devolverá true o false indicando si el préstamo se ha podido realizar o no. No se podrá realizar un préstamo si: no existe el socio con el identificador proporcionado; no existe el libro con la signatura indicada; existiendo el libro, su estado indica que ya está prestado. 
A la hora de prestar el libro, habrá que indicar que su estado pasa de disponible a prestado indicando, al mismo tiempo, el socio que lo posee. Por otra parte habrá que incluir el libro en la lista de libros que tiene en préstamo el socio. 

- **Devolver un libro**: será necesario indicar la signatura del libro a devolver. Esta funcionalidad devolverá true o false en función a que se haya podido realizar o no la devolución del libro. No se podrá devolver un libro siéste no existe o su estado indica que está disponible. 
A la hora de efectuar la devolución habrá que indicar que su estado pasa de prestado a disponible; habrá que eliminar el libro de la lista de libros que posee en préstamo el socio que lo tenía en préstamo y, por último, habrá que eliminar toda referencia del socio en el libro. 

- **Mostrar libro**: a esta funcionalidad se le pasará como parámetro la signatura de un libro y tendrá que mostrar en pantalla todos sus datos: título, autor, estado y si éste fuese prestado, el código, nombre y dirección del socio que lo tuviera. Si el libro no existiera, se mostrará un mensaje que lo indique.

- **Mostrar socio**: a esta funcionalidad se le pasará como parámetro el código del socio y mostrará en pantalla todos sus datos: nombre, dirección así como todos los libros que tiene en préstamo (por cada uno su signatura y título). Si el socio no existiera, se mostrará un mensaje que lo indique.

Puedes incluir todas las funcionalidades que precises. El programa que debes implementar debe comprobar el correcto funcionamiento de todas las funcionalidades que implementes


---
<sub>Autor: Roberto Berjón</sub>