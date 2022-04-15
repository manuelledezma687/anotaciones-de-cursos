###TESTING Y PRUEBAS DE SOFTWARE.###

##ESTRATÉGIAS DE PRUEBAS.
    Arquitectura, Performance, Usabilidad, Escalabilidad.
    Qué problemas tenemos actualmente? Qué problemas debemos evitar?

##TIPOS DE PRUEBAS.

    *Pruebas Estáticas* 
    Artefactos:
       -- Especificaciones.
       -- Epicas, historias de usuarios, criterios de aceptación.    
       -- código fuente.
       -- Guias de usuarios.
       -- Páginas web.
       -- Contratos, planes de proyecto.
       -- Especificaciones y diseño de arquitectura.
       -- Configuraciones.

     Beneficios:
       -- Detección temprana de defectos.
       -- MAyor eficiencia encontrando defectos.
       -- Identificar defectos que en pruebas dinánicas son más dificiles de encontrar.
       -- Reduce la aparición de defectos.
       -- Reduce el costo de desarrollo y pruebas.
       -- Mejora la comunicacion entre el equipo.

    *Pruebas dinámicas* 
    Estas son las pruebas en periodo de ejecución en si y se pueden dividir:
        -Prueba de Caja Negra: No se ve el código.
          * Casos de Uso.
          * Transición de Estados.
          * Tablas de desiciones.
          * Valores límites.
        -Pruebas de Caja Blanca: Se observa el código.
          * Cobertura de declaración y código.
          * Integraciones entre redes y datos.
        -Pruebas de Caja Gris:
          * Integraciones.
          * Ciclos end to end.
     
    *Pruebas basada en Experiencia.*
    -Pruebas exploratorias.
    -Predicción de errores.


##PRUEBAS ESTÁTICAS VS PRUEBAS DINÁMICAS.
    - Se encuentran defectos en los Artefactos, en las dinámicas en tiempo de ejecución.
    - En las estaticas los defectos se encuentran con menos esfuerzos.
    - En las estaticas se mejoran las consistencias en los artefactos, en las dinánicas se encuentran en los aspectos visibles y de comportamiento.
    - Los defectos encontrados en las pruebas estáticas son más baratos.

##PROCESO DE REVISIÓN.
    -Planeación: Alcance, criterio, identificar.
    -Inicio de la revisión: Distribución de los artefactos o productos de trabajo.
        -Se explica todo el proceso.
        -Se responden preguntas.
    -Reivison individual.
    -Análisis y documentación de problema.
        -Evaluan y documentan caracteristicas de calidad.
        -Evaluar hallazgos contra criterios de salida.
    -Corrección y reporte: Reportan y corrijen los defectos (se hacen seguimiento, se revisan si los criterios de salida se cumplen).

##ROLES.
    Hay revisiones formales e informales por lo tanto no todos los roles aplican en todo momento.
    -Autor : escribe el documento.
    -Administrador: gerencia.
    -Facilitador: Moderador, guia proceso de revisión.
    -Lider de revisión: EL responsable o a cargo.
    -Revisores: Los que revisan
    -Secretario: Toma nota y levanta todos los defectos.

##TIPOS DE REVISIÓN.
    Tienen como objetivo encontrar defectos o problemas.
    -Revisión: informal, tutorial, técnica, inspección.

    -Ad hoc (informal), check list, Escenarios, perspectiva(se comparte opiniones en los involucrados), roles (similar a la perspectiva).

    -Cada revision debe tener objetivos claros, grandes documentos se trabajan en fragmentos pequeños, tiempo de preparacion, las revisiones se pueden
    integrar en las politicas de calidad de la empresa.

##NIVELES DE PRUEBAS
    *Componentes o unitarias* Estas las hace el desarrollador y consta de probar una unidad.
    *Integración* Del mismo modo, pero evaluando el comportamiento entre componentes.
    *Sistemas* En esta capa entramos los testers con pruebas de caja negra o incluso de caja blanca.
    *Aceptación* Las hace el cliente o el PO, y estás se dividen entre pruebas alpha y beta.

##PRUEBAS RELACIONADAS AL CAMBIO.
    Por cada iteración debemos procurar que lo que funciona siga funcionando en el sistema, adémas de retestear funcionalidades que estaban en 
    pendiente con respecto a un defecto.
    *Pruebas de confirmación* Verifican que una funcionabilidad fue corregida.
    *Pruebas de regresión* Verifican que el sistema siga funcionando en base a los nuevos cambios introducidos, por lo general la mayor parte
    se automatiza.

