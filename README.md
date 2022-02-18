# Entregaindividual

La direccion de github de este repositorio es: [github](https://github.com/jzazooro/Entregaindividual.git)

### Ejercicio 08: porcentajes, IVA e inversiones

**Entrada**
   * Precio sin impuestos: Real # lo que cuesta el producto sin tener en cuenta los impuestos

**Variable**
   * IVA: Entero # impuesto sobre el valor añadido por comprar un producto
   * Resto de impuestos: Entero # impuestos por comprar un producto

**Resultado**
   * Precio con impuestos: Real # precio final del producto contando los impuestos

**Precondición**
   * Precio inicial>0

**Realización**
```
Si IVA = 21%
     Impuestos totales = 21% + resto de impuestos
Si IVA = 10%
     Impuestos totales = 10% + resto de impuestos
Si IVA 4% 
     Impuestos totales= 4% + resto de impuestos
Precio con impuestos = precio sin impuestos * impuestos totales
```

### Ejercicio 09: media aritmetica ponderada

**Entrada:**
   * Coeficiente de ponderación 1: Real
   * Coeficiente de ponderación 2: Real
   * Coeficiente de ponderación 3: Real 

**Variables:**
   * Numero 1: Real
   * Numero 2: Real
   * Numero 3: Real
   * Numero de números: Entero #los números de números que usamos para hacer las medias

**Resultado:**
   * Media aritmética: Real 
   * Media ponderada: Real

**Realización:** 
```
   Media aritmética= (numero 1 más numero 2 más numero 3) / número de números
   Media ponderada= (numero 1 * peso numero 1 mas numero 2 * peso numero 2 más numero 3 * peso numero 3) / número de números
```
