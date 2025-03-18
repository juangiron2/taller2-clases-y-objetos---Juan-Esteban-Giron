class Cuenta:
    def __init__(self, numero_cuenta, doc_identidad, nombre, saldo):
        self.__numero_cuenta = numero_cuenta  # Atributo privado
        self.doc_identidad = doc_identidad
        self.nombre = nombre
        self.saldo = saldo
    
    @property
    #Los properties son una herramienta de Python para implementar la encapsulación y proporcionar una interfaz limpia 
    # y controlada para acceder y modificar los atributos de una clase.
    
    def numero_cuenta(self):
        return self.__numero_cuenta
    
    def depositar_dinero(self, monto):
        retencion = monto * 0.19
        monto_final = monto - retencion
        self.saldo += monto_final
        return f"Se depositaron {monto_final:.2f} después de la retención del 19%. Nuevo saldo: {self.saldo:.2f}"
    
    def retirar_dinero(self, monto):
        if self.saldo >= monto:
            self.saldo -= monto
            return f"Se retiraron {monto:.2f}. Nuevo saldo: {self.saldo:.2f}"
        else:
            return "Fondos insuficientes para realizar el retiro."
    
    def mostrar_datos(self):
        return f"Número de cuenta: {self.__numero_cuenta}\n" \
               f"Documento de Identidad: {self.doc_identidad}\n" \
               f"Nombre: {self.nombre}\n" \
               f"Saldo: {self.saldo:.2f}"
