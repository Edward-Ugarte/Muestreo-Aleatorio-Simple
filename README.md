# Muestreo-Aleatorio-Simple
📏 Estimación del Tamaño Muestral e Intervalo de Confianza
Diseñar una muestra es darle forma a la inferencia. Con cuatro métodos y una sola intención: precisión.

📌 Propósito
Este script en Hansl permite:
- Calcular el tamaño muestral necesario para estimar la media de una población finita con error E, desvío σ, y nivel de confianza Z.
- Contrastar cuatro métodos algebraicamente equivalentes para verificar consistencia teórica.
- Calcular el intervalo de confianza al 95 % alrededor de una media poblacional dada (media = 20), con corrección por población finita incluida.

⚙️ Parámetros de entrada
| Parámetro | Descripción | Valor | 
| media | Media poblacional esperada | 20 | 
| sigma | Desvío estándar poblacional | 100 | 
| E | Error absoluto deseado | 15 | 
| Z | Valor crítico (nivel de confianza 95%) | 1.96 | 
| N | Tamaño de población finita | 500 | 



🧪 Métodos implementados
Se presentan cuatro métodos equivalentes para estimar el tamaño muestral n bajo población finita:
- Método A:
[ n = \frac{Z2}{E^2} \quad \text{con corrección: } \frac{n}{1 + \frac{n}{N}} ]
- Método B:
[ n = \frac{N \cdot Z2}{N \cdot E2 \cdot \sigma^2} ]
- Método C:
[ n = \frac{\sigma^2}{(E/Z)2}{N}} ]
- Método D:
Variante modular con redondeo entero:
[ n = \left\lceil \frac{Z2}{E^2 (1 + \frac{1}{N})} \right\rceil ]
Todos convergen numéricamente al mismo valor bajo condiciones ideales.

📐 Intervalo de confianza corregido
A partir del valor de n (método D), se estima:
[ IC = \bar{x} \pm Z \cdot \frac{\sigma}{\sqrt{n}} \cdot \sqrt{1 - \frac{n}{N}} ]
En este caso, el intervalo se centra en la media 20, con un margen corregido según la fracción de muestreo.

🔄 Salidas del script
- Tamaño muestral estimado por cada método (n_A, n_B, n_C, n_D)
- Margen de error corregido
- Límite inferior y superior del intervalo de confianza
- Resumen numérico claro y etiquetado
