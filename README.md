# Muestreo-Aleatorio-Simple
📏 Estimación del Tamaño Muestral e Intervalo de Confianza
Diseñar una muestra es darle forma a la inferencia conn tres métodos y una sola intención: precisión.

📌 Propósito
Este script en Hansl permite:
- Calcular el tamaño muestral necesario para estimar la media de una población finita con error E, desvío σ, y nivel de confianza Z.
- Contrastar devlos tres métodos algebraicamente equivalentes para verificar consistencia teórica.
- Calcular el intervalo de confianza al 95 % alrededor de una media poblacional dada (media = 20), con corrección por población finita incluida.

⚙️ Parámetros de entrada
| Parámetro | Descripción | Valor | 
| media | Media poblacional esperada | 20 | 
| sigma | Desvío estándar poblacional | 100 | 
| E | Error absoluto deseado | 15 | 
| Z | Valor crítico (nivel de confianza 95%) | 1.96 | 
| N | Tamaño de población finita | 500 | 



🧪 Métodos implementados
Se presentan  tres métodos 

🔄 Salidas del script
- Tamaño muestral estimado por cada método (n_A, n_B, n_C )
- Margen de error corregido
- Límite inferior y superior del intervalo de confianza
- Resumen numérico claro y etiquetado
