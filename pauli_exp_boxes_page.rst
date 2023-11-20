
`PauliExponential` Boxes in `pytket`
================================

Motivation and Context
----------------------
Pauli Exponential Boxes (`PauliExpBoxes`) in `pytket` are crucial constructs commonly used in various quantum algorithms and high-level circuit descriptions. These boxes represent the exponential of a Pauli tensor, a fundamental component in Trotterising evolution operators and native device operations.

The reader should be familiar with basic quantum computing concepts and `pytket`'s circuit manipulation functionalities. For an introduction, refer to [Introduction to Pytket](link_to_intro_page).

These Pauli gadget circuits have interesting algebraic properties which are useful for circuit optimisation. For instance Pauli gadgets are unitarily invariant under the permutation of their qubits. For further discussion see the research publication on phase gadget synthesis [Cowt2020]_. Ideas from this paper are implemented in TKET as the `OptimisePhaseGadgets <https://cqcl.github.io/tket/pytket/api/passes.html#pytket.passes.OptimisePhaseGadgets>`_ and `PauliSimp <https://cqcl.github.io/tket/pytket/api/passes.html#pytket.passes.PauliSimp>`_ optimisation passes.

Mathematical Description
------------------------
A Pauli Exponential Box in pytket represents the operation:

.. math::
    \begin{equation}
    e^{-i rac{	heta}{2} P}\,, \quad P \in \{I, X, Y, Z\}^{\otimes n}
    \end{equation} 

where $ \theta $ is a phase angle, and $P$ is a tensor product of Pauli matrices. This operation is crucial in quantum algorithms for simulating quantum systems and in constructing various quantum gates.

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

Feature 2: `PauliExpPairBox`
-----------------------------------------------------
The `PauliExpPairBox` represents a pair of exponentials of a tensor of Pauli operations. This can be useful for creating entangled states or specific quantum gates.

.. code-block:: python

    from pytket.circuit import PauliExpPairBox, Circuit
    from pytket.pauli import Pauli

    # Create a pair of Pauli exponentials
    pair_box = PauliExpPairBox([Pauli.X, Pauli.Y], [Pauli.Z, Pauli.Z], 0.5)

    # Create a circuit and add the PauliExpPairBox
    circuit = Circuit(2)
    circuit.add_pauliexppairbox(pair_box, [0, 1])

Feature 3: PauliExpCommutingSetBox
-----------------------------------------------------
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

Trotterization with PauliExpBoxes
---------------------------------
Trotterization is an advanced technique used in quantum computing for simulating the evolution of quantum systems. It involves breaking down a complex exponential operator into a product of simpler exponentials that are easier to implement on quantum hardware.

In pytket, PauliExpBoxes can be used to implement Trotterization steps. A minimal example demonstrating this is shown below:

.. code-block:: python

    from pytket.circuit import PauliExpBox, Circuit
    from pytket.pauli import Pauli
    import numpy as np

    # Define the Trotter step for a Hamiltonian H = X0 X1 + Y0 Y1
    theta = np.pi / 4  # Example evolution time
    trotter_step = Circuit(2)
    trotter_step.add_pauliexpbox(PauliExpBox([Pauli.X, Pauli.X], theta), [0, 1])
    trotter_step.add_pauliexpbox(PauliExpBox([Pauli.Y, Pauli.Y], theta), [0, 1])

    # Example: Apply 3 Trotter steps
    for _ in range(3):
        trotter_step.append(trotter_step)

This example represents a simple case of trotterizing a two-qubit Hamiltonian. In practice, the Hamiltonian and the Trotter step count can be more complex, depending on the quantum simulation requirements.

Refer to [Link to Knowledge Article SU2] for more comprehensive insights into trotterization techniques in quantum computing.




References
----------
1. [Cowt2020] - [Title of the research paper/publication]
2. [Link to OptimisePhaseGadgets documentation]
3. [Link to PauliSimp documentation]
