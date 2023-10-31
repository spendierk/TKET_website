
Introduction to TKET
=====================

TKET is an advanced, open-source software development kit designed for gate-based quantum computers like Quantinuum's ion-trap devices. Its primary role is to compile and optimize quantum circuits for a variety of quantum hardware and simulators, ensuring high performance and compatibility.


In the current NISQ (Noisy Intermediate-Scale Quantum) era, devices have limited qubits and higher error rates. TKET plays a crucial role in optimizing and simplifying quantum circuits to navigate these challenges, ensuring reliable outcomes even with device constraints and noise considerations.

Key Features:
-------------

- **Quantum Compiler**: TKET is a high-performance compiler that tailors quantum circuits to the constraints of specific quantum hardware.
- **Platform Agnostic**: It can target various quantum processing units (QPUs) and simulators.
- **Integration with Libraries**: Compatible with popular quantum libraries such as Qiskit, Cirq, Braket, PennyLane, and more.
- **Python Interface**: TKET is accessible through its Python package, pytket, available on GitHub. Install with the command pip install pytket.

Quantum Computing Stack Overview:
---------------------------------

1. **Use Cases**: Specific tasks like machine learning and chemistry tackled using quantum algorithms.
2. **Software Applications**: Generate quantum circuits, like a QFT, with universal gates.
3. **TKET Optimization**: Refines circuits based on hardware limitations, such as stricter gatesets and qubit connectivity.
4. **Hardware Translation**: Post-TKET processing translates optimized circuits into machine code for QPUs.

.. note:: Visual Element Suggestion: A vertical stack diagram illustrating the quantum computing stack, highlighting TKET's position and its role in optimization.

Backend Support:
----------------

Through pytket, users can interact with TKET and platforms like Qiskit, Cirq, and PennyLane. Once circuits are optimized, TKET can compile them for devices like Quantinuum's ion trap and IBMQ's superconducting units. TKET offers Python packages for various backends, with cloud integration for AWS Braket and Microsoft Azure.

Support & Collaboration:
------------------------

For any issues, feature suggestions, or collaborations, visit our `GitHub repository <#>`_ or contact us at `tket-support@cambridgequantum.com <mailto:tket-support@cambridgequantum.com>`_. Join our `Slack channel <#>`_ and `mailing list <#>`_ for updates and discussions.

Citations:
----------

For academic references, please cite our `software overview paper <#>`_. For specific compilation tasks, refer to our `other papers <#>`_.
