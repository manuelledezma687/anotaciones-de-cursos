
# TESTING Y PRUEBAS DE SOFTWARE.

## LAS PRUEBAS.

    Las pruebas son un proceso que no se limita sólo a la ejecución de las pruebas,
    esta última es un subproceso, las pruebas tienen distintos objetivos entre ellos:
    
    - Prevenir la aparación de defectos.
    - Verificar el cumplimiento de requerimientos.
    - Generar confianza sobre los niveles de calidad del objeto bajo prueba.
    - Encontrar defectos y fallos para corregirlos.
    - Proveer información para toma de desiciones.

## ESTRATÉGIAS DE PRUEBAS.

    Arquitectura, Performance, Usabilidad, Escalabilidad.
    Qué problemas tenemos actualmente? Qué problemas debemos evitar?

## PRUEBAS VS DEBUG.
    
    Las pruebas se identifica un defecto en la aplicación, se establece donde ocurre 
    y como ocurre, mientras que en la depuración además de indetificar, se localiza y 
    se corrige el defecto (con el objetivo de ser corregido).

## EL DEBUG.

    Revisión Línea a linea, observar comportamiento.
    Herramientas: Debugger, manual, Local/remoto.
    Mensajes en la consola, compilación, verificaciones sintácticas y lógicas.

## TÉCNICAS DE DEPURACIÓN.

    Reportes: Previene ataques.
    Logs: rastreos, historial.
    Debuggin: Inspección.

## FASES DE LA DEPURACIÓN.

    - Modelo que falla --> breakpoints.
    - Diseñar matriz de pruebas.
    - Datos de pruebas.
    - Inspección.

## ERROR, FALLA Y DEFECTO.

    *ERROR* Equivocación humana.
    *DEFECTO* Causa producida por el error en el sistema.
    *FALLO* Consecuencia dada por el defecto encontrado en el sistema.

## CAUSA RAÍZ DE UN DEFECTO.
    Encontrar que está provocando que se produzcan defectos en un producto.
    - Falta de documentación, comunicación, preparación, mal endendimiento de 
    requerimientos.

## 7 PRINCIPIOS DE LAS PRUEBAS DE SOFTWARE.

    - Las pruebas muestran la presencia de defectos, na la ausencia.
    - Pruebas exhaustivas son imposibles.
    - Pruebas tempranas ahorran tiempo y dinero.
    - Los defectos se agrupan.
    - Cuidado con la paradoja de los pesticidas.
    - Las pruebas dependen del contexto.
    - Ausencia de errores es una falacia.

## PROCESO DE PRUEBAS.
    No hay una estructura global, pueden fusionarse o no algunos pasos.
    - Planeación: Se fijan los objetivos, recursos,
    - Monitoreo y control: Progreso (actual y esperando).
    - Análisis: Qué probar? alcance? analizar historias de usuarios, riezgos, etc.
    - Diseño: Se diseñan los casos de pruebas, identificar data de prueba, necesidades de 
      ambiente de pruebas.
    - Implementación: Construir ambiente de pruebas, suite de pruebas.
    - Ejecución: Se ejecutan las pruebas y se recojen resultados, medir resultados, 
      reportar defectos.
    - Finalización: Elaborar informes y reportes.

## ARTEFACTOS DE PRUEBAS.

    - Planeación: 1 o más planes de pruebas.
    - Monitoreo y control: Reportes de pruebas y status.
    - Análisis: Definición y priorización de condiciones de pruebas.
    - Diseño: Casos de pruebas.
    - Implementación: Procedimiento de pruebas, suite de pruebas.
    - Ejecución: Resultados de pruebas, reportes de defectos y documentación.
    - Finalización: Resumén reportes de pruebas.

## NIVELES DE PRUEBAS.

    *Componentes o unitarias* Estas las hace el desarrollador y consta de probar una unidad.
    *Integración* Del mismo modo, pero evaluando el comportamiento entre componentes.
    *Sistemas* En esta capa entramos los testers con pruebas de caja negra o incluso de caja blanca.
    *Aceptación* Las hace el cliente o el PO, y estás se dividen entre pruebas alpha 
    (instalaciones de la organización)y beta (mismos usuarios pero desde su ubicación).
    Cada nivel de prueba tiene objetivos específicos, base de pruebas, objeto de pruebas, defectos
    típicos, enfoque y responsabilidades.

