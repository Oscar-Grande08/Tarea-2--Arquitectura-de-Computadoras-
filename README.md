# Tarea 2 Arquitectura de Computadoras.
bienvenido a este repositorio en el cual podrás encontrar información referente a distintas arquitecturas computacionales como: computación cuántica, neuromórfico, biológico, heterogénea o de borde. 
## **Computacion Cuantica**.
La computacion cuantica usa estados y operaciones que obedecen la mecanica cuantica para el procesaiento de informacion. En lugar de bits clasicos como 0 o 1, ahora usaremos qubits que pueden estar en estado de superposicion y entrelazarse. Los algoritmos cuanticos manipulan amplitudes complejas y explotan la interferencia para aumentar probabilidades de respuestas correctas y cancelar las incorrectas.Los modulos de computo cuantico son los siguientes: 
- Modelo de puertas (gate model o circuito cuantico): Analogo al circuito logico clasico, secuencia de puertas unitarias y mediciones al final (modelo unniversal).
- Computacion adiabatica/ Quantum annealing: Tranaforma paso a paso un Hamiltoniano para encontrar estados de baja energia lo cual es util para optimizacion que es un modelo distinto al de puertas.
  (un Hamiltoniano es un operador que actua como operador sobrel estado cuantico, representando el observable de la energia )
- Computacion basada en medidasn (Mbqc/ cluster states): se prepara un gran estado entrelazado (cluster) en el cual se realizan medidas adpatativas. ( Un cluster es un tipo de estado cuántico altamente entrelazado, donde los qubits están organizados en una red (como una cuadrícula o grafo) el cual almacena informacion de una forma no clasica.)
- Modelos Hibridos (NisQ): ejecuta subrutinas cuanticas en harware con ruido y usando correciones clasicas de ser necesario.

Lo que hace esto es generar una manipulacion global de amplitudes y entrelzamientos que permitira realizar una solucion o proceso requerido con muhcos paso menos, pero hasta el momento no garantiza que todo funciones con la misma velocidad de solucion, puede que otro problema especifico tarde mas, hasta puede tardar mas que de la manera clasica.
Ahora conozcamos bien que es un Qubit ya que es escencial en la computacion cuantica: 
un Qubit es un vector unitario en un espacio de Hilbert de dimension 2:
- ψ⟩=α∣0⟩+β∣1⟩,   α,β∈C,  ∣α∣^2+∣β∣^2=1.

El estado de n Qubits vive en el producto tensorial El numero de amplitudes escasa como 2^n. Lo cual explica la grande capacidad teorica y porque el simular sostemas cuanticos crece exponencialmente para lo clasico.

