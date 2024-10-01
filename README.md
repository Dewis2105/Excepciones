# Excepciones
#excepciones
#Fabricio Renzo Chicmana Vincula
def leer_numero_natural():
    """
    Función que solicita al usuario que ingrese un número natural.
    Si el ingreso es inválido, se vuelve a pedir hasta que sea correcto.
    """
    while True:
        try:
            numero = int(input("Ingrese un número natural: "))
            if numero <= 0:
                raise ValueError("El número debe ser un entero positivo.")
            return numero
        except ValueError as e:
            print(f"Error: {e}. Por favor, ingrese un número válido.")

def calcular_divisores(numero):
    """
    Función que calcula y devuelve una lista con los divisores del número ingresado.
    """
    divisores = [i for i in range(1, numero + 1) if numero % i == 0]
    return divisores

def main():
    """
    Función principal que orquesta el flujo de la aplicación.
    """
    # Leer número natural con validación
    numero = leer_numero_natural()
    
    # Calcular divisores
    divisores = calcular_divisores(numero)
    
    # Mostrar divisores
    print(f"Los divisores de {numero} son: {divisores}")

if __name__ == "__main__":
    main()
