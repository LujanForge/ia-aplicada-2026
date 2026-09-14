# Ficha inicial del proyecto

## Problema
El cáncer es una de las principales causas de mortalidad a nivel mundial, y la rapidez con la que se detecta la enfermedad es uno de los factores que más incide en la supervivencia del paciente. Actualmente, gran parte de los diagnósticos se realizan cuando el cáncer ya se encuentra en etapas avanzadas, lo que reduce significativamente las probabilidades de un tratamiento exitoso. Esto ocurre con frecuencia porque los métodos convencionales no siempre detectan señales tempranas en los datos genéticos del paciente, y cuando lo hacen, el margen de acción ya es limitado.

## Contexto
El proyecto se desarrolla en el marco de la materia Inteligencia Artificial Aplicada, por el equipo GenIA, con un plazo de 4 meses. Se trabajará con datos genómicos públicos y validados, principalmente el dataset TCGA (The Cancer Genome Atlas), que ya ha sido utilizado en estudios académicos. No se requiere infraestructura clínica ni acceso a pacientes reales, ya que los datos son abiertos y verificables. El proyecto se acota a un tipo de cáncer o gen específico para garantizar su viabilidad dentro del plazo establecido por la materia.

## Usuarios afectados
Los beneficiarios finales serían los pacientes en riesgo de cáncer, que podrían recibir un diagnóstico más temprano y con ello mayores probabilidades de un tratamiento exitoso. Los usuarios directos de la herramienta serían investigadores y personal médico que analizan datos genómicos, y que hoy dependen de métodos manuales o de software especializado costoso. Es importante distinguir entre ambos: el paciente se beneficia del resultado, pero quien usa la solución día a día es el investigador o el médico.

## Tipo de IA propuesto
IA predictiva (aprendizaje automático supervisado). El problema consiste en clasificar muestras genéticas según la presencia o ausencia de células cancerígenas, a partir de patrones en los datos de expresión génica o mutaciones específicas. La IA generativa no es adecuada porque no se trata de crear contenido nuevo, sino de predecir una categoría a partir de datos existentes. Un agente añadiría complejidad innecesaria en esta fase. Esta conclusión coincide con lo observado en la comparación de modelos de la Parte 2, donde ChatGPT y Deepseek recomendaron IA predictiva para un problema de clasificación binaria, mientras Gemini propuso un agente más complejo.

## Qué dijeron los modelos
En la comparación de la Parte 2, los tres modelos coincidieron en que se necesitan datos etiquetados y en mencionar el riesgo de privacidad. ChatGPT y Deepseek recomendaron IA predictiva; Gemini propuso un agente más complejo. Esa misma lógica aplica al proyecto GenIA: se necesita IA predictiva entrenada con datos etiquetados del TCGA, y el riesgo de privacidad es aún más delicado por tratarse de datos genómicos.

## Primer riesgo identificado
El riesgo principal es la privacidad y el posible mal uso de los datos genéticos. Aunque el TCGA es un dataset público, los datos genómicos son altamente sensibles y podrían permitir la reidentificación de personas. Además, un modelo con falsos positivos o falsos negativos podría generar diagnósticos erróneos con consecuencias graves para los pacientes. También existe el riesgo de sesgo si el dataset no representa a todas las poblaciones, lo que afectaría la equidad del modelo. Finalmente, el antecedente de Theranos recuerda que cualquier promesa sin sustento científico puede generar daño público y desconfianza.