##Arquitectura De Un Computador Cuantico: 
#Hardware
1. Qubits:
- Tipos fisicos comunes: superconductores (transmon), iones atrapados, fotones (ópticos), qubits de espín (puntos cuánticos), defectos en sólidos (NV centers), qubits topológicos (propuesta).
2. Acoplamientos o Buses:
- Permiten que qubits interactúen (ej., acoplamiento capacitivo en superconductores, fonones compartidos en iones). Diseño crítico para implementar puertas de dos qubits con alta fidelidad.
3. Subsistema de Refrigeracion:
- Muchos de estos sistemas necesitan y requieren de criogenia la cual es una dilucion a milikelvin para eliminar aquellas excitacion y variaciones termicas. Acompañados de camaras de vacio ultraligado, laseres o campos electromagneticos para los Iones.
4. Control fisico de pulsos y electronica:
- Generadores de pulsos microwave o laser que aplican rotaciones y puertas
- control clasico para generar formas de onda, secuencias y tener el control en tiempo real.
- Detectores que traducen el estado cuantico a un estado clasico para mayor comprension, esto se conoce como readout.
5. Aislacion y Calibracion:
- Requiere de blindaje contra el ruido electromagnetico, vibraciones o aquellas gradientes termicas. Acompañadas de calibracion concurrente para ajustar las frecuencias, fases y lograr compensar el drift.
#Software
1. Capa De Correcion y Estabilidad.
- Este con el objetivo de convertir qubits fisicos ruidoso en qubits logicos robustos mediante codificacion.
- qubits ancilla, mediciones de sindorme, rutinas de correccion clasicas en tiempo real.
- Overhead masivo en cantidad de qubits fisicos por qubit logico, lo cuales importante sin QEC eficiente, no se logra computo profundo y largo.
2. Capa De Control Clasico y Retroalimentacion.
- Interpretar sindromes y aplicar correcion rapida a latencia baja para lograr controlar en tiempo real.
- El Co-procesador clasico optimiza la compilacion, planifica ls secuencias y maneja el schedule de pulsos y ajustes dinamicos.
3. Capa De Software y Compilacion:
- lenguajes y abstraciion para lenguaje de mas alto nivel (QASM, OpenQASM, Quil, Cirq,Q#).
- Compilador o Transpiler el cual mapea circuitos logicos o qubits fisicos, impotimizando puertas y minimizando a profundidad.
- Tecnicas de benchmarking (randomized benchmarking, tomography, cross-entropy benchmarking) con el fin para la simulacion y verificaion.
4. Capa De Comunicacion.
- Interconexiones cuanticas atraves de fibra para fotones, enlaces de microoondas, transductores los cuales osn necesarios para conectar arquitecturas modulares o redes cuanticas.
- Quantum Repeaters los cuales se usan para extender alcance en redes mediante entrelazamiento purificacion y swapping.
5. Capa De Aplicaciones.
- Apis y Librerias como Qiskit,Cirq,Forest,Pennnylane las cuales permiten a investigadores y usuarios construir algoritmos y ejecutar en hardware real o simuladores.

## Historia De La Computacion Cuantica.
- **Decada de los 1980 donde nacieron las ideas funcionales**

  1. Paul Beniof propuso modelos fisicos de maquinas de Turing cuanticas.
  2. Richard Feynman en 1981-1982 argumento que simular sistemas cuanticos con maquinas clasicas es ineficiente y propuso usar maquinas cuanticas para simular fisica.
  3. David Deutsch en 1985 formaliza el concepto de "computadora cuanticas universal" y elabora el modelo de circuito cuantico.
- **Cirptografia cuantica y comunicacion**
   1. Bennet y Brassard en 1984 postularon el protocolo de distribucion cuantida de claves.
- **Algoritmos cuanticos**
  1. Peter shor en 1994 propone el algoritmo polinominal para la factorizacion de enteros, acompañado de un disipador enorme de interes practico.
  2. Lov Grover en 1996 plantea el algoritmo de busqueda con acelaeracion cuadratica.
- **Propuesta de hardware y primeros experimentos**
  1. Propuestas para ion traps en mediados de los 90 y para superconductores como candidatos practicos.
  2. primeras implementaciones experimentales de puertas cuanticas y protocolos en plataformas como NMR y iones.
  3. Alrededor de los años 2000 se logro las demostraciones de subrutinas cuanticas, incluida la factorizacion del numero 15 con equipos NMR las cuales realizan una implementacion a pequeña escala.
- **Nacimiento de la era NISSQ y comercializacion**
  1. Proliferacion de laboratorios y empresas de superconductores, iones atrapados, fotonica, en el año 2010.
  2. Desarrollo y acceso remoto a cloud acces para procesadores cuanticos.
  3. En 2019 obtienen reclamos de "quantum supremacy advantage" por experimentos de tarea especifica en proceadores superconductores (discusiones tecninas y replicacion abierta).
- **Presente en proceso de NISQ a QEC.**
  1. Desarrollo intensico de correccion de errores, escalado modular, transductores fotonicos y redes cuanticas experimentales.
  2. Investigacion en codigos topologicos, destilacion de estados magicos y arquitecturas para miles o millones de qubits
## Ventajas y Desventajas.
- **Ventajas**
  1. Simulacion eficiente de sistemas cuanticos: modelar moleculas, reacciones quimicas y materiales con coste polinomico en muchos casos donde la clasica escala exponencialmente. Esto impacta quimica cuantica, descubrimiento de farmacos y ciencia de materiales.
  2. Algoritmos con aceleracion notable: Como shor realiza una factorizacion en tiempo polinomial (amenaza para criptografia asimetrica clasica) o Grover el cual realiza una cuadratica para bsuqueda no estructurada. Algoritmos lineales cuanticos los cuales ofrecen potencial para resolver sistemas lineales bajo condiciones restrictivas (condicion numerica, preparacion y lectura de estados).
  3. Nuevas formas de comunicacion segura: QKD proporciona seguridad basda en leyes fisicas (deteccion de eavesdroppers).
  4. Nuevas arquitecturas computacionales que proporcionasn modelos hibridos clasicos o cuanticos para optimizacion y machine learning cuantico el cual se encuentra en investigacion.
  5. Posible ventaja exponencial para problemas especificos cuando sea posible llear a hardware escalable y sea tolerante a fallos.
- **Desventajas**
   1. Ruido y decoherencia: qubits fisicos interactuan con el ambiente lo cual genera perdida de coherencia y esto limita la profundidad del circuito y tiempo de computo.
   2. correcion de errores costosa: overhead enorme, para obtener un qubit logico fiable se necesitan muchos qubits fisicos y complejos esquemas de control en tiempo real.
   3. Aplicabilidad limitada al dia de hoy en la cual se pueden generar pocas aplicaciones con ventaja practica demostrada en hardware Nisq lo cual muchas promesas dependen de un hardware intolerante.
   4. Requisitos de infraestructura como criogenia, vacio , lasers, blindaje y electronica de alta precision lo cual genera un costo bastante elevado.
   5. Riesgos en seguridad cuando la capacidad cuantica practica llegue, la criptografia clasica quedara vulnerada y esto ya genera migracion a criptografia post cuantica.
   6. Lectura y preparacion de estados ya que para preparar estados iniciales utiles y leer la solucion eficientemente no siempre es trivial.
   7. Falta de talento y estadarizacion ya que es un campo en evolucion con herramientas y metricas aun en evolucion y definicion estarndarizada.

## Terminos importantes.
- **Superposicion**:

Un qubit puede estar en una combinacion lineal de estados de base 0 y 1. Matematicamente a=0 y b=1 y estos son vectores, pues estos contienen informacion relativa y magnitud. La fase relativa entre amplitudes es fisica y puede producir interferencias y la representacion geometrica la cual es un estado puro de un qubit corresponde a un punto en la superficie preparando una superposicion equi probable de 0 y 1, esto significa que la descripcion del sistema requiere de ambas amplitudes y la informacion se manifiesta en la probabilidad de resultados y en la interferencia.

- **Entrelazamiento**

Estado multipartito que no puede factorizarse como producto de estados de subsistemas. Es una correlación cuántica no clasica. Matematicamente en un estados de 2 qubits es separable si existe una magnitud A y una magnitud B tales que su prodcuto sean una nueva magnitud, si no existe, este esta entrelazado. Para medidas de entrelazamiento para bipartitos puros, la entropia de von Neumm¿ann del reducido S(pA)=-Tr(pA.logpA)para un estado puramente entrelazado, la tasa reducida es mixta y S>0.

- **Interferencia cuantica**

los caminos de amplitud compleja se suman las fases relativas hacen que probabilidades se refuercen o cancelen. El cual es el mecanismo que permite a algoritmos cuanticos “seleccionar” soluciones correctas. Matematicamente si dos amplitudes A1 y A2 conducen a un mismo resultado, amplitus total a= A1+A2. Para la probabilidad solo basta hallar la magintud de a total elevada al cuadrado, que contiene terminos cruzados 2Re(A1.A2*) las cuales son las responsables de interferencias

- **Medicion probabilistica**

Su principio es el de la regla de Born el cual es si un sitema esta en un vector y medimos en la base, la probabilidad de obtener la base es "Pi" la cual es igual a la magnitud de la base y el vector al cuadrado. Y tras la medicion proyectiva, el estado colapsa a su base o a su proyeccion. Este permite medidas no proyectivas y describen aparatos de medicion mas generales, un POVM es una coleccion de operadores positivos. Esto significa que solo obtenemos informacion probabilistica lo cual requiere repetir bastantes veces para estimar amplitudes.

-**Desafio de coherencia**

roceso por el cual la fase relativa (coherencia) entre amplitudes se degrada debido a interaccion con el entorno, es la principal limitación practica. Donde T1 es el tiempo de relajacion en que la poblacion del estado excitado decae al estado base por intercambio de energia con el entorno. Y T2 es la decoherencia lo cual significa el tiempo en que desaparece la coherencia de fase normalmente T2< 2T1. Los modelos de ruido son los canales cuanticos y las contramedidas tecnicas son; mejora de materiales, aislamiento, dynamical decoupling, quantum error correction y mejora en fidelidad de puertas y readout.

## Tipos De Comunicacion Cuantica.
1. Quantum Key Distribution
2. Teletransportacion cuantica
3. Distrrbucion entrelazada y swapping
4. Quantum repeaters y la internet cauntica
5. Comunicacion calsica asistida cuanticamente

## Compuertas Cuanticas. 
En el modelo de puertas las operaciones sobre qubits son unitarias, las compuertas se implementan fisicamente por pulsos que genern transformaciones U en el estado. Estas se representan en matrices unitarias que preservan la probabilidad total. 
- Tipos principales:
  Compuertas de un qubit: son las de un qubit como Pauli-X que invierte el 0 en 1.
  Pauli-Y o Pauli-Z las cuales generan rotaciones en diferentes ejes de la esfera de Bloch.
  Hadamard crea una superpiscion equilibrada.

  Compuertas de 2 qubits: CNOT cambia el segundo qubit si el primero es 1, este es fundamental para entrelazamiento
  
Compuertas Universales: combinando Hadamard + CNOT + rotaciones. se puede construir cualquier operacion cuantica
# Computacion Neuromorfica.
Este es un sistema de computo cuya arquitectura y mecanismo de almacenamientos son diseñados explicitamente para emular el procesamiento nueronal y sinaptico del cerebro. Es un hardaware cuyo modelo dde operacion (paralelismo masivo,eventos discretos, memoria distribuida en la sinapsis y plasticidad local) replicando los principios biologicos para obetener eficiencia energetica y latencias bajas. Donde se busca diseñar un modelos neuronal de hardware, de modo que la computacion y la memoria no esten separados con el fin de evitar un cuello de botella.
## Como Funciona?
1. Modelos de neurona (dinamica temporal)**.Los chips neuromorficos suelen implementar modelos de neurona de diferente complejidad segun la aplicacion y el trade-off.
-  Hodgkin- Huxley: Modelo biofisico detallado (canales ionicos). Ecuaciones diferenciales no lineales con variables gating m,h,n. Es costoso computacionalmente y rara vez implementado a escala en hardware por su complejidad.
-  Izhihevich: Modelo compacto capaz de reproducir muchos patrones de disparo (bursts, chattering) con ecuaciones de segundo orden. Su condicion de disparo si v> 30mV entonces se usa cuando se busca riqueza dinamica de bajo coste.
-  Leaky Integrate aand Fire: Este es el mas comun en hardware Si el voltaje suministrado alcanza un voltaje umbral emite speak y re resetea en Vreset y a menudo se aplica un periodo refractorio. fisicamente un condensador ingresa corriente sinaptica, una resistencia o transistor implementa la fuga, unn comparador detecta cuando el voltaje cruza el voltaje umbral y dispara una señal digital, tras lo cual un circuito de reset descarga el capacitor.


2. Modelos De sinapsis y corriente sinaptica:
- La entrada sinaptica es una suma de efectos causados por spikers sinapticos:
<img width="200" height="210" alt="Captura de pantalla 2025-09-05 060136" src="https://github.com/user-attachments/assets/ed5b81e5-55e4-4b69-8e9e-02051cc348a9" />
 donde alpha es la forma de la respuesta sinaptica o una funcion alpha al infinito y wj son los pesos sinapticos que se almacenan en memoria local.

3. Codigo De Informacion:
-  Rate coding: La informacion se codifica en la tasa de disparo promedio. Facil de entender pero poco eficiente en latencia.
-  Temporal Coding: La informacion codifica en tiempos relativos de los spikes lo cual termina siendo mas eficiente pero mas dificil de entrenar.
-  Population Coding: Conjuntos de neuronas las cuales representan variables mediante patrones distribuidos.
-  Event-Driven: El sistema computea solo cuando ocurren eventos lo que reduce consumo energetico en entornos esporadicos.

4. Reglas De Plasticidad: Un rasgo distintivo de la neuromorfica es el aprendizaje local, las sinapsis actualizan su peso basdas en la actividad local. Las reglas moduladas por recompensa (STDP) multiplicada por un faactor de recompensa global, util para aprendizaje reforzado en hardware local.
5. Arquitectura de ejecucion:
- El evento se dirige al empaquetado de ahi parte al envio por red AER o equivalente, despues llega al core receptor y va a la lectura de pesos sinapticos y realiza el calculo de suma ponderada para luego actualizar la membrana y realizar el posible disparo.
- El sistema es asincrono y orientado a eventos lo cual sucede cuando solo hay actividad de spikes, esto reduce consumo frente a ciclos de reloj constantes.
6. Entrenamiento:
- Off line training: Entrenar una red densa en GPU y convertir tasas a spikes, util cuando se prioriza precision.
- Entrenamiento directo de SNN: con reglas locales o con surrogate gradients para aproximar el gradiente en presencia de la no diferenciabilidad del spike. Surrogate gradients permiten backprop tipo temporal usando aproximaciones suaves de la funcion de disparo.
- On-chip Learning: Cambiar pesos directamente en hardware basado en actividad local lo cual es requerido para adaptibilidad online, robotica y sensores.
## Ventajas:
1. Eficiencia energetica real, el event-driven y sparse computation reducen consumo en tareas con baja tasa de eventos.
2. Latencia ultra baja, tiene un procesamiento en el dominio temporal de los spikes permite respuestas en ms o menos (clave en control de tiempo real).
3. Escalado para problemas paralelizables la topologia distribuida y local favorece paralelismo masivo.
4. Robustez y tolerancia a fallos, la informacion distribuida permite degradacion graciosa.
5. Procesamiento en memoria y sensor, en memresistors y DVS permiten colocar computo donde se genera la informacion
## Desventajas: 
1. Dificultad de entrenamiento y rendimiento inferior en algunas tareas: SNNs puras suelen requerir tecnicaas especiales o conversion de las ANNS para alcanzar la precision de redes convencionales.
2. Variabilidad de dispositivos analogicos y memristivos en el que se deriva temporal, ruido y drift limitan reproducibilidad.
3. Falta de estandares de programacion y toolchains maduras las cuales dificultan la adopcion industrial.
4. Complejidad en diseño de comunicacion y congestion en AER para sistemas grandes.
5. Compromiso y precision en energia, ya que lograr la misma precision que un ANN puede costar en latencia o consumo si se fuerza la equivalencia estricta.
## Hardware: 
1. Chips digitales orientados a eventos: Arrays digitales que implementan una logica de integracion y generacion de spikes e enteros o fixed point, memoria SRAM para pesos y routers digitales para spikes. son robustos y de mayor facilidad de diseño y sse integran bien con procesos CMOS estandar. este cuenta tambien con nucleos con filas de sinapsis indexadas cada spike desencadena lectura secuencial o acceso paralelo a bancos de pesos.
2. Chips analogicos y mixed-signal: circuitos neuronales en circuito analogico  los cuales se ven en transistores trabajando en subthreshold para emular exponencial I-V y consumir pW-nW por neurona. Para la sinapsis implementadas como elementos analogicos son los capcitores y resistores programables, algo contradictorio es la sensibilidad al ruido, temperatura o procesos.
3. In- Memory computing con crossbar memristivo (RRAM,PCM,WRAM variantes) En los cuales se almacena conductancias en celdas memristivas ubicadas en la interseccion filasxcolumnas. Al aplicar voltajes en filas y la corriente en columna realiza una operacion de producto-suma de forma fisica y paralela. Para representar pesos negativos se usan dos dispositivos diferenciales por sinapsis.
4. Comunicaciones y Routing: AER es el estandar operativo de facto para muchos chips cada spike se representa como un paquete con la direccion de neurona emisora. los routers AER son asincronos y permiten multicast per itiendo dirigirse a multiples destinos.
5. Memorias y dispositvos no volatiles en neuromorficos: SRAM/DRAM usados en chips digitales para pesos y estados temporales rapidos, per voluminosos y consumidores de energia. MRAM ReRAM, PCM (memristivos) permiten almacenar pesos de manera no volatil, densidad alta y posibilidad de in-memory compute. Ideal para edge con bajo consumo standby.
6. Fotonica Neuromorfica: La luz permite operaciones con ancho de banda enorme y latencias muy bajas. Implementado en moduladores y resonadores donde realizan implementos de pesos y sumas opticas que se convierten a dominio electrico.
7. Plataformas y ejemplos de arquitectura: Spinnaker (digital masivo): millones de nucleos ARM diseñados para simular grandes redes spiking mediante software distribuido, en enfasis de escalabilidad y flexibilidad.
8. true North: nucleos neuromorficos que integran memoria local de pesos, logica de neuron spiking y routers AER lo que añade capacidades de aprendizaje local on-chip.
## Tipos de computacion neuromorfica que existen.
1. Paradigma operativo: usan spikes discretos en tiempo; event-driven; priorizan latencia y eficiencia temporal. chips que aceleran redes profundas tradicionales (convolucionales, transformers) usando formatos low-precision o in-memory. Pueden llamarse “neuromorficos” por su inspiración en co-diseño, pero en práctica operan con activaciones continuas.combinan sensores DVS (Dynamic Vision Sensors) con procesadores neuromorficos. Aquí el flujo es completamente asíncrono desde el sensor hasta la inferencia.
   
2. Tecnologia de implementacion: Implementaciones puramente digitales orientadas a eventos, integra dinamica neuronal en circuitos analogicos las cuales cuentan con routing y control digital. los Crossbar arrays analogicos para pesos y MAC fisicos y con procesamiento de luz.
  
3. Modo de aprendizaje: capacidades de plasticidad local implementadas en el hardware lo cual es vital paara sistemas autonomos o roboticos. constante entrenamiento en GPU Y CPU  para mapear pesos a hardware neuromorfico para inferencia eficiente, con actualizacion periodica de pesos locales con correcciones offline 
4. Escala y arquitectura de red: miles o millones de nucleos pequeños CPUs para simular SNNs. con un enfoque en densidad sinapticas y dot-product paralelo para redes con gran gan-in.
   
5. Area de aplicacion: en campos como vision, robotica, edge. En Edge son sensores siempre en on, con reconocimiento activado por eventos y bajo consumo. En robotica cuenta con control reactivo con latencia minima. y en Sistemas biomedicos cuenta con implantes o interfaces neuronales donde eficiencia y latencia son criticas.

## Ordenadores Biologicos.
Es un sistema de procesamiento de informacion que utiliza componentes vivos o biomoleculares como ADN, ARN, proteinas, celulas o tejidos) para realizar operaciones logicas, amtematicas, o de almacenamiento de datos. En lugar de usar transistores y silicio, emplea procesos biologicos naturales como la replicacion, transcripcion o traduccion las interacciones anzimaticas y redes metabolicas para procesar informacion. Sus caracteristicas principales son el encuentro se substrato vivo el cual funciona a partir de material genetico o celular, con un paralelismo masico de millones de moleculas las cuales pueden interactuar simultaneamente con un ambiente molecular en el cual se realizan los calculos en soluciones quimicas o entornos celulares y en un proposito interdisciplinar donde se combina biologia sintetica, bioquimica, ingenieria de sistemas, nanotecnologia y ciencias de la computacion. 

