# Reto-3
Reto numero 3 programacion de computadoras
# 1. Algoritmos para identificar numeros primos hasta n
-Pseudo codigo:
------------
     definir crib_eratostenes(numero n hasta el que queremos analizar):
     primos= [] <-----conjunto vacio que llenaremos con primos
     no_primos= [] <-----conjunto vacio que llenaremos con no primos
     para i en el rango (2, n+1) <----- rango en el que se realizara el proceso, iniciando en 2
     si i no esta en no_primos: <-----como primero queremos anexar los primos tenemos que comprobar que iniciemos con numeros primos
     agregar i a primos
     para j en el rango i**2, con el limite de n+1 y un crecimiento de i: <----- usaremos una segunda variable llamada j unicamente para sacar los no primos
     se agregara j al conjunto de no primos
     se regresara el valor primos y se acabara la funcion <----- asi al realizar la funcion solo obtendremos los primos
     imprimir criba_eratostenes hasta n
     imprimir longitud de criba_eratostenes hasta n <----- nos dara la longitud del conjunto de los primos
  
-Codigo python:
------------
    def criba_eratostenes(n): 
    primos = [] 
    no_primos = [] 
    for i in range (2, n + 1): 
       if i not in no_primos: 
          primos.append (i)  
          for j in range (i * i, n +1, i):
              no_primos.append(j) 
    return primos 
    print (criba_eratostenes(n)) 
    print(len(criba_eratostenes(n))) 

 -Diagrama:
------------
    [![](https://mermaid.ink/img/pako:eNpdUkFuGzEM_Aqh0xqND83RhwaN7eQS9NLe6hxoiY6VaCmXklI4tt9WIC8LtVY2bRdYiCI4w5nZPRgbHZmZ2YT4225RMvxYrBj0-frzW-lJYoKd-F6PLaaMUBh46APfw3T65XgXiFHARn4snHXuGa3XQxttcmTYA8dWH-G6A2QM_kXBH6S_CkEiILaFOEutgAJ4ziTPGCI4gktA4E-fJ2ed11UFzA-vf3SusexIMjFZqpPvK69OZ8C8qk7-eNvhg9CDrscwyq_8YVQ8-QvB8diSua0bF51nbz1WXwHVtHhch0GvulkXq_UmCrjISpkKVPUCZ5CgLuxjdWYLOkFXF4_y41rVe-3VDLFa91G8Q9f0LKqAZUcp0wdeU2t-8H9DYwQNvxwiu_knMqFUQq7LgBL0uFexQ8xXp2kLbOPfv9eZ5qbFMq9Xfc2FUaoevdMf6jA0Td5STysz09KhPK3Mik86hyXH73u2Zpal0IUpO4eZFl4dYG9mGwyJTm8QEuUP?type=png)](https://mermaid.live/edit#pako:eNpdUkFuGzEM_Aqh0xqND83RhwaN7eQS9NLe6hxoiY6VaCmXklI4tt9WIC8LtVY2bRdYiCI4w5nZPRgbHZmZ2YT4225RMvxYrBj0-frzW-lJYoKd-F6PLaaMUBh46APfw3T65XgXiFHARn4snHXuGa3XQxttcmTYA8dWH-G6A2QM_kXBH6S_CkEiILaFOEutgAJ4ziTPGCI4gktA4E-fJ2ed11UFzA-vf3SusexIMjFZqpPvK69OZ8C8qk7-eNvhg9CDrscwyq_8YVQ8-QvB8diSua0bF51nbz1WXwHVtHhch0GvulkXq_UmCrjISpkKVPUCZ5CgLuxjdWYLOkFXF4_y41rVe-3VDLFa91G8Q9f0LKqAZUcp0wdeU2t-8H9DYwQNvxwiu_knMqFUQq7LgBL0uFexQ8xXp2kLbOPfv9eZ5qbFMq9Xfc2FUaoevdMf6jA0Td5STysz09KhPK3Mik86hyXH73u2Zpal0IUpO4eZFl4dYG9mGwyJTm8QEuUP)

# 2. Algoritmo de raices exactas
-pseudo codigo:
------------
    variables
    r=numero del que queremos su raiz exacta
    R= raiz de r aproximado al entero mas cercano
    Si R*R=r r es un numero entero
    en otro caso
    r no es entero


-Codigo en python:
------------
    r: int(input("numero que se quiere saber su raiz exacta:"))
    R: round(sqr(r))   #round sirve para redondear el resultado de la raiz
    if R*R == r:
     print("tenemos una raiz exacta")
     else:
     print ("esta raiz no es exacta")

-Diagrama:
-------------

    [![](https://mermaid.ink/img/pako:eNptUT1PAzEM_StWpqvULowdQLQHG1PZOAaTmDYiH4eTFErb34bEL8O5K9CBSJYiv-fnZ3uvdDSk5urZxTe9Qc5w33YB5F0_uLhGttlHYLSaEtA76ozpEWazywMFHUNmZHgtBKF44pggSBhkDFAC1roPoJCJEXagCzqqlAMsGs0kpRewlRb4VPNVhqlnSrWiCpxUpTSVUUvAnnS2W_SVNBmtLqohWDbkSOQAXW1lGE0EdzJhyP2p6eh78cgCygzwC53kloNcu__6TILa9WD76jiC7TD8yh5umpt0NuSwmsk5R-a8bUIE-p8moaZK2nq0Ri6wH5Iqb8hTp-bylT2-dKoLR-FhyXG1C1rNMxeaqtIbzNRaXDP6nyQZmyPfjRcdDnv8BgX-pCc?type=png)](https://mermaid.live/edit#pako:eNptUT1PAzEM_StWpqvULowdQLQHG1PZOAaTmDYiH4eTFErb34bEL8O5K9CBSJYiv-fnZ3uvdDSk5urZxTe9Qc5w33YB5F0_uLhGttlHYLSaEtA76ozpEWazywMFHUNmZHgtBKF44pggSBhkDFAC1roPoJCJEXagCzqqlAMsGs0kpRewlRb4VPNVhqlnSrWiCpxUpTSVUUvAnnS2W_SVNBmtLqohWDbkSOQAXW1lGE0EdzJhyP2p6eh78cgCygzwC53kloNcu__6TILa9WD76jiC7TD8yh5umpt0NuSwmsk5R-a8bUIE-p8moaZK2nq0Ri6wH5Iqb8hTp-bylT2-dKoLR-FhyXG1C1rNMxeaqtIbzNRaXDP6nyQZmyPfjRcdDnv8BgX-pCc)
