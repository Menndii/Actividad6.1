#Actividad6.1

#Ejercicio1y2

```sh
read -p "Ingresa un número entero: " numero
if [ $numero -gt 0 ]
then
  echo "El número es positivo"
else
  echo "El número no es positivo"
fi
```

#Ejercicio3
```sh
read -p "Ingresa un número entero: " numero
if [ $numero -eq 0 ]
then
  echo "El número es igual a cero"
else
  echo "El número no es igual a cero"
fi
```

#Ejercicio4
```sh
read -p "Ingresa un número entero: " numero
if [ $numero -eq 0 ]
then
  echo "El número es igual a cero"
else
  echo "El número no es igual a cero"
fi
```

#Ejercicio5
```sh
if [ "$#" -eq 3 ]
then
  echo "El número de parámetros es igual a 3"
else
  echo "Error: El número de parámetros no es igual a 3"
fi
```

#Ejercicio6
```sh
if [ "$#" -eq 2 ]
then
  suma=$(( $1 + $2 ))
  echo "La suma de $1 y $2 es: $suma"
else
  echo "Error: El número de parámetros no es igual a 2"
fi
```

#Ejercicio7
```sh
if [ "$#" -eq 3 ]
then
  num1=$1
  num2=$2
  operacion=$3
  resultado=0

  case "$operacion" in
    "+") resultado=$((num1 + num2));;
    "-") resultado=$((num1 - num2));;
    "x") resultado=$((num1 * num2));;
    "/") resultado=$((num1 / num2));;
    *) echo "Error: El tercer parámetro debe ser uno de los siguientes símbolos: +, -, x, /"; exit 1;;
  esac

  echo "El resultado de la operación es: $resultado"
else
  echo "Error: El número de parámetros no es igual a 3"
fi
```
#Ejercicio11
```sh
for i in {1..50}; do echo "hola"; done
```
#Ejercicio12
```sh
for ((i=1; i<=10; i++))
do
  echo "Ingresa una palabra:"
  read palabra
  echo "La palabra es: $palabra"
done
```
#Ejercicio13
```sh
if [ $# -eq 0 ]; then
    echo "Debe proporcionar un número como argumento."
    exit 1
fi
n=$1
for (( i=0; i<$n; i++ )); do
    echo "hola"
done
```
#Ejercicio14
```sh
n=$1
for i in $(seq 0 $n); do
    echo $i
done
```
#Ejercicio15
```sh
import sys

n = int(sys.argv[1])
suma = 0

for i in range(1, n+1):
    suma += i

print("La suma de los números entre 1 y", n, "es:", suma)
```
#Ejercicio17
```sh
echo "Ingrese palabras. Escriba ':q' para salir."

while true; do
    read palabra
    if [ "$palabra" = ":q" ]; then
        echo "Programa finalizado."
        break
    else
        echo "La palabra ingresada es: $palabra"
    fi
done
```
#Ejercicio18
```sh
echo "Escribe palabras para guardar en un archivo. Escribe ':q' para salir."

read palabra

while [ "$palabra" != ":q" ]; do
    echo $palabra >> palabras.txt
    read palabra
done

echo "Archivo 'palabras.txt' creado con éxito."
```
#Ejercicio20
```sh
touch numeros.txt
nano numeros.txt
#Añadimos los numeros que querramos que pertenezcan al archivo
1 2 3 4 5 6 7 8 9 10
touch buscar_numero.sh
nano buscar_numero.sh


echo "Ingresa un número: "
read numero
if grep -wq $numero "numeros.txt"; then
    echo "El número $numero se encuentra en el archivo numeros.txt."
else
    echo "El número $numero no se encuentra en el archivo numeros.txt."
fi
```


