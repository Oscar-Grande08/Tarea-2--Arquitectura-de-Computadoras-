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