la diferencia con neuromorfico o cuantico es que el neuromorfico imita al cerebro con silicio, el cuantico aprovecha fenomenos de la mecanica cuantica y el biologico usa directamente la biologia como hardware.

## Tipos Ordenadores Biologicos 
1. Computacion basada en ADN: el cual usa moleculas de ADN como soporte para codificar informacion, donde el ADN almacena la informacion en secuencias de nucleotidos (A,T,C,G)
y puede procesarse mediante hibridacion, enzimas y reacciones quimicas, donde es altamente paralelo y billones de moleculas pueden realizar calculos en un tubo de ensayo al mismo tiempo y asi poder resolver problemas de combinatoria, criptografia, almacenamiento de datos.

2. Computacion Celular: Se emplean celulas vivas como bacterias, levaduras o celulas humanas modificadas geneticamente, cada celula puede funcionar como una unidad de procesamiento que responde a estimulos quimicos o luminicos y prodcue una salida como proteina, fluorescencia o metabolito. Esta se basa en redes reguladoreas de genes sinteticos, que actuan como compuertas logicas biologicas (AND, OT, NOT).
3. Computacion basada en proteinas y enzimas: Utiliza enzimas o proteinas que actuan como catalizadores pra procesar la informacion, como reacciones enzimaticas que realizan sumas,restas o clasificacion molecular con alta velocidad quimica y precision molecular.
4. Computacion hibrida: Intebgra sistemas biologicos con dispostivos electronicos como interfaces de ADN o proteinas con transistores y biosensores, creando biochips que combinan lo mejor de ambos mundos, lo cual lo hace ser un campo emergente con gran potencial en bioinformaticas, medicina personalizada y bio-robotica.