## PRUEBAS RELACIONADAS AL CAMBIO.

    Por cada iteración debemos procurar que lo que funciona siga funcionando en el sistema, 
    adémas de retestear funcionalidades que estaban en pendiente con respecto a un defecto.
    *Pruebas de confirmación* Verifican que una funcionabilidad fue corregida.
    *Pruebas de regresión* Verifican que el sistema siga funcionando en base a los nuevos 
    cambios introducidos, por lo general la mayor parte se automatiza.

## ACTIVADORES PARA LAS PRUEBAS DE MANTENIMIENTO.
    Las pruebas estan orientadas a mantenimiento, ya no están en ambiente de pruebas.
    - Modificaciones en el código.
    - Migraciones.
    - Actualizaciones de versiones.
    - Agregar o retirar componentes o interfaces.


## CLASIFICACIÓN DE LAS PRUEBAS.

    *Funcionales* Lo que el sistema hace: Unitarias, integrales, sistema y aceptación.
    *NO-Funcionales* Cómo lo hace el sistema? Performance, carga, estrés, usabilidad, 
    fiabilidad, operacional, deployment, portabilidad, preparación.


## PRUEBAS ESTÁTICAS VS PRUEBAS DINÁMICAS.

    - Se encuentran defectos en los Artefactos, en las dinámicas en tiempo de ejecución.
    - En las estaticas los defectos se encuentran con menos esfuerzos.
    - En las estaticas se mejoran las consistencias en los artefactos, en las dinánicas 
    se encuentran en los aspectos visibles y de comportamiento.
    - Los defectos encontrados en las pruebas estáticas son más baratos.

## TIPOS DE PRUEBAS.

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
          * Casos de Uso. Generalmente usan lenguaje de negocio, sirven como base para hacer las
        pruebas de aceptación, se identifican precondiciones y postcondiciones, se hace un camino feliz 
        y luego 3 o más exntesiones donde hay escenarios distintos.
          * Transición de Estados. Se definen los estados del software, los eventos que causan
        las transiciones, acciones resultantes.
          * Tablas de desiciones. Se plantean distintas situaciones en datos de entrada 
        por cada combinaciones de entradas salen distintas condiciones de salida.    
        ( Verdadero o falso, etc)
          * Particiones de equivalencias. Se dividen en diferentes particiones o clases,
        cada una comparte el mismo comportamiento, una partición por cada ramificación,
        adicional se incluye una partición inválida que no está en los requermientos.
        Se debe cumplir cada partición al menos una vez.
          * Valores límites. Valor mínimo y máximo para límites, agregar además el valor 
        anterior y siguiente cada límite.
        -Pruebas de Caja Blanca: Se observa el código.
          * Cobertura de sentencias. Se necesita probar al menos 1 vez cada sentecia.
          * Cobertura de decisión. Se necesita probar al menos 1 vez cada decisión 
            (verdadera y falsas).
            Podemos afirmar que el 100% de las coberturas de desición son el 100% de 
            cobertura de sentecia pero no al revés.
        -Pruebas de Caja Gris:
          * Integraciones.
          * Ciclos end to end.
     
    *Pruebas basada en Experiencia.*
    El probador tiene acceso a amplio conocimiento técnico y de negocio y puede optar por las
    siguientes pruebas.
    - Pruebas exploratorias. No se diseñan casos de pruebas, se va navegando y explorando la
    Aplicación, más adecuadas cuando no hay requerimientos o son muy pocos.
    - Predicción de errores. Pensar en todo aquello que puede fallar y escribir casos de pruebas
    que ayuden a encontrar ese defecto.
    - Pruebas basadas en lista de comprobación. Check list en cosas que se van a comprobar.

