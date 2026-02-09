# 02-Granja

Se pretende digitalizar los activos de una granja en una app para su desarrollo se han especificado los siguientes requisitos.

La fuente de ingresos principal que se va a implementar son los animales, esto se considera que se realiza una inversión económica anual y se espera también un retorno de ingresos anuales.

Los **Animales** pueden ser de tres tipos: **vacas**, **gallinas** y **ovejas**.

---

## Parte 1 - Clases (3 puntos)

- Crea la **interface Activo(inversión: Int, retorno: Int, diario:Boolean) 1 punto**.
    - Tiene la funcion **masRentable(entrada:Activo)**, devuelve true si el valor de la entrada es menor.

- La clase abstracta animal **Animal(...,nombre)**, tiene la *función abstracta sonido*, que devuelve un String con el sonido del animal. Tiene tres clases hijas **1 punto**.
    - **Vaca(...,)**, su sonido es 'Muuu'
    - **Gallina(...,)**, su sonido es 'Cocoroco'
    - **Oveja(...,)**, su sonido es 'Beee'

La clase animal tiene la función `imprimir` que devuelve esto **1 punto**:
`Vaca - rentabilidad: 200.0, nombre:vaca1`
Esta línea es la que te permite imprimir el nombre de la clase: ${this::class.simpleName}
la rentabilidad es simplemente el retorno menos la inversión.

---

## Parte 2 - Extensiones (1 punto)

- Crea una función de extensión `Boolean.aTexto(): Boolean`, que en caso de `true` devuelve **"SI"** y en caso de `false` devuelve **"NO"**. **0,5 puntos**.

- Crea **otra** función de extensión libremente (por ejemplo, sobre `String`, o sobre una de las clases que has creado) y **pruébala en cualquier parte** de tu código, dejando un comentario en `MainActivity` indicando dónde encontrarla y cómo se usa. **0,5 puntos**.

---

## Parte 3 - Funcional (6 puntos)

- El sistema dispone de una **lista de Activos** en el que se pueden visualizar  animales. **1 punto**

- Hay un botón **"Añadir Animal"** para crear nuevos elementos y añadirlos a la lista.  
  - El **formulario** se conecta correctamente con el **ViewModel**. **1 punto**
  - Se **validan** los datos del formulario y se muestra un **error** en caso de información incorrecta. **1 punto**  
- Al pulsar acepta o cancelar se limpian los valores del formulario. **1 punto**  
- Desarrolla un botón para **pruebas**. **2 puntos**  
    - Introduce a la lista datos de ejemplo. 
    - Prueba la creación de todas las clases que se han definido.
