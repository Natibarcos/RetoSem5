def main():
    try:
        # Solicitar al usuario el año actual y un año cualquiera
        año_actual = int(input("Ingresa el año actual: "))
        año_cualquiera = int(input("Ingresa un año cualquiera: "))

        # Validar si se ha ingresado dos veces el mismo año
        if año_actual == año_cualquiera:
            print("¡Has ingresado el mismo año dos veces!")
            return

        # Calcular la diferencia de años
        diferencia_años = abs(año_actual - año_cualquiera)

        # Mostrar el resultado
        if año_actual < año_cualquiera:
            print(f"Faltan {diferencia_años} años para llegar al año {año_cualquiera}.")
        else:
            if diferencia_años == 1:
                print(f"Ha pasado 1 año desde el año {año_cualquiera}.")
            else:
                print(f"Han pasado {diferencia_años} años desde el año {año_cualquiera}.")

    except ValueError:
        print("Por favor, ingresa un año válido (número entero).")

if __name__ == "__main__":
    main()
