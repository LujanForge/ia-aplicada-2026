Política de datos del proyecto Cerbero
1. Alcance

Esta política cubre todos los datos que el proyecto Cerbero usa para entrenar y operar un modelo de IA que detecta indicios de cáncer a partir de datos genéticos.

Datos sensibles: D1 (expresión génica y mutaciones de TCGA), D2 (datos clínicos de TCGA), D3 (muestra genética del paciente) y D6 (resultado de la predicción).
Datos personales: D4 (identificación del paciente: nombre, teléfono, edad), D5 (datos del médico usuario) y D7 (registros de acceso al sistema).
Datos no personales: D8 (métricas del modelo).
El dato de mayor riesgo es D3, porque identifica a la persona de forma permanente y revela información de su familia.
2. Ciclo de vida

El recorrido completo de los datos está en ciclo_vida_dato_proyecto.png (tabla del ciclo de vida y recorrido de D3).

Captura: recepción del paciente y toma de muestra. Responsable: Recepcionista / Secretaria.
Almacenamiento: separación de datos personales y genómicos con ID seudónimo en una base de datos en la nube. Responsable: Responsable de Infraestructura y Seguridad.
Uso: entrenamiento del modelo con TCGA y análisis de la muestra del paciente. Responsable: Científicos de datos del equipo.
Compartición: envío del resultado al médico tratante usando solo el ID del paciente. Responsable: Líder del proyecto.
Retención: conservación durante el plazo del seguimiento del caso. Responsable: Responsable de Infraestructura y Seguridad.
Eliminación: borrado seguro de datos y muestras, incluidos los respaldos en la nube. Responsable: Oficial de Seguridad.
3. Normativa aplicable

El detalle está en matriz_cumplimiento_proyecto.xlsx.

LFPDPPP (DOF 20/03/2025): es obligatoria porque el proyecto trata datos personales sensibles en México. Aplican los principios del art. 5, el consentimiento expreso y por escrito (art. 8), el aviso de privacidad (arts. 14 y 15) y el derecho de oposición a decisiones automatizadas (art. 26, fr. II).
Ley de IA de la UE (Reglamento 2024/1689): no es obligatoria en México, pero se toma como referencia porque Cerbero sería un sistema de alto riesgo (art. 6(1) y anexo I) si se usara en Europa.
NIST AI RMF 1.0: es voluntario; se usa como guía para gestionar riesgos de IA que la ley mexicana no cubre, como la evaluación de sesgos.
4. Controles comprometidos
Consentimiento expreso y por escrito, y aviso de privacidad que indique el uso de IA y cómo pedir revisión humana. Responsable: Recepcionista / Secretaria.
Captura solo de los datos necesarios y revisión del formulario cada semestre. Responsable: Líder del proyecto.
Cifrado, acceso por rol, ID seudónimo y acuerdos de confidencialidad con el proveedor de nube y el laboratorio. Responsable: Responsable de Infraestructura y Seguridad.
Ficha de riesgos antes de cualquier prueba con pacientes. Responsable: Líder del proyecto.
Medición de sesgo por sexo y edad, y validación del modelo con población mexicana. Responsable: Científicos de datos del equipo.
Revisión médica obligatoria de cada predicción antes de comunicarla. Responsable: Médico tratante.
Plazo de retención de 2 años, revisión cada 6 meses y borrado seguro con acta. Responsable: Oficial de Seguridad.
5. Manejo de datos con herramientas de IA

Estas reglas aplican al usar ChatGPT, Gemini, Deepseek, Dify u otras herramientas de IA durante todo el curso.

Prohibido: ingresar D3, D4, D5, D6 o D7, ni ningún dato que permita identificar a un paciente o a un médico real, aunque sea solo una parte.
Prohibido: pegar registros completos por paciente de D1 o D2, aunque vengan de TCGA y estén desidentificados.
Permitido: pedir ayuda con código, conceptos, errores o redacción, usando datos ficticios o sintéticos creados por el equipo.
Permitido: compartir datos agregados, como nombres de genes, estadísticas generales o las métricas del modelo (D8).
Condición: antes de usar cualquier dato real, se debe seudonimizar o agregar, y revisar que la herramienta no lo use para entrenar sus modelos.
Condición: todo uso de IA se registra en la declaración de uso de IA de cada entrega.
6. Revisión
Esta política se revisa cada 6 meses o antes, si cambia el proyecto, los datos que se usan o la ley aplicable.
La revisa todo el equipo (Luis, Enrique y Daniel) y la aprueba el Líder del proyecto.
Cada cambio se registra con un commit en el repositorio, indicando qué se modificó.
Versión 1.0, octubre de 2026.
