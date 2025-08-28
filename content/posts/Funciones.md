---
title: Funciones
date: 2023-10-27
tags:
  - python
  - programación
  - funciones
  - conceptos
draft: false
category: tutorial
topics:
  - conceptos básicos de programación
  - estructura de código
  - reutilización de código
---
### **Concepto de Funciones**

Una función es un bloque de código reutilizable que realiza una tarea específica. Pensá en una función como un "verbo" o una "acción" en tu programa. El propósito principal de las funciones es:

- **Modularidad:** Dividir un programa grande y complejo en partes más pequeñas y manejables.
- **Reutilización de Código:** Evitar la repetición de código. Si una tarea se realiza varias veces, la encapsulás en una función y la llamás cada vez que la necesitás, en lugar de reescribir el código.
- **Abstracción:** Ocultar los detalles internos de una operación. Por ejemplo, al usar la función `print()`, no necesitás saber cómo el sistema operativo muestra el texto en la pantalla; solo lo que la función lo hace.

### **Tipos de Funciones**

En Python, hay dos tipos principales de funciones:

1. **Funciones Integradas (Built-in Functions):** Son funciones que ya vienen con Python y están listas para usar. Ejemplos de ello son `print()`, `input()`, `int()`, `float()`, `round()`. No necesitás definirlas; solo las llamas para que realicen su tarea.
    
    [Funciones Integradas](https://www.notion.so/Funciones-Integradas-2427be926879800f9d6bea4551c02d7e?pvs=21)
    
2. **Funciones Propias (User-Defined Functions):** Son las funciones que creás para resolver problemas específicos de tu programa.
    
    [Funciones Propias](https://www.notion.so/Funciones-Propias-2427be926879805e94b6dd4cc1136034?pvs=21)
    

### **Anatomía de una Función Propia**

Para crear tus propias funciones, usas la palabra clave `def`. Su estructura es la siguiente:

Python

```jsx
def nombre_de_la_funcion(parametro1, parametro2):
    # Cuerpo de la función (código indentado)
    # ...
    return valor_opcional
```

- **`def`:** La palabra clave para "definir" una función.
- **`nombre_de_la_funcion`:** El nombre que le das a tu función. Debe ser descriptivo (por ejemplo, `saludar`, `cuadrado`, `calcular_promedio`).
- **Paréntesis `()`:** Contienen los **parámetros**, que son las variables que la función espera recibir como entrada. Si la función no necesita entradas, los paréntesis se dejan vacíos.
- **Cuerpo de la Función:** Es el bloque de código que se ejecuta cuando se llama a la función. Es crucial que esté **indentado** (con sangría) para que Python sepa que pertenece a la función.
- **`return`:** (Opcional) La palabra clave `return` se usa para que una función devuelva un valor como resultado. Si una función no tiene una sentencia `return`, devuelve `None` por defecto.

### **Conceptos Clave Relacionados con Funciones**

- **Parámetros vs. Argumentos:**
    
    - Un **parámetro** es la variable que se define en la declaración de la función (ej. `def saludar(nombre):`).
        
        [Parámetros](https://www.notion.so/Par-metros-2427be92687980da8065ee4edb756cfa?pvs=21)
        
    - Un **argumento** es el valor real que se pasa a la función cuando la llamas (ej. `saludar("Juan")`).
        
        [Argumentos](https://www.notion.so/Argumentos-2427be926879809fb46bd004d5fdb64a?pvs=21)
        
    
    ```python
    
    # 'nombre' es un PARÁMETRO
    def saludar(nombre):
        print(f"Hola, {nombre}")
    
    # 'David' es el ARGUMENTO
    saludar("David")
    ```
    

En este caso:

- En la línea 2, `nombre` es el **parámetro** de la función `saludar`.
- En la línea 5, cuando llamás a la función, `"David"` es el **argumento** que le estás pasando a ese parámetro.

En resumen, los **parámetros** van en la declaración de la función, y los **argumentos** van en la llamada de la función.

### **Relación entre Parámetros y Argumentos**

|Perspectiva|Término|Cuándo se usa|
|---|---|---|
|**En la definición de la función**|**Parámetro**|Cuando se crea la función|
|**Al llamar a la función**|**Argumento**|Cuando se ejecuta la función|

```python
#
# ---- Perspectiva: En la definición de la función ----
#
# 'lado' es un PARÁMETRO. Es un nombre que la función
# espera recibir para poder hacer su trabajo.
#
def calcular_area_cuadrado(lado):
    # La función usa el parámetro 'lado' como si fuera una variable.
    area = lado * lado
    return area

#
# ---- Perspectiva: Al llamar a la función ----
#
# '5' es el ARGUMENTO. Es el valor real que le pasamos
# a la función.
#
resultado_1 = calcular_area_cuadrado(5)

# '12' también es un ARGUMENTO.
resultado_2 = calcular_area_cuadrado(12)

# Imprimimos los resultados para ver el efecto.
print(resultado_1) # Esto imprimirá 25
print(resultado_2) # Esto imprimirá 144
```

- **Efectos Secundarios (Side Effects):** Algunas funciones no devuelven un valor con `return`, sino que simplemente realizan una acción (un efecto secundario). La función `print()` es un ejemplo: su efecto secundario es mostrar texto en la pantalla.
- **Valores de Retorno (`return values`):** Una función que devuelve un valor con `return` permite que el resultado de su trabajo sea almacenado en una variable o usado por otra parte del código. Por ejemplo, `cuadrado(2)` devuelve el valor `4`, que puedes asignar a una variable.
- **Orden de Definición:** Python es un lenguaje que se ejecuta de forma secuencial. Por lo tanto, debes **definir una función antes de que la llames** en tu código. Es por esto que una práctica común es definir la mayoría de las funciones al principio del archivo.
- **La Función `main()`:** Es una convención popular en muchos lenguajes, incluido Python, usar una función `main()` para contener la lógica principal del programa. Esto ayuda a organizar el código, manteniendo la lógica principal separada de las funciones auxiliares.