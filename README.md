def main():
    try:
        # Solicitar al usuario el año actual y un año cualquiera
        anio_actual = int(input("Ingresa el año actual: "))
        anio_cualquiera = int(input("Ingresa un año cualquiera: "))

        # Validar si se ha ingresado dos veces el mismo año
        if anio_actual == anio_cualquiera:
            print("¡Has ingresado el mismo año dos veces!")
            return

        # Calcular la diferencia de años
        diferencia_anios = abs(anio_actual - anio_cualquiera)

        # Mostrar el resultado
        if anio_actual < anio_cualquiera:
            print(f"Faltan {diferencia_anios} años para llegar al año {anio_cualquiera}.")
        else:
            if diferencia_anios == 1:
                print(f"Ha pasado 1 año desde el año {anio_cualquiera}.")
            else:
                print(f"Han pasado {diferencia_anios} años desde el año {anio_cualquiera}.")

    except ValueError:
        print("Por favor, ingresa un año válido (número entero).")

if __name__ == "__main__":
    main()
