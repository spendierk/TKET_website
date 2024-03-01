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

The following schematic provides a glimpse into TKET's architecture, highlighting its compatibility with quantum libraries and its ability to target a diverse range of quantum devices and simulators.

.. image:: https://github.com/spendierk/TKET_website/blob/main/tket_architecture.jpg
   :alt: TKET Architecture diagram
   :width: 600px
   :align: center

- **Quantum Compiler**: Anchored by a C++ core, TKET is an efficient compiler adjusting quantum circuits for specific quantum hardware and simulator constraints. Here, quantum circuits undergo rewriting, device constraint resolution, and optimization.
- **Platform Agnostic Execution**: TKET targets various quantum processors and simulators, with added cloud access through select platforms.
- **Library Integration**: TKET simplifies circuit creation, facilitates code reuse, and is compatible with leading quantum libraries.
- **Python Interface**: Access TKET via its Python frontend, ``pytket``. Installation is as simple as ``pip install pytket``. For installation issues, refer to our `troubleshooting guide <https://cqcl.github.io/tket/pytket/api/install.html>`_.
- **Extension Modules**: ``pytket`` `extensions <https://cqcl.github.io/pytket-extensions/api/index.html>`_ connect to different backends and support the cross-compilation of circuits from well-known quantum libraries. 


Quantum Software Workflow
------------------------
To understand TKET's full potential, let's see where it fits within the quantum computing landscape. This schematic illustrates the quantum computing stack, from high-level tasks down to physical quantum hardware or simulator execution.

.. image:: https://github.com/spendierk/TKET_website/blob/main/QA_workflow3.jpg
   :alt: Quantum Computing Stack diagram
   :width: 800px
   :align: center

- **Use Cases**: Problems addressed using quantum computing, encompassing areas like machine learning, chemistry, or optimization.
- **Application Software**: Specialized algorithms generate quantum circuits for a given use case.
- **Quantum Circuit**: The fundamental quantum algorithm uses universal gate sets and all-to-all connectivity to describe the quantum Fourier transform (QFT), for example.
- **Classical Simulator**: This tool allows quantum circuits to run on a classical simulator, such as a state vector simulator.
- **Quantum Circuit Compiler**: Quantum circuits are tailored for specific quantum hardware constraints using TKET, for example, considering qubit connectivity, native gate sets, and quantum gate error rates. Circuit optimization also occurs at this stage.
- **QIR/QASM**: QIR (Quantum Intermediate Representation) and QASM (Quantum Assembly Language) are hardware-agnostic descriptions of quantum algorithms that are transformed into concrete, executable forms tailored to the specific requirements of the simulation or quantum hardware environments.
- **Quantum Simulator/Emulator**: A tool that simulates/emulates quantum computer behavior, letting developers test and refine algorithms without using actual quantum hardware.
- **Machine Code**: Post-optimization, the circuit is converted into machine code for quantum processors (QPUs) or quantum simulators.
- **Quantum Processor**: The hardware layer where quantum circuits are physically executed to produce results.

TKET supports a variety of optimization levels, from basic translations of circuits to fit hardware constraints to advanced optimizations that significantly reduce gate counts. For users seeking to push the boundaries of optimization, TKET offers detailed control over the compilation process, enabling fine-tuning to achieve the best possible performance for specific quantum circuits.



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
