# Reto SOLID – Análisis de Diseño y Principios de Arquitectura

## 📌 Contexto

Una empresa desarrolló un sistema de gestión de dispositivos inteligentes basado en una interfaz llamada `DispositivoInteligente`, la cual declara los siguientes métodos:

- `encender()`
- `apagar()`
- `imprimir()`
- `escanear()`
- `volar()`

Existen clases como `Impresora` y `Drone` que implementan esta interfaz. Sin embargo, cuando un método no aplica a su naturaleza (por ejemplo, una impresora no puede volar o un drone no puede imprimir), la implementación lanza una excepción del tipo `UnsupportedOperationException`.

Adicionalmente, existe una clase llamada `CentroControl` que recibe un objeto del tipo `DispositivoInteligente` y ejecuta directamente el método `volar()`, asumiendo que cualquier dispositivo inteligente puede hacerlo.

---

## 🎯 Objetivo del Reto

El equipo deberá realizar un análisis crítico del diseño actual y responder lo siguiente:

1. ¿Qué principios SOLID están siendo vulnerados en este diseño?
2. ¿Por qué lanzar `UnsupportedOperationException` puede considerarse una señal de mal diseño contractual?
3. ¿Qué problemas podrían presentarse en tiempo de ejecución debido a la forma en que `CentroControl` utiliza la abstracción?
4. ¿Cómo debería replantearse la estructura de interfaces para que cada clase implemente únicamente los comportamientos que realmente puede cumplir?
5. ¿Cómo debería modificarse la dependencia de `CentroControl` para evitar asumir capacidades que no todos los dispositivos poseen?
6. Si se quisiera agregar un nuevo `RobotMultifuncional` capaz de imprimir, escanear y volar, ¿sería posible hacerlo sin modificar código existente? Justifiquen su respuesta en términos de principios de diseño.

---

## 🧠 Criterios de Evaluación

Se evaluará:

- Identificación correcta de los principios SOLID involucrados.
- Argumentación técnica clara y fundamentada.
- Propuesta de rediseño coherente.
- Justificación del cumplimiento o incumplimiento del principio Open/Closed.
- Claridad conceptual en la explicación del contrato de las interfaces.

---

## ⚠ Restricciones

- No se permite simplemente eliminar métodos sin justificar arquitectónicamente la decisión.
- La propuesta debe estar alineada con buenas prácticas de diseño orientado a objetos.
- Se debe argumentar cómo el rediseño mejora la mantenibilidad y extensibilidad del sistema.

---

## 🏁 Entregable

Documento técnico donde se exponga:

- Análisis del problema.
- Principios violados.
- Justificación técnica.
- Propuesta de rediseño conceptual.
- Argumentación sobre extensibilidad futura del sistema.

---

Este reto busca evaluar la capacidad del equipo para detectar problemas de diseño, comprender contratos de abstracción y aplicar correctamente los principios SOLID en escenarios reales.