## PROCESO DE REVISIÓN.

    -Planeación: Alcance, criterio, identificar.
    -Inicio de la revisión (monitoreo y control): Distribución de los artefactos o 
    productos de trabajo.
        -Se explica todo el proceso.
        -Se responden preguntas.
    -Reivison individual.
    -Análisis y documentación de problema.
        -Evaluan y documentan caracteristicas de calidad.
        -Evaluar hallazgos contra criterios de salida.
    -Corrección y reporte: Reportan y corrijen los defectos (se hacen seguimiento, 
    se revisan si los criterios de salida se cumplen).

## ROLES.

    Hay revisiones formales e informales por lo tanto no todos los roles aplican en todo momento.
    -Autor : escribe el documento.
    -Administrador: gerencia.
    -Facilitador: Moderador, guia proceso de revisión.
    -Lider de revisión: EL responsable o a cargo.
    -Revisores: Los que revisan
    -Secretario: Toma nota y levanta todos los defectos.

## TIPOS DE REVISIÓN.

    Tienen como objetivo encontrar defectos o problemas.
    -Revisión: informal, tutorial, técnica, inspección.

    - Ad hoc (informal), check list, Escenarios, perspectiva(se comparte opiniones 
    en los involucrados), roles (similar a la perspectiva), no se basa en un proceso 
    documentado. uso común en entorno ágil.

    - Tutorial(Walkthrough): La preparación individual es opcional, el escriba es obligatorio, 
    el checklist es opcional, se produce documentación, se enfoca en encontrar defectos, 
    los potenciales defectos son registrados.

    - Revisión técnica: Se enfoca en hacer consensos y detectar potenciales problemas, 
    expertos técnicos, el escriba es obligatorio, el checklist es opcional.

    - Inspección: Se enfoca en detectar potenciales problemas, checklist obligatorio, 
    preparación obligatoria, proceso formal y definido, criterios de entrada y salida para la 
    inspección, roles claramente definidos. Es liderada por un facilitador o moderador entrenado.

    - Cada revision debe tener objetivos claros, grandes documentos se trabajan en fragmentos pequeños, 
    tiempo de preparacion, las revisiones se pueden
    integrar en las politicas de calidad de la empresa, ni el Autor ni el escriba pueden liderar.

## HERRAMIENTAS DE APOYO DE PRUEBAS.

    Herramientas que nos ayuden al analisis, ejecución (automatizador).
    Son más eficientes.

## CLASIFICACIÓN DE LAS HERRAMIENTAS.

    Herramientas para la gestión:
    Herramientas de gestión de pruebas y ciclo de vida de desarrollo (ALM).
    Herramientas de gestión de requerimientos.
    Herramientas de gestión de defectos (ideal para desarrolladores).
    Herramientas de gestión de configuración.
    Herramientas de integración contínua. (dev)
    -Herramientas para pruebas estáticas --> cobertura de código.
    Herramientas para pruebas de rendimiento (análisis dinámico).

## LA AUTOMATIZACIÓN.

    Son dificiles de construir pero fácil de ejecutar, más eficientes, más mantenibles.
    Las personas subestiman el esfuerzo requerido para mantener los activos de pruebas
    generados.
    Una desventaja es la dependencía de la herramienta. Problemas con el proveedor o incluso
    de compatibilidad.

## NIVELES DE INDEPENDENCIA.

    Probadores no independientes.
    Probadores/ desarrolladores independientes en el equipo (pruebas cruzadas).
    Equipo de pruebas dentro de la organización.
    Equipo de pruebas fuera de la organización.

    Entre sus beneficios:
    Usan otro enfoque y son roles con habilidades diferentes.
    Verifica, cuestiona y refuta suposiciones durante la especificación 
    de requerimientos.
    No hay presión de la compañía o compañeros.

    Entre sus contra:
    Se aisla del equipo, pueden no sentirse responsables de la calidad los desarrolladores.
    Se ve como un cuello de botella para la madurez de la aplicación.
    Pueden no tener cierta información a la mano al momento de dudas.

