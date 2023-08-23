Simulador de Sistema de Comunicación de un Robot Espacial

El programa es una simulación de un esquema  de comunicación basado en el modelo propuesto por Claude Shannon, consta de cinco componentes clave: Fuente de información, Transmisor, Canal, Receptor y Destino de información. El objetivo es demostrar cómo estos componentes trabajan juntos para transmitir datos desde un robot explorador en el espacio hasta una estación espacial de científicos.

Componentes Simulados:

Fuente de Información: La fuente de información es el robot explorador Perseverance 21, el cual es enviado a una misión para registrar datos geológicos del planeta Marte. Los datos que recopila son:

-Objeto: Aquí se le dará una lista que tiene opciones y aleatoriamente elegirá una y en la simulación representa que eso detecto el robot.
Estas son las opciones: "mineral", "roca", "cristal", "hielo", "agua", "meteorito", "objeto no identificado".

-Ubicación: Recopila aleatoriamente una cantidad de un rango entre -1000 y 1000, para las coordenadas x,y,z. 

-Imágenes: Este es un atributo más en la simulación pero no será modificado realmente como los dos anteriores ya que solo es una lista que contiene estas opciones: "imagen1.jpg", "imagen2.jpg".

La función “recopilar_datos()” es quien se encargará del proceso. 

Transmisor: 

Aquí sucede la transmisión de datos, para esto el robot codifica los datos a binario para poder comprenderlos y transmitirlos

La función “transmisor_de_la_nave_espacial(datos_recopilados)” codifica los datos en cadenas binarias (sólo el de objeto y ubicación).

Canal:

Para la transmisión de los datos a través de un canal, se asume una representación de una fibra óptica.

El ruido se introduce en la función canal. La simulación del ruido consiste en cambiar bits aleatoriamente, para esto se establece un porcentaje de 1% para objeto y 5% para la ubicación. Esos porcentajes son bajos para no perder por completo la información correcta.

La función “fibra_optica(datos_transmitidos)” es quien de representar el canal por fibra óptica para la transmisión y del proceso para incluir ruido.

Receptor: 

Para simular el receptor se crea una función que se encarga de la decodificación de las cadenas binarias recibidas en información legible.

La función receptor(datos_con_ruido) decodifica las cadenas binarias a sus formatos originales.

Destino de Información:

Finalmente, se simula la recepción de la información decodificada por parte de una estación espacial de científicos. Aquí se mandan a llamar las funciones por orden para visualizar la información final. 


Notas:
Al final se hace una comparación de la información de los cambios que tuvo durante el proceso. Para esto se visualiza:

-Datos originales.

-Datos transmitidos.

-Datos con ruido.

-Datos receptados.

El programa utiliza valores y probabilidades de ruido predefinidos para simplificar la simulación.
La simulación del canal se logra a través de la función “fibra_optica(datos_transmitidos)”, donde se introduce el ruido. El programa no incluye una implementación real de fibra óptica; en cambio, se centra en la introducción del ruido y la decodificación de datos.

El programa ofrece una representación simplificada del modelo de comunicación de Shannon aplicado a la comunicación espacial, demostrando cómo los datos pasan por los diferentes componentes antes de llegar al destino final.

