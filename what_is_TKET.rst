
What is TKET?
=====================
TKET is an advanced, open-source software development kit for gate-based quantum computers. Its primary role is to compile and optimize quantum circuits for various quantum hardware and simulators, ensuring high performance and compatibility.

In the current NISQ (Noisy Intermediate-Scale Quantum) era, devices often come with limited qubits and higher error rates. TKET plays a pivotal role in this landscape, optimizing and refining quantum circuits to mitigate these challenges. This ensures that users obtain the most accurate outcomes, even when working with device constraints and noise considerations.

**Key Features of TKET:**

- **Ease of Use:** Effortlessly apply gate-level quantum computers to solve challenging problems.
- **Advanced Compiler:** Automatically handles the intricacies of NISQ technology, optimizing quantum circuits for peak performance on various quantum hardware and simulators.
- **Language, Hardware, and Simulator Flexibility:** TKET is independent of the programming language and the specific quantum computer or simulator, ensuring broad compatibility and flexibility.
- **User-Centric:** Allows users to focus solely on their techniques or projects without getting bogged down by underlying complexities.
  
**Benefits for Users:**

- Code for quantum computers in your language of choice.
- Execute quantum algorithms with enhanced efficiency.
- Achieve high accuracy results without compromising on the problem-solving focus.

This documentation targets readers who are already familiar with the basics of quantum computing via the circuit model and want to explore the tools available in TKET. It provides a comprehensive, feature-focussed tour of the platform to take you from “Hello world” to playing with advanced techniques for speeding up and improving the accuracy of your quantum experiments.

Quantum Computing Stack Overview:
---------------------------------
The following schematic provides a comprehensive overview of the quantum computing stack, detailing the progression from high-level tasks to the physical execution on quantum hardware.

.. image:: https://github.com/spendierk/TKET_website/blob/main/QA_workflow.jpg
   :alt: Alternative text for the image
   :width: 800px
   :align: center

- **Use Cases**: These represent specific tasks or challenges one might want to address using quantum computing, like machine learning, chemistry, or optimization problems.
- **Applications Software**: At this layer, specialized algorithms, such as the Quantum Fourier Transform (QFT), are created to generate quantum circuits using a universal set of gates.
- **Quantum Circuit**: Represents the raw quantum algorithm with universal gatesets. Here, you can visualize algorithms like QFT as they are intended to operate at a high level.
- **TKET Optimization**: A critical phase where quantum circuits are refined and optimized considering specific quantum hardware constraints. These constraints include limited qubit connectivity, native gatesets (e.g., ECR, ID, RZ, SX, X), and error rates.
- **Quantum Simulator**: Before running a quantum algorithm on an actual quantum processor, it can be tested on a quantum simulator. This software tool mimics the behavior of a quantum computer, allowing developers to understand potential outcomes, troubleshoot issues, and refine algorithms without directly using quantum hardware.
- **Hardware Translation**: Once the circuit is optimized with tools like TKET, it is translated into machine code that quantum processors (QPUs) understand. This code can be directly executed on QPUs or simulated using quantum simulators.
- **Quantum Processor**: This is the hardware layer where the quantum computations physically take place. Quantum circuits in machine code are executed on these quantum processing units to get the desired results.



Key Features:
-------------
The second schematic illustrates the architecture of TKET, showcasing its versatile compatibility with quantum libraries, its robust compiler capabilities, and the diverse range of quantum processing units and simulators it targets.

.. image:: https://github.com/spendierk/TKET_website/blob/main/tket_architecture.jpg
   :alt: Alternative text for the image
   :width: 600px
   :align: center

- **Quantum Compiler**: TKET, underpinned by a high-performance C++ library, is a high-performance compiler that tailors quantum circuits to the constraints of specific quantum hardware and simulators. Within TKET's C++ core, quantum circuits are rewritten, device constraints are solved, and optimization is performed.
- **Platform Agnostic**: TKET can target a variety of quantum processing units (QPUs) and simulators. This is where quantum circuits are executed. Cloud access through specific platforms is also available.
- **Integration with Libraries**: TKET is compatible with popular quantum libraries, offering the ability to build circuits seamlessly.
- **Python Interface**: TKET is accessible through its Python frontend package, ``pytket``, available on GitHub and installed with the command ``pip install pytket``. For any difficulties with installation, please consult our `troubleshooting <https://cqcl.github.io/tket/pytket/api/install.html>`_ page.
- **Extension Modules**: ``pytket`` `extensions <https://cqcl.github.io/pytket-extensions/api/index.html>`_ facilitate connections to various backends, representing links to QPUs or simulators. Cloud extensions further enhance access to platforms like Azure and Braket. Additionally, these modules support the cross-compilation of circuits from popular quantum libraries, seamlessly integrating ``pytket``'s compilation strengths with other software tools.


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


References
-------
.. [Pres2018] Preskill, J., 2018. Quantum Computing in the NISQ era and beyond. Quantum, 2, p.79.
.. [Arut2019] Arute, F., Arya, K., Babbush, R., Bacon, D., Bardin, J.C., Barends, R., Biswas, R., Boixo, S., Brandao, F.G., Buell, D.A. and Burkett, B., 2019. Quantum supremacy using a programmable superconducting processor. Nature, 574(7779), pp.505-510.

