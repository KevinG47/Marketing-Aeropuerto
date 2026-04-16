# 🛫 Sistema de Alertas Predictivas: American Regional Airways

Proyecto de Machine Learning enfocado en mejorar la experiencia y satisfacción del pasajero mediante notificaciones proactivas de retrasos.

## 🎯 La Misión (Departamento de Marketing)
Un pasajero prevenido es un pasajero menos frustrado. Nuestro objetivo no es evitar el retraso (eso es de Operaciones), sino **gestionar la expectativa del cliente**. Si le avisamos con tiempo que su vuelo tiene alto riesgo de demora, puede decidir llegar más tarde al aeropuerto o prepararse para la espera, mejorando su percepción de nuestra transparencia.

## 📊 Estrategia y Hallazgos
1. **El Motor:** Se entrenó un modelo de Random Forest (procesando +5 millones de vuelos con PySpark) que identifica los vuelos en riesgo, siendo la Hora de Salida (`DEP_HOUR`) la variable más crítica.
2. **Priorizando al Pasajero (Threshold Tuning):** Ajustamos la sensibilidad del modelo bajando el umbral de alerta al 40%. Matemáticamente esto aumenta las falsas alarmas, pero para Marketing es un éxito: logramos **evitar que más de 35,000 pasajeros** llegaran ciegos al aeropuerto sin saber que su vuelo iba a retrasarse.
3. **Automatización:** Se extrajeron las reglas del Árbol de Decisión para integrarlas al sistema CRM y disparar los correos o mensajes push automáticamente.

