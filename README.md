# Primera actividad
**Caso de estudio: Sistema de scooters eléctricos**

NOMBRE: Corro Quezada Andy

MATRÍCULA: S25018136

**Objetivo:** Comprender la estructura de un sistema orientado a objetos identificando clases, atributos y métodos, diferenciando el concepto abstracto (Clase) de su implementación (Objeto).

## **Paso 1: Lectura del caso de estudio**

Lee detenidamente la siguiente descripción del requerimiento para identificar las entidades principales del sistema.

> "Se requiere diseñar la lógica para una aplicación de renta de **scooters**. En el sistema, cada **Scooter** cuenta con un número de identificación (ej. 'S-001'), un nivel de batería (del 0 al 100) y un estado lógico que indica si está disponible para usarse o no. Los scooters pueden ejecutar tres acciones: desbloquearse para iniciar un viaje, terminar su viaje, y recargar su batería al 100%.
>
> Por otro lado, la entidad **Usuario** se registra con su nombre y mantiene un saldo monetario en su cuenta. El usuario puede realizar dos acciones operativas: agregar más saldo a su cuenta y rentar un scooter específico."

## **Paso 2: Análisis y diccionario de clases**

Completa la siguiente estructura identificando los atributos y métodos. Recuerda que los sustantivos suelen representar Clases o Atributos, mientras que los verbos representan Métodos. Utiliza los modificadores de acceso y tipos de datos adecuados en cada línea vacía.

ENTIDAD 1

SCOOTER
ATRIBUTOS

- NÚMERO DE IDENTIFICACIÓN
- NIVEL DE BATERÍA
- ESTADO LÓGICO, ESTÁ OCUPADO O NO

MÉTODOS

- DESBLOQUEARSE PARA INICIAR VIAJE
- TERMINAR SU VIAJE
- RECARGAR SU BATERÍA AL 100

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

## **Paso 3: Diseño del diagrama de clases UML**

A partir de la información estructurada en el paso anterior, elabora un Diagrama de Clases formal. Asegúrate de incluir los tres bloques estándar (Nombre de la clase, Atributos y Métodos) y adjuntar la captura o imagen del diagrama resultante en tu documento.

### **Entidad 1: `Scooter`**

<img width="568" height="438" alt="image" src="https://github.com/user-attachments/assets/7601de56-d7e6-41b4-a1d0-f0725766b3ad" />

### **Entidad 2: `Usuario`**

<img width="570" height="376" alt="image" src="https://github.com/user-attachments/assets/ed71b66c-7e7f-4c80-a185-7be645fc32b9" />

## **Diagrama completo**

<img width="1518" height="600" alt="image" src="https://github.com/user-attachments/assets/0935c915-56d9-4f9d-89b4-d8adc5c757a1" />

## **Paso 4: Instanciación (de la teoría a la realidad)**

El diagrama de clases funciona como un molde estructural. A continuación, define instancias en memoria asignando valores concretos a los atributos de cada objeto para ejemplificar su estado.

**Instancia de Scooter 1**

- `id = S-301`
- `nivelBateria = 50`
- `estaDisponible = true`

**Instancia de Usuario 1**

- `nombre = Andy`
- `saldo = 135.0`

## **Paso 5: Pregunta de análisis lógico**

Justifica tu respuesta a la siguiente interrogante lógica basándote en los conceptos de POO estudiados:

Si la Instancia de Usuario 1 intenta ejecutar el método `rentar()` enviando como parámetro un Scooter que tiene un 15% de batería, ¿cómo debería comportarse internamente la lógica del sistema?

Primero se evaluaría un condicional donde se verifique que el usuario tenga el saldo suficiente para rentar el scooter y llamar a la función iniciar viaje que tendrá su propio funcionamiento donde verificará si tiene batería y si está disponible; dependiendo si retorna true o false, el saldo e iniciar viaje se evaluarían con un AND para restarle al saldo del usuario el costo de rentar el scooter y retornar verdadero donde sí se pudo rentar; si no se cumple con el condicional retornará falso.

## SECCIÓN IA

Durante la realización de esta actividad usé la Inteligencia Artificial como soporte teórico de mis respuestas y diseñador gráfico de mis diagramas UML. Con su ayuda, pude precisar mis explicaciones y dar una mejor presentación general a la actividad.
