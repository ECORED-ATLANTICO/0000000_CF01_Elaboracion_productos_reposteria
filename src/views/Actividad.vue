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
      tema:
        'Reconociendo mi taller ideal: diagnóstico de BPM, equipos y materias primas.',
      titulo: 'Cuestionario',
      introduccion:
        '<b> Objetivo:</b> evaluar la comprensión de los conceptos fundamentales sobre normativa, identificación de equipos y selección de materias primas en un entorno simulado de producción de repostería, mediante el análisis crítico de un caso y la aplicación de cuestionarios de verificación.',
      barajarPreguntas: true,
      titulo_aprobado: '¡BUEN TRABAJO!',
      titulo_reprobado: 'VUELVA A INTENTARLO',
      preguntas: [
        {
          id: 1,
          texto: '¿Qué establece la Ley 9 de 1979 en Colombia?',
          imagen: require('@/assets/actividad/imagen1.png'),
          barajarRespuestas: true,
          opciones: [
            {
              id: 'a',
              texto:
                'Las normas generales para la higiene en la manipulación de alimentos y el Código Sanitario Nacional.',
              esCorrecta: true,
            },
            {
              id: 'b',
              texto: 'El código de colores para la separación de residuos.',
              esCorrecta: false,
            },
            {
              id: 'c',
              texto:
                'Las normas para la certificación de negocios de repostería.',
              esCorrecta: false,
            },
            {
              id: 'd',
              texto: 'Los requisitos para la elaboración de masas hojaldradas.',
              esCorrecta: false,
            },
          ],
          mensaje_correcto:
            'Muy bien, la Ley 9 de 1979 (Código Sanitario Nacional) establece las normas generales para la protección del medio ambiente y la higiene en la manipulación de alimentos.',
          mensaje_incorrecto:
            'Respuesta incorrecta, revise nuevamente el contenido del componente formativo.',
        },
        {
          id: 2,
          texto:
            '¿Cuál es el tipo de harina más recomendado para la elaboración de bizcochos esponjosos?',
          imagen: require('@/assets/actividad/imagen2.png'),
          barajarRespuestas: true,
          opciones: [
            {
              id: 'a',
              texto: 'Harina de fuerza (alta en gluten).',
              esCorrecta: false,
            },
            { id: 'b', texto: 'Harina de maíz.', esCorrecta: false },
            {
              id: 'c',
              texto: 'Harina floja (baja en gluten).',
              esCorrecta: true,
            },
            { id: 'd', texto: 'Harina de almendra.', esCorrecta: false },
          ],
          mensaje_correcto:
            'Correcto, las grasas sólidas vegetales (manteca) se utilizan en repostería tradicional y en algunas masas para aportar una textura crujiente.',
          mensaje_incorrecto:
            'Respuesta incorrecta, revise nuevamente el contenido del componente formativo.',
        },
        {
          id: 3,
          texto:
            '¿Cuál es la función de las grasas sólidas vegetales (manteca) en repostería?',
          imagen: require('@/assets/actividad/imagen3.png'),
          barajarRespuestas: true,
          opciones: [
            {
              id: 'a',
              texto: 'Aportar un sabor lácteo característico.',
              esCorrecta: false,
            },
            {
              id: 'b',
              texto: 'Aportar una textura crujiente a algunas masas.',
              esCorrecta: true,
            },
            {
              id: 'c',
              texto: 'Actuar como el principal agente leudante.',
              esCorrecta: false,
            },
            {
              id: 'd',
              texto: 'Aumentar el contenido de humedad del producto final.',
              esCorrecta: false,
            },
          ],
          mensaje_correcto:
            'Así es. Las grasas solidas aportan una textura crujiente a algunas masas.',
          mensaje_incorrecto:
            'Respuesta incorrecta, revise nuevamente el contenido del componente formativo.',
        },
        {
          id: 4,
          texto:
            '¿Cuál es la diferencia técnica entre el bicarbonato de sodio y el polvo de hornear?',
          imagen: require('@/assets/actividad/imagen4.png'),
          barajarRespuestas: true,
          opciones: [
            {
              id: 'a',
              texto:
                'El bicarbonato no necesita un ácido para activarse, el polvo de hornear sí.',
              esCorrecta: false,
            },
            {
              id: 'b',
              texto:
                'El bicarbonato se usa solo para masas fritas y el polvo de hornear solo para masas horneadas.',
              esCorrecta: false,
            },
            {
              id: 'c',
              texto:
                'El bicarbonato necesita un ácido para activarse, mientras que el polvo de hornear contiene su propio ácido y se activa con líquido y calor.',
              esCorrecta: true,
            },
            {
              id: 'd',
              texto:
                'El bicarbonato es un leudante biológico y el polvo de hornear es químico.',
              esCorrecta: false,
            },
          ],
          mensaje_correcto:
            'Excelente, el bicarbonato de sodio necesita de un ácido (como jugo de limón, yogur o cacao) para activarse y producir gas. El polvo de hornear es el que contiene su propio ácido y se activa con líquido y calor.',
          mensaje_incorrecto:
            'Respuesta incorrecta, revise nuevamente el contenido del componente formativo.',
        },
        {
          id: 5,
          texto: '¿Cuál es la función principal de un abatidor de temperatura?',
          imagen: require('@/assets/actividad/imagen5.png'),
          barajarRespuestas: true,
          opciones: [
            {
              id: 'a',
              texto:
                'Mantener los alimentos a temperatura ambiente de forma estable.',
              esCorrecta: false,
            },
            {
              id: 'b',
              texto:
                'Enfriar los alimentos calientes rápidamente para evitar la proliferación bacteriana.',
              esCorrecta: true,
            },
            {
              id: 'c',
              texto:
                'Calentar los alimentos de manera uniforme mediante convección.',
              esCorrecta: false,
            },
            {
              id: 'd',
              texto:
                'Enfriar los alimentos lentamente para preservar su sabor.',
              esCorrecta: false,
            },
          ],
          mensaje_correcto:
            'Correcto, la función del abatidor es enfriar rápidamente los alimentos calientes (de 65°C a 10°C en menos de 90 minutos) para evitar la proliferación bacteriana, no para hacerlo lentamente.',
          mensaje_incorrecto:
            'Respuesta incorrecta, revise nuevamente el contenido del componente formativo.',
        },
        {
          id: 6,
          texto:
            '¿Qué norma sanitaria vigente en Colombia establece los requisitos para la elaboración de alimentos y refuerza la obligatoriedad de las Buenas Prácticas de Manufactura (BPM)?',
          imagen: require('@/assets/actividad/imagen6.png'),
          barajarRespuestas: true,
          opciones: [
            { id: 'a', texto: 'Resolución 2674 de 2013.', esCorrecta: true },
            { id: 'b', texto: 'Ley 9 de 1979.', esCorrecta: false },
            { id: 'c', texto: 'Decreto 3075 de 1997.', esCorrecta: false },
            { id: 'd', texto: 'NTC-ISO 22000.', esCorrecta: false },
          ],
          mensaje_correcto:
            'Bien, tal como se cita en el documento, la Resolución 2674 de 2013 es la norma vigente que establece los requisitos sanitarios y refuerza la implementación de las BPM.',
          mensaje_incorrecto:
            'Respuesta incorrecta, revise nuevamente el contenido del componente formativo.',
        },
        {
          id: 7,
          texto:
            'La <em>mise en place</em> en el ámbito de la repostería profesional se refiere a:',
          imagen: require('@/assets/actividad/imagen7.png'),
          barajarRespuestas: true,
          opciones: [
            {
              id: 'a',
              texto:
                'La limpieza del área de trabajo después de finalizar la producción.',
              esCorrecta: false,
            },
            {
              id: 'b',
              texto:
                'La preparación y organización de todos los ingredientes y herramientas antes de comenzar a cocinar.',
              esCorrecta: true,
            },
            {
              id: 'c',
              texto: 'Un tipo de horno francés para cocción uniforme.',
              esCorrecta: false,
            },
            {
              id: 'd',
              texto:
                'La técnica de decoración con boquilla de pétalo para simular flores.',
              esCorrecta: false,
            },
          ],
          mensaje_correcto:
            'Correcto la <em>mise en place</em> es una filosofía de trabajo que significa "poner en su lugar" e implica preparar y organizar todos los ingredientes y herramientas antes de comenzar a cocinar.',
          mensaje_incorrecto:
            'Respuesta incorrecta, revise nuevamente el contenido del componente formativo.',
        },
        {
          id: 8,
          texto:
            '¿Qué tipo de riesgo previene el uso de calzado antideslizante en una cocina?',
          imagen: require('@/assets/actividad/imagen8.png'),
          barajarRespuestas: true,
          opciones: [
            { id: 'a', texto: 'Riesgo ergonómico.', esCorrecta: false },
            { id: 'b', texto: 'Riesgo químico.', esCorrecta: false },
            { id: 'c', texto: 'Riesgo biológico.', esCorrecta: false },
            { id: 'd', texto: 'Riesgo físico.', esCorrecta: true },
          ],
          mensaje_correcto:
            'Muy bien, el calzado antideslizante previene riesgos físicos (caídas).',
          mensaje_incorrecto:
            'Respuesta incorrecta, revise nuevamente el contenido del componente formativo.',
        },
        {
          id: 9,
          texto: '¿Cómo se clasifican la levadura fresca y la levadura seca?',
          imagen: require('@/assets/actividad/imagen9.png'),
          barajarRespuestas: true,
          opciones: [
            { id: 'a', texto: 'Leudantes químicos.', esCorrecta: false },
            { id: 'b', texto: 'Leudantes físicos.', esCorrecta: false },
            { id: 'c', texto: 'Leudantes biológicos.', esCorrecta: true },
            {
              id: 'd',
              texto: 'Agentes de sabor sin función leudante.',
              esCorrecta: false,
            },
          ],
          mensaje_correcto:
            'Bien ambos tipos de levadura son hongos vivos que fermentan los azúcares para producir gas, por lo que se clasifican como agentes leudantes biológicos.',
          mensaje_incorrecto:
            'Respuesta incorrecta, revise nuevamente el contenido del componente formativo.',
        },
        {
          id: 10,
          texto: '¿En qué consiste la contaminación cruzada?',
          imagen: require('@/assets/actividad/imagen10.png'),
          barajarRespuestas: true,
          opciones: [
            {
              id: 'a',
              texto:
                'La mezcla accidental de dos ingredientes dulces como azúcar y miel.',
              esCorrecta: false,
            },
            {
              id: 'b',
              texto:
                'La transferencia de microorganismos patógenos de un alimento contaminado a otro que no lo está.',
              esCorrecta: true,
            },
            {
              id: 'c',
              texto:
                'El uso del mismo molde para dos preparaciones diferentes.',
              esCorrecta: false,
            },
            {
              id: 'd',
              texto:
                'La adición accidental de un ingrediente no contemplado en la receta.',
              esCorrecta: false,
            },
          ],
          mensaje_correcto:
            'Correcto, la contaminación cruzada es la transferencia de microorganismos patógenos (bacterias, virus) de un alimento contaminado (generalmente crudo) a otro que no lo está.',
          mensaje_incorrecto:
            'Respuesta incorrecta, revise nuevamente el contenido del componente formativo.',
        },
        {
          id: 11,
          texto:
            '¿De qué es responsable la reacción de <em>Maillard</em> en los productos horneados?',
          imagen: require('@/assets/actividad/imagen1.png'),
          barajarRespuestas: true,
          opciones: [
            {
              id: 'a',
              texto: 'Del color dorado y el sabor tostado.',
              esCorrecta: true,
            },
            {
              id: 'b',
              texto:
                'De la disolución del azúcar <em>glass</em> en los glaseados.',
              esCorrecta: false,
            },
            {
              id: 'c',
              texto: 'Del aumento de volumen por acción del vapor.',
              esCorrecta: false,
            },
            {
              id: 'd',
              texto: 'De la activación de la levadura.',
              esCorrecta: false,
            },
          ],
          mensaje_correcto:
            'Correcto, la reacción de <em>Maillard</em> es una reacción química entre aminoácidos y azúcares que ocurre con el calor, responsable del color dorado y el sabor tostado en productos horneados. La disolución del azúcar <em>glass</em> es una propiedad física.',
          mensaje_incorrecto:
            'Respuesta incorrecta, revise nuevamente el contenido del componente formativo.',
        },
        {
          id: 12,
          texto:
            '¿Para qué tipo de decoración se utilizan específicamente las boquillas o duyas con forma de pétalo?',
          imagen: require('@/assets/actividad/imagen2.png'),
          barajarRespuestas: true,
          opciones: [
            {
              id: 'a',
              texto: 'Para escribir mensajes sobre el pastel.',
              esCorrecta: false,
            },
            {
              id: 'b',
              texto: 'Para rellenar <em>profiteroles</em> o <em>éclairs</em>.',
              esCorrecta: false,
            },
            {
              id: 'c',
              texto: 'Para hacer bordes ondulados en conchas marinas.',
              esCorrecta: false,
            },
            {
              id: 'd',
              texto: 'Para crear decoraciones que simulan flores.',
              esCorrecta: true,
            },
          ],
          mensaje_correcto:
            'En la clasificación de boquillas, el documento menciona las "Especiales: De pétalo para flores".',
          mensaje_incorrecto:
            'Respuesta incorrecta, revise nuevamente el contenido del componente formativo.',
        },
        {
          id: 13,
          texto:
            '¿Qué característica hace que los hornos de convección sean ideales para hornear bizcochos?',
          imagen: require('@/assets/actividad/imagen3.png'),
          barajarRespuestas: true,
          opciones: [
            {
              id: 'a',
              texto: 'Utilizan piedra refractaria que acumula calor.',
              esCorrecta: false,
            },
            {
              id: 'b',
              texto: 'Los carros con bandejas giran en su interior.',
              esCorrecta: false,
            },
            {
              id: 'c',
              texto:
                'Utilizan un ventilador para distribuir el calor de manera uniforme.',
              esCorrecta: true,
            },
            {
              id: 'd',
              texto: 'Alcanzan temperaturas superiores a los 300°C.',
              esCorrecta: false,
            },
          ],
          mensaje_correcto:
            'Bien, se describe que el horno de convección, al usar un ventilador, distribuye el calor uniformemente y es ideal para masas batidas como bizcochos y ponqués.',
          mensaje_incorrecto:
            'Respuesta incorrecta, revise nuevamente el contenido del componente formativo.',
        },
        {
          id: 14,
          texto:
            '¿Cuál es la aplicación correcta del método PEPS en un taller de repostería?',
          imagen: require('@/assets/actividad/imagen4.png'),
          barajarRespuestas: true,
          opciones: [
            {
              id: 'a',
              texto:
                'Un procedimiento de limpieza para superficies en contacto con alimentos.',
              esCorrecta: false,
            },
            {
              id: 'b',
              texto:
                'Una técnica de decoración para garantizar la uniformidad en los pasteles.',
              esCorrecta: false,
            },
            {
              id: 'c',
              texto: 'Un método de horneado para cocciones homogéneas.',
              esCorrecta: false,
            },
            {
              id: 'd',
              texto:
                'Una técnica de rotación de inventarios para usar primero los productos más antiguos.',
              esCorrecta: true,
            },
          ],
          mensaje_correcto:
            'Correcto, el PEPS es un método de rotación de inventarios que consiste en utilizar primero los productos que ingresaron primero (con fecha de vencimiento más cercana) para evitar su deterioro.',
          mensaje_incorrecto:
            'Respuesta incorrecta, revise nuevamente el contenido del componente formativo.',
        },
        {
          id: 15,
          texto:
            '¿Cuál es la especificación correcta para la mantequilla utilizada en repostería de calidad?',
          imagen: require('@/assets/actividad/imagen5.png'),
          barajarRespuestas: true,
          opciones: [
            {
              id: 'a',
              texto:
                'Debe tener un contenido de grasa mínimo del 82 % y ser con sal para potenciar sabores.',
              esCorrecta: false,
            },
            {
              id: 'b',
              texto:
                'Debe tener un contenido de grasa mínimo del 70 % y ser sin sal.',
              esCorrecta: false,
            },
            {
              id: 'c',
              texto:
                'Debe tener un contenido de grasa mínimo del 82 % y ser sin sal.',
              esCorrecta: true,
            },
            {
              id: 'd',
              texto:
                'Debe ser margarina para garantizar una textura más crujiente.',
              esCorrecta: false,
            },
          ],
          mensaje_correcto:
            'Muy bien, si bien es cierto que la mantequilla de calidad debe tener un mínimo de 82 % de grasa, el documento especifica que debe ser mantequilla sin sal (a menos que la receta indique lo contrario), no con sal.',
          mensaje_incorrecto:
            'Respuesta incorrecta, revise nuevamente el contenido del componente formativo.',
        },
        {
          id: 16,
          texto: '¿Cuál es la composición correcta del chocolate blanco?',
          imagen: require('@/assets/actividad/imagen6.png'),
          barajarRespuestas: true,
          opciones: [
            {
              id: 'a',
              texto: 'Pasta de cacao, manteca de cacao, leche y azúcar.',
              esCorrecta: false,
            },
            {
              id: 'b',
              texto: 'Manteca de cacao, leche y azúcar.',
              esCorrecta: true,
            },
            {
              id: 'c',
              texto: 'Pasta de cacao, leche y azúcar.',
              esCorrecta: false,
            },
            {
              id: 'd',
              texto: 'Manteca de cacao, pasta de cacao y azúcar.',
              esCorrecta: false,
            },
          ],
          mensaje_correcto:
            'Correcto, el chocolate blanco contiene manteca de cacao, leche y azúcar, pero no contiene pasta de cacao, lo que lo diferencia de los otros tipos de chocolate.',
          mensaje_incorrecto:
            'Respuesta incorrecta, revise nuevamente el contenido del componente formativo.',
        },
        {
          id: 17,
          texto:
            '¿Cuáles son las dos funciones principales de tamizar la harina?',
          imagen: require('@/assets/actividad/imagen7.png'),
          barajarRespuestas: true,
          opciones: [
            {
              id: 'a',
              texto: 'Aumentar su peso y eliminar el gluten.',
              esCorrecta: false,
            },
            {
              id: 'b',
              texto: 'Mezclarla con la levadura y activar el almidón.',
              esCorrecta: false,
            },
            {
              id: 'c',
              texto:
                'Eliminar grumos y oxigenar la mezcla para una textura más ligera.',
              esCorrecta: true,
            },
            {
              id: 'd',
              texto: 'Enfriarla y darle un sabor más neutro.',
              esCorrecta: false,
            },
          ],
          mensaje_correcto:
            'Muy bien, tamizar cumple dos funciones importantes: eliminar grumos e impurezas, y oxigenar la mezcla, lo que ayuda a lograr una textura más ligera y esponjosa.',
          mensaje_incorrecto:
            'Respuesta incorrecta, revise nuevamente el contenido del componente formativo.',
        },
        {
          id: 18,
          texto: '¿A qué se refiere el término "Punto de humeo"?',
          imagen: require('@/assets/actividad/imagen8.png'),
          barajarRespuestas: true,
          opciones: [
            {
              id: 'a',
              texto:
                'A la temperatura donde un merengue alcanza su punto máximo de esponjosidad.',
              esCorrecta: false,
            },
            {
              id: 'b',
              texto:
                'A la temperatura donde un bizcocho está completamente horneado.',
              esCorrecta: false,
            },
            {
              id: 'c',
              texto: 'A la fase del horneado donde el producto libera vapor.',
              esCorrecta: false,
            },
            {
              id: 'd',
              texto:
                'A la temperatura donde una grasa o aceite comienza a descomponerse y desprender humo.',
              esCorrecta: true,
            },
          ],
          mensaje_correcto:
            'Correcto el glosario define el "Punto de humeo" como la temperatura a la cual una grasa o aceite comienza a descomponerse y a desprender humo visible y sustancias tóxicas. No tiene relación con la esponjosidad de un merengue.',
          mensaje_incorrecto:
            'Respuesta incorrecta, revise nuevamente el contenido del componente formativo.',
        },
        {
          id: 19,
          texto:
            'Según el documento, ¿Las mangas pasteleras de tela son siempre preferibles a las desechables por razones de higiene?',
          imagen: require('@/assets/actividad/imagen9.png'),
          barajarRespuestas: true,
          opciones: [
            {
              id: 'a',
              texto: 'No, porque las de tela siempre deben ser de plástico.',
              esCorrecta: false,
            },
            {
              id: 'b',
              texto:
                'No, el documento no establece una preferencia absoluta; las desechables pueden ser más higiénicas en ciertos contextos.',
              esCorrecta: true,
            },
            {
              id: 'c',
              texto: 'Sí, porque la tela es un material más natural.',
              esCorrecta: false,
            },
            {
              id: 'd',
              texto: 'Sí, porque se pueden esterilizar a altas temperaturas.',
              esCorrecta: false,
            },
          ],
          mensaje_correcto:
            'Perfecto. el documento no establece una preferencia absoluta. Menciona que existen mangas desechables o de tela (lona o plástico), pero no indica que unas sean "siempre preferibles" por razones de higiene. De hecho, las desechables pueden ser más higiénicas en ciertos contextos al no requerir lavado y reutilización.',
          mensaje_incorrecto:
            'Respuesta incorrecta, revise nuevamente el contenido del componente formativo.',
        },
        {
          id: 20,
          texto:
            '¿Qué son los POES (Procedimientos Operativos Estandarizados de Saneamiento)?',
          imagen: require('@/assets/actividad/imagen10.png'),
          barajarRespuestas: true,
          opciones: [
            {
              id: 'a',
              texto:
                'Unos equipos de refrigeración para enfriar rápidamente los alimentos.',
              esCorrecta: false,
            },
            {
              id: 'b',
              texto: 'Un tipo de boquilla para decoración de pastelería.',
              esCorrecta: false,
            },
            {
              id: 'c',
              texto:
                'Unos protocolos escritos que describen cómo realizar las tareas de limpieza y desinfección.',
              esCorrecta: true,
            },
            {
              id: 'd',
              texto: 'Un método de rotación de inventarios.',
              esCorrecta: false,
            },
          ],
          mensaje_correcto:
            'Muy bien, el glosario define claramente los POES como "protocolos escritos que describen cómo llevar a cabo las tareas de limpieza y desinfección."',
          mensaje_incorrecto:
            'Respuesta incorrecta, revise nuevamente el contenido del componente formativo.',
        },
      ],
      mensaje_final_aprobado: '¡Excelente! Ha superado la actividad.',
      mensaje_final_reprobado:
        'Le recomendamos volver a revisar el componente formativo e intentar nuevamente la actividad didáctica.',
    },
  }),
}
</script>
