# UML
Apuntes y ejercicios de UML

# UML : Básico
============

## Estructura de una Clase ##

 | **NombreDeLaClase** |
 | ------------------- |
 | atributos           |
 | ------------------- |
 | métodos             |

- **NombreDeLaClase**: Nombre de la clase, debe ir en notación *StudlyCaps*, centrado y en negritas.
- **atributos**: Lista de atributos, en notación *camelCase*.
- **métodos**: Lista de métodos, en notación *camelCase*.

### Visibilidad ###

- Pública: `+`
- Protegida: `#`
- Privada: `-`

### Estructura de Atributos ###

```java
public String nombre;
```

- `public`: Visibilidad.
- `nombre`: Nombre del atributo.
- `String`: Tipo de variable.

### Estructura de Métodos ###

```java
public void agregarEntrada(BlogEntrada nuevaEntrada, Autor autor) {
    // Código del método
}
```

- `public`: Visibilidad.
- `agregarEntrada`: Nombre del método.
- `()` : Paréntesis para parámetros.
  - `nuevaEntrada`: Nombre del primer parámetro.
  - `BlogEntrada`: Tipo del parámetro.
- `void`: Tipo de retorno.

### Métodos o Atributos ###

- Los métodos o atributos **estáticos** deben estar subrayados.
- Los métodos o atributos *abstractos* deben estar en _itálica_. Incluso el nombre de la clase debe estar en itálica si se trata de una clase abstracta.

---

## Relaciones entre Clases ##

Hay cinco tipos de relaciones:

1. [**Dependencia**](#dependencia): `<---` Flecha con línea punteada.
2. [**Asociación**](#asociación): `<———` Línea sólida normal.
3. [**Agregación**](#agregación): `<>———` Flecha con punta de diamante vacía.
4. [**Composición**](#composición): `<>---` Flecha con punta de diamante rellena.
5. [**Herencia**](#herencia): `<|———` Flecha con punta de triángulo vacía.

### Dependencia

Una _dependencia_ es una relación de uso entre dos entidades, en la que una utiliza a la otra. Es la relación más débil y se representa con una línea punteada y una flecha `<---`.

    A ----> B

- La clase **A** depende de la clase **B**.
- **A** usa **B** sin mantener una relación de largo plazo.
- Un cambio en **B** puede afectar a **A**.

Ejemplo en Java:

```java
public class A {
    public void ejecutar() {
        B b = new B();
        // Uso de B dentro de A
    }
}

public class B {
    // Implementación de la clase B
}
```

### Asociación

La asociación implica que una clase tiene una referencia a otra, generalmente como atributo. Se representa con una línea sólida `<———`.

    A ———> B

Ejemplo en Java:

```java
public class A {
    private B b; // A tiene una asociación con B

    public A() {
        this.b = new B();
    }
}
```

### Agregación

La **agregación** es una forma especial de asociación en la que una clase "posee" a otra, pero ambas pueden existir de forma independiente. Se representa con una línea sólida y un rombo vacío.

    A <>——— B

Ejemplo en Java:

```java
import java.util.List;
import java.util.ArrayList;

public class A {
    private List<B> listaB; // A agrega varios objetos de tipo B

    public A() {
        listaB = new ArrayList<>();
    }

    public void agregarB(B b) {
        listaB.add(b);
    }
}

public class B {
    // Implementación de la clase B
}
```

### Composición

La **composición** es una forma más fuerte de agregación donde la existencia de los objetos agregados depende de la clase contenedora. Se representa con una línea sólida y un rombo relleno.

    A <>--- B

Ejemplo en Java:

```java
public class A {
    private B b; // B es parte integral de A

    public A() {
        b = new B(); // La creación de B depende de A
    }
}

public class B {
    // Implementación de la clase B
}
```

### Herencia

La **herencia** establece una relación entre una clase padre (superclase) y una clase hija (subclase). Se representa con una flecha con punta de triángulo vacía `<|———`.

    A
    ^
    |
    B

Ejemplo en Java:

```java
public class A {
    // Código de la clase A
}

public class B extends A {
    // Código de la clase B que hereda de A
}
```
```
