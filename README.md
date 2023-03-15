# Actividad6.1
#Ejercicio1y2
'''sh
read -p "Ingresa un número entero: " numero
if [ $numero -gt 0 ]
then
  echo "El número es positivo"
else
  echo "El número no es positivo"
fi
'''

#Ejercicio3
'''sh
read -p "Ingresa un número entero: " numero
if [ $numero -eq 0 ]
then
  echo "El número es igual a cero"
else
  echo "El número no es igual a cero"
fi
'''
#Ejercicio4
'''sh
read -p "Ingresa un número entero: " numero
if [ $numero -eq 0 ]
then
  echo "El número es igual a cero"
else
  echo "El número no es igual a cero"
fi
'''
#Ejercicio5
'''sh
if [ "$#" -eq 3 ]
then
  echo "El número de parámetros es igual a 3"
else
  echo "Error: El número de parámetros no es igual a 3"
fi
'''
#Ejercicio6
'''sh
if [ "$#" -eq 2 ]
then
  suma=$(( $1 + $2 ))
  echo "La suma de $1 y $2 es: $suma"
else
  echo "Error: El número de parámetros no es igual a 2"
fi
'''
#Ejercicio7
'''sh
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
'''
#Ejercicio8
'''sh