## Principales hitos de los ordenadores Biologicos.
- 1994: Es cuando Leonard Adleman resolvio un problema del camino hamiltoniano(NP-completo) utilizando moleculas de ADN en un tubo de ensayo.
- 1997: Richard Lipton y otros demostraron como implementar operaciones logicas con cadenas de ADN, abriendo la puerta a la logica booleana molecular.
- 2002: James J Collins y su equipo diseñaron un cricuito genetico sintetico que actuaba como un oscilador dentro de bacterias, marcando el nacimiento de la biologia sintetica como soporte de computacion.
- 2004: Ehud Shapiro y su equipo crearon un sistema de ADN y enzimas capaz de funcionar como un automata finito, procesando entrada y produciendo salidas moleculares, el sistema funcionaba con precision en medio liquido.
- 2010: Computacion celular programable con el auge d eCRISPR y la edicion genetica, se lograron celulas vivas programadas para detectar señales y responder con proteinas fluorescentes.
- 2017: Almacenamiento masivo de datos en ADN donde microsoft y la universidad de Washington codificaron 200 MB de datos digitales en moleculas de ADN, demostrando un almacenamiento ultradenso donde 1g de ADN puede guardar hasta 215 petabytes.
- 2020 en adelante: Bioordenadores hibridos y biomemoria, donde se encuentra la investigacion en memristores biologicos, proteinas como elemnetos logicos y biochips hibridos que conectan ADN con electronica. Tambien hitos reciente sincluyen la creacion de tejidos neuronales en chips para pruebas de farmacos y procesamiento sensorial. 

