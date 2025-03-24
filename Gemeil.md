# Gemeil
Diseñar un programa Java que simule el comportamiento del gestor de correo **“Gemeil”** en cuanto a la gestión de contactos de sus cuentas de correo electrónico. Para ello hay que tener en cuenta las siguientes consideraciones:

**a)** Una cuenta (**Account**) posee los siguientes datos:  
- **email**: dirección de correo electrónico. No puede haber dos cuentas con el mismo email (por lo tanto actúa como identificador de la cuenta).  
- **password**: contraseña de la cuenta.  
- **contactos**: contendrá un *set* en el que se almacenan todos los contactos de una cuenta. Un contacto representa un destinatario del correo electrónico.

**b)** Como se ha mencionado en el enunciado, el usuario podrá tener más de una cuenta de correo. Sin embargo, cada cuenta no solo guardará su *email* y su *password*, sino también su **inbox**. Un objeto de tipo *Singleton* hace referencia a un objeto que solo se puede crear una vez en toda la ejecución del programa. Una clase *Singleton* se caracteriza porque en ella se implementa un patrón de diseño *Singleton*. La clase *Singleton* que se utilizará será la clase **Inbox**, que simulará la bandeja de entrada de un cliente de correo. La clase **Inbox** se encargará de almacenar todos los correos que se reciben y envían. No se podrán crear más de una instancia de la clase **Inbox**. Cada cuenta tiene su propia instancia de la clase **Inbox**.

**c)** Para la gestión de cuentas se añaden las siguientes características propias de la implementación:  
- Se podrá crear una nueva cuenta a partir de su *email* y su *password*.  
- El *password* se almacenará encriptado. Para ello se puede usar cualquier algoritmo de encriptación.  
- Cuando se añade una cuenta, se valida que no exista ya una cuenta con el mismo *email*.

**d)** Para la gestión de contactos se pide implementar las siguientes funcionalidades:  
- **addContact**: esta funcionalidad permitirá añadir un contacto a la cuenta.  
- **removeContact**: esta funcionalidad permitirá eliminar un contacto de la cuenta.  
- **findAccount**: esta funcionalidad buscará una cuenta a partir de su *email*. En caso de no existir, se devolverá `null`. También debe verificar que la *password* introducida es la correcta.  
- **logInAccount**: esta funcionalidad permitirá loguearse en la cuenta a partir de su *email* y su *password*. Además, se validará que la *password* introducida es la correcta.  
- **listAccounts**: esta funcionalidad listará todas las cuentas creadas en el sistema. Para cada cuenta se mostrará su *email*, *password* y lista de contactos (para esto último se invocará a la funcionalidad `listContacts` de `Account`).

---

Las funcionalidades proporcionadas por **Account** son las siguientes:

- **addSingle**: esta funcionalidad recibe como parámetro el nombre del contacto y la dirección de correo electrónico asociado.  
  Comprueba las siguientes condiciones de error notificadas mediante excepciones:  
  - **DuplicatedContactException**: no se permite que haya dos contactos con el mismo nombre. Esta excepción tendrá una propiedad de lectura que represente el nombre del contacto (el valor de dicha propiedad se establecerá en el momento de la creación de la excepción).  
  - **RestrictedContactException**: se propaga esta excepción cuando el email que se recibe como parámetro es el mismo que el asociado a la cuenta **Account** en la que se está intentando añadir el contacto.

- **addGroup**: esta funcionalidad recibe como parámetro un *set* de contactos que representan, respectivamente, el nombre y el correo del *Contact* que se quiere añadir. Al extraer el *Group*, se añaden todos los contactos que no estaban ya añadidos. Para los contactos que sí estaban añadidos, se notificará la excepción **DuplicatedContactException**, y para aquellos que no se pudieron añadir, se notificará la excepción **RestrictedContactException**.

- **ContactNotFoundException**: se propaga esta excepción cuando el contacto no existe. Esta excepción tiene una propiedad de lectura que representa el nombre del



---
<sub>Autor: Roberto Berjón</sub>