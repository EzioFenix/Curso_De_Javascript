# Curso Jhon Mircha Javascript


# Clase 21 Arrow Functions

Recordemos cual es la diferencia entre funcion **expresada** y **declarada**

- **expresada:** la que se asigna a una variable.
  
```js
const saludo= function ()
{
    console.log("Hola");
}
```

- **Declarada:** La función tiene un nombre y por tanto se puede invocar mediante ella. Una ventaja de esta es que puede ser invocada antes de ser  escrita, cosa que con la expresada no, ya que la función esta asociada a una variable y esta solo existe  cuando se declara.
  - Al proceso por el cual el interprete de javascript cambia el orden, haciendo que  internamente la funcon este declara antes de ser invocada , aunque yo lo haya escrito al revés , se le conoce como **hoisting (levantado)**

Ejemplo

```js
funcition saludar()
{
    console.log("Hola");
}
```

## Arrow function

Es una nueva manera de declarar funciones, aunque con su implementación cambia el scope.

```js
const saludar=()=>
{
    console.log("Hola");
}
saludar()
```

Ahora, si tu función tiene una sola linea puedes omitir las llaves,

```js
const saludar=()=> console.log("Hola");
```

Otra cosa muy cool de las arrow fuctions , es que tienen un `return` implicito si se hace de una sola linea.

```js
suma=(a,b)=> return a+b;
console.log(suma(1+2))
```

en cosola:

> 3

## El contexto en las arrow fuctions

El contexto cambia en las arrow fuctions, ya que si por ejemplo crearmaos un objeto  y dentro de el declaramos una funcion y dentro de ella escribieramos `console.log(${this})` el resultado es diferente de una con arrow fuction donde imprimiría el objeto contenedor  de donde se encuentra el objeto  es decir **window**
, sin embargo , si lo hacemos usando una funcion corriente mostraía el **objeto**

### Ejemplo 

**código**

```js
//t22-1.html
function perro()
{
    console.log(this)
}
const perro2={
    nombre:"Kenai",
    ladrar:function()
    {
        console.log(this);
    }
}
const perro3={
    nombre:"Kenai",
    ladrar:()=>
    {
        console.log(this);
    }
}
perro()
perro2.ladrar()
perro3.ladrar()
```

![](img/Screenshot_1.png)

**Conslusiones:**

A donde apunta, si dentro ejecutamos un `this`

- funcioón flecha--> padre del contenedor
- funcion normal --> objeto windows
- funcion dentro del objeto--> objeto


# Recorramos un arreglo con Foreach

a este método de lo arreglos se le tienen que pasar una función, que ademas a dicha función se le pueden pasar dos varibales a1, a2

- a1 --> el elemento del arreglo
- a2 --> el indice del elemento del arreglo

**Estructura con forEach**

```js
arreglo.forEach(fuction(a1,a2)
{
    codigo
})
```

# Ejemplo

vamos a recorre un arreglo con 5 elementos, 1 usando una funcion normal , 2 usando una función flecha

**Codigo**

```js
const numeros=[1,2,3,4,5]
numeros.forEach(function(elemento,index)
{
    console.log(`${elemento} en la posición ${index}`)
})
numeros.forEach((e,i)=>
{
    console.log(`${e} en la posición ${i}`)

})
```

**Resultado**

![](img/Screenshot_2.png)

