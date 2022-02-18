# Entregaindividual

La direccion de github de este repositorio es: [github](https://github.com/jzazooro/Entregaindividual.git)

### Ejercicio 08 a: porcentajes, IVA e inversiones

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

### Ejercicio 08 b

**entrada**
   * inversion: Real # dinero al que se le atribuyen los intereses
   * tiempo: Entero # meses
   * contante de interes: Real # multiplicador que decide los intereses

**variable**
   * capital total: Real # dinero teniendo en cuenta las ganancias de los intereses
   * interes: Real # dinero ganado debido a las inversiones realizadas
  
  **realizacion**
  ```
  interes= inversion * tiempo * contante de proporcionalidad
  capital total=inversion + interes
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

### Ejercicio 10: area del triangulo

**Entrada**
   * Hipotenusa: Real # longitud de la hipotenusa
   * Lado: Real # longitud de uno de los lados

**Resultado**
   * Área del triángulo: Real #	

**Precondición** 
   + Hipotenusa>0
   * Lado>0

**Realización**
```
     Área del triángulo=(hipotenusa * lado) / 2
```

### Ejercicio 11: salario y horas extra
    
**Precondición**
   * salario_mensual_bruto > 0

**constante**
   * CANTIDAD_SEMANAS : ENTERO ← 52 # Cantidad de semanas de trabajo
   * CANTIDAD_HORAS_SEMANA : ENTERO ← 35  # Cantidad legal de horas de trabajo semanales

**realización**
    # Cálculo del  precio_hora de la remuneración bruta de base
```
    Resultado ← salario_mensual_bruto x 12 / (REAL(CANTIDAD_HORAS_SEMANA) x REAL(CANTIDAD_SEMANAS))
```
**postcondición**
   * Resultado = salario_mensual_bruto x 12,0 / REAL(35 x 52)

### Ejercicio 12: cuenta de deposito

Tipo cuenta estructura

**Variables:**
   * saldo: Real
   * invariante: real # El descubierto no está autorizado

**Realización:** 
```   
saldo ≥ 0
```

fin cuenta

### Ejercicio 12 b: operaciones aplicables
abrir(c : CUENTA ; saldo_inicial : REAL) # Inicializar cuenta mediante un `saldo_inicial'.

**Precondición**

   * saldo_inicial > 0

**realización**

   * c.descubierto ← 0
   * c.saldo ← saldo_inicial

**postcondición**

    c.descubierto = 0 # El descubierto no está autorizado
    antiguo(saldo_inicial) = saldo_inicial
    c.saldo = saldo_inicial

fin abrir

abonar(c : CUENTA ; crédito : REAL) # Crédito cuenta de la suma crédito

**Precondición**
   * c.saldo ≠ NULO
   * crédito ≠ NULO

**realización**

```
    c.saldo ← c.saldo + crédito
```

**postcondición**
    # El descubierto autorizado y el importe del `crédito' no se modifican
```
    antiguo(c).descubierto = descubierto
    antiguo(c).crédito = crédito
    c.saldo = antiguo(c).saldo + crédito
```

fin abonar

cargar(c : CUENTA ; débito : REAL) # Carga cuenta con la suma débito

**Precondición**
   * c.saldo ≠ NULO
   * débito ≠ NULO
   * c.saldo + c.descubierto ≥ débito ≥ 0

**realización**

```
    abonar(c, –débito)
```

**postcondición**

    # El descubierto autorizado y el importe del `débito' no se
    # modifican
```
    antiguo(c).descubierto = descubierto
    antiguo(débito) = débito
    c.saldo = antiguo(c).saldo – débito
```

fin cargar

consultar(c : CUENTA) : REAL # El saldo de la cuenta

**precondición**
   * c.saldo ≠ NULO

**realización**

```
    Resultado ← c.saldo
```

**postcondición**

   * Resultado = c.saldo

fin consultar

es_acreedora(c : CUENTA) : BOOLEANO # ¿es acreedora de la cuenta?

**precondición**
   * c.saldo ≠ NULO

**Realización**

```
    Resultado ← (c.saldo > 0)
```

**postcondición**

   * Resultado = (c.saldo > 0)

fin es_acreedora

es_deudora (c : CUENTA) : BOOLEANO # ¿es deudora de la cuenta?

**precondición**

   * c.saldo ≠ NULO

**Realización**

```
     Resultado ← (– c.descubierto ≤ c.saldo ≤ 0)
```

**postcondición**
  
   * Resultado = (– c.descubierto ≤ c.saldo ≤ 0)

fin es_deudora

### Ejercicio 12 c: descubiertos

abrir(Cuenta ; saldo_inicial : REAL ; descubierto_MAX : REAL)

   * Inicializar cuenta mediante un saldo_inicial y un descubierto_MAX

**Precondición**

   * saldo_inicial > 0
   * descubierto_MAX ≥ 0

**realización**

```
c.descubierto ← descubierto_MAX
c.saldo ← saldo_inicial
```

**postcondición**

```
c.descubierto = descubierto_MAX
c.saldo = saldo_inicial
```

fin abrir


