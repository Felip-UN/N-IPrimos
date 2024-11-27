# N-IPrimos
## Descripcion
Plantear el algoritmo para obtener los números primos hasta n
### Aclaraciones
Queremos verificar si X(El numero que escribamos) es primo y lo que tengo planeado esta relacionado con un metodo que nos enseño un profesor de matematicas que MUY posiblemente sea correcto por lo que estaria mas enfocado en valores grandes


El planteamiento seria asi
## Pseudocodigo
```python
n : entero >= 2
Pi = [2, 3, 5, 7, 11, 13, 17, 19, 23, 29, 37, 41, 43, 47] #Lista con los primeros 15 numeros primos

numeros_N = 2

if n > 47
  ejecutar un bucle mientras numeros_N < n ,si numeros_N >= n rompe el bucle
    if numeros_N da modulo 0 por algun valor de la lista Pi
      numeros_N += 1
    else
      agregar ese numero a la lista Pi
      numeros_N += 1
  print (Pi)
else
  eliminar cualquier valor de la lista Pi > n
  print (Pi)
```

Si un número pasa la prueba de no ser divisible por los primeros 15 primos, es un buen indicio de que es primo, aunque no garantiza con certeza que lo sea 

## Diagrama de flujo
```mermaid
---
config:
  layout: fixed
---
flowchart TD
    n2["Inicio"] --> n4["Ingresa un numero entero mayor o igual a 2 (n)"]
    n5["Crear una lista con los 15 primeros numeros primos definida como Pi<br>[2, 3, 5, 7, 11, 13, 17, 19, 23, 29, 37, 41, 43, 47]"] --> n6@{ label: "<pre style=\"font-family:\"><span class=\"pl-s1\">n</span> <span class=\"pl-c1\" style=\"color:\">&gt;</span> <span class=\"pl-c1\" style=\"color:\">47 ?</span></pre>" }
    n6 --> n8@{ label: "<pre style=\"font-family:\"><span class=\"pl-s1\">eliminar</span> <span class=\"pl-s1\">cualquier</span> <span class=\"pl-s1\">valor &gt; n</span> <span class=\"pl-s1\">de \n</span><span class=\"pl-s1\">la </span><span class=\"pl-s1\">lista </span><span class=\"pl-v\" style=\"color:\">Pi</span></pre>" } & n19["numeros_N &lt; n ?"]
    n8 --> n12["print(Pi)"]
    n4 --> n13["Definimos numeros_N = 2"]
    n13 --> n5
    n11["numeros_N da modulo 0 por algun valor de la lista Pi?"] --> n14["agregar ese numero a la lista Pi"] & n15["numeros_N += 1"]
    n14 --> n18["numeros_N += 1"]
    n19 --> n12 & n11
    n18 --> n19
    n15 --> n19
    n12 --> n22["End"]
    n20["No"]
    n21["Si"]
    n9["Si"]
    n10["No"]
    n16["Si"]
    n17["No"]
    n2@{ shape: rounded}
    n6@{ shape: diam}
    n8@{ shape: rect}
    n19@{ shape: diam}
    n12@{ shape: rect}
    n13@{ shape: rect}
    n11@{ shape: diam}
    n22@{ shape: rounded}
    n20@{ shape: text}
    n21@{ shape: text}
    n9@{ shape: text}
    n10@{ shape: text}
    n16@{ shape: text}
    n17@{ shape: text}
    classDef Sky stroke-width:1px, stroke-dasharray:none, stroke:#374D7C, fill:#E2EBFF, color:#374D7C
```