## LIDER DE PRUEBA VS PROBADORES.

    El lider: 
    Desarrollar y revisar una política de estrategias de pruebas.
    Escribir y actualizar plan de pruebas.
    Planificación de pruebas.
    Seguimiento, seleccionar y diseñar métricas para el seguimiento.
    Motivar, promover y desarrollar habilidades de los probadores.

    Probadores: 
    Revisar y contribuir al plan de pruebas.
    Diseñar e implementar casos de pruebas.
    Preparar y buscar datos de pruebas.
    Automatizar pruebas.

## PLAN DE PRUEBAS.

    Se trabaja durante todo el ciclo de pruebas, actividad contínua.
    Se ṕuede documentar un plan maestro y otros separados para niveles de pruebas.
    Incluye alcance, objetivos y riesgos.
    Presupuesto para actividades de pruebas.
    Nivel de detalle de la documentación.
    Recursos.

## ENFOQUE DE PRUEBAS.

    Analítica: 
    Factores como requerimientos, riesgos. 
    Basada en Modelos: 
    Características no funcionales como negocios, estados.
    Metodica: 
    Definen paso a paso todo, se sigue el proceso.
    Cumplimientos de procesos: 
    Se analiza, diseña e implementa pruebas, basada en standares externos.
    Aversión a la regresión:
     NO se introduce regresion en la aplicación, sino que se prueba todo.
    Dirigida, se basa con guía o asesoramiento de un experto en el tema.
    Reactiva, se reacciona a los cambios, a como llegan vamos viendo y evaluando.

## CRITERIOS DE ENTRADA Y SALIDA.

    Cuando una prueba puede iniciar y cuando puede finalizar: 
    Definición de listo (Historias de usuario lista para abordar), Definición de completado.

## CRONOGRAMA DE PRUEBAS.
    
    Define cuando se van a ejecutar de pruebas, determinar dependencias y priorizaciones,
    Pruebas de regresión, el orden de las pruebas.
    Ejemplo:
    |CASOS DE PRUEBA|PRIORIDAD| DEPENDENCIA
        CASO 1              3
        CASO 2              1
        CASO 3              7
        CASO 4              8       CASO 3
        CASO 5              9       CASO 1

    Se deben ejecutar primeros los casos dependientes de las pruebas de prioridad más alta,
    quedando así el orden : 1,5,3,4,2

##FACTORES QUE INFLUENCIAN EL ESFUERZO DE PRUEBAS.
    
    Características del producto:
    - Riesgo asociado al producto.
    - Calidad de base de pruebas.
    - Complejidad del producto.
    - Nivel de Documentación.
    - Requerimientos.

    Características del proceso de desarrollo:
    - Estabilidad del equipo.
    - Presión del tiempo.

    Características de las personas:
    - Habilidades.
    - Experiencia.
    - Cohesión y liderazgo del equipo.

    Resultado de las pruebas:
    - Cantidad y severidad de los defectos.
    - El retrabajo.

## TÉCNICAS DE ESTIMACIÓN DE PRUEBAS.

    - Basada en métricas: se estima en base a métricas de proyectos similares.
    BurnDown: gráficas que miden el esfuerzo y el tiempo en tareas.
    - Técnia basada en expertos: Basada en la experiencia de los que harán el desarrollo.
    Votación entre miembros del equipo, se confrota a las personas que votan o muy bajo o 
    muy alto para determinar sus razones y luego se somete de vuelta a votación 
    (se puede votar hasta 3 veces para determinar).

## MONITOREO Y CONTROL.

    - Repriorización de pruebas.
    - Cambiar el cronograma de pruebas.
    Metricas usadas:
    % de trabajo en preparación de ambientes de pruebas.
    % en ejecución.
    Información de defectos.
    Cobertura de las pruebas.
    Costos de las pruebas.

## ARMADO DE REPORTES DE PRUEBAS.

    PROPÓSITO: Resumir y comunicar información de las actividades de prueba, durante y al finalizar
    las pruebas.
    CONTENIDO: 
    - Resumen de las pruebas realizadas.
    - Desviaciones con respecto al plan.
    - Estatus del producto y calidad.
    - Impedimentos.
    - Metricas de defectos, casos de pruebas, cobertura, etc.
    - Riesgos residuales.
    - Artefactos de trabajo producidos.
    AUDIENCIA:
    - Equipo de pruebas.
    - Equipo de desarrollo.
    - Usuarios de negocio.
    - Involucrados en el proyecto.
    Informe de progreso: resumen de las pruebas que se están ejecutando (todavía en ejecución).
    Informe de resumen de pruebas: Informe que se hace al final.

