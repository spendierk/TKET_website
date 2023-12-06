What is TKET?
==============

TKET is an open-source quantum software development kit (SDK) for gate-based quantum computers. It compiles and optimizes quantum circuits, ensuring compatibility and high performance on various quantum devices and simulators. TKET is a platform-agnostic software and extracts the most out of the available noisy intermediate-scale quantum (NISQ) devices of today.

.. note:: 
 This user manual targets readers who are already familiar with the basics of quantum computing via the circuit model and want to explore the tools available in TKET. It guides readers from basic "Hello world" to advanced methods for faster, more precise quantum experiments.

Why TKET?
==============

Quantum computing is difficult because of:
--------------------------------------
- **Technical Limitations**: Algorithm performance is limited by the number of gates (circuit depth).
- **Resource Constraints**: Current quantum computers don't have enough qubits for many applications.
- **Noise Constraints**: Existing qubits and quantum gates are noisy, requiring us to use fewer gates to limit errors. 
- **Device Constraints**: Specific challenges arise from gate choice, qubit connectivity, and hardware-specific nuances.

TKET addresses these constraints and limitations in quantum computing.

Key TKET Features and Advantages
===============================
- **Direct Operations**: With TKET, tell it what you want, and it handles the complex parts.
- **Smart Compiler**: TKET deals with common constraints found in NISQ devices.
- **Flexibility**: Use TKET no matter your coding language or the quantum computer/simulator you're using.
- **Focus on Your Work**: TKET handles the technical side so that you can work on your main project.

TKET is designed to be an advanced optimizing compiler that prioritizes ease of use and efficiency in leveraging gate-level quantum computers.

Quantum Computing Stack:
------------------------
To understand TKET's full potential, let's see where it fits within the quantum computing landscape. This schematic illustrates the quantum computing stack, from high-level tasks down to physical quantum hardware or simulator execution.

.. image:: https://github.com/spendierk/TKET_website/blob/main/QA_workflow3.jpg
   :alt: Quantum Computing Stack diagram
   :width: 800px
   :align: center

- **Use Cases**: Problems addressed using quantum computing, encompassing areas like machine learning, chemistry, or optimization.
- **Application Software**: Specialized algorithms generate quantum circuits from a universal set of gates, like the Quantum Fourier Transform (QFT).
- **Quantum Circuit**: The fundamental quantum algorithm uses universal gate sets and all-to-all connectivity, illustrating the core operations of algorithms like QFT.
- **Classical Simulator**: This tool allows quantum circuits to run on a classical simulator, such as a state vector simulator.
- **Quantum Circuit Compiler**: Quantum circuits are tailored for specific quantum hardware constraints using TKET, considering qubit connectivity, native gates, and error rates. Circuit optimization also occurs at this stage.
- **QIR/QASM**: QIR (Quantum Intermediate Representation) and QASM (Quantum Assembly Language) are hardware-agnostic descriptions of quantum algorithms that are transformed into concrete, executable forms tailored to the specific requirements of the simulation or quantum hardware environments.
- **Quantum Simulator/Emulator**: A tool that simulates/emulates quantum computer behavior, letting developers test and refine algorithms without using actual quantum hardware.
- **Machine Code**: Post-optimization, the circuit is converted into machine code for quantum processors (QPUs) or quantum simulators.
- **Quantum Processor**: The hardware layer where quantum circuits are physically executed to produce results.

Having outlined the quantum computing stack, let's focus on TKET's role. Its architecture bridges high-level applications to quantum hardware, ensuring efficient execution of quantum algorithms.

TKET Architecture Overview:
---------------------------
The following schematic provides a glimpse into TKET's architecture, emphasizing its compatibility with quantum libraries, advanced compilation, and diverse target quantum devices and simulators.

.. image:: https://github.com/spendierk/TKET_website/blob/main/tket_architecture.jpg
   :alt: TKET Architecture diagram
   :width: 600px
   :align: center

- **Quantum Compiler**: Anchored by a C++ core, TKET is an efficient compiler adjusting quantum circuits for specific quantum hardware and simulator constraints. Here, quantum circuits undergo rewriting, device constraint resolution, and optimization.
- **Platform Agnostic Execution**: TKET targets various quantum processors and simulators, with added cloud access through select platforms.
- **Library Integration**: TKET simplifies circuit creation, facilitates code reuse, and is compatible with leading quantum libraries.
- **Python Interface**: Access TKET via its Python frontend, ``pytket``. Installation is as simple as ``pip install pytket``. For installation issues, refer to our `troubleshooting guide <https://cqcl.github.io/tket/pytket/api/install.html>`_.
- **Extension Modules**: ``pytket`` `extensions <https://cqcl.github.io/pytket-extensions/api/index.html>`_ connect to different backends and support the cross-compilation of circuits from well-known quantum libraries. 

TKET's architecture is enhanced with several technical features. It allows the construction of quantum circuits using various tools, such as standard gates and circuit boxes, and supports importing circuits through QASM and QIR formats. The rebasing feature facilitates the conversion of circuits between different gate sets. For efficient quantum algorithm execution, TKET employs qubit placement, routing, and optimizations customized for specific hardware limitations. Additionally, it supports ZX Diagrams, enabling a visual approach to quantum computation.

This guide further explains these and other features, including code implementations and examples, to illustrate TKET's capabilities in detail.


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


References (need to update?)
-------
.. [Pres2018] Preskill, J., 2018. Quantum Computing in the NISQ era and beyond. Quantum, 2, p.79.
.. [Arut2019] Arute, F., Arya, K., Babbush, R., Bacon, D., Bardin, J.C., Barends, R., Biswas, R., Boixo, S., Brandao, F.G., Buell, D.A. and Burkett, B., 2019. Quantum supremacy using a programmable superconducting processor. Nature, 574(7779), pp.505-510.

