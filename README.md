def saludar(nombre):
    print(f"Hola, {nombre}")
saludar("Ingeniero, Dexel Mas") 

def ejercicio1():
    print("Ejercicio 1")
    nombre = input("¿Cual es su nombre: ")
    numero = int(input("Ingrese un numero entero: "))
    for _ in range(numero):
        print(nombre)

def ejercicio2():
    print("Ejercicio 2")
    nombrecompleto = input("Ingrese su nombre completo: ")
    print(nombrecompleto.lower())
    print(nombrecompleto.upper())
    print(nombrecompleto.title())

def ejercicio3():
    print("Ejercicio 3")
    nombre = input("¿Cual es su nombre: ?")
    print(f"{nombre.upper()} tiene {len(nombre)} letras")

def ejercicio4():
    print("Ejercicio 4")
    telefono = input("Ingrese número de teléfono (+502-XXXXXXXX-XX): ")
    partes = telefono.split('-')
    if len(partes) == 3 and partes[0] == "+502":
        print(f"Número sin prefijo/extensión: {partes[1]}")
    else:
        print("Formato inválido.")

def ejercicio5():
    print("Ejercicio 5")
    frase = input("Ingrese una frase: ")
    print(frase[::-1])

def ejercicio6():
    print("Ejercicio 6")
    frase = input("Ingrese una frase: ")
    vocal = input("Ingrese una vocal: ").lower()
    if vocal in "aeiou":
        frase_modificada = frase.replace(vocal, vocal.upper())
        print(frase_modificada)
    else:
        print("No ingresó una vocal válida.")

def ejercicio7():
    print("Ejercicio 7")
    correo = input("Ingrese su correo electrónico: ")
    nombre_usuario = correo.split('@')[0]
    nuevo_correo = f"{nombre_usuario}@upana.edu.gt"
    print(f"Nuevo correo: {nuevo_correo}")

def ejercicio8():
    print("Ejercicio 8")
    precio = input("Ingrese el precio (ejemplo: 123.45): ")
    quetzales, centavos = precio.split('.')
    print(f"Quetzales: {quetzales}, Centavos: {centavos}")

def ejercicio9():
    print("Ejercicio 9")
    fecha = input("Ingrese su fecha de nacimiento (dd/mm/aaaa): ")
    dia, mes, anio = fecha.split('/')
    print(f"Día: {dia}, Mes: {mes}, Año: {anio}")

def ejercicio10():
    print("Ejercicio 10")
    productos = input("Ingrese productos separados por comas: ")
    lista_productos = [p.strip() for p in productos.split(',')]
    for producto in lista_productos:
        print(producto)

def mostrar_menu():
    print("\n=== MENÚ DE EJERCICIOS DE CADENAS ===")
    for i in range(1, 11):
        print(f"{i}. Ejercicio {i}")
   
def main():
    while True:
        mostrar_menu()
        opcion = input("Seleccione un ejercicio (1-10): ")
        if opcion == "1":
            ejercicio1()
        elif opcion == "2":
            ejercicio2()
        elif opcion == "3":
            ejercicio3()
        elif opcion == "4":
            ejercicio4()
        elif opcion == "5":
            ejercicio5()
        elif opcion == "6":
            ejercicio6()
        elif opcion == "7":
            ejercicio7()
        elif opcion == "8":
            ejercicio8()
        elif opcion == "9":
            ejercicio9()
        elif opcion == "10":
            ejercicio10()

        else:
            print("Opción inválida. Intente nuevamente.")

if __name__ == "__main__":
    main()

    
