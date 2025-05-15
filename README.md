PlusvaDani-AytoManises
Descripción
PlusvaDani-AytoManises es una aplicación web diseñada para calcular una estimación del Impuesto sobre el Incremento de Valor de los Terrenos de Naturaleza Urbana (IIVTNU), comúnmente conocido como plusvalía municipal, correspondiente al Ayuntamiento de Manises.   

La herramienta permite a los usuarios introducir los datos relevantes de una transmisión de propiedad para obtener un cálculo informativo de la cuota tributaria potencial. Es importante destacar que esta aplicación ofrece una simulación y sus resultados no son vinculantes ni sustituyen la liquidación oficial emitida por el Ayuntamiento.

Funcionalidades Principales
La aplicación ofrece las siguientes características:

Cálculo de la Plusvalía Municipal: Estima el impuesto utilizando dos métodos de cálculo según la normativa vigente: el Método Objetivo y el Método Real (basado en la ganancia patrimonial).
Entrada de Datos Sencilla: Un formulario intuitivo permite ingresar toda la información necesaria:
Fecha de adquisición del inmueble.
Fecha de transmisión del inmueble.
Valor catastral total del inmueble.
Valor del suelo, que puede especificarse como un porcentaje del valor catastral total o como un importe directo.
Valor de adquisición (compra) del inmueble.
Valor de transmisión (venta) del inmueble.
Validación de Datos: Incorpora validaciones para asegurar que los datos introducidos sean coherentes y correctos (ej. fechas válidas, valores numéricos positivos).
Resultados Detallados: Muestra un desglose de los cálculos para ambos métodos:
Método Objetivo: Periodo de tenencia (años y meses), valor catastral del suelo utilizado, coeficiente aplicable según los años de tenencia, base imponible y cuota íntegra.
Método Real (Ganancia): Valor de transmisión, valor de adquisición, incremento patrimonial total, proporción del suelo sobre el valor catastral total, base imponible y cuota íntegra.
Conclusión Clara: Indica la cuota final estimada a liquidar, seleccionando automáticamente el método que resulte más beneficioso para el contribuyente (es decir, la menor de las dos cuotas calculadas, o cero si no hay sujeción al impuesto). También se informa si la transmisión no está sujeta a plusvalía y por qué.
Impresión de Resultados: Facilidad para imprimir el resumen de los cálculos.
Limpieza de Formulario: Opción para reiniciar todos los campos del formulario.
Información Adicional: Incluye una nota legal aclarando el carácter meramente informativo de los cálculos y proporciona un enlace a la ordenanza fiscal municipal del Ayuntamiento de Manises.
¿Cómo Funciona el Cálculo?
La aplicación implementa la lógica de cálculo de la plusvalía municipal siguiendo estos pasos principales:

Recopilación de Datos: El usuario introduce la información requerida a través del formulario.
Cálculo por Método Objetivo:
Se determina el número de años completos de tenencia del terreno.
Se obtiene el valor catastral del suelo (ya sea por porcentaje o importe directo).
Se aplica un coeficiente establecido por el Ayuntamiento de Manises (según una tabla interna COEFICIENTES_POR_ANO para periodos de 1 a 19 años, o un COEFICIENTE_MAXIMO de 0.40 para 20 años o más) al valor catastral del suelo para obtener la base imponible.
La cuota se calcula aplicando el tipo de gravamen (fijado en el 28%, TIPO_GRAVAMEN = 0.28) a esta base imponible.
Nota: Las transmisiones realizadas antes del 1 de enero de 2024 o con menos de un año de tenencia pueden tener particularidades o no estar sujetas bajo este método según la configuración.
Cálculo por Método Real (Ganancia):
Se calcula la ganancia patrimonial total (diferencia entre el valor de transmisión y el valor de adquisición).
Si no hay ganancia (o hay pérdida), la cuota por este método es cero.
Si hay ganancia, se calcula la proporción que el valor catastral del suelo representa sobre el valor catastral total.
La base imponible es la parte de la ganancia patrimonial total que corresponde a esa proporción del suelo.
La cuota se obtiene aplicando el tipo de gravamen (28%) a esta base imponible.
Determinación de la Cuota Final:
La aplicación compara las cuotas resultantes de ambos métodos.
La cuota a liquidar será la menor de las dos, o cero si alguna de ellas indica no sujeción o un importe negativo. La aplicación indicará qué método se ha aplicado.
Entrada de Datos
Para utilizar la calculadora, necesitarás los siguientes datos:

Fecha de adquisición: Fecha en la que se compró o adquirió el inmueble.
Fecha de transmisión: Fecha en la que se vende o transmite el inmueble. (Debe ser igual o posterior al 1 de enero de 2024 para que la calculadora funcione con los coeficientes actuales).
Valor catastral total (€): El valor catastral total del inmueble que figura en el recibo del IBI o en la Sede Electrónica del Catastro.
Indicación del Valor del Suelo:
Porcentaje valor del suelo (%): El porcentaje que el valor del suelo representa sobre el valor catastral total (suele venir en el recibo del IBI).
Importe del valor del suelo (€): El valor catastral específico del suelo.
Valor de adquisición/compra (€): El precio por el que se compró el inmueble en su día.
Valor de transmisión/venta (€): El precio por el que se vende el inmueble actualmente.
Resultados Proporcionados
La aplicación mostrará:

Un resumen de los cálculos realizados por el Método Objetivo.
Un resumen de los cálculos realizados por el Método Real.
Una Conclusión con:
El título "No sujeto a Plusvalía" o "Cuota Estimada a Liquidar".
El importe de la cuota final (si procede) o un mensaje explicativo.
Información sobre el método de cálculo que ha resultado más beneficioso y, por tanto, aplicado.
