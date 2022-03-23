# NotasCursoJS
Algunas notas de pequeños detalles de JS

## Recursividad

La recursividad es cuando una función se llama a sí misma dentro de su propio contexto de ejecución.

```javascript
// tot es una variable, puedo ponerla en el argumento o también dentro de la function.
function sumaRecursiva (num, tot = 0) {
// Esta primera es la condición para parar la recursividad. Si no la tengo será una function que se ejecutará de manera infinita.
    if (num <= 0) return tot;
// Sumo el contenido de num + el contenido de tot
    tot += num;
    num -= 1;
// Llamo nuevamente a la function. Esto me dará la recursividad.
    return sumar(num, tot);
}
```

## PROTOTYPE

### Constructor function

```javascript
//Constructor inicia con mayúscula
function Animal (nombre, genero) {
    //Atributos
    this.nombre = nombre;
    this.genero = genero;
}
```

### Generar nuevas instancias

Function que crea una nueva instancia basado en el constructor Animal

```javascript
const snoopy = new Animal("Snoopy", "macho")

const lolaBunny = new Animal("Lola Bunny", "Hembra")
```

## Agregar métodos al prototype del constructor

Los métodos es mejor crearlos fuera del constructor porque al generar nuevas instancias se hace una copia de todo lo que se encuentra dentro del mismo. Entonces todos los métodos se repetirán en cada instancia, lo que ocupará memoria a la larga y será menos eficiente.

```javascript
Animal.prototype.sonar = function () {
    //Recordar usar el this en la function si necesita usar uno de los atributos del objeto.
    console.log(`Hola me llamo ${this.nombre}`)
}
```
## Class

```javascript
class Animal {
    constructor (nombre, genero) {
        //Acá van los atributos
        this.nombre = nombre;
        this.genero = genero;
    }
    //Los metodos van fuera del constructor pero dentro de la class
    sonar() {
        console.log(`Me llamo ${this.nombre} y hago sonido porque estoy vivo`)
    }
}

//Generar nuevas instancias
const mimi = new Animal("Mimi", "Hembra"),
scooby = new Animal("Scooby", "Macho");
```
### Binary Search Tree

Post Order: 1 left, 2 Right, 3 cb.
Preorder: 1 cb, 2 left, 3 right.
Inorder: 1 left, 2 cb, 3 rifht.
BFS: nodo, left, right (con push hacia array)
