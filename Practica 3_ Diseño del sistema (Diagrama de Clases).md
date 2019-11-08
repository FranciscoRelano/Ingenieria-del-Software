# Practica 3: Diseño del sistema

![](https://www.vectorlogo.es/wp-content/uploads/2014/12/logo-vector-universidad-cordoba.jpg)

Por el grupo 36 y su integrante

Francisco Relaño Peña

# Especificación de clases

### Clase: Paciente
Esta clase sirve para determinar la entidad paciente.
|Datos:| ||
|----|---|-----|
|+ DNI     |_Date_   | Identifica a la entidad conformada por el paciente.|
|+ Nombre     |_Date_   | Contiene el nombre completo del paciente.|
|+ Domicilio    |_Date_   | Identifica la localización física del paciente.|
|+ Dirección Postal     |_String_   | Determina la localización postal del paciente según el formato _Código Postal / Localidad_.|
|+ Teléfono     |_Entero_   | Determina el número de teléfono asociado con el paciente.|
|+ Seguro     |_Booleano_   | Identificador del método de pago.|
|+ Tratamiento| _Entero_| Identifica el vector de tratamientos, y el último de ellos  que sigue. |

|Métodos||
|----|----|
|CreatePaciente() | Crea una nueva entidad paciente en el directorio. En caso de que ya exista, pide confirmación para sobreescribirla.|
|ConsultPaciente()| Accede a los datos del paciente sin tener privilegio de modificación.|
|ModificaPaciente()| Modifica los datos del paciente y los almacena en el registro.|

### Clase: Citas
Esta clase sirve para almacenar las citas del paciente.
|Datos:| ||
|----|---|-----|
|+ Fecha     |_Date_   | Identificador del método de pago.|
|+ Profesional| _Cadena de caracteres_| Identifica al doctor a cargo de la cita. |

|Métodos||
|----|----|
|Programar() | Programa automáticamente la próxima cita para una fecha seis meses posterior a la del momento actual.|
|Aplazar()| Modifica la fecha de la cita por una posterior.|
|Cancelar()| Cancela la cita en su totalidad, quedando ésta fuera del registro. |

### Clase: Tratamiento
Esta clase sirve para definir el tratamiento que sigue el paciente.
|Datos:| ||
|----|---|-----|
|+ ID Tratamiento     |_Número entero_   | Identificador del tratamiento como elemento individual.|
|+ Tipo     |_Cadena de caracteres_   | Identificador del método de pago.|
|+ Nombre     |_Cadena de caracteres_   | Nombre del tratamiento.|
|+ Posología     |_Número flotante_   | Define la dosis del tratamiento.|
|+ Fecha de Inicio     |_Date_   | Determina la fecha de inicio.|


|Métodos||
|----|----|
|AddTratamiento() | Añade nuevo elemento al vector de tratamientos y lo guarda en el registro. El elemento deberá de ser rellenado manualmente por el usuario|
|ModificaTratamiento()| Modifica el tratamiento. Incluye la opción de eliminarlo|


### Clase: Factura
Esta clase sirve para almacenar el valor de la factura del paciente.
|Datos:| ||
|----|---|-----|
|+ Coste     |_Número flotante_   | Determina la cuota total a pagar.|
Esta clase no posee funciones asociadas.

### Clase: Método de pago
Esta clase sirve para determinar cual de entre los posibles métodos de pago se ha realizado.
|Datos:| ||
|----|---|-----|
|+ Tipo     |_Cadena de caracteres_   | Identificador del método de pago.|

Esta clase no posee funciones asociadas.
### Clase: Metálico
Esta clase sirve para contener las funciones y datos asociadas con el pago en metálico.

|Datos:| ||
|----|---|-----|
|+ Total     |_Número flotante_   | Determina cantidad total pagada mediante método.|


Esta clase no posee funciones asociadas.
### Clase: Tarjeta de crédito

Esta clase sirve para contener las funciones y datos asociadas con el pago mediante tarjeta de crédito.

|Datos:| ||
|----|---|-----|
|+ ID Tarjeta     |_Cadena de caracteres_   | Identificador de la tarjeta de crédito.|
|+ Fecha |_Date_     | Fecha en la que se realizó la transacción.|

|Métodos||
|----|----|
|confirmatarjeta() |Valida la identificación de la tarjeta.|

### Clase: Cheque
Esta clase sirve para contener las funciones y datos asociadas con el pago mediante cheque.

|Datos:| ||
|----|---|-----|
|+ ID Banco    |_Cadena de caracteres_   | Identificador de la entidad bancaria.|
|+ Nombre |_Cadena de caracteres_     | Identificador del firmante del cheque.|

Esta clase no posee funciones asociadas.




# Diagrama de clases
![](https://i.imgur.com/P88lFzd.pngg)
