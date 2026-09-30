# Promedio-Calificaciones-
# 🎓 Ejercicio 2: Control de Notas de Estudiantes
**Autor:** Cristian Gómez T.  
**Materia:** Programación / Estructuras de Datos  

---

## 📋 1. Análisis del Algoritmo

Este programa calcula el promedio ponderado de tres notas enteras y determina si un estudiante aprueba o reprueba la asignatura en base a una condición mínima.

### Componentes del Sistema:
*   **Entradas:** 
    *   `n1`, `n2`, `n3`: Tres números enteros que representan las calificaciones individuales.
*   **Proceso:**
    1.  Calcular la media aritmética de las notas:  
        \[\text{promedio} = \frac{n1 + n2 + n3}{3}\]
    2.  Evaluar el rendimiento mediante una estructura condicional doble (`if-else`). El estudiante requiere una nota mínima de **7.0**.
*   **Salidas:**
    *   El valor numérico del promedio final.
    *   La cadena de texto con el `Estado` ("El estudiante aprueba" o "El estudiante reprueba").

---

## 💻 2. Pseudocódigo

```text
Algoritmo DeterminarEstadoEstudiante
    // Declaración de variables
    Definir n1, n2, n3 Como Enteros
    Definir promedio Como Real
    Definir estado Como Cadena

    // Entrada de datos
    Escribir "Ingrese la primera nota (n1):"
    Leer n1
    Escribir "Ingrese la segunda nota (n2):"
    Leer n2
    Escribir "Ingrese la tercera nota (n3):"
    Leer n3

    // Proceso: Cálculo del promedio
    promedio <- (n1 + n2 + n3) / 3

    // Proceso: Evaluación de la condición
    Si promedio >= 7 Entonces
        estado <- "El estudiante aprueba"
    Sino
        estado <- "El estudiante reprueba"
    FinSi

    // Salidas
    Escribir "El promedio es: ", promedio
    Escribir "Se encuentra en estado: ", estado
FinAlgoritmo
```

---

## ☕ 3. Código Fuente en Java

A continuación se presenta la implementación limpia en **Java**, utilizando la clase `Scanner` para capturar los datos desde la consola:

```java
import java.util.Scanner;

public class ControlNotas {
    public static void main(String[] args) {
        // Creación del objeto Scanner para lectura de datos
        Scanner teclado = new Scanner(System.in);
        
        // 1. Declaración de variables
        int n1, n2, n3;
        double promedio;
        String estado;
        
        System.out.println("=== SISTEMA DE CALIFICACIONES ===");
        
        // 2. Entrada de datos
        System.out.print("Ingrese la primera nota (n1): ");
        n1 = teclado.nextInt();
        
        System.out.print("Ingrese la segunda nota (n2): ");
        n2 = teclado.nextInt();
        
        System.out.print("Ingrese la tercera nota (n3): ");
        n3 = teclado.nextInt();
        
        // 3. Proceso: Cálculo del promedio
        promedio = (n1 + n2 + n3) / 3.0; // Se divide por 3.0 para mantener los decimales
        
        // 4. Proceso: Condicional
        if (promedio >= 7.0) {
            estado = "El estudiante aprueba";
        } else {
            estado = "El estudiante reprueba";
        }
        
        // 5. Salidas del sistema
        System.out.println("\n=== RESULTADOS ===");
        System.out.printf("El promedio es: %.2f\n", promedio);
        System.out.println("Se encuentra en estado: " + estado);
        
        // Cerrar el recurso Scanner
        teclado.close();
    }
}
```

---

## 🚀 Tecnologías Utilizadas
*   **Lenguaje:** Java 17+
*   **Lógica:** Pseudocódigo estructurado
*   **Formato:** Markdown para documentación
