from cuentamodelo import Cuenta

def menu(cuentaClientes):
    while True:
        print("\n1. Crear nueva cuenta")
        print("2. Depositar dinero")
        print("3. Retirar dinero")
        print("4. Mostrar datos de cuenta")
        print("5. Salir")
        opcion = input("Seleccione una opción: ")

        if opcion == '1':
            numero_cuenta = int(input("Ingrese el número de cuenta: "))
            doc_identidad = int(input("Ingrese el Documento de Identidad: "))
            nombre = input("Ingrese el nombre del cliente: ")
            saldo = float(input("Ingrese el saldo inicial: "))
            cuenta = Cuenta(numero_cuenta, doc_identidad, nombre, saldo)
            cuentaClientes.append(cuenta)
            print("Cuenta creada con éxito.")
        
        elif opcion == '2':
            num_cuenta = int(input("Ingrese el número de cuenta: "))
            cuenta = next((c for c in cuentaClientes if c.numero_cuenta == num_cuenta), None)
            if cuenta:
                monto = float(input("Ingrese el monto a depositar: "))
                print(cuenta.depositar_dinero(monto))
            else:
                print("Cuenta no encontrada.")
        
        elif opcion == '3':
            num_cuenta = int(input("Ingrese el número de cuenta: "))
            cuenta = next((c for c in cuentaClientes if c.numero_cuenta == num_cuenta), None)
            if cuenta:
                monto = float(input("Ingrese el monto a retirar: "))
                print(cuenta.retirar_dinero(monto))
            else:
                print("Cuenta no encontrada.")
        
        elif opcion == '4':
            num_cuenta = int(input("Ingrese el número de cuenta: "))
            cuenta = next((c for c in cuentaClientes if c.numero_cuenta == num_cuenta), None)
            if cuenta:
                print(cuenta.mostrar_datos())
            else:
                print("Cuenta no encontrada.")
        
        elif opcion == '5':
            print("Saliendo del programa...")
            break
        else:
            print("Opción inválida. Intente de nuevo.")
