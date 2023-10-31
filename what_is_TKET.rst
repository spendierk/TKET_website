
Introduction to TKET
=====================
TKET is an advanced, open-source software development kit for gate-based quantum computers. Its primary role is to compile and optimize quantum circuits for various quantum hardware and simulators, ensuring high performance and compatibility.

In the current NISQ (Noisy Intermediate-Scale Quantum) era, devices have limited qubits and high error rates. TKET is crucial in optimizing and simplifying quantum circuits to navigate these challenges, ensuring reliable outcomes even with device constraints and noise considerations.


Quantum Computing Stack Overview:
---------------------------------
1. **Use Cases**: Specific tasks like machine learning and chemistry tackled using quantum algorithms.
2. **Software Applications**: Generate quantum circuits, like the quantum Fourier transform (QFT), with universal gates.
3. **TKET Optimization**: Refines circuits based on hardware limitations, such as stricter gatesets and qubit connectivity.
4. **Hardware Translation**: Post-TKET processing translates optimized circuits into machine code for QPUs.


Key Features:
-------------
.. image:: https://github.com/spendierk/TKET_website/blob/main/tket_architecture.jpg
   :alt: Alternative text for the image
   :width: 400px
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

