# Primera actividad
**Caso de Estudio: Sistema de Scooters Eléctricos**

NOMBRE: Corro Quezada Andy

MATRICULA: S25018136

**Objetivo:** Comprender la estructura de un sistema orientado a objetos identificando clases, atributos y métodos, diferenciando el concepto abstracto (Clase) de su implementación (Objeto).

## **Paso 1: Lectura del Caso de Estudio**

Lee detenidamente la siguiente descripción del requerimiento para identificar las entidades principales del sistema.

> "Se requiere diseñar la lógica para una aplicación de renta de **scooters**. En el sistema, cada **Scooter** cuenta con un número de identificación (ej. 'S-001'), un nivel de batería (del 0 al 100) y un estado lógico que indica si está disponible para usarse o no. Los scooters pueden ejecutar tres acciones: desbloquearse para iniciar un viaje, terminar su viaje, y recargar su batería al 100%.
>
> Por otro lado, la entidad **Usuario** se registra con su nombre y mantiene un saldo monetario en su cuenta. El usuario puede realizar dos acciones operativas: agregar más saldo a su cuenta y rentar un scooter específico."

## **Paso 2: Análisis y Diccionario de Clases**

Completa la siguiente estructura identificando los atributos y métodos. Recuerda que los sustantivos suelen representar Clases o Atributos, mientras que los verbos representan Métodos. Utiliza los modificadores de acceso y tipos de datos adecuados en cada línea vacía.

ENTIDAD 1

SCOOTER
ATRIBUTOS

- NUMERO DE IDENTIFICACION
- NIVEL DE BATERIA
- ESTADO LOGICO, ESTA OCUPADO O NO

METODOS

- DESBLOQUEARSE PARA INICIAR VIAJE
- TERMINAR SU VIAJE
- RECARGAR SU BATERIA AL 100

ENTIDAD 2

USUARIO

ATRIBUTOS

- NOMBRE
- SALDO MONETARIO

METODOS

- AGREGAR SALDO
- RENTAR UN SCOOTER ESPECÍFICO

### **Entidad 1: `Scooter`**

**Atributos (Acceso privado `-`):**

- `identificador : String` (identificador)
- `bateria : int` (batería)
- `disponibilidad : boolean` (estado de disponibilidad)

**Métodos (Acceso público `+`):**

- `+ iniciarViaje() : boolean` (iniciar viaje)
- `+ finalizarViaje() : void` (finalizar viaje)
- `+ cargarBateria() : void` (llenar batería)

### **Entidad 2: `Usuario`**

**Atributos (Acceso privado `-`):**

- `- nombre : String` (nombre)
- `- dinero : double` (dinero)

**Métodos (Acceso público `+`):**

- `+ agregarSaldo(monto: double) : void` (agregar saldo)
- `+ rentarScooter(scooter: Scooter) : boolean` (rentar scooter)

## **Paso 3: Diseño del Diagrama de Clases UML**

A partir de la información estructurada en el paso anterior, elabora un Diagrama de Clases formal. Asegúrate de incluir los tres bloques estándar (Nombre de la clase, Atributos y Métodos) y adjuntar la captura o imagen del diagrama resultante en tu documento.

**Entidad 1: `Scooter`**

<img width="567" height="375" alt="image" src="https://github.com/user-attachments/assets/0c9aa688-5a9e-451b-8a81-94e55f00856d" />

### **Entidad 2: `Usuario`**

<img width="1026" height="673" alt="image" src="https://github.com/user-attachments/assets/440a398f-2ae8-4af5-9464-e4e97023642c" />

## **Paso 4: Instanciación (De la Teoría a la Realidad)**

El diagrama de clases funciona como un molde estructural. A continuación, define instancias en memoria asignando valores concretos a los atributos de cada objeto para ejemplificar su estado.

**Instancia de Scooter 1**

- `id = S-301`
- `nivelBateria = 50`
- `estaDisponible = true`

**Instancia de Usuario 1**

- `nombre = Andy`
- `saldo = 135.0`

## **Paso 5: Pregunta de Análisis Lógico**

Justifica tu respuesta a la siguiente interrogante lógica basándote en los conceptos de POO estudiados:

Si la Instancia de Usuario 1 intenta ejecutar el método `rentar()` enviando como parámetro un Scooter que tiene un 15% de batería, ¿cómo debería comportarse internamente la lógica del sistema?

Primero se evaluaría un condicional donde se verifique que el usuario tenga el saldo suficiente para rentar el scooter y llamar a la función iniciar viaje que tendrá su propio funcionamiento donde verificará si tiene batería y si está disponible; dependiendo si retorna true o false, el saldo e iniciar viaje se evaluarían con un AND para restarle al saldo del usuario el costo de rentar el scooter y retornar verdadero donde sí se pudo rentar; si no se cumple con el condicional retornará falso.

## SECCION IA

Trate de resolverlo en IntelliJ por mi cuenta y me salió todo mal al querer acceder a datos privados desde otra entidad, muchos errores por practicar en frío, le pasé mi código a la IA para verificar errores y resolverlos por mi propia cuenta; al final encontré más errores por arreglar y ver de mejor manera los objetos en programación.
