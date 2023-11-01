What is TKET?
==============

TKET is an open-source quantum SDK designed for gate-based quantum computers. It compiles and optimizes quantum circuits, ensuring compatibility and high performance on various quantum devices and simulators. With the challenges of the Noisy Intermediate-Scale Quantum (NISQ) era, TKET stands out in mitigating device constraints and noise for accurate results.

.. note:: 
 This guide is crafted for those already acquainted with the circuit model of quantum computing to explore TKET in detail, from its basics to advanced features, helping users enhance their quantum computing experiments.

Some Challenges with Quantum Computing
--------------------------------------
- **Not Enough Qubits**: Many exciting quantum applications require a greater number of qubits than what is currently available.
- **Complex Noise on Qubits**: The qubits we do have are subject to intricate noise patterns, which are challenging to model accurately.
- **Two-Qubit Gate Errors**: The error rate for two-qubit gates is typically orders of magnitude larger than single-qubit gate errors. Reducing the number of two-qubit gates is crucial to improve computational accuracy.
- **Early Stages of Quantum Error Correction**: Quantum error correction, essential for robust quantum computation, is still in its experimental infancy.
- **Influence of Low-Level Details**: The performance of quantum algorithms can be significantly impacted by low-level factors such as gate count and qubit connectivity.

Addressing these quantum computing challenges, TKET emerges as an indispensable tool. Its design and features are tailored to navigate the complexities of quantum computing and offer a streamlined experience. Let's delve into the key aspects that make TKET a standout quantum SDK.

Key TKET Features and Advantages
===============================
- **Ease of Use:** Solve complex problems using gate-level quantum computers.
- **Advanced Compiler:** Seamlessly navigate the intricacies of NISQ technology with optimized circuits across different hardware and simulators.
- **Flexibility:** Code with independence, no constraints on programming language, quantum computer, or simulator.
- **Efficiency:** Prioritize and streamline your problem-solving, allowing TKET to handle the underlying technicalities.
- **User-Centric Approach:** Remain focused on your projects and techniques, letting TKET manage the complexities.

TKET is designed to be an advanced optimizing compiler that prioritizes ease of use and efficiency in leveraging gate-level quantum computers.

Quantum Computing Stack:
------------------------
To understand TKET's full potential, let's see where it fits within the quantum computing landscape. This schematic illustrates the quantum computing stack, from high-level tasks down to physical quantum hardware or simulator execution.

.. image:: https://github.com/spendierk/TKET_website/blob/main/QA_workflow.jpg
   :alt: Quantum Computing Stack diagram
   :width: 800px
   :align: center

- **Use Cases**: Tasks or challenges addressed using quantum computing, such as machine learning, chemistry, or optimization.
- **Application Software**: Here, specialized algorithms generate quantum circuits from a universal set of gates, like the Quantum Fourier Transform (QFT).
- **Quantum Circuit**: The raw quantum algorithm using universal gate sets, showcasing high-level operations of algorithms like QFT.
- **TKET Optimization**: A crucial stage where quantum circuits are tailored for specific quantum hardware constraints, considering qubit connectivity, native gates, and error rates.
- **Quantum Simulator**: A tool that emulates quantum computer behavior, letting developers test and refine algorithms without using actual quantum hardware.
- **Hardware Translation**: Post-optimization, the circuit is converted into machine code for quantum processors (QPUs) or quantum simulators.
- **Quantum Processor**: The hardware layer where quantum circuits are physically executed to produce results.

Having outlined the quantum computing stack, let's now focus on TKET's role. Its architecture seamlessly bridges high-level applications to quantum hardware, ensuring efficient execution of quantum algorithms.

TKET Architecture Overview:
---------------------------
The following schematic provides a glimpse into TKET's architecture, emphasizing its broad compatibility with quantum libraries, advanced compilation, and diverse target quantum devices and simulators.

.. image:: https://github.com/spendierk/TKET_website/blob/main/tket_architecture.jpg
   :alt: TKET Architecture diagram
   :width: 600px
   :align: center

- **Quantum Compiler**: Anchored by a C++ core, TKET is an efficient compiler adjusting quantum circuits for specific quantum hardware and simulator constraints. Here, quantum circuits undergo rewriting, device constraint resolution, and optimization.
- **Platform Agnostic Execution**: TKET targets various quantum processors and simulators, with added cloud access through select platforms.
- **Library Integration**: Compatible with leading quantum libraries, TKET simplifies circuit creation and facilitates code reuse.
- **Python Interface**: Access TKET via its Python frontend, ``pytket``. Installation is as simple as ``pip install pytket``. For installation issues, refer to our `troubleshooting guide <https://cqcl.github.io/tket/pytket/api/install.html>`_.
- **Extension Modules**: ``pytket`` `extensions <https://cqcl.github.io/pytket-extensions/api/index.html>`_ connect to different backends and support the cross-compilation of circuits from well-known quantum libraries. 

In addition to the core attributes of its architecture, TKET further bolsters its capability with an array of other notable features. From the flexibility of constructing quantum circuits with an assortment of tools, including standard gates and circuit boxes, to the ease of importing circuits via QASM and QIR. Its rebasing capability ensures your circuits can transition between different gatesets effortlessly. To optimize the execution of quantum algorithms, TKET integrates advanced qubit placement, routing, and custom optimization techniques tailored for unique hardware constraints. For enthusiasts of graphical computation, the support for ZX Diagrams offers an intuitive representation. 

In this guide, we'll delve deeper into these and additional features, offering detailed code implementations and examples to showcase the full breadth of TKET's capabilities.


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