# Computacion Heterogenea.
La computacion heterogenea es una paradigma arquitectonico que combina diferentes tipos de unidades de procesamiento (CPU,GPU,FPGA,TPU,ASIC, entre otros) estos van dentro de un mismo sistema para ejecutar aplicaciones de manera mas eficiente que con una arquitectura homogenea basada unicamente en CPU. Esta arquitectura no busca reemplazar un tipo de procesador con otro, si no integrarlos en un ecosistema donde cada unidad resuelva la parte de un problema que mejor se ajuste a sus capacidades.
Siendo un sistema de computo Hibrido con multiples instrucciones de arquitectura conocidas como: Instruction set Architectures (ISAs), gestionado por software como compiladores, runtimes, APIs, OpenCL, SYCL o ROCm que orquestan la ejecucion en los distintos dispositivos 
Este aprovecha las fortalezas especoficas de cada tipo de procesador:

-CPU: "Central Processing Unit". El es flexible, secuencial, optimizada para tareas de control, operaciones generales y flujo de programa.

-GPU: "Graphics Processing Unit" Masivamente paralela orientada a calculos numericos repetitivos y procesamiento vectorial o matricial.

-FPGA:"Field Proggrammable Gate Array". Reconfigurable y de muy baja latecnias y eficiente energeticamente para algortimos especificos.