## GESTIÓN DE CONFIGURACIÓN.

    Elementos de software únicos, versionados y con seguimiento.
    Elementos de pruebas referenciados, versionados,etc.
    Documentación y elementos del software referenciados de manera clara.

## PRUEBAS BASADAS EN RIESGOS.

    Riesgos del producto: Interfaz, tecnología, etc.
    Riesgos del proyecto: Riesgos de retraso, presupuesto, de tiempo, etc.

##GESTIÓN DE DEFECTOS.
    Al momento de encontrar un defecto debemos comprobar la presencia del mismo probando
    varias veces, para elaborar un reporte de defectos, debemos acotar lo siguiente:
    

    |IDENTIFICADOR|TITULO|FECHA Y AUTOR|IDENTIFICADOR DEL ELEMENTO DE PRUEBA|FASE DE 
    CICLO DE VIDA DE DESARROLLO|PASOS PARA REPRODUCIRLO|RESULTADO ACTUAL Y 
    ESPERADO|IMPACTO|PRIORIDAD|ESTADO

##CICLO DE VIDA DEL BUG O DEFECTO.

    Reporte --> Desarrollador --> Reparación --> Status Arreglado --> confirmado --> se cierra.

## SUGERENCIAS CONVERTIDAS EN DEFECTOS.

    - Detiene el proceso.
    - Hace lenta la operación.
    - Deja cometer muchos errores al usuario.
    - No funciona sin internet.

## BUGS.

    *Funcionales* Comportamiento no esperado de los elementos.
    *Visual* Logotipo, diseño deformado, imágenes rotas.
    *Crash* Páginas rotas, no continua la página.
    *Contenido* Gramática, traducciones.
    *Performance* Carga de la página.

## DEFINAMOS CALIDAD.

    la calidad es la que satisface la necesidad del cliente, entre sus verbos están: 
    Calificar, enumerar, certificar, definir patrones de medición, compara,
    mediciones del producto, aprueba o confirma.
    El analista funcional --> requerimientos del Product Owner.

    *QA* Asegura la calidad del proceso.
    *QC* Asegura la calidad del producto.

## CICLO DEMING.

    Planifica --> Hace --> Evalúa --> Ajustes.

## EL TESTER Y SUS VARIANTES.

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

## CICLO BÁSICO DEL SOFTWARE.

    Definición de Objetivos --> Análisis de requerimientos --> Diseño --> 
    Programación --> Pruebas de Verificación 
    --> Pruebas Beta --> Implementación --> Mantenimiento.

## EL RETRABAJO.

    *Retraso* 
    -Falta de documentación.
    -Falta de capacitación.
    -Falta de herramientas.
    -Falta de comunicación.

    *Acciones de control*
    - Identificar un riesgo.
    - Idenfiticar falta de ambientes.
    - Si el contexto de salida no se cumple.

## LENGUAJE GHERKIN.

    Es un pseudocódigo utilizado en programación para definir comportamientos 
    en el sistema, es simple, reduce el tiempo de comprensión
    y va de la mano con las historias de usuario.
    Ejemplo:
    FEATURE (Atributo)|SCENARIO (Escenario)|BACKGROUND|GIVEN (requerimientos)|
    WHEN (cuando)|THEN (entonces)|AND (y)|

## KPI.

    Indicadores claves.
    Recopilación de datos --> Agrupamiento y clasificación --> Comportamiento --> Informes.    
    *Medición* / CAntidad de tareas estipuladas y realizadas.

## OTROS INFORMES.

    Avance de pruebas.
    Cobertura de la ejecución del test plan.
    Bugs corregidos vs reportados.
    Distribución de tipos de defectos.
    Tiempo para arreglar defectos.
    Trazabilidad de pruebas.
    
