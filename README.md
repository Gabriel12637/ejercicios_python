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


##Desarrolla un programa en Python que permita gestionar una lista de tareas pendientes. El programa
# debe cumplir con los siguientes requisitos:
#
##- Debe permitir agregar nuevas tareas a la lista.
##- Debe permitir marcar tareas como completadas, lo que las eliminará de la lista de tareas pendientes.
##- Debe mostrar la lista actual de tareas pendientes.
##- Debe proporcionar un menú interactivo que permita al usuario seleccionar entre las opciones anteriores 
# y salir del programa.
##El menú debe presentar las siguientes opciones:
#
##- Agregar tarea
##- Marcar tarea como completada
##- Mostrar tareas
##- Salir

# Lista de tareas pendientes
tareas = []

# Menú interactivo
while True:
    print("\nMenú de opciones:")
    print("1. Agregar tarea")
    print("2. Marcar tarea como completada")
    print("3. Mostrar tareas")
    print("4. Salir")

    opcion = input("Seleccione una opción: ")

    if opcion == "1":
        tareas.append(input("Ingrese la nueva tarea: "))
        print("Tarea agregada exitosamente.")
    elif opcion == "2":
        if tareas:
            print("Tareas pendientes:")
            for i, tarea in enumerate(tareas):
                print(f"{i + 1}. {tarea}")
            num_tarea = int(input("Ingrese el número de la tarea completada: "))
            if 1 <= num_tarea <= len(tareas):
                tarea_completada = tareas.pop(num_tarea - 1)
                print(f"Tarea '{tarea_completada}' marcada como completada.")
            else:
                print("Número de tarea inválido.")
        else:
            print("No hay tareas pendientes.")
    elif opcion == "3":
        if tareas:
            print("Tareas pendientes:")
            for i, tarea in enumerate(tareas):
                print(f"{i + 1}. {tarea}")
        else:
            print("No hay tareas pendientes.")
    elif opcion == "4":
        print("¡Gracias por utilizar la lista de tareas pendientes!")
        break
    else:
        print("Opción no válida. Inténtelo de nuevo.")

#*Ejercicio Diecisiete*
##Crea un programa en Python que simule el funcionamiento de un cajero automático. El programa debe permitir
# al usuario realizar las siguientes operaciones:
#
##- Verificar el saldo de su cuenta.
##- Depositar dinero en su cuenta.
##- Retirar dinero de su cuenta.
##- Salir del programa.
##El programa debe iniciar con un saldo inicial predeterminado y mostrar un menú con las siguientes opciones:
#
##- Verificar saldo
##- Depositar dinero
##- Retirar dinero
##- Salir

# Saldo inicial del cajero automático
saldo = 1000

# Menú interactivo del cajero automático
while True:
    print("\nMenú de opciones:")
    print("1. Verificar saldo")
    print("2. Depositar dinero")
    print("3. Retirar dinero")
    print("4. Salir")

    opcion = input("Seleccione una opción: ")

    if opcion == "1":
        print(f"Su saldo actual es: ${saldo}")
    elif opcion == "2":
        monto_deposito = float(input("Ingrese la cantidad a depositar: $"))
        saldo += monto_deposito
        print(f"Se han depositado ${monto_deposito}. Saldo actual: ${saldo}")
    elif opcion == "3":
        monto_retiro = float(input("Ingrese la cantidad a retirar: $"))
        if monto_retiro <= saldo:
            saldo -= monto_retiro
            print(f"Ha retirado ${monto_retiro}. Saldo actual: ${saldo}")
        else:
            print("Saldo insuficiente.")
    elif opcion == "4":
        print("¡Gracias por utilizar el cajero automático!")
        break
    else:
        print("Opción no válida. Inténtelo de nuevo.")

#*Ejercicio Dieciocho*
##Escriba un programa que solicite una contraseña (el texto de la contraseña no es importante) y la vuelva a 
# solicitar hasta que las dos contraseñas coincidan.

# Solicitar y validar la contraseña
while True:
    contraseña1 = input("Ingrese la contraseña: ")
    contraseña2 = input("Confirme la contraseña: ")

    if contraseña1 == contraseña2:
        print("Contraseña confirmada. ¡Contraseñas coinciden!")
        break
    else:
        print("Las contraseñas no coinciden. Inténtelo de nuevo.")
