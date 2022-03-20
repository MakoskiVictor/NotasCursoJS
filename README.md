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

