# Curso Javascript-Ejercicios 

Impartido por John Ortiz Ordoñez


---

# Bitácora


---

# Ejercicio 100: Obtener las Partes o Palabras de una Cadena de Caracteres con split

## Teoria

Podemos partir una cadena usando un caracter diferenciador, será como el caracter que te diga donde partir partir la cadena. 

- El resultado de usar split es una arreglo con las particiones


```js
let nombre="Victor Miguel Barrera Peña"
const particion= nombre.slipt(" ")
```

particion es igual a 

>[Victor, Miguel, Barrera, Peña]

tambien podemos espcificifar a split cuantas particiones quermeos guardar en la variable, supongamos que en el anerior ejemplo no queremos guardar el "peña", lo hariamos con 

```js
let nombre="Victor Miguel Barrera Peña"
const particion= nombre.slipt(" ",3)
```

particion es igual a 

>[Victor, Miguel, Barrera]