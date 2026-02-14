# Redes Neuronales Recurrentes: Modelando Memoria y Secuencia 🔁🧠

Bienvenido al módulo de **Redes Neuronales Recurrentes (RNN)** dentro del curso *Tópicos de Machine Learning y Redes Neuronales*.

Hasta este punto del libro hemos trabajado principalmente con modelos diseñados para datos **independientes**:

- Regresión
- Clasificación
- Redes Feedforward
- Convolucionales

Sin embargo, muchos problemas reales no son independientes… son **secuenciales**.

---

## 🌎 ¿Dónde aparecen los datos secuenciales?

En Inteligencia de Negocios y Analítica encontramos secuencias constantemente:

- Series de tiempo de ventas
- Tráfico web diario
- Open Rate de campañas
- Producción agrícola
- Precios financieros
- Demanda energética
- Texto y lenguaje natural

En todos estos casos, el presente depende del pasado.

> El orden de los datos contiene información.

---

## 🧩 La limitación de las redes tradicionales

Una red neuronal clásica (Feedforward):

- recibe una entrada \(x\)
- la procesa
- produce una salida \(\hat{y}\)

Pero no tiene memoria.

Si le damos el valor de hoy, no sabe qué pasó ayer.

Esto es crítico en series de tiempo:

- Tendencias se acumulan.
- Patrones se repiten.
- Los ciclos importan.

Aquí es donde nacen las RNN.

---

## 🔁 ¿Qué hace distinta a una RNN?

Las Redes Neuronales Recurrentes introducen un concepto clave:

### Estado oculto (hidden state)

En cada instante \(t\), la red combina:

- el dato actual \(x_t\)
- la memoria previa \(h_{t-1}\)

\[
h_t = f(x_t, h_{t-1})
\]

Esto permite que la red mantenga un **resumen comprimido del pasado**.

Podemos pensarlo como:

> “Todo lo que la red considera relevante hasta ahora”.

---

## 🧠 De la memoria corta a la memoria larga

Las RNN simples funcionan… pero tienen una limitación matemática importante:

### Gradiente desvaneciente

Durante el entrenamiento:

- el error se propaga hacia atrás en el tiempo,
- multiplicando gradientes repetidamente.

Esto hace que la señal de aprendizaje de eventos lejanos se pierda.

Resultado:

- La red aprende lo reciente.
- Olvida lo antiguo.

---

## 🔋 La solución: LSTM

Las arquitecturas **Long Short-Term Memory (LSTM)** fueron diseñadas para resolver este problema.

Introducen:

- Estado de celda (memoria persistente)
- Compuertas de control:
  - Olvido
  - Entrada
  - Salida

Esto permite:

- Recordar patrones largos
- Filtrar ruido reciente
- Modelar ciclos complejos

---

## 🧭 Ruta de aprendizaje del módulo

El módulo está diseñado de forma progresiva:

### 1️⃣ Fundamentos conceptuales
Definición de RNN, memoria, unrolling y compuertas LSTM.

### 2️⃣ Simulación manual
Cálculo paso a paso del flujo de memoria.

### 3️⃣ Implementación desde cero
Construcción de una SimpleRNN en NumPy.

### 4️⃣ Caso de negocio real
Predicción de exportaciones de café colombiano.

### 5️⃣ Mejora arquitectónica
Comparación SimpleRNN vs LSTM.

### 6️⃣ Caso financiero avanzado
Predicción de Bitcoin con BiLSTM y regularización.

---

## 🎯 Objetivo del módulo

Al finalizar, podrás:

- Entender cuándo usar RNN vs redes tradicionales.
- Explicar el rol del estado oculto y la memoria.
- Implementar RNN y LSTM.
- Construir pipelines de series de tiempo.
- Evaluar modelos secuenciales en negocio y finanzas.

---

## ⚠️ Nota importante

Aunque veremos aplicaciones en mercados financieros, estos modelos:

- No garantizan rentabilidad.
- Son sensibles a cambios de régimen.
- Requieren validación rigurosa.

El foco del módulo es **modelado secuencial**, no trading.

---

## 🚀 Comencemos

En el siguiente notebook abriremos la “caja negra” de las RNN para entender, paso a paso, cómo fluye la memoria en el tiempo.

