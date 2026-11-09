<template lang="pug">
  .curso-main-container.pb-3
    BannerInterno(icono="far fa-question-circle" titulo="Actividad didáctica")
    .container.tarjeta.tarjeta--blanca.p-4.p-md-5
  
      #Actividad                
        <Actividad :cuestionario="cuestionario"/>
  
  </template>

<script>
import Actividad from 'ecored-pkg-fliz/plugin/components/actividad/Actividad.vue'
export default {
  name: 'ActividadDidactica',
  components: {
    Actividad,
  },
  data: () => ({
    cuestionario: {
      tema: 'Gestión de requerimientos e indicadores de desempeño',
      titulo: 'Cuestionario',
      introduccion:
        '<b>Objetivo:</b> evaluar y reforzar su capacidad para reconocer la normativa y los procedimientos relacionados con la gestión de requerimientos, el sistema de calidad y la interpretación, aplicabilidad y reporte de indicadores de gestión en la atención al cliente.',
      barajarPreguntas: true,
      titulo_aprobado: '¡BUEN TRABAJO!',
      titulo_reprobado: 'VUELVA A INTENTARLO.',
      preguntas: [
        {
          id: 1,
          texto:
            '¿Cuál es el propósito principal de la normativa de protección de datos personales en la atención al cliente?',
          imagen: require('@/assets/actividad/imagen1.png'),
          barajarRespuestas: true,
          opciones: [
            {
              id: 'a',
              texto:
                'Garantizar el manejo adecuado de la información personal y los derechos de sus titulares.',
              esCorrecta: true,
            },
            {
              id: 'b',
              texto:
                'Permitir que cualquier colaborador comparta libremente los datos de los clientes.',
              esCorrecta: false,
            },
            {
              id: 'c',
              texto:
                'Reemplazar los procedimientos internos de atención por registros informales.',
              esCorrecta: false,
            },
            {
              id: 'd',
              texto:
                'Limitar el uso de bases de datos únicamente a documentos físicos.',
              esCorrecta: false,
            },
          ],
          mensaje_correcto:
            'Identifica que la normativa busca proteger los datos personales y garantizar los derechos de las personas sobre su información.',
          mensaje_incorrecto:
            'Respuesta incorrecta. Revise nuevamente el contenido del componente formativo e inténtelo otra vez.',
        },
        {
          id: 2,
          texto:
            '¿Cuál de los siguientes conjuntos corresponde a datos personales mencionados en el componente formativo?',
          imagen: require('@/assets/actividad/imagen1.png'),
          barajarRespuestas: true,
          opciones: [
            {
              id: 'a',
              texto:
                'Nombre, documento de identidad, teléfono y correo electrónico.',
              esCorrecta: true,
            },
            {
              id: 'b',
              texto:
                'Código de producto, lote, inventario y fecha de despacho.',
              esCorrecta: false,
            },
            {
              id: 'c',
              texto:
                'Nombre del proveedor, referencia comercial, precio y cantidad.',
              esCorrecta: false,
            },
            {
              id: 'd',
              texto: 'Área de trabajo, horario de atención, meta e indicador.',
              esCorrecta: false,
            },
          ],
          mensaje_correcto:
            'Reconoce que el nombre, el documento, los teléfonos y el correo electrónico son datos que permiten identificar a una persona.',
          mensaje_incorrecto:
            'Respuesta incorrecta. Revise nuevamente el contenido del componente formativo e inténtelo otra vez.',
        },
        {
          id: 3,
          texto:
            'De acuerdo con el componente formativo, ¿a quiénes debe cobijar la política organizacional de protección de datos?',
          imagen: require('@/assets/actividad/imagen1.png'),
          barajarRespuestas: true,
          opciones: [
            {
              id: 'a',
              texto:
                'Únicamente al personal vinculado mediante contrato laboral.',
              esCorrecta: false,
            },
            {
              id: 'b',
              texto:
                'A colaboradores, contratistas, operadores y terceros que tengan acceso a la información.',
              esCorrecta: true,
            },
            {
              id: 'c',
              texto: 'Solamente a los responsables del área de tecnología.',
              esCorrecta: false,
            },
            {
              id: 'd',
              texto:
                'Exclusivamente a las personas encargadas de recibir peticiones y reclamos.',
              esCorrecta: false,
            },
          ],
          mensaje_correcto:
            'Identifica que la responsabilidad sobre el manejo de la información comprende a todas las personas naturales o jurídicas que acceden a ella para realizar labores contratadas.',
          mensaje_incorrecto:
            'Respuesta incorrecta. Revise nuevamente el contenido del componente formativo e inténtelo otra vez.',
        },
        {
          id: 4,
          texto:
            'En el contexto logístico, ¿qué significa la trazabilidad de una mercancía?',
          imagen: require('@/assets/actividad/imagen1.png'),
          barajarRespuestas: true,
          opciones: [
            {
              id: 'a',
              texto:
                'La capacidad de rastrearla a lo largo de la cadena de distribución mediante un número de lote o de serie.',
              esCorrecta: true,
            },
            {
              id: 'b',
              texto:
                'La posibilidad de modificar su precio durante el proceso de almacenamiento.',
              esCorrecta: false,
            },
            {
              id: 'c',
              texto:
                'La clasificación de los productos únicamente por su fecha de vencimiento.',
              esCorrecta: false,
            },
            {
              id: 'd',
              texto:
                'El registro exclusivo de las unidades que llegan al cliente final.',
              esCorrecta: false,
            },
          ],
          mensaje_correcto:
            'Comprende que la trazabilidad permite rastrear las mercancías durante la cadena de distribución a partir de un número de lote o de serie.',
          mensaje_incorrecto:
            'Respuesta incorrecta. Revise nuevamente el contenido del componente formativo e inténtelo otra vez.',
        },
        {
          id: 5,
          texto:
            '¿Cuál de las siguientes opciones representa una ventaja de la trazabilidad total en la cadena de suministro?',
          imagen: require('@/assets/actividad/imagen2.png'),
          barajarRespuestas: true,
          opciones: [
            {
              id: 'a',
              texto:
                'Aumentar la transparencia y reducir la probabilidad de errores de registro.',
              esCorrecta: true,
            },
            {
              id: 'b',
              texto: 'Eliminar la necesidad de controlar las existencias.',
              esCorrecta: false,
            },
            {
              id: 'c',
              texto:
                'Evitar la coordinación con autoridades y organismos pertinentes.',
              esCorrecta: false,
            },
            {
              id: 'd',
              texto: 'Impedir la activación de alertas ante incumplimientos.',
              esCorrecta: false,
            },
          ],
          mensaje_correcto:
            'Reconoce que la trazabilidad contribuye a la transparencia, al control y seguimiento de existencias y a la reducción de errores.',
          mensaje_incorrecto:
            'Respuesta incorrecta. Revise nuevamente el contenido del componente formativo e inténtelo otra vez.',
        },
        {
          id: 6,
          texto:
            'Una empresa necesita conocer en tiempo real las entradas y salidas de los productos almacenados. ¿Qué recurso señala el componente formativo como necesario?',
          imagen: require('@/assets/actividad/imagen2.png'),
          barajarRespuestas: true,
          opciones: [
            {
              id: 'a',
              texto:
                'Un sistema de información para consultar el estado del inventario.',
              esCorrecta: true,
            },
            {
              id: 'b',
              texto: 'Un registro verbal que se actualice al cierre del mes.',
              esCorrecta: false,
            },
            {
              id: 'c',
              texto: 'Un aviso general ubicado en el punto de atención.',
              esCorrecta: false,
            },
            {
              id: 'd',
              texto:
                'Un informe de satisfacción elaborado al finalizar el año.',
              esCorrecta: false,
            },
          ],
          mensaje_correcto:
            'Identifica que un sistema de información permite conocer en tiempo real el estado de las entradas y salidas de los productos.',
          mensaje_incorrecto:
            'Respuesta incorrecta. Revise nuevamente el contenido del componente formativo e inténtelo otra vez.',
        },
        {
          id: 7,
          texto: '¿Cuál opción describe adecuadamente las PQRF?',
          imagen: require('@/assets/actividad/imagen2.png'),
          barajarRespuestas: true,
          opciones: [
            {
              id: 'a',
              texto:
                'Peticiones, quejas, reclamos, sugerencias y felicitaciones.',
              esCorrecta: true,
            },
            {
              id: 'b',
              texto: 'Procesos, calidad, resultados, funciones y reportes.',
              esCorrecta: false,
            },
            {
              id: 'c',
              texto: 'Pedidos, cantidades, registros, formatos y facturas.',
              esCorrecta: false,
            },
            {
              id: 'd',
              texto: 'Procedimientos, quejas, respuestas, fórmulas y fechas.',
              esCorrecta: false,
            },
          ],
          mensaje_correcto:
            'Reconoce los cinco componentes de las PQRF y su relación con los requerimientos y comunicaciones de los usuarios.',
          mensaje_incorrecto:
            'Respuesta incorrecta. Revise nuevamente el contenido del componente formativo e inténtelo otra vez.',
        },
        {
          id: 8,
          texto:
            'Al recibir una PQR, ¿qué debe permitir establecer claramente el formato de recepción?',
          imagen: require('@/assets/actividad/imagen2.png'),
          barajarRespuestas: true,
          opciones: [
            {
              id: 'a',
              texto:
                'La tipología en la que se clasifica la inquietud del cliente.',
              esCorrecta: true,
            },
            {
              id: 'b',
              texto:
                'El indicador financiero que se presentará a la dirección.',
              esCorrecta: false,
            },
            {
              id: 'c',
              texto:
                'La cantidad de productos que se encuentran en inventario.',
              esCorrecta: false,
            },
            {
              id: 'd',
              texto: 'El nivel de cumplimiento de los proveedores externos.',
              esCorrecta: false,
            },
          ],
          mensaje_correcto:
            'Comprende que el formato de recepción permite clasificar de manera clara la solicitud según su tipología.',
          mensaje_incorrecto:
            'Respuesta incorrecta. Revise nuevamente el contenido del componente formativo e inténtelo otra vez.',
        },
        {
          id: 9,
          texto:
            'Según el componente formativo, ¿qué debe hacer la organización cuando no sea posible responder una petición, queja o reclamo dentro del tiempo previsto?',
          imagen: require('@/assets/actividad/imagen3.png'),
          barajarRespuestas: true,
          opciones: [
            {
              id: 'a',
              texto:
                'Informar al peticionario los tiempos de respuesta y las causas de la demora.',
              esCorrecta: true,
            },
            {
              id: 'b',
              texto: 'Cerrar el requerimiento sin comunicar una decisión.',
              esCorrecta: false,
            },
            {
              id: 'c',
              texto:
                'Solicitar que el cliente presente nuevamente la misma solicitud.',
              esCorrecta: false,
            },
            {
              id: 'd',
              texto:
                'Eliminar el registro para evitar que aparezca como pendiente.',
              esCorrecta: false,
            },
          ],
          mensaje_correcto:
            'Identifica que, si no es posible cumplir los tiempos, se debe informar al peticionario sobre los tiempos de respuesta y las causas de la mora.',
          mensaje_incorrecto:
            'Respuesta incorrecta. Revise nuevamente el contenido del componente formativo e inténtelo otra vez.',
        },
        {
          id: 10,
          texto:
            '¿Cuál es el orden del ciclo básico de PQR presentado en el componente formativo?',
          imagen: require('@/assets/actividad/imagen3.png'),
          barajarRespuestas: true,
          opciones: [
            {
              id: 'a',
              texto:
                'Recepción, análisis, distribución, gestión, respuesta, seguimiento e indicadores.',
              esCorrecta: true,
            },
            {
              id: 'b',
              texto:
                'Análisis, respuesta, recepción, indicadores, distribución, gestión y seguimiento.',
              esCorrecta: false,
            },
            {
              id: 'c',
              texto:
                'Recepción, distribución, respuesta, análisis, indicadores, seguimiento y gestión.',
              esCorrecta: false,
            },
            {
              id: 'd',
              texto:
                'Distribución, recepción, seguimiento, gestión, análisis, indicadores y respuesta.',
              esCorrecta: false,
            },
          ],
          mensaje_correcto:
            'Reconoce la secuencia del ciclo de PQR desde la recepción del requerimiento hasta el seguimiento y la generación de indicadores.',
          mensaje_incorrecto:
            'Respuesta incorrecta. Revise nuevamente el contenido del componente formativo e inténtelo otra vez.',
        },
        {
          id: 11,
          texto:
            '¿Cuál de los siguientes objetivos debe orientar las estrategias de atención al cliente, según el componente formativo?',
          imagen: require('@/assets/actividad/imagen3.png'),
          barajarRespuestas: true,
          opciones: [
            {
              id: 'a',
              texto: 'Confianza, puntualidad, integralidad y trazabilidad.',
              esCorrecta: true,
            },
            {
              id: 'b',
              texto: 'Rentabilidad, publicidad, expansión y contratación.',
              esCorrecta: false,
            },
            {
              id: 'c',
              texto: 'Inventario, almacenamiento, transporte y facturación.',
              esCorrecta: false,
            },
            {
              id: 'd',
              texto:
                'Producción, comercialización, financiación y distribución.',
              esCorrecta: false,
            },
          ],
          mensaje_correcto:
            'Identifica los objetivos que orientan las estrategias de atención al cliente y el trámite de sus requerimientos.',
          mensaje_incorrecto:
            'Respuesta incorrecta. Revise nuevamente el contenido del componente formativo e inténtelo otra vez.',
        },
        {
          id: 12,
          texto:
            '¿Qué caracteriza a la norma ISO 9001:2015 en el contexto presentado en el componente formativo?',
          imagen: require('@/assets/actividad/imagen3.png'),
          barajarRespuestas: true,
          opciones: [
            {
              id: 'a',
              texto:
                'Es una norma de Sistemas de Gestión de la Calidad que especifica requisitos para desarrollar programas organizacionales.',
              esCorrecta: true,
            },
            {
              id: 'b',
              texto:
                'Es una norma que establece exclusivamente los tiempos de respuesta de las PQR.',
              esCorrecta: false,
            },
            {
              id: 'c',
              texto:
                'Es un procedimiento destinado únicamente al control de inventarios.',
              esCorrecta: false,
            },
            {
              id: 'd',
              texto:
                'Es un acuerdo comercial que reemplaza los protocolos de servicio.',
              esCorrecta: false,
            },
          ],
          mensaje_correcto:
            'Reconoce que ISO 9001:2015 especifica requisitos para un Sistema de Gestión de la Calidad que las organizaciones pueden utilizar para desarrollar sus programas.',
          mensaje_incorrecto:
            'Respuesta incorrecta. Revise nuevamente el contenido del componente formativo e inténtelo otra vez.',
        },
        {
          id: 13,
          texto:
            '¿Cuál es una característica del sistema de calidad mencionada en el componente formativo?',
          imagen: require('@/assets/actividad/imagen4.png'),
          barajarRespuestas: true,
          opciones: [
            {
              id: 'a',
              texto: 'Mejora de la satisfacción de los consumidores.',
              esCorrecta: true,
            },
            {
              id: 'b',
              texto: 'Reducción de la comunicación interna.',
              esCorrecta: false,
            },
            {
              id: 'c',
              texto:
                'Eliminación de la formación y participación de los trabajadores.',
              esCorrecta: false,
            },
            {
              id: 'd',
              texto: 'Disminución de la capacidad de acceso a los mercados.',
              esCorrecta: false,
            },
          ],
          mensaje_correcto:
            'Identifica que el sistema de calidad contribuye a mejorar la satisfacción de los consumidores, entre otras características.',
          mensaje_incorrecto:
            'Respuesta incorrecta. Revise nuevamente el contenido del componente formativo e inténtelo otra vez.',
        },
        {
          id: 14,
          texto:
            '¿Qué es un protocolo del sistema de calidad, de acuerdo con el componente formativo?',
          imagen: require('@/assets/actividad/imagen4.png'),
          barajarRespuestas: true,
          opciones: [
            {
              id: 'a',
              texto:
                'Un grupo de métodos para asegurar que un producto o servicio cumpla ciertos criterios.',
              esCorrecta: true,
            },
            {
              id: 'b',
              texto:
                'Un listado de datos personales que puede consultar cualquier usuario.',
              esCorrecta: false,
            },
            {
              id: 'c',
              texto:
                'Un informe que presenta exclusivamente los resultados financieros.',
              esCorrecta: false,
            },
            {
              id: 'd',
              texto:
                'Una herramienta para sustituir los acuerdos entre cliente y proveedor.',
              esCorrecta: false,
            },
          ],
          mensaje_correcto:
            'Comprende que el protocolo reúne métodos orientados a asegurar que el producto o servicio cumpla criterios de calidad o requisitos del comprador.',
          mensaje_incorrecto:
            'Respuesta incorrecta. Revise nuevamente el contenido del componente formativo e inténtelo otra vez.',
        },
        {
          id: 15,
          texto:
            '¿Cuál es la finalidad principal de un Acuerdo de Nivel de Servicio (ANS o SLA)?',
          imagen: require('@/assets/actividad/imagen4.png'),
          barajarRespuestas: true,
          opciones: [
            {
              id: 'a',
              texto:
                'Establecer y garantizar condiciones y niveles de calidad del servicio entre cliente y proveedor.',
              esCorrecta: true,
            },
            {
              id: 'b',
              texto:
                'Definir las categorías de datos personales de los colaboradores.',
              esCorrecta: false,
            },
            {
              id: 'c',
              texto:
                'Reemplazar los indicadores de gestión de todas las áreas.',
              esCorrecta: false,
            },
            {
              id: 'd',
              texto:
                'Registrar únicamente las quejas recibidas por una organización.',
              esCorrecta: false,
            },
          ],
          mensaje_correcto:
            'Reconoce que el ANS establece compromisos entre cliente y proveedor y busca mantener y garantizar la calidad del servicio brindado.',
          mensaje_incorrecto:
            'Respuesta incorrecta. Revise nuevamente el contenido del componente formativo e inténtelo otra vez.',
        },
        {
          id: 16,
          texto: '¿Qué representa un KPI o indicador clave de rendimiento?',
          imagen: require('@/assets/actividad/imagen4.png'),
          barajarRespuestas: true,
          opciones: [
            {
              id: 'a',
              texto:
                'Una medida que evalúa cómo una empresa ejecuta su visión estratégica.',
              esCorrecta: true,
            },
            {
              id: 'b',
              texto:
                'Un documento que contiene exclusivamente las funciones de cada colaborador.',
              esCorrecta: false,
            },
            {
              id: 'c',
              texto:
                'Una solicitud que presenta un cliente para manifestar su inconformidad.',
              esCorrecta: false,
            },
            {
              id: 'd',
              texto:
                'Un registro que permite identificar únicamente los productos defectuosos.',
              esCorrecta: false,
            },
          ],
          mensaje_correcto:
            'Identifica que un KPI es una medida que permite evaluar la ejecución de la visión estratégica de la empresa.',
          mensaje_incorrecto:
            'Respuesta incorrecta. Revise nuevamente el contenido del componente formativo e inténtelo otra vez.',
        },
        {
          id: 17,
          texto:
            '¿Cuál de los siguientes elementos hace parte de la estructura de un indicador de gestión presentada en el componente formativo?',
          imagen: require('@/assets/actividad/imagen5.png'),
          barajarRespuestas: true,
          opciones: [
            {
              id: 'a',
              texto:
                'Meta, responsable, forma de cálculo, unidad y periodicidad.',
              esCorrecta: true,
            },
            {
              id: 'b',
              texto: 'Logotipo, eslogan, publicidad, presupuesto y proveedor.',
              esCorrecta: false,
            },
            {
              id: 'c',
              texto: 'Nombre del cliente, dirección, teléfono, correo y firma.',
              esCorrecta: false,
            },
            {
              id: 'd',
              texto:
                'Producto, empaque, transporte, almacenamiento y despacho.',
              esCorrecta: false,
            },
          ],
          mensaje_correcto:
            'Reconoce elementos técnicos de un indicador, como la meta, el responsable, la forma de cálculo, la unidad y la periodicidad.',
          mensaje_incorrecto:
            'Respuesta incorrecta. Revise nuevamente el contenido del componente formativo e inténtelo otra vez.',
        },
        {
          id: 18,
          texto:
            'Una organización formula un objetivo SMART para sus indicadores. ¿Qué conjunto corresponde a los criterios descritos en el componente formativo?',
          imagen: require('@/assets/actividad/imagen5.png'),
          barajarRespuestas: true,
          opciones: [
            {
              id: 'a',
              texto: 'Específico, medible, alcanzable, relevante y a tiempo.',
              esCorrecta: true,
            },
            {
              id: 'b',
              texto: 'Simple, moderno, automático, rentable y tecnológico.',
              esCorrecta: false,
            },
            {
              id: 'c',
              texto: 'Seguro, medible, amplio, recurrente y temporal.',
              esCorrecta: false,
            },
            {
              id: 'd',
              texto: 'Sostenible, múltiple, analítico, rápido y trazable.',
              esCorrecta: false,
            },
          ],
          mensaje_correcto:
            'Identifica los cinco criterios SMART que orientan la formulación de objetivos para los indicadores de gestión.',
          mensaje_incorrecto:
            'Respuesta incorrecta. Revise nuevamente el contenido del componente formativo e inténtelo otra vez.',
        },
        {
          id: 19,
          texto:
            '¿Qué acción hace parte de los pasos para establecer indicadores de gestión?',
          imagen: require('@/assets/actividad/imagen5.png'),
          barajarRespuestas: true,
          opciones: [
            {
              id: 'a',
              texto:
                'Identificar el proceso, área o actividad que se va a medir.',
              esCorrecta: true,
            },
            {
              id: 'b',
              texto:
                'Definir el indicador sin identificar el proceso relacionado.',
              esCorrecta: false,
            },
            {
              id: 'c',
              texto: 'Evitar la recolección de información del proceso.',
              esCorrecta: false,
            },
            {
              id: 'd',
              texto:
                'Suspender la medición después de obtener el primer resultado.',
              esCorrecta: false,
            },
          ],
          mensaje_correcto:
            'Comprende que se debe identificar el proceso, área o actividad que se desea medir y luego definir responsables, objetivos y variables.',
          mensaje_incorrecto:
            'Respuesta incorrecta. Revise nuevamente el contenido del componente formativo e inténtelo otra vez.',
        },
        {
          id: 20,
          texto:
            'Una jefatura necesita explicar qué factores incidieron en los resultados de un KPI e incluir datos históricos para compararlos. ¿Qué tipo de informe debe utilizar?',
          imagen: require('@/assets/actividad/imagen5.png'),
          barajarRespuestas: true,
          opciones: [
            { id: 'a', texto: 'Informe analítico.', esCorrecta: true },
            { id: 'b', texto: 'Informe operativo.', esCorrecta: false },
            { id: 'c', texto: 'Informe estratégico.', esCorrecta: false },
            { id: 'd', texto: 'Informe de recepción.', esCorrecta: false },
          ],
          mensaje_correcto:
            'Distingue el informe analítico porque detalla el KPI y explica los factores que impactaron sus resultados; también puede incluir datos históricos para comparación.',
          mensaje_incorrecto:
            'Respuesta incorrecta. Revise nuevamente el contenido del componente formativo e inténtelo otra vez.',
        },
      ],
      mensaje_final_aprobado:
        '¡Excelente! Ha superado la actividad y demuestra apropiación de los contenidos relacionados con la normativa y el trámite de requerimientos, el sistema de calidad y los indicadores de gestión.',
      mensaje_final_reprobado:
        'Aún puede fortalecer sus conocimientos. Le recomendamos volver a revisar el componente formativo e intentar nuevamente la actividad didáctica.',
    },
  }),
}
</script>
