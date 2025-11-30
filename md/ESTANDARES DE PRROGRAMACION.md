UNIVERSIDAD PRIVADA DE TACNA
FACULTAD DE INGENIERÍA
Escuela Profesional de Ingeniería de Sistemas
Plataforma Móvil de Exámenes de Simulacro de
Exámenes de Certificación de Inglés “SimulApp”
Curso: Patrones de Software
Docente: Mag. Patrick Cuadros Quiroga
Integrantes:
Cabrera Catari, Camila Fernanda (2021069824)
Melendez Huarachi, Gabriel (2021070311)
Tacna – Perú
2025
SISTEMA SIMULAPP (^) Versión: 1.
Documento de Estándares de Programación

Plataforma Móvil de Exámenes de Simulacro de
Exámenes de Certificación de Inglés “SimulApp”
Versión {1.2}
Universidad Privada de Tacna Pág. 4 de
SISTEMA SIMULAPP (^) Versión 1.
Documento de Estándares de Programación
Historia de Revisión
Historial de revisiones
Íte
m
Fecha Versió
n
Descripción Equipo
1 29/11/2025 1.2 Versión 1.2. GFMH
Curso Patrones de Software Página 3 de 12

Documento de Estándares de Programación
SISTEMA SIMULAPP Versión: 1.
OBJETIVO Tabla de Contenidos
DECLARACIÓN DE VARIABLES
2.1 Descripción de la Variable.
2.2 Variables de Tipo Arreglo
Definición de Controles
3.1 Tipo de datos
3.2 Prefijo para el Control
3.3 Nombre descriptivo del Control
3.4 Declaración de variables, atributos y objetos
3.5 Declaración de clases
3.6 Declaración de métodos
3.7 Declaración de funciones
3.8 Control de versiones de código fuente
Clases.
Métodos, Procedimientos y Funciones definidos por el Usuario.
Beneficios
Conclusiones
Universidad Privada de Tacna Pág. 4 de
SISTEMA SIMULAPP (^) Versión 1.
Documento de Estándares de Programación

Estándares de Programación
1. OBJETIVO

Reglamentar la forma en que se implementará el código fuente del proyecto, pasando, por las
variables, controles, clases, métodos, ficheros, archivos y todo aquello que esté implicado en el
código,

Mejorar y uniformizar a través de las reglas que se proponen, el estilo de programación que tiene
cada programador.

Los nombres de variables serán mnemotécnicos con lo que se podrá saber el tipo de dato de
cada variable con sólo ver el nombre de la variable.
Los nombres de variables serán sugestivos, de tal forma que se podrá saber el uso y
finalidad de dicha variable o función fácilmente con solo ver el nombre de la variable.
La decisión de poner un nombre a una variable o función será mecánica y automática, puesto
que seguirá las reglas definidas por nuestro estándar.
Permite el uso de herramientas automáticas de verificación de nomenclaturas.
Por tanto, se seguirán dichos patrones para un entendimiento legible del código y para facilitar el
mantenimiento del mismo.

Curso Patrones de Software Página 5 de 12

SISTEMA SIMULAPP Versión: 1.
Documento de Estándares de Programación

2. DECLARACIÓN DE VARIABLES

Se propone que la declaración de las variables, se ajusten al motivo para la que se requieran. El
mnemotécnico definido se establece tomando en consideración principalmente lo siguiente:
▪ La longitud debe ser lo más recomendable posible. No debe ser tan grande de tal forma que
el programador tenga la facilidad de manejo sobre la variable y ni tan corta que no pueda
describirse claramente. Para el caso establecemos una longitud máxima de variable de 16
caracteres.
▪ Alcance de la variable
A medida que aumenta el tamaño del proyecto, también aumenta la utilidad de reconocer
rápidamente el alcance de las variables. Esto se consigue al escribir un prefijo de alcance de
una letra delante del tipo de prefijo propio, sin aumentar demasiado la longitud del nombre de
las variables.
▪ El tipo de dato al que pertenece la variable.
Por lo tanto la estructura de la variable es como sigue:
Estructura Descripción de la Variable
LONGITUD.
MAX. ^1 ^16 ^
FORMATO
Minúscula la primera parte y luego la
segunda con Mayúsculas
EJEMPLO numCuenta
Siendo el nombre que identifica a la variable: numCuenta

