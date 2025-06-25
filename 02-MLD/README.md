# 🧠 Modelo Lógico de Datos (MLD)

Esta carpeta contiene el **Modelo Lógico de Datos (MLD)** derivado del modelo entidad-relación (MER) previamente desarrollado.

---

## 📌 Estado del avance

- [x] 1. Modelo Lógico
- [x] 2. Entidades Fuertes
- [x] 3. Entidades Débiles
- [x] 4. Entidad Asociativa
- [x] 5. Atributos de Especialización
- [x] 6. Cardinalidad

---
---


## 1. ¿Qué es el Modelo Lógico? 🧾

El **Modelo Lógico de Datos** es una representación más detallada y técnica del modelo conceptual (MER). Se enfoca en **cómo se organizarán los datos** en una base de datos relacional, sin todavía considerar aspectos físicos o tecnológicos.

Se encarga de:
- Especificar tablas lógicas basadas en entidades
- Establecer claves primarias (PK) y foráneas (FK)
- Eliminar redundancias (normalización)
- Preparar el modelo para la implementación física

---
---

## 2. Entidades Fuertes

### Representación de Entidades Fuertes

![Entidades Fuertes](./img/entidades-fuertes.png)

---
---

## 3. Entidades Débiles

### Representación de Entidades Débiles

![Entidades Débiles](./img/entidades-debiles.png)

---
---

## 4. Entidad Asociativa

**Definición:** Una tabla que se crea para representar **una relación de muchos a muchos** entre dos entidades.

- Ejemplo: La tabla "ITEMS" que conecta "PEDIDO" y "LIBRO".
- Atributos clave:
  - Claves foráneas: "cod_pedido" (de "Pedido") y "código del libro" (de "Libro").
  - Atributos propios: cantidad, valor.

### Representación de Entidad Asociativa

![Entidad Asociativa](./img/entidad-asociativa.png)

---
---

## 5. Atributos de Especialización

**Definición:** Tablas que se crean para detallar diferentes tipos de una entidad más general.
- Ejemplo: "Persona Natural (PN)" y "Persona Jurídica (PJ)" que especializan la entidad "Cliente".

- Clave foránea común:
  - "cod_cliente" (código del cliente) que relaciona ambas tablas con "Cliente".
- Atributos específicos:
  - Persona Natural (PN): DNI, RUT.
  - Persona Jurídica (PJ): NIT, RUES.

### Representación de Atributos de Especialización

![Atributos de Especialización](./img/atributo-especializacion.png)

---
---

## 6. Cardinalidad

**Definición:** Define la relación numérica entre las instancias de las entidades.

- Componentes:
  - Cardinalidad mínima: El número mínimo de instancias que deben estar relacionadas.
  - Cardinalidad máxima: El número máximo de instancias que pueden estar relacionadas.


- Ejemplos en el modelo:
  - Cliente a Pedido: 1 a N (un cliente puede tener muchos pedidos).
  - Persona Jurídica a Cliente: 0 a 1 (una persona jurídica puede o no ser un cliente).
  - Pedido a Items: 1 a N (un pedido debe tener al menos un item).
  - Libro a Inventario: 0 a N (un libro puede no estar en inventario o estar varias veces).
  - Editorial a Libro: 1 a N (una editorial puede tener muchos libros).


### Representación de Cardinalidad

![Cardinalidad](./img/cardinalidad.png)

---
