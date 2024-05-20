1
# Pedir la edad del cliente al usuario
edad = int(input("Ingrese la edad del cliente: "))

# Calcular el precio de entrada según la edad
if edad < 4:
    precio_entrada = 0  # Cliente menor de 4 años entra gratis
elif 4 <= edad <= 18:
    precio_entrada = 5  # Cliente de 4 a 18 años paga 5 soles
else:
    precio_entrada = 10  # Cliente mayor de 18 años paga 10 soles

# Mostrar el precio de entrada al cliente
print(f"El precio de entrada para un cliente de {edad} años es: {precio_entrada} soles")

2
# Pedir al usuario que ingrese una palabra
palabra = input("Ingresa una palabra: ")

# Mostrar la palabra ingresada por el usuario 10 veces
for _ in range(10):
    print(palabra)
3
# Pedir al usuario un número entero positivo
numero = int(input("Ingresa un número entero positivo: "))

# Validar que el número sea positivo
if numero <= 0:
    print("Por favor, ingresa un número entero positivo.")
else:
    # Mostrar los números impares hasta el número ingresado
    impares = [str(num) for num in range(1, numero+1) if num % 2 != 0]
    resultado = ", ".join(impares)
    print(f"Los números impares hasta {numero} son: {resultado}")
4
# Pedir al usuario una palabra
palabra = input("Ingresa una palabra: ")

# Mostrar las letras de la palabra introducida empezando por la última
for i in range(len(palabra)-1, -1, -1):
    print(palabra[i])

5
# Pedir al usuario una palabra
palabra = input("Ingresa una palabra: ")

# Mostrar las letras de la palabra introducida empezando por la última
for letra in reversed(palabra):
    print(letra)
6
# Pedir al usuario un número entero
numero = int(input("Ingresa un número entero: "))

# Mostrar el triángulo rectángulo como en la imagen adjunta
for i in range(1, numero + 1):
    print("*" * i)

7
# Pedir al usuario que ingrese una frase
frase = input("Ingresa una frase: ")

# Pedir al usuario que ingrese una letra
letra = input("Ingresa una letra: ")

# Contar el número de veces que aparece la letra en la frase
contador = frase.count(letra)

# Mostrar el resultado al usuario
print(f"La letra '{letra}' aparece {contador} veces en la frase '{frase}'.")

8
# Pedir al usuario una palabra
palabra = input("Ingresa una palabra: ")

# Mostrar las letras de la palabra introducida empezando por la última
for i in range(len(palabra)-1, -1, -1):
    print(palabra[i])
9
# Pedir al usuario la cantidad de números a introducir
num_numeros = int(input("¿Cuántos números vas a introducir? "))

# Inicializar una variable para almacenar el número anterior
anterior = None

# Pedir y comparar los números ingresados
for i in range(num_numeros):
    numero = float(input(f"Ingrese el número {i+1}: "))
    
    # Verificar si el número es mayor que el anterior
    if anterior is not None and numero <= anterior:
        print(f"El número {numero} no es mayor que el anterior.")
    
    # Actualizar el número anterior con el número actual
    anterior = numero

1# Pedir al usuario que ingrese una frase
frase = input("Ingresa una frase: ")

# Pedir al usuario que ingrese una letra
letra = input("Ingresa una letra: ")

# Contar el número de veces que aparece la letra en la frase
contador = frase.count(letra)

# Mostrar el resultado al usuario
print(f"La letra '{letra}' aparece {contador} veces en la frase '{frase}'.")
11

# Pedir al usuario la cantidad de números a introducir
num_numeros = int(input("¿Cuántos números vas a introducir? "))

# Inicializar la variable de suma
suma = 0

# Pedir y sumar los números introducidos
for i in range(num_numeros):
    numero = float(input(f"Ingrese el número {i+1}: "))
    suma += numero

# Mostrar la suma de los números introducidos
print(f"La suma de los números introducidos es: {suma}")
12

# Pedir al usuario la cantidad de números a introducir
num_numeros = int(input("¿Cuántos números vas a introducir? "))

# Contador para los números negativos
contador_negativos = 0

# Pedir y contar los números introducidos que son negativos
for i in range(num_numeros):
    numero = float(input(f"Ingrese el número {i+1}: "))
    
    if numero < 0:
        contador_negativos += 1

# Mostrar la cantidad de números negativos introducidos
print(f"Ha introducido {contador_negativos} números negativos.")