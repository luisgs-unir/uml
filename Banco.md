# Banco

Se quiere realizar un programa en Java que simule el funcionamiento de una entidad financiera. En la entidad financiera se almacenarán los clientes de la entidad, así como el nombre y CIF de la entidad financiera.

Las entidades financieras podrán tener dos tipos de clientes: Clientes empresa y Clientes particulares, independientemente del tipo de cliente para todos ellos se almacena su identificación (única para cada cliente), su nombre y sus cuentas. Además si se trata de un cliente empresa se almacenará:
- Número de empleados de la empresa
- Empresa con fines sociales. Indicará si se trata de una empresa con fines sociales o no.

Por otro lado si se trata de un cliente particular se almacenará:
- Edad
- Nómina. Indica si tiene o no domiciliada la nómina

Con respecto a las cuentas la información a almacenar es la siguiente:
- Número de cuenta. Identificará a la cuenta, no habrá dos cuentas con el mismo número de cuenta.
- Saldo: Saldo disponible en la cuenta.

Cuando se crea una cuenta será necesario indicar al menos el número de cuenta, si no se indica el saldo se tomará que éste es 0.

La entidad financiera, además de poder añadir clientes, debe tener al menos las siguientes
funcionalidades:

- **addCuenta**. Esta funcionalidad recibirá como parámetro el identificador del cliente y la cuenta que añadirá esa cuenta al cliente.
- **cargarCominisión**: Esta funcionalidad recibirá como parámetro la comisión a cargar y se cargará dicha comisión en todas las cuentas de todos los clientes particulares excepto en aquellos que tengan domiciliada la nómina.
- **Realizar ingreso**. Esta funcionalidad recibe como parámetro el identificador del cliente, el número de cuenta y la cantidad a ingresar y realiza el ingreso. Si no existe el cliente o no posee el número de cuenta se mostrará un mensaje indicándolo.
- **visualizarInfoClientes**: Esta funcionalidad visualizará la información de todos los clientes para ellos utilizará la funcionalidad visualizarInfoCliente de cliente.
- **Cancelar cuenta**: Esta funcionalidad recibe como parámetro el identificador del cliente y el número de cuenta y cancelará esa cuenta. Esta operación sólo podrá realizarse si el saldo de la cuenta es positivo, en caso contrario se mostrará un mensaje indicándolo. 

Las funcionalidades que al menos debe tener para cliente: 
- **Consultar saldo**. Esta funcionalidad mostrara el saldo total del cliente teniendo en cuenta todas sus cuentas.
- **visualizarInfoCliente**. Esta funcionalidad mostrará por pantalla toda la información de un cliente (Identificación, nombre, número empleados y si es una empresa social en el caso de ser un cliente de empresa y si se trata de uno particular edad y si tiene domiciliada la nómina.) Además se mostrará la información de todas sus cuentas invocando a **visualizarInfoCuenta** de cuenta



---
<sub>Autor: Roberto Berjón</sub>