# 🧩 Modelo Entidad-Relación (MER)

Esta carpeta contiene el **Modelo Entidad-Relación (MER)** correspondiente a la etapa conceptual del proyecto.


---

## 📌 Estado del avance

- [x] 1. Modelo Conceptual
- [x] 2. Entidades y tipos
- [ ] 3. Modelo y Diagrama Entidad-Relación
- [ ] 4. Relaciones y tipos
- [ ] 5. Cardinalidad
- [ ] 6. Atributos y tipos

---
---

## 1. ¿Qué es el Modelo Conceptual?

El **modelo conceptual** es la primera etapa del diseño de una base de datos, donde se modela el mundo real desde el punto de vista de los datos. Tiene las siguientes características:

- Es **independiente de la implementación** (no depende del hardware, software, ni del SGBD).
- Usa conceptos del **modelo Entidad-Relación (MER)** para representar la información.
- Sirve como **puente entre los requisitos del usuario y el diseño lógico y físico** de la base de datos.


---
---


## 2. ¿Qué es una Entidad?

Una **entidad** es un elemento del mundo real o del negocio que tiene existencia propia dentro del sistema y del cual queremos guardar información estructurada.

Se representan mediante un rectángulo.

> Ejemplo: Cliente, Libros, Editorial, Pedido, Inventario, etc.



### 🧩 2.1. Tipos de Entidades

#### 2.1.1. 🟨 Entidad Fuerte

- **Definición:** Es una entidad que tiene existencia propia, que no depente de otra, y tiene una clave primaria que la identifica de forma única.
- **Ejemplo:**
  - `Cliente`
  - `Editorial`
  
  

#### 2.1.2. 🟦 Entidad Débil

- **Definición:** Es una entidad que **no posee clave primaria propia** y depende de otra entidad para poder identificarse. Se apoya en una clave externa.
- **Ejemplo:**
  - `Libro`: depende de la `Editorial`
  - `Pedido de compra`: depende de un `Cliente` y un `Libro`

### 2.1.3. 🟩 Entidad de Especialización/Generalización

- Se da cuando una entidad general se divide en subtipos más específicos que comparten atributos comunes, pero también tienen atributos particulares.
- **Ejemplo en este modelo:**
  - Entidad general: `Cliente`
  - Subtipos:
    - `PersonaNatural` (atributos: `DNI`, `RUT`)
    - `PersonaJuridica` (atributos: `NIT`, `RUES`)

---


---
