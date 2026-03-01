# Testing con Junit

Este es un ejemplo sencillo de pruebas unitarias usando Junit 5

Observa que este proyecto no tiene ninguna clase con el método `main`, no nos hace fatal. Además, tampoco tiene ningún `scanner` ni ningún `print`.

Haz un fork de este proyecto en tu repositorio de Github y contesta a las siguientes preguntas:

1. ¿Qué sentido puede tener este proyecto y para que lo podrías usar?
La razón por la que lo usamos es para detectar fallos con la ayuda de los test para poder evitar integrar código roto o mal funcionamiento de este. Lo que logramos también es poder documentar las pruebas para qeu que quede registrado su funcionamiento.
2. Revisa las pruebas de la suma y comenta lo que te parezca de interés
El proyecto está dividido en dos partes:
una carpeta donde está la clase Calculadora con los métodos (sumar, restar, etc.) y otra carpeta donde están las pruebas (CalculadoraTest). Esto está bien porque separa el código que hace las operaciones del código que las comprueba.
3. Realiza un estudio de caja negra de la división e implementa las pruebas en junit: Se realizará en markdown.

## 3. Caja negra de la división (dividir(a,b)) + pruebas

### Entradas
- `a`: número entero
- `b`: número entero

### Intervalos 
Para ambos valores:
- (-, 0) → negativos
- {0} → cero
- (0, +∞) → positivos

### Comportamiento esperado
- Si `b ≠ 0` → devuelve `a / b` (división entera)
- Si `b = 0` → lanza `OperacionNoValidaException`

### Valores elegidos 
- Para `a`: `4`, `-4`, `0`
- Para `b`: `2`, `-2`, `0`

### Casos de prueba
| Caso | a  | b  | Resultado esperado |
|------|----|----|-------------------|
| 1 | 4  | 2  | 2 |
| 2 | -4 | 2  | -2 |
| 3 | 4  | -2 | -2 |
| 4 | 0  | 2  | 0 |
| 5 | 4  | 0  | Excepción |

## Instrucciones

El alumno deberá hacer un fork de este proyecto e implementar la solución solicitada (preguntas y código).

>Se deberá utilizar este fichero, y los artefactos de código del proyecto, para resolver el ejercicio.


**Si no se puede acceder al repositorio la evaluación del ejercicio será de 0. No se evaluarán entregas modificadas/entregadas fuera del plazo establecido en la tarea**