Universidad Privada de Tacna Pág. 6 de 12

Alcance Prefijo Ejemplo
Clase lógica cls clsUsuario
Entidad/modelo mdl mdlProducto
Negocio srv srvUsuario
Presentación (pantallas) scr scrLogin
Privado _var _cantidadVenta
SISTEMA SIMULAPP (^) Versión 1.
Documento de Estándares de Programación
2.1 Descripción de la Variable.
Las variables deben tener nombres descriptivos que indiquen claramente su propósito,
evitando abreviaturas oscuras.
Formato (Dart/Flutter): Se utilizará lowerCamelCase.
Formato (Python/API): Se utilizará snake_case.
Ejemplos del proyecto:
● Correcto: imageUrl, fechaEscaneo, tipoEnfermedad.
● Incorrecto: x, f_esc, temp1.
2.2 Variables de Tipo Arreglo
En el caso de las definiciones de arreglos de elementos se declarará la variable con el prefijo
de “lista”, el cual nos dará entender que se trata de una variable del tipo arreglo la cual
contendrá de cero a mas datos, según el tamaño declarado.
Ejemplos:
● escaneos: Para la lista de documentos de escaneos.
● supportedFormats: Para la lista de formatos de imagen permitidos (['image/jpg',
'image/png']).
● enfermedades: Lista de strings con nombres de patologías

3. inición de Controles

Para poder determinar el nombre de un control dentro de cualquier aplicación de tipo visual,
se procede a identificar el tipo al cual pertenece y la función que cumple dentro de la
aplicación.
3.1 Tipo de datos

Curso Patrones de Software Página 7 de 12

Tipo de
variable
Mnemónico Descripción
Byte by Entero de 8 bits sin signo.
Integer in Entero de 32 bits con signo.
Char ch Un carácter UNICODE de 16 bits
String st Cadena de caracteres
Date dt Formato de fecha/hora
Boolean bl Valor lógico: verdadero y falso
Float fl Coma flotantes, 11-12 dígitos significativos.
Double db Coma flotante, 64 bits (15-16 dígitos significativos)
Object ob Objeto genérico
SISTEMA SIMULAPP (^) Versión: 1.
Documento de Estándares de Programación
3.2 Prefijo para el Control
En Flutter, los identificadores de widgets deben reflejar su tipo y función. Aunque Flutter no
usa prefijos húngaros estrictos, se recomienda sufijar el nombre con el tipo de Widget para
claridad en el árbol de widgets.
● Sufijos recomendados: ...Button, ...Page, ...Screen, ...Dialog.
● Ejemplos en Arquitectura:
○ RegisterPage: Para la pantalla de registro.
○ HistorialPage: Para la pantalla de visualización de historial.
○ UIFotoScreen: Para la pantalla de captura.
3.3 Nombre descriptivo del Control
Formado por la descripción de la función que lleva a cabo el control, esta debe ser descrita
en forma específica y clara.
3.4 Declaración de variables, atributos y objetos

Se debe declarar una variable por línea.
Título Descripción
Sintaxis [TipoVariable] [Nombre de la Variable]
Descripción Todas las variables o atributo tendrán una longitud máxima de 30
caracteres.
El nombre de la variable puede incluir más de un sustantivo los
cuales se escribirán juntos.
Si se tuvieran variables que puedan tomar nombres iguales, se le
agregará un número asociado (si está dentro de un mismo método
será correlativo).
Observaciones En la declaración de variables o atributos no se deberá utilizar
caracteres como:
● Letra Ñ o ñ.
● Caracteres especiales ¡, ^, #, $, %, &, /, (, ), ¿, ‘, +, -, *, {, },
[, ].
● Caracteres tildados: á, é, í, ó, ú.
Ejemplo Public String nombre
Indica una variable o atributo que guardará un nombre.
Universidad Privada de Tacna Pág. 8 de 12

