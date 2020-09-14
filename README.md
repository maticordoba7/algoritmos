# Algoritmos
En este repositorio estaré publicando mis soluciones a algunos problemas triviales

1 - Find Needle

 Problema: encontrar el índice de la aparicion de un string (needle) dentro de otro (haystack), de existir deberia devolver ese índice de lo contario devolveria -1.
 
 Solución:
   
   ```js
   
  const findNeedle = (needle, haystack) => {
    for (let i = 0; i < haystack.length; i++) {
      for( let j = 0; j < needle.length; j++) {
        if(haystack[i + j] !== needle[j]) break
        if (j + 1 === needle.length) return i
      }
    }
    return -1
  }
  
   ```
  
2 - Sum Array

Poblema: dado un arreglo de números ordenados y un número entero, verificar si dos números suman el número entero.
    
  Solución:
     
   ```js
   
  const sumArray = (array, n) => {
      for (let i = 0; i < array.length; i++){
        for( let j = i + 1; j < array.length; j++){
          if (array[i] + array[j] === n) return true
          }
        }
        return false
      }
  
   ```

  
3 - Max Value
  
 Problema: dado un arreglo de acciones, encontrar la mayor ganancia posible de   comprar a un horario y vender después.
  
  Solución:
  
  
   ```js
   
  const mayor_ganancia = (array) => {
      var mayor_ganancia = 0
      for (let i = 0; i < array.length ; i++) {
        for (let j = i +1 ; j < array.length; j++) {
          if(array[j] - array[i] > mayor_ganancia){
            mayor_ganancia = array[j] - array[i]
            }     
         }
       }
       return ("La mayor ganancia es: " + mayor_ganancia)
      }
  
   ```
    
4 - Multidimensional Sum Array

 Problema: Dado un arreglo que está compuesto de subarreglos de longitud variada. Encontrar la suma de cada uno de los elementos.
  
  Solución:
    
   ```js
   
  const mdSumArray = (arr) => {
      let sum = 0
      for (let i = 0; i < arr.length; i++){
        if(Array.isArray(arr[i])) sum += mdSumArray(arr[i])
        else { 
          sum += arr[i]
        }
      }
    return sum
    }
  
   ```