##CLASIFICACIÓN DE LAS PRUEBAS.
    *Funcionales* Lo que el sistema hace: Unitarias, integrales, sistema y aceptación.
    *NO-Funcionales* Cómo lo hace el sistema? Performance, carga, estrés, usabilidad, fiabilidad, operacional, deployment, portabilidad, preparación.

##BUGS.
    *Funcionales* Comportamiento no esperado de los elementos.
    *Visual* Logotipo, diseño deformado, imágenes rotas.
    *Crash* Páginas rotas, no continua la página.
    *Contenido* Gramática, traducciones.
    *Performance* Carga de la página.

##DEFINAMOS CALIDAD.
    la calidad es la que satisface la necesidad del cliente, entre sus verbos están: Calificar, enumerar, certificar, definir patrones de medición, compara,
    mediciones del producto, aprueba o confirma.
    El analista funcional --> requerimientos del Product Owner.

    *QA* Asegura la calidad del proceso.
    *QC* Asegura la calidad del producto.

##CICLO DEMING.
    Planifica --> Hace --> Evalúa --> Ajustes.

##EL TESTER Y SUS VARIANTES.
    *El tester* 
    - Analiza requisitos.
    - Confecciona pruebas.
    - Diseña Casos de Prueba.
    - EStablece ambientes de prueba.
    - Ejecuta casos.
    - Crea set de datos de pruebas.

    *Especialidades en el testing*
    - Automation Tester: Perfil de programador, automatiza pruebas.
    - Security Tester: Protocolos y standares.
    - Data Science Tester: Análisis y limṕieza.
    - Tester manual: Pensamiento lateral.
    - SDET: Integración.
    - Devops: Entrega, soporte.
    - QA: Procesos de calidad.
    - QC: Soluciones y estratégias de calidad.

##CICLO BÁSICO DEL SOFTWARE.
    Definición de Objetivos --> Análisis de requerimientos --> Diseño --> Programación --> Pruebas de Verificación 
    --> Pruebas Beta --> Implementación --> Mantenimiento.

##GESTIÓN DE PRUEBAS.
    Planeación --> Monitoreo --> Análisis --> Diseño --> Implementación --> Ejecución --> Finalización --> Reportes.

##EL RETRABAJO.
    *Retraso* 
    -Falta de documentación.
    -Falta de capacitación.
    -Falta de herramientas.
    -Falta de comunicación.

    *Acciones de control*
    - Identificar un riesgo.
    - Idenfiticar falta de ambientes.
    - Si el contexto de salida no se cumple.

##ERROR, FALLA Y DEFECTO.
    *ERROR* Equivocación humana.
    *DEFECTO* Causa producida por el error en el sistema.
    *FALLO* Consecuencia dada por el defecto encontrado en el sistema.

##GESTIÓN DEL BUG.
    Reporte --> Desarrollador --> Reparación --> Status Arreglado --> confirmado --> se cierra.

##SUGERENCIAS CONVERTIDAS EN DEFECTOS.
    - Detiene el proceso.
    - Hace lenta la operación.
    - Deja cometer muchos errores al usuario.
    - No funciona sin internet.

##EL DEBUG.
    Revisión Línea a linea, observar comportamiento.
    Herramientas: Debugger, manual, Local/remoto.
    Mensajes en la consola, compilación, verificaciones sintácticas y lógicas.

##TÉCNICAS DE DEPURACIÓN.
    Reportes: Previene ataques.
    Logs: rastreos, historial.
    Debuggin: Inspección.

##FASES DE LA DEPURACIÓN.
    - Modelo que falla --> breakpoints.
    - Diseñar matriz de pruebas.
    - Datos de pruebas.
    - Inspección.

##LENGUAJE GHERKIN.
    Es un pseudocódigo utilizado en programación para definir comportamientos en el sistema, es simple, reduce el tiempo de comprensión
    y va de la mano con las historias de usuario.
    Ejemplo:
    FEATURE (Atributo)|SCENARIO (Escenario)|BACKGROUND|GIVEN (requerimientos)|WHEN (cuando)|THEN (entonces)|AND (y)|

##KPI.
    Indicadores claves.
    Recopilación de datos --> Agrupamiento y clasificación --> Comportamiento --> Informes.    
    *Medición* / CAntidad de tareas estipuladas y realizadas.

##OTROS INFORMES.
    Avance de pruebas.
    Cobertura de la ejecución del test plan.
    Bugs corregidos vs reportados.
    Distribución de tipos de defectos.
    Tiempo para arreglar defectos.
    Trazabilidad de pruebas.
    
    



