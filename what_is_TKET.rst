
Introduction to TKET
=====================

TKET is an advanced, open-source software development kit for gate-based quantum computers. Its primary role is to compile and optimize quantum circuits for various quantum hardware and simulators, ensuring high performance and compatibility.

In the current NISQ (Noisy Intermediate-Scale Quantum) era, devices have limited qubits and high error rates. TKET is crucial in optimizing and simplifying quantum circuits to navigate these challenges, ensuring reliable outcomes even with device constraints and noise considerations.

Key Features:
-------------

.. image:: /path/to/image.jpg
   :alt: Alternative text for the image
   :width: 300px
   :align: center

- **Quantum Compiler**: TKET, underpinned by a high-performance C++ library, is a high-performance compiler that tailors quantum circuits to the constraints of specific quantum hardware and simulators.
- **Platform Agnostic**: TKET can target various quantum processing units (QPUs) and simulators.
- **Integration with Libraries**: TKET is compatible with popular quantum libraries such as Qiskit, Cirq, Braket, PennyLane, and more.
- **Python Interface**: TKET is accessible through its Python package, ``pytket``, available on GitHub. Install with the command ``pip install pytket``. For any difficulties with installation, please consult our `troubleshooting <https://cqcl.github.io/tket/pytket/api/install.html>`_ page.

Quantum Computing Stack Overview:
---------------------------------

1. **Use Cases**: Specific tasks like machine learning and chemistry tackled using quantum algorithms.
2. **Software Applications**: Generate quantum circuits, like the quantum Fourier transform (QFT), with universal gates.
3. **TKET Optimization**: Refines circuits based on hardware limitations, such as stricter gatesets and qubit connectivity.
4. **Hardware Translation**: Post-TKET processing translates optimized circuits into machine code for QPUs.


Backend Support:
----------------

Through ``pytket``, users can interact with TKET and platforms like Qiskit, Cirq, and PennyLane. Once circuits are optimized, TKET can compile them for devices like Quantinuum's ion trap and IBMQ's superconducting units. TKET offers Python packages for various backends, with cloud integration for AWS Braket and Microsoft Azure.


How To Cite
-----------

If you wish to cite TKET in any academic publications, we recommend citing our `software overview paper <https://doi.org/10.1088/2058-9565/ab8e92>`_ for most cases.

If your work is on the topic of specific compilation tasks, it may be more appropriate to cite one of our other papers:

- `"On the qubit routing problem" <https://doi.org/10.4230/LIPIcs.TQC.2019.5>`_ for qubit placement (aka allocation, mapping) and routing (aka swap network insertion, connectivity solving).
- `"Phase Gadget Synthesis for Shallow Circuits" <https://doi.org/10.4204/EPTCS.318.13>`_ for representing exponentiated Pauli operators in the ZX calculus and their circuit decompositions.
- `"A Generic Compilation Strategy for the Unitary Coupled Cluster Ansatz" <https://arxiv.org/abs/2007.10515>`_ for sequencing of terms in Trotterisation and Pauli diagonalisation.

We are also keen for others to benchmark their compilation techniques against us. We recommend checking our `benchmark repository <https://github.com/CQCL/tket_benchmarking>`_ for examples on how to run basic benchmarks with the latest version of ``pytket``. Please list the release version of ``pytket`` with any benchmarks you give, and feel free to get in touch for any assistance needed in setting up fair and representative tests.

Support
-------

.. Github issues

If you spot any bugs or have any feature suggestions, feel free to add to the issues board on our `Github examples repository <https://github.com/CQCL/pytket>`_. We appreciate exact error messages and reproduction steps where possible for bug reports to help us address them quickly.

.. For more specific assistance, e-mail tket-support
.. To open up direct support channels or collaboration with teams, e-mail Denise?

There is a public Slack channel for community discussion and support. Click `here <https://join.slack.com/t/tketusers/shared_invite/zt-18qmsamj9-UqQFVdkRzxnXCcKtcarLRA>`_ to join.

You can also join our `mailing list <https://list.cambridgequantum.com/cgi-bin/mailman/listinfo/tket-users>`_ for updates on new ``pytket`` releases and features. If you would like to open up direct support channels for your team, engage in research collaborations, or inquire about commercial licenses, please contact us (info@cambridgequantum.com). If you have support questions, please send them to tket-support@cambridgequantum.com. 


.. [Pres2018] Preskill, J., 2018. Quantum Computing in the NISQ era and beyond. Quantum, 2, p.79.
.. [Arut2019] Arute, F., Arya, K., Babbush, R., Bacon, D., Bardin, J.C., Barends, R., Biswas, R., Boixo, S., Brandao, F.G., Buell, D.A. and Burkett, B., 2019. Quantum supremacy using a programmable superconducting processor. Nature, 574(7779), pp.505-510.

