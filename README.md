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


En el estado de n qubits vive en el producto 

