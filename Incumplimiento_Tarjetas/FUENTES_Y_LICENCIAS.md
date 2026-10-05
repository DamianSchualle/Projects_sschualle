# Fuentes y licencia — C2

Yeh, I. (2009). Default of Credit Card Clients. UCI Machine Learning Repository. https://archive.ics.uci.edu/dataset/350/default+of+credit+card+clients . DOI https://doi.org/10.24432/C55S3H . Licencia CC BY 4.0: https://creativecommons.org/licenses/by/4.0/ . Datos originales descargados el 18/09/2026 desde https://archive.ics.uci.edu/static/public/350/default+of+credit+card+clients.zip . Adaptación docente, sin aval implícito de los autores.

El Excel original tiene 30.000 filas, ID, 23 características y etiqueta. Se leyó `default of credit card clients.xls` con encabezado en la segunda fila, usando xlrd; la conversión CSV no curada y los hashes se conservan en material docente. Se excluyeron SEX, EDUCATION, MARRIAGE y AGE; ID se conserva únicamente como clave; quedan 19 predictores. Se renombró la etiqueta como incumplimiento sin cambiar sus valores.

IDs únicos: 30.000. Existen 35 repeticiones si se omite sólo ID y 732 si además se omite demografía; no se eliminan clientes distintos por compartir un perfil. No se fabricaron nulos, no se modificaron montos/códigos y no se equilibraron artificialmente las clases. Se usó separación estratificada 70/15/15, semilla 42, en dos pasos: 70/30 y luego mitad/mitad de la reserva. CSV por partición ordenados por ID.

Historia abril–septiembre de 2005, Taiwán. Mes objetivo siguiente al historial. Esta evaluación entre clientes del mismo corpus no valida un período posterior. Los códigos PAY -2 y 0 no están definidos en la ficha y se conservan como categorías separadas; no se adivina su significado. Importes negativos de estados de cuenta se conservan porque no hay evidencia suficiente para corregirlos. La causa individual de esos signos y la definición contractual completa de incumplimiento no se deducen de la ficha.

La exclusión de demografía no demuestra ausencia de sesgos. Los resultados son académicos y no justifican decisiones sobre clientes reales ni cálculos de provisiones regulatorias. La comparación conjunta de métodos y variables no aísla el aporte causal de cada mes.
