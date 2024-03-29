What is TKET?
==============

TKET is an open-source quantum software development kit (SDK) for gate-based quantum computers. It compiles and optimizes quantum circuits, including the optimization of quantum kernels—a combination of quantum and classical operations—ensuring compatibility and high performance on various quantum devices and simulators. Additionally, TKET facilitates the dispatch of these optimized kernels to the quantum computer and processes the received counts, or measurement outcomes, from the quantum computation. TKET is a platform-agnostic software and extracts the most out of the available noisy intermediate-scale quantum (NISQ) devices of today.

TKET is available under the Apache 2 license and implemented in C++, with a Python module, ``pytket``, providing a more accessible interface for users. This arrangement leverages the high performance of C++ for core operations while utilizing Python for tasks like network communication and result processing. TKET integrates with a wide range of quantum computing platforms and frameworks through extension modules, such as ``pytket-quantinuum`` for Quantinuum hardware and ``pytket-qiskit`` for IBM's quantum SDK Qiskit and their quantum systems, among others.

Why TKET?
==============
Quantum computing involves the manipulation of quantum bits (qubits) to perform computations that classical computers find challenging. A quantum computation consists of initializing qubits, applying a series of quantum gates (operations), and measuring the qubits to obtain an outcome. The sequence of gates, known as a quantum circuit, is critical in determining the computation's success.

Quantum computing is difficult because of:
--------------------------------------
- **Technical Limitations**: Algorithm performance is limited by the number of gates (circuit depth).
- **Resource Constraints**: Current quantum computers don't have enough qubits for many applications.
- **Noise Constraints**: Existing qubits and quantum gates are noisy, requiring us to use fewer gates to limit errors. 
- **Device Constraints**: Specific challenges arise from gate choice, qubit connectivity, and hardware-specific nuances.

TKET addresses these constraints and limitations in quantum computing.

Quantum Software Workflow
=========================

The workflow within a gate-based quantum computer ecosystem involves a series of translations and transformations to take a high-level quantum circuit description and make it executable on quantum hardware or simulators.

High-Level User Engagement
--------------------------
At the highest level, users provide a high-level description of the quantum circuit they wish to execute. This description avoids individual gate considerations in favor of large algorithmic components and many-qubit operations, such as Quantum Fourier Transforms or Trotterised Hamiltonians, without the need to account for specific gate-set or architectural constraints of the quantum machine.

TKET's Role
------------
TKET functions as a sophisticated circuit compiler that transforms high-level circuit descriptions into a 'Compiled Quantum Intermediate Form.' This form is comparable to assembly language in classical computing, tailored to meet the operational capabilities and architectural constraints of specific quantum hardware. For example, TKET can also apply error mitigation strategies to enhance the reliability and accuracy of quantum computations.

The intermediate form generated by TKET can be represented in various formats, including Extended QASM, HUGR, and QIR, which accommodate the nuances of different quantum computing frameworks. Additionally, TKET ensures compatibility with other frameworks, for example, by supporting the conversion of quantum circuits into Qiskit Objects or JSON format. These capabilities ensure the processed quantum circuits are ready for execution, with all hardware constraints satisfied and optimizations applied.


Intermediate and Low-Level Processing
--------------------------------------
After TKET's compilation, the Compiled Quantum Intermediate Form is handed off to a lower-level compiler, such as L3. This compiler translates the platform-independent circuit description into actual control signals that are suitable for quantum processors. Alternatively, the intermediate form may be passed to a quantum simulator, enabling the circuit to be run on a classical computer, thus providing a flexible approach to quantum circuit testing and validation.

.. COMMENT
.. add workflow schematic like Ross's from his RIKEN talk
.. The provided schematic visualizes the workflow from the end user's application software through the TKET compilation process to the ultimate execution on either quantum or classical processing units. This workflow enables users to concentrate on the algorithmic dimensions of quantum computing while leveraging TKET and subsequent tools to manage the complexities of circuit optimization, translation, and execution.

Key TKET Features and Advantages
===============================
TKET facilitates the process of preparing, optimizing, and executing quantum circuits. It acts as a bridge between the algorithmic intentions of the user, expressed in Python, and the specific requirements of quantum hardware. By providing tools for circuit optimization, TKET helps reduce the number of gates and, consequently, the computation's noise and duration. This optimization is crucial in the NISQ era, where minimizing errors is essential for obtaining reliable results.

- **Direct Operations**: With TKET, tell it what you want, and it handles the complex parts.
- **Smart Compiler**: TKET deals with common constraints found in NISQ devices.
- **Flexibility**: Use TKET no matter your coding language or the quantum computer/simulator you're using.
- **Focus on Your Work**: TKET handles the technical side so that you can work on your main project.

Extensions and Interoperability
--------------------------------
A key feature of TKET is its extensive support for interoperability with other quantum computing frameworks and hardware platforms. Through extension modules, users can easily integrate TKET with their preferred quantum computing resources. These extensions cover a wide range of functionalities, from accessing different quantum hardware and simulators to interfacing with other quantum programming languages and libraries. This flexibility makes TKET a versatile tool for quantum software development, accommodating a variety of use cases and preferences.

.. COMMENT
.. add here a schematic like Ross's from his RIKEN talk
.. The following schematic provides a glimpse into TKET's architecture, highlighting its compatibility with quantum libraries and its ability to target a diverse range of quantum devices and simulators.

How To Cite
-----------

For general references to TKET, cite our `software overview paper <https://doi.org/10.1088/2058-9565/ab8e92>`_. For specific compilation topics, consider:

- `Qubit routing <https://doi.org/10.4230/LIPIcs.TQC.2019.5>`_.
- `Phase Gadget Synthesis <https://doi.org/10.4204/EPTCS.318.13>`_.
- `Compilation Strategy for Unitary Coupled Cluster Ansatz <https://arxiv.org/abs/2007.10515>`_.

For benchmarking against TKET, see our `benchmark repository <https://github.com/CQCL/tket_benchmarking>`_. Please specify the ``pytket`` release version in benchmarks. For benchmark guidance, contact us.


Support
-------
- Report bugs or suggest features on our `GitHub issues board <https://github.com/CQCL/pytket>`_. Detailed error messages and steps to reproduce help expedite resolutions.

- Engage in community discussions and seek support in our `Slack channel <https://join.slack.com/t/tketusers/shared_invite/zt-18qmsamj9-UqQFVdkRzxnXCcKtcarLRA>`_.

- For team-specific support, research partnerships, or commercial license queries, contact us at info@cambridgequantum.com. For support-related questions, write to tket-support@cambridgequantum.com.



