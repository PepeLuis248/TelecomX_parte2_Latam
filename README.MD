TelecomX2: Predicción de Cancelación (Churn)

Desarrollar modelos predictivos capaces de prever qué clientes tienen mayor probabilidad de cancelar sus servicios.

La empresa quiere anticiparse al problema de la cancelación, y te corresponde a ti construir un pipeline robusto para esta etapa inicial de modelado.

Crear una conclusión estratégica señalando los principales factores que influyen en la cancelación.

Para desarrollar un modelo predictivo capaz de prever que clientes tienen mayor probabilidad de cancelar sus compras o sus pagos; he realizado un exhaustivo estudio de un recorrido por todos los posibles métodos de valuación y evolución de los modelos, utilizando el archivo datos_TelecomX_Fla.json del Challenges TelecomX1. Dado que la variable objetivo es Churn (abandono del cliente, es binaria), este es un problema de clasificación binaria. Se pueden aplicar modelos como:

Modelos clásicos de clasificación:

1-Regresión logística (LogisticRegression)

2-Árboles de decisión

3-K-Nearest Neighbors (KNN)

4-SVM (Support Vector Machines)

5-RamdomForetClassifier

Insights Finales Basados en la Correlación con Churn

Factores que Aumentan la Probabilidad de Cancelación

1. Altos Cargos Mensuales (`Charges.Monthly`):  
   Clientes con facturas mensuales más altas tienden a cancelar más, posiblemente por una percepción de bajo valor en relación al costo.

2. Facturación Electrónica (`PaperlessBilling`):  
   Los usuarios que reciben facturación digital presentan mayor churn. Esto puede estar vinculado a perfiles más jóvenes y digitales, propensos a cambiar de proveedor.

3. Adultos Mayores (`SeniorCitizen`):  
   Ligeramente más propensos a cancelar, probablemente por ingresos fijos o menor afinidad con servicios tecnológicos.

4. Servicios de Streaming (`StreamingTV` / `StreamingMovies`):
   Tener estos servicios no garantiza permanencia. Puede reflejar usuarios exigentes o acostumbrados a comparar.

5. Múltiples Líneas (`MultipleLines`):
   No se asocia fuertemente con retención. Tal vez sea un servicio fácilmente reemplazable por promociones de la competencia.

---

Factores que Disminuyen la Probabilidad de Cancelación

1. Antigüedad del Cliente (`tenure`):
   A mayor tiempo con la empresa, menor es la probabilidad de baja. Es fundamental trabajar la retención en los primeros meses.

2. Tipo de Contrato (`Contract`): 
   Contratos a plazo fijo (anual, bianual) reducen significativamente el churn. Indican compromiso y fidelidad.

3. Tipo de Internet (`InternetService`):  
   Servicios con mejor calidad (como fibra óptica) están asociados con menor churn. La calidad del servicio es clave.

4. Método de Pago (`PaymentMethod`): 
   Métodos como débito automático muestran menor tasa de cancelación. Indican estabilidad financiera o menor fricción.

5. Gasto Total (`Charges.Total`):
   Quienes ya invirtieron más en la empresa tienden a quedarse. Esto puede deberse al “efecto inversión”.

6. Servicios de Valor Agregado (`OnlineSecurity`, `TechSupport`): 
   Mejoran la percepción de calidad y satisfacción, favoreciendo la retención.

7. Vínculos Personales (`Partner`, `Dependents`,): 
   Clientes con familia o pareja tienen menor churn, posiblemente por mayor estabilidad o decisiones compartidas.

---

Recomendaciones Estratégicas
  Fidelizar a nuevos clientes durante los primeros meses, con beneficios personalizados o atención diferencial.
- Promover contratos a largo plazo con descuentos, promociones exclusivas o mejoras en el servicio.
- Fomentar métodos de pago automáticos, ofreciendo incentivos para reducir cancelaciones por olvido o problemas administrativos.
- Detectar clientes con altos cargos mensuales y ofrecerles mejoras o bonificaciones personalizadas.
- Ofrecer servicios de valor agregado, como seguridad en línea o soporte técnico premium, como herramientas de fidelización.
- Segmentar campañas de retención según tipo de cliente (edad, perfil digital, estado civil, presencia de dependientes).



