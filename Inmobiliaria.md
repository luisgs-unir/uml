# Inmobiliaria

Se desea realizar un programa en Java que simule el funcionamiento de una Inmobiliaria. En la inmobiliaria se tendrá un registro de todas las Viviendas que se tienen a la venta, así como de todos los Vendedores de la inmobiliaria.

Se dispone de tres tipos distintos de viviendas: chalets individuales, chalet en una urbanización y pisos. Para cada vivienda, independientemente de su tipo, se almacena: código (identificador único de la vivienda), dirección, precio y la información de sus Estancias. Las estancias pueden ser de dos tipos Habitaciones o Terrazas.

Para una habitación habrá que saber si es interior o exterior y los metros cuadrados que tiene. Mientras que para una terraza se necesita saber los metros cuadrados que tiene y si está cerrada.

Además, si la vivienda es un piso se almacenará su altura (entero). Mientras que si la vivienda es un Chalet habrá que almacenar los metros cuadrados de terreno que tiene y si dispone o no de piscina. Y en el caso de ser un chalet de una urbanización se almacenará si es pareado o adosado y el nombre de la urbanización en la que se encuentra.

Y para cada Vendedor se almacenará nif, nombre y las viviendas vendidas por él. Las viviendas deben disponer de la funcionalidad calcular metros cuadrados para el cálculo de estos metros se tendrá en cuenta lo siguiente:

- Si la vivienda es un piso se calculará sumando los metros cuadrados de todas sus habitaciones y los metros cuadrados de las terrazas que computarán sólo al 50%. Si la vivienda es un chalet individual se calculará sumando los metros de todas las estancias y los metros de su terreno.
- Si la vivienda es un chalet de una urbanización se calculará sumando los metros de todas las estancias y los de la parcela sólo al 50%.

La inmobiliaria además de las funcionalidades de añadir vendedor y añadir vivienda, también tendrá las siguientes:

- Realizar una venta. A esta funcionalidad se le pasará como parámetro el código de la vivienda a vender y el nif del vendedor y se realizará la venta. Para ello se eliminará la vivienda de las disponibles para vender en el inmobiliaria y se añadirá a las viviendas vendidas con ese vendedor. Si no se pudiese realizar esta venta porque no se encontrase la vivienda o el vendedor se indicará con un mensaje de error.
- Listar las viviendas con metros cuadrados. A esta funcionalidad se le pasará como parámetro el número de metros cuadrados y se visualizará la información de todas las viviendas de la inmobiliaria que tengan al menos esos metros cuadrados. Para la visualización se utilizará el método toString que será codificado para las viviendas mostrando el tipo de vivienda, su direccion, el número de habitaciones, los metros cuadrados,el precio y si es un piso su altura, si es un chalet si tiene piscina y si es un chalet de una urbanización el nombre de la urbanización.
- Visualizar comisiones de vendedores. Esta funcionalidad mostrará el nombre y la comisión que recibe cada uno de los vendedores de la inmobiliaria. Para ello habrá que codificar en vendedor la funcionalidad calcular comisión que se calculará como el 20% del precio de todos los pisos vendidos por él.

Además para a cada vivienda habrá que poder añadirle estancias, es decir, codificar la funcionalidad addEstancia a la que se le pasará una habitación o una terraza y se añadirán a la vivienda

---
<sub>Autor: Roberto Berjón</sub>