Tipo de
control
Prefijo Ejemplo
Label lbl lblNombre
TextBox txt txtApellido
Button btn btnLogin
RadioButton rdo rdoSeleccion
CheckBox chk chkRuta
DropDownList cmb cmbDocumentos
SISTEMA SIMULAPP (^) Versión 1.
Documento de Estándares de Programación
3.5 Declaración de clases
Título Descripción
Sintaxis [Tipo] Class [Nombre de Clase]
Descripción El nombre de las clases tendrá una longitud máxima de 30
caracteres y las primeras letras de todas las palabras estarán en
mayúsculas. Tipo se refiere a si la clase será: Private, Public o
Protected.
Observaciones En la declaración de clases no se deberá utilizar caracteres como:
● Letra Ñ o ñ.
● Caracteres especiales ¡, ^, #, $, %, &, /, (, ), ¿, ‘, +, -, *, {, },
[, ].
● Caracteres tildados: á, é, í, ó, ú.
Ejemplo Private Class Empleado
Indica una clase Empleado
3.6 Declaración de métodos
Título Descripción
Sintaxis nombreProcedim[(ListaParámetros)]
Descripción El nombre del método constará hasta de 25 caracteres.
La primera letra de la primera palabra del nombre será escrita en
minúscula y las siguientes palabras empezarán con letra
mayúscula.
Observaciones En la declaración de métodos no se deberá utilizar caracteres
como:
● Letra Ñ o ñ.
● Caracteres especiales ¡, ^, #, $, %, &, /, (, ), ¿, ‘, +, -, *, {, },
[, ], _.
● Caracteres tildados: á, é, í, ó, ú.
Ejemplo Protected calcularSueldo(String empleado)
Indica un método calcularSueldo que recibe una variable por valor
de tipo string al ámbito de la clase
3.7 Declaración de funciones
Título Descripción
Sintaxis [TipoDato] nombreFuncion[(ListaParámetros)]
Descripción El nombre del objeto constará hasta de 25 caracteres, no es
necesario colocar un nombre que indique la clase a la cual
pertenece.
La primera letra de la primera palabra del nombre será escrita
en mayúsculas
El tipo de dato de retorno se coloca al final y será obligatorio
colocarlo.
Observaciones En la declaración de objetos no se deberá utilizar caracteres
como:
● Letra Ñ o ñ.
● Caracteres especiales ¡, ^, #, $, %, &, /, (, ), ¿, ‘, +, -,
*, {, }, [, ], _.
● Caracteres tildados: á, é, í, ó, ú.
Ejemplo Public int sumar(int A, int B)
Indica una función que suma dos variables enteras
Curso Patrones de Software Página 9 de 12

SISTEMA SIMULAPP (^) Versión: 1.
Documento de Estándares de Programación
3.8 Control de versiones de código fuente
Cada modificación realizada será guardada de la forma:
3.9 Controles ADO.NET
Objetos de ADO.NET Aunque hay miles de objetos disponibles como parte de .NET, es
probable que se use ADO.NET como parte de las aplicaciones, por lo tanto algunos
estándares para nombrar los objetos de ADO.NET más comunes. A continuación, se listan
los prefijos que se utiliza:
Ejemplos: de declaración de
los objetos ADO.net

drEmps As
New SqlDataReader()
drCust As New SqlDataReader()
dsEmps As DataSet
dsCust As DataSet
4. Clases.
El nombre de las clases debe ser auto descriptivo de manera que no se requiera, en lo posible,
entrar al código de la función para saber qué es lo que realiza.
El estándar para nombres de clases es usar iniciar con las siglas cls, la cual debe estar escrita
en minúscula seguido del nombre que identifica la clase, la primera letra del nombre debe
iniciar con mayúscula
▪ Ejemplos: clsCuenta, clsEmpleado, clsFactura
Universidad Privada de Tacna Pág. 10 de 12

