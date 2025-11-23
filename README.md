# Cálculo Numérico - Métodos de Resolución

Este proyecto contiene implementaciones de métodos numéricos fundamentales para la resolución de problemas matemáticos. Los algoritmos fueron desarrollados mediante el análisis y estudio de los métodos de cálculo numérico, utilizando diversas herramientas de internet para la comprensión y validación de los conceptos teóricos.

**Realizado por: William Flores**

---

## 📋 Descripción del Proyecto

Este repositorio incluye implementaciones en Python de tres métodos numéricos esenciales:

1. **Método de Bisección** - Para encontrar raíces de funciones
2. **Método de Newton-Raphson** - Para encontrar raíces de funciones de forma iterativa
3. **Polinomio de Taylor** - Para aproximar funciones mediante series de Taylor

Todos los métodos incluyen visualización detallada del proceso de cálculo, mostrando paso a paso cada iteración y los valores intermedios.

---

## 📁 Archivos del Proyecto

### `biseccion.py`

**Descripción:** Implementa el método de bisección para encontrar raíces de funciones continuas en un intervalo dado.

**Funcionalidad:**
- Divide iterativamente el intervalo `[a, b]` a la mitad
- Determina en qué subintervalo se encuentra la raíz basándose en el cambio de signo
- Continúa hasta alcanzar la precisión deseada o el número máximo de iteraciones
- Muestra en consola cada iteración con los valores de `a`, `b`, punto medio `m`, y los valores de la función

**Parámetros:**
- `f`: Función objetivo (callable)
- `a`: Extremo inferior del intervalo inicial
- `b`: Extremo superior del intervalo inicial
- `er`: Error máximo permitido
- `n`: Número máximo de iteraciones
- `mostrar_proceso`: Si es `True`, muestra el proceso de cálculo (por defecto: `True`)

**Retorna:** Tupla `(raiz_aproximada, error_final)`

---

### `newton_raphson.py`

**Descripción:** Implementa el método de Newton-Raphson (también conocido como método de Newton) para encontrar raíces de funciones de forma iterativa.

**Funcionalidad:**
- Utiliza la fórmula: `x_{n+1} = x_n - f(x_n) / f'(x_n)`
- Requiere la función y su derivada
- Converge más rápido que el método de bisección cuando la aproximación inicial es buena
- Muestra en consola cada iteración con los valores de `x_actual`, `f(x)`, `f'(x)`, `x_nuevo` y el error relativo

**Parámetros:**
- `f`: Función objetivo (callable)
- `df`: Derivada de la función objetivo (callable)
- `x0`: Aproximación inicial a la raíz
- `er`: Cota máxima del error relativo permitido
- `n`: Número máximo de iteraciones
- `mostrar_proceso`: Si es `True`, muestra el proceso de cálculo (por defecto: `True`)

**Retorna:** Tupla `(raiz_aproximada, error_final)`

---

### `polinomio-de-taylor.py`

**Descripción:** Implementa el cálculo del polinomio de Taylor para aproximar funciones mediante series de Taylor.

**Funcionalidad:**
- Calcula el polinomio de Taylor de grado `n` alrededor de un punto `a`
- Soporta funciones simbólicas usando `sympy` y funciones lambda
- Calcula automáticamente las derivadas necesarias
- Estima el error del resto (término de Lagrange)
- Muestra en consola cada término del polinomio, las derivadas calculadas y el polinomio acumulado

**Parámetros:**
- `f`: Función objetivo (callable o expresión simbólica de sympy)
- `a`: Punto alrededor del cual se expande el polinomio (centro de expansión)
- `n`: Grado del polinomio de Taylor
- `x_eval`: (Opcional) Punto donde se desea evaluar el polinomio
- `mostrar_proceso`: Si es `True`, muestra el proceso de cálculo (por defecto: `True`)

**Retorna:** 
- Si `x_eval` está definido: Tupla `(valor_numerico, error_resto)`
- Si `x_eval` es `None`: Tupla `(polinomio_simbolico, None)`

**Dependencias:** Requiere la librería `sympy` para cálculos simbólicos.

---

## 🚀 Requisitos

### Librerías necesarias:

- `math` - Librería estándar de Python (incluida por defecto)
- `sympy` - Para cálculos simbólicos (requiere instalación)

### Instalación de dependencias:

```bash
pip install sympy
```

---

## 💻 Uso

Cada archivo puede ejecutarse directamente desde la línea de comandos:

```bash
python biseccion.py
python newton_raphson.py
python polinomio-de-taylor.py
```

También puedes importar las funciones en otros scripts:

```python
from biseccion import biseccion
from newton_raphson import newton_raphson
from polinomio_de_taylor import polinomio_taylor

# Ejemplo de uso
f = lambda x: x**2 - 4
raiz, error = biseccion(f, 0, 5, 0.01, 50)
```

---

## 📊 Características

- ✅ Visualización detallada del proceso de cálculo
- ✅ Tablas de iteraciones con todos los valores intermedios
- ✅ Cálculo automático de errores
- ✅ Soporte para funciones simbólicas y numéricas
- ✅ Validación de parámetros de entrada
- ✅ Manejo de casos especiales (raíces exactas, derivadas nulas, etc.)

---

## 📝 Notas

Este proyecto fue desarrollado como parte del estudio de métodos numéricos, utilizando diversas herramientas y recursos de internet para la comprensión teórica y práctica de los algoritmos implementados. Los métodos han sido validados y probados con diferentes funciones y casos de uso.

---

## 👤 Autor

**William Flores**

---

## 📚 Referencias

Los métodos implementados están basados en los fundamentos del cálculo numérico y fueron desarrollados mediante el análisis de:
- Teoría de métodos numéricos
- Recursos educativos en línea
- Documentación de librerías matemáticas
- Ejemplos y ejercicios prácticos

---

## 📄 Licencia

Este proyecto es de uso educativo y académico.

