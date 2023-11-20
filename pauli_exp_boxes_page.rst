
PauliExponential Boxes in Pytket
================================

Motivation and Context
----------------------
Pauli Exponential Boxes (PauliExpBoxes) in pytket are crucial constructs commonly used in various quantum algorithms and high-level circuit descriptions. These boxes represent the exponential of a Pauli tensor, a fundamental component in Trotterising evolution operators and native device operations.

The reader should be familiar with basic quantum computing concepts and pytket's circuit manipulation functionalities. For an introduction, refer to [Introduction to Pytket](link_to_intro_page).

PauliExpBoxes are integral to the broader scope of quantum circuit optimization and manipulation in TKET. They leverage the algebraic properties of Pauli gadgets for efficient quantum computation.

See [Cowt2020] for more on phase gadget synthesis, related to PauliExpBox optimizations in TKET.

Implementation/Usage
---------------------

Feature 1: Adding a PauliExpBox to a Circuit
---------------------------------------------
The `add_pauliexpbox` method allows appending a PauliExpBox to a circuit. This box can be applied to either integer indices or specific qubits in a circuit.

.. code-block:: python

    from pytket.circuit import PauliExpBox, Circuit
    from pytket.pauli import Pauli

    # Create a PauliExpBox
    xyyz = PauliExpBox([Pauli.X, Pauli.Y, Pauli.Y, Pauli.Z], -0.2)

    # Create a circuit and add the PauliExpBox
    circuit = Circuit(4)
    circuit.add_pauliexpbox(xyyz, [0, 1, 2, 3])

Feature 2: PauliExpCommutingSetBox and PauliExpPairBox
-----------------------------------------------------
`PauliExpPairBox` and `PauliExpCommutingSetBox` in pytket allow for the implementation of complex quantum operations involving pairs and sets of commuting Pauli exponentials.

**PauliExpPairBox Example:**

The `PauliExpPairBox` represents a pair of exponentials of a tensor of Pauli operations. This can be useful for creating entangled states or specific quantum gates.

.. code-block:: python

    from pytket.circuit import PauliExpPairBox, Circuit
    from pytket.pauli import Pauli

    # Create a pair of Pauli exponentials
    pair_box = PauliExpPairBox([Pauli.X, Pauli.Y], [Pauli.Z, Pauli.Z], 0.5)

    # Create a circuit and add the PauliExpPairBox
    circuit = Circuit(2)
    circuit.add_pauliexppairbox(pair_box, [0, 1])

**PauliExpCommutingSetBox Example:**

The `PauliExpCommutingSetBox` is used for a set of commuting exponentials of Pauli operations. This is particularly useful in algorithms where commuting operations can be grouped for efficiency.

.. code-block:: python

    from pytket.circuit import PauliExpCommutingSetBox, Circuit
    from pytket.pauli import Pauli

    # Create a set of commuting Pauli exponentials
    commuting_set_box = PauliExpCommutingSetBox([Pauli.X, Pauli.Z], [0.3, 0.7])

    # Create a circuit and add the PauliExpCommutingSetBox
    circuit = Circuit(2)
    circuit.add_pauliexpcommutingsetbox(commuting_set_box, [0, 1])

Advanced Topics/Features
------------------------
Advanced uses of PauliExpBoxes may involve optimizing phase gadgets and employing complex algebraic properties for circuit optimization.

Refer to [Advanced Pytket Techniques](link_to_advanced_techniques_page) for a deeper exploration of these topics.

References
----------
1. [Cowt2020] - [Title of the research paper/publication]
2. [Link to OptimisePhaseGadgets documentation]
3. [Link to PauliSimp documentation]
