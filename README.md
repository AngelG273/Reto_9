# Reto_9

Punto 1
```Python
def calcular_promedio(arr):
    if len(arr) == 0: 
        return "El arreglo está vacío"  # Evita la división por cero

    suma = sum(arr)  # Calcula la suma de los elementos del arreglo
    cantidad = len(arr)  # Obtiene la cantidad de elementos en el arreglo
    promedio = suma / cantidad  # Calcula el promedio
    
    return promedio  

if __name__ == "__main__":
  # Definimos un arreglo de números
  numeros = [3.5, 5.0, 7.2, 10.1, 2.3]  
  # Llamamos a la función
  promedio = calcular_promedio(numeros) 
  print(f"El promedio es: {promedio}")   

```
Punto 2
```Python
#Saber cuantos elementos tienen los arreglos
def calcular_longitud(arr):
    contador = 0
    for _ in arr:
        contador += 1
    return contador

#Comparar el numero de elementos dentro de cada arreglo 
def producto_punto(arr1, arr2):
    longitud1 = calcular_longitud(arr1)
    longitud2 = calcular_longitud(arr2)
#verificar que tengan la mismaa cantidad de elmentos
    if longitud1 != longitud2:
        return "Los arreglos deben tener el mismo tamaño"
#Se define las variables  para poder multiplicar cada elemento del primer arreglo con el del segundo arreglo
    producto_punto = 0
    indice = 0
    while indice < longitud1:
        producto_punto += arr1[indice] * arr2[indice]
        indice += 1

    return producto_punto

if __name__ == "__main__":
  arreglo1 = [2, 4, 6]
  arreglo2 = [1, 3, 5]

  resultado = producto_punto(arreglo1, arreglo2)
  print(f"El producto punto es: {resultado}")
```
Punto 3
```Python
def mover_ceros_al_final(arr):
    no_ceros = [num for num in arr if num != 0]  # Filtramos los números distintos de 0
    ceros = [0] * (len(arr) - len(no_ceros))  # Creamos una lista con la cantidad de ceros necesarios
    return no_ceros + ceros  # Concatenamos los números con los ceros al final

if __name__ == "__main__":
  arr = [0, 1, 9, 0, 3, 4, 0, 5]
  resultado = mover_ceros_al_final(arr)
  print(resultado)  # Salida: [1, 9, 3, 4, 5, 0, 0, 0]
```