-TPU:"Tensor Processing Unit". Procesador especializado en operaciones de aprendizaje automatico,

## Historia Computacion Heterogenea.

- 1960-1980: Ya en los supercomputadores vectoriales, se empieza a explorar la idea de aceleradores especializados para mejorar el rendimiento de operaciones matematicas pero sin embargo la integraccion con CPUs aun era limitada asi que coexistian, pero no existia una arquitectura de software unificada.

- 1990: "GPUs como coprocesadores graficos". Las GPUs comenzaron como dispositivos dedicados al renderizado grafico. Estas no estaban pensadas para computo general, pero su naturaleza paralela atrajo la atencion de investigadores.

- 2000-2006: "GPGPU General purpose compiuting on GPUs". Investigadores empezaron a usar Gpus para computo cientifico antes de existir CUDA los cuales se programabn con shaders graficos. Ya en 2006 Nvidia lanza CUDA, marcando un antes y un despues al permitir programar GPUs en C/C++ para tareas generales.

- 2007-2010: "Consolidacion" Aparece OpenCL (Khronos Group), un estandar abierto para programacion en multiples dispositivos heterogeneos, donde AMD y NVIDIA lideran el campo.

- 2010-presente: "Ecosistemas heterogeneos integrados". La ley de Moore desacelera y obliga a buscar paralelismo y especializacion, A su vez google desarrolla TPus en 2015 para aprendizaje profundo, mientras intel y AMD integran Apus (CPUs + GPU en un mismo chip). Arquitecturas HPC como exascale computing se basan casi siempre en heterogenidad y actualmente frameworks como SYCL o ROCm buscan portabilidad y eficiencia en sistemas heterogeneos.

## Ventajas Computacion Heterogenea.
- **Maximo rendimiento por tarea** en donde cada procesador se dedica a lo que mejor hace, donde la CPU controla la logica y la GPU entrena redes neuronales y la FPGA acelera criptografia.
- **Eficiencia Energetica** Ya que un acelerador especializado como un ASIC puede ser entre 10 y 100 veces mas eficiente que una CPU para la misma tarea.
- **Escalabilidad y Flexibilidad** Permite escalar sistemas hacia aplicaciones muy diversas, desde HPC hasta Iot.
- **Versatibilidad en Aplicaciones** Usada en simulaciones cientificas, inteligencia artificial, procesamiento de imagenes, Big Data, criptografia cuantica post-cuantica, etc.
- **Supercomputacion Moderna** Todos los superordenadores top del ranking TOP500 como frontier, Aurora, Fugaku son heterogeneos porque ya no es viable escalar solo con CPUs.

## Desventajas.
-

