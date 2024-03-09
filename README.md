# Reto_3
En este repositorio se desarrolla el reto 3, aunque sé que en algunas partes se debe hacer correciones :)
## Algoritmo para obtener los números primos hasta n
### Pseudocodigo
```
[variables]
n : entero
i : entero
j : entero
div: entero
inicio
  j := 2
  div := 0
  Mientras ( j <=  n) hacer
      Si 
	 i : = 2
	 Mientras (i < ((j^0.5)+1) hacer
    	    Si modulo(n,i) == 0 entonces
      	       (i es divisor de j)
      	    div: =+1
            sino
      	       (i no es divisor de j)
    	    i := i + 1
         Fin de mientras
     	Mientras (div ==2 ) hacer
     	   Si
	      mostrar ("j es numero primo")
     	   sino 
	      ("j no es primo")
   	Fin mientras
     j : =+1
   sino 
   Fin mientras
fin
```

### Diagrama de Flujo 
```mermaid
graph TD;
    A(Inicio) 
    A-->B[Número n]
    B-->Cd[j = 2]
    Cd-->Bb{¿j <= n?}
     Bb-->|No|Fin
    Bb-->|Si|E[i=2]
    E-->F{modulo j/i es cero?}
    F-->|si| G[i es divisor de j]
    G-->Ij[div=+1]-->K
    F-->|no| H[i No es divisor]
    G-->I[i=+1];H-->I
    I-->K{¿i < j^0.5 +1?}
    K-->|si|F
    K-->|no| L{div ==2}
    L-->|si|M[j es primo]
    L-->|No|N[j no es es primo]
    M-->O[j=+1]; N-->O
    O-->P{j < n}
    P-->|si|Bb
    P-->|no|Fin
    Fin[Fin]
```
## Algoritmo para hallar raíces cuadradas 
### Pseudocodigo
```
[variables]
n : entero positivo
cant : cantidad de cifras de n
a : entero
i : entero
pot : entero = 0
dif : entero = 0
mult : entero = 0
inicio
   Si (cant es par)
      a = las dos cifras de n de izquierda a derecha
      i = 1
      Mientras (i < a)
	Si (i**2 cercano o igual a "a")
	   pot = numero i
	   dif = i**2 -a
	   cant =-2
	      Mientras (cant > 0)
		dif = dif se le agraga las dos cigras siguiente de numero n
		j = 1
		mult = ((potx2) agregar cifra de j ) x j
		Si (mult cercano o igual a dif) hacer
		   pot =+ numero j
		   cant =-2
		sino (j=+1)
	      Fin mientras
	sino (i=+1)
      Fin mientras
fin
```
### Diagrama de Flujo
```mermaid
graph TD;
    A(Inicio) 
    A-->B[Número n]
    B-->D[cant= cantidad de la cifras de n ]
    D-->F{¿cant es par?}
    F-->|si|G[a = las dos primeras cifras de izquierda a derecha de n]
    F-->|No|H[Agregar agregar un cero al ultimo dijito de la izquierda]
    H-->I[cant = cant =+1]-->F
    G-->J[i = 1]
    J-->K{i < = a}-->|No|Fin
    K-->|si|M{¿i**2 cercano o == a?}
    M-->|Si|N[pot = numero i]
    N-->O[dif = i**2 - a]-->Oo[cant=-2]
    M-->|No|Ll[i =+ 1]-->M
    Oo-->P{cant > 0}-->|No|Fin
    P-->|Si|Q[dif = dif + las dos cifras siguiente de n]
    Q-->Qq[j = 1]
    Qq-->R[mult = potx2 agregar cifra j x j]
    R-->S{mult cercano o igual a dif}
    S-->|Si|T[pot =+ numero J]-->V[cant =-2]-->P
    S-->|No|U[j=+1]-->R
```
