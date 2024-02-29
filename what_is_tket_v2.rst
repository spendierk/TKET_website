What is TKET?
==============

TKET is an open-source, platform-agnostic quantum software development kit (SDK) designed for optimizing quantum circuits across various quantum computing devices and simulators. Its primary goal is to maximize the performance of quantum algorithms within the noisy intermediate-scale quantum (NISQ) era. TKET stands out for its ability to compile and optimize quantum kernels, a combination of quantum and classical operations, into a form that quantum devices can execute efficiently.

TKET is available under the Apache 2 license and implemented in C++, with a Python module, `pytket`, providing a more accessible interface for users. This arrangement leverages the high performance of C++ for core operations while utilizing Python for tasks like network communication and result processing. TKET integrates with a wide range of quantum computing platforms and frameworks through extension modules, such as `pytket-quantinuum` for Quantinuum hardware and `pytket-qiskit` for IBM's Qiskit, among others.

Quantum Computing with TKET
===========================

Quantum computing involves the manipulation of quantum bits (qubits) to perform computations that classical computers find challenging. A quantum computation consists of initializing qubits, applying a series of quantum gates (operations), and measuring the qubits to obtain an outcome. The sequence of gates, known as a quantum circuit, is critical in determining the computation's success.

TKET's Role in Quantum Computing
--------------------------------

TKET facilitates the process of preparing, optimizing, and executing quantum circuits. It acts as a bridge between the algorithmic intentions of the user, expressed in Python, and the specific requirements of quantum hardware. By providing tools for circuit optimization, TKET helps reduce the number of gates and, consequently, the computation's noise and duration. This optimization is crucial in the NISQ era, where minimizing errors is essential for obtaining reliable results.

TKET supports a variety of optimization levels, from basic translations of circuits to fit hardware constraints to advanced optimizations that significantly reduce gate counts. For users seeking to push the boundaries of optimization, TKET offers detailed control over the compilation process, enabling fine-tuning to achieve the best possible performance for specific quantum circuits.

Extensions and Interoperability
--------------------------------

A key feature of TKET is its extensive support for interoperability with other quantum computing frameworks and hardware platforms. Through extension modules, users can easily integrate TKET with their preferred quantum computing resources. These extensions cover a wide range of functionalities, from accessing different quantum hardware and simulators to interfacing with other quantum programming languages and libraries. This flexibility makes TKET a versatile tool for quantum software development, accommodating a variety of use cases and preferences.


How To Cite
===========

For general references to TKET, cite our `software overview paper <https://doi.org/10.1088/2058-9565/ab8e92>`_. For specific compilation topics, consider:

- `Qubit routing <https://doi.org/10.4230/LIPIcs.TQC.2019.5>`_.
- `Phase Gadget Synthesis <https://doi.org/10.4204/EPTCS.318.13>`_.
- `Compilation Strategy for Unitary Coupled Cluster Ansatz <https://arxiv.org/abs/2007.10515>`_.

For benchmarking against TKET, see our `benchmark repository <https://github.com/CQCL/tket_benchmarking>`_. Please specify the ``pytket`` release version in benchmarks. For benchmark guidance, contact us.


Support
=======
- Report bugs or suggest features on our `GitHub issues board <https://github.com/CQCL/pytket>`_. Detailed error messages and steps to reproduce help expedite resolutions.
- Engage in community discussions and seek support in our `Slack channel <https://join.slack.com/t/tketusers/shared_invite/zt-18qmsamj9-UqQFVdkRzxnXCcKtcarLRA>`_.
- For team-specific support, research partnerships, or commercial license queries, contact us at info@cambridgequantum.com. For support-related questions, write to tket-support@cambridgequantum.com.