Título Descripción
Formato [NOMBRE DOCUMENTO][ _ ][FECHA][ _ ][HORA] donde y la
fecha estará en formato yyyymmdd y la hora en formato HHMM.
Descripción Se generarán archivos con las siguientes extensiones:.zip o .rar.
Por ejemplo: WSTENNIS_20070421_2056.zip
Componente Prefijo
DataSet Ds
DataTable Dt
DataView Dv
DataRow Drw
Connection* Cnn
Command* Cmd
DataAdapter* Da
CommandBuilder* Bld
DataReader* Dr
SISTEMA SIMULAPP (^) Versión 1.
Documento de Estándares de Programación
Nota:
▪ No se hará uso de los caracteres: Espacio en blanco " ", Caracter de subrayado "_".
Tk tkinter
Label Da atributos al texto
Entry Permite almacenar un grupo de datos
Button Permite dar caracteristicas y funcionalidades al
botón

5. Métodos, Procedimientos y Funciones definidos por el Usuario.

El nombre de las funciones y procedimientos debe ser auto descriptivo de manera que no se
requiera, en lo posible, entrar al código de la función para saber qué es lo que realiza.
verbo-Sustantivo
El estándar para nombres de procedimiento es usar un Verbo que describa la acción realizada
seguida por un sustantivo (objeto sobre el cual actúa). Se recomienda:
▪ Usar un nombre que represente una acción y un objeto. El nombre del procedimiento debe
indicar qué hace el procedimiento a... o qué hace el procedimiento con....
▪ El verbo debe estar en infinitivo.
▪ Ser consistente en el orden de las palabras. Si se va a usar verboNombre , siempre usar
verboNombre.
▪ Ser consistente en los verbos y sustantivos usados. Por ejemplo, si tiene un procedimiento
asignarNombre , en vez de colocarNombre.
▪ Para la acción modificar cuentas del cliente se define:
modificar Cuenta
Verbo: modificar
Sustantivo: Cuenta
Nota:
▪ No se hará uso de los caracteres: Espacio en blanco " ", Carácter de subrayado "_".
▪ La nomenclatura de argumentos o parámetros pasados a los procedimientos/funciones
así como para valores devueltos por funciones sigue las mismas convenciones que la
nomenclatura para variables.
calcular() Función que se encarga de procesar los datos
(altura, peso) y devolver el resultado (IMC)
Altura Texto que indica al usuario que debe introducir
su altura.
Peso Texto que indica al usuario que debe introducir
su peso.
Curso Patrones de Software Página 11 de 12

SISTEMA SIMULAPP (^) Versión: 1.
Documento de Estándares de Programación
Historial Texto que indica el historial de resultados
obtenidos.
Boton Botón que de ser presionado arroja los
resultados de los datos introducidos.

6. Beneficios

● La documentación hace más legible un programa.
● Al documentar bien un programa desde un principio se evita que para cada modificación
deba estudiarse profundamente el funcionamiento del programa, redescubriendo todo lo
no documentado, con la ventaja adicional de que generalmente quién modifica el
programa no es siempre quién lo escribió.
● Facilita la reutilización de módulos y rutinas desde cualquier otro programa o el mismo.
● Ayuda a determinar cuándo debe ser reescrito un código. Si existen problemas para
explicar el código con un comentario, probablemente el código esté mal escrito.
7. Conclusiones

● Una buena programación e implementación legible, solo se logra usando y llevando de la
mano un buen estándar o patrón de programación.
● Es muy importante que el programador tenga un conocimiento previo del estándar o en
su defecto que lea el documento para prever diferencias.
● Al documentar se obtienen dos cosas fundamentales, un documento legible y segundo
una buena base para los futuros desarrollos de mantenimiento del código.
Universidad Privada de Tacna Pág. 12 de 12