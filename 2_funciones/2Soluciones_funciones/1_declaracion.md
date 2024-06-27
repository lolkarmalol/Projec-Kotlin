# Declaracion de funciones

[Aqui](https://www.develou.com/funciones-en-kotlin/) hay informacion sobre funciones en Kotlin que te puede servir como complemento.

## Enunciados
1. Define una función llamada `suma_numeros_positivos` que reciba una lista de números y devuelva la suma de los números positivos. Utiliza "continue" dentro de la función para ignorar los números negativos durante la suma.

<details>
<summary>Solucion</summary>

```kotlin
fun suma_numeros_positivos(lista: List<Int>): Int {
    var suma = 0

    for (numero in lista) {
        if (numero <= 0) {
            continue
        }
        suma += numero
    }

    return suma
}
```
</details>

2. Crea una función llamada `buscar_elemento` que reciba una lista y un elemento a buscar. Esta función debería devolver True si el elemento está en la lista y False si no lo está. Utiliza "break" para detener la búsqueda una vez que se encuentre el elemento.

<details>
<summary>Solución</summary>

```kotlin
fun buscar_elemento(lista: List<Int>, elemento: Int): Boolean {
    for (num in lista) {
        if (num == elemento) {
            return true
        }
    }
    return false
}
```
</details>


3. Escribe una función llamada `eliminar_vocales` que tome una cadena de texto como argumento y devuelva la misma cadena pero sin ninguna vocal. Utiliza "continue" dentro de la función para evitar agregar las vocales a la cadena resultante.

<details>
<summary>Solución</summary>

```kotlin
fun eliminar_vocales(cadena: String): String {
    val resultado = StringBuilder()

    for (caracter in cadena) {
        when (caracter.toLowerCase()) {
            'a', 'e', 'i', 'o', 'u' -> continue
            else -> resultado.append(caracter)
        }
    }

    return resultado.toString()
}
```
</details>


4. Define una función llamada `imprimir_numeros_impares` que imprima todos los números impares hasta un número dado. Utiliza "continue" dentro de la función para omitir los números pares durante la impresión.

<details>
<summary>Solución</summary>

```kotlin
fun imprimir_numeros_impares(hasta: Int) {
    for (i in 1..hasta) {
        if (i % 2 == 0) {
            continue
        }
        println(i)
    }
}
```
</details>


5. Crea una función llamada `filtrar_nombres` que tome una lista de nombres y un número mínimo de letras como argumentos y devuelva una lista con los nombres que tengan más letras que el número dado. Utiliza "continue" dentro de la función para evitar agregar los nombres que no cumplan con el requisito.

<details>
<summary>Solución</summary>

```kotlin
fun filtrar_nombres(nombres: List<String>, longitudMinima: Int): List<String> {
    val nombresFiltrados = mutableListOf<String>()

    for (nombre in nombres) {
        if (nombre.length <= longitudMinima) {
            continue
        }
        nombresFiltrados.add(nombre)
    }

    return nombresFiltrados
}
```
</details>


6. Desarrolla una función llamada `imprimir_secuencia` que imprima una secuencia de números del 1 al 20, pero solo los números impares. Utiliza "continue" dentro de la función para omitir los números pares durante la impresión.

<details>
<summary>Solución</summary>

```kotlin
fun imprimir_secuencia() {
    for (i in 1..20) {
        if (i % 2 == 0) {
            continue
        }
        println(i)
    }
}
```
</details>

7. Define una función llamada `sumar_pares` que tome una lista de números y devuelva la suma de todos los números pares en la lista. Utiliza "continue" dentro de la función para ignorar los números impares durante la suma.

<details>
<summary>Solución</summary>

```kotlin
fun sumar_pares(lista: List<Int>): Int {
    var suma = 0

    for (numero in lista) {
        if (numero % 2 != 0) {
            continue
        }
        suma += numero
    }

    return suma
}
```
</details>

8. Crea una función llamada `encontrar_mayor` que tome una lista de números y devuelva el primer número mayor que 100 en la lista. Utiliza "break" dentro de la función para detener la búsqueda una vez que se encuentre dicho número.

<details>
<summary>Solución</summary>

```kotlin
fun encontrar_mayor(lista: List<Int>): Int? {
    for (numero in lista) {
        if (numero > 100) {
            return numero
        }
    }
    return null
}
```
</details>

9. Escribe una función llamada `calcular_primos` que devuelva una lista con los primeros 50 números primos. Utiliza "break" dentro de la función para salir del bucle una vez que se hayan encontrado los 50 números primos.

<details>
<summary>Solución</summary>

```kotlin
fun calcular_primos(): List<Int> {
    val primos = mutableListOf<Int>()
    var num = 2

    while (primos.size < 50) {
        var esPrimo = true

        for (i in 2 until num) {
            if (num % i == 0) {
                esPrimo = false
                break
            }
        }

        if (esPrimo) {
            primos.add(num)
        }

        num++
    }

    return primos
}
```
</details>

10. Define una función llamada `calcular_factorial` que tome un número como argumento y devuelva su factorial. Utiliza "continue" dentro de la función para evitar multiplicar por 0 y "break" para salir del bucle una vez que se haya calculado el factorial.

<details>
<summary>Solución</summary>

```kotlin
fun calcular_factorial(numero: Int): Long {
    var factorial: Long = 1

    for (i in 1..numero) {
        factorial *= i
    }

    return factorial
}
```
</details>


