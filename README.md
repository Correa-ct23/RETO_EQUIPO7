# Reto de Diseño – Aplicación de ISP y Liskov

## 📌 Contexto

Una empresa desarrolló un sistema de gestión de dispositivos inteligentes utilizando una interfaz llamada `DispositivoInteligente`, la cual declara los siguientes métodos:

- `encender()`
- `apagar()`
- `imprimir()`
- `escanear()`
- `volar()`

Clases como `Impresora` y `Drone` implementan esta interfaz. Sin embargo, cuando un método no aplica a su naturaleza (por ejemplo, una impresora no puede volar o un drone no puede imprimir), la implementación lanza una excepción del tipo `UnsupportedOperationException`.

Adicionalmente, existe una clase llamada `CentroControl` que recibe un objeto del tipo `DispositivoInteligente` y ejecuta directamente el método `volar()`, asumiendo que cualquier dispositivo inteligente puede hacerlo.

---

## 🎯 Objetivo del Reto

El equipo deberá analizar el diseño actual y realizar un rediseño conceptual aplicando exclusivamente:

- Principio de Segregación de Interfaces (ISP)
- Principio de Sustitución de Liskov (LSP)

---

## 🧠 Actividades a Desarrollar

1. Identificar y explicar claramente cómo el diseño actual viola el principio de Segregación de Interfaces (ISP).
2. Analizar por qué el uso de `UnsupportedOperationException` puede evidenciar un problema en el contrato de la abstracción.
3. Explicar cómo el comportamiento de `CentroControl` puede generar una violación del principio de Sustitución de Liskov (LSP).
4. Proponer un rediseño donde:
   - Cada clase implemente únicamente los comportamientos que realmente puede cumplir.
   - Las dependencias se establezcan sobre abstracciones coherentes con el comportamiento requerido.
5. Justificar cómo el nuevo diseño garantiza el cumplimiento de ISP y LSP.

---

## ⚠ Restricciones

- No se permite eliminar métodos sin justificación conceptual.
- No se permite modificar el comportamiento real de los dispositivos (una impresora no puede volar).
- La solución debe enfocarse exclusivamente en ISP y LSP.

---

Este reto busca evaluar la capacidad del equipo para identificar contratos mal definidos y rediseñar correctamente las abstracciones respetando los principios fundamentales de la orientación a objetos.
