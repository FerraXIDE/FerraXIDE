# FerraX IDE

A visual IDE for quantum programming, powered by the Text4q language.

FerraX IDE is a visual Integrated Development Environment (IDE) designed to make quantum programming accessible. It allows users to create, visualize, and simulate quantum circuits using simple natural-language–like syntax or the Text4q language, automatically generating Python (Qiskit) code.

---

# Key Features

* Visual and Interactive IDE: Full web-based interface with editor, circuit panel, and integrated tools.
* Text4q Language: Write quantum commands using a simple and clear syntax (e.g., `Create 2`, `H 0`, `CX 0 1`). Ideal for learning.
* Multilingual: Support for Spanish, English, French, Zapotec (Isthmus of Tehuantepec), Maya (Yucatec), and Nahuatl (Eastern Huasteca).
* Code Generation: Translates your commands into ready-to-use Python/Qiskit code, with one-click copy.
* Real-Time Visualization: The quantum circuit updates instantly as you program.
* Integrated Bloch Sphere: Visualize the state of a single qubit in 3D with interactive controls.
* Result Simulation: Run basic simulations and view probability histograms.

---

# Getting Started

FerraX IDE is a web application. No installation is required—just a modern web browser.

1. Open FerraX IDE.

2. Write your first program in the left panel:

   ```text4q
   Create 2
   H 0
   CX 0 1
   Measure 0
   Measure 1
   ```

3. Watch how the quantum circuit is automatically drawn in the central panel.

4. Copy the generated Qiskit code from the bottom panel and run it in your Python environment.

---

# Example: Bell State (Entanglement)

Text4q code:

```text4q
Create 2
H 0
CX 0 1
```

Generated circuit:

* Two qubits (`q0`, `q1`)
* Hadamard gate on `q0`
* CNOT gate with control `q0` and target `q1`

Generated Qiskit code:

```python
from qiskit import QuantumCircuit
qc = QuantumCircuit(2, 2)
qc.h(0)
qc.cx(0, 1)
# qc.measure_all()  # When adding "Measure" commands
```

---

# Project Structure

```
FerraX-IDE/
├── main.html          # Main web application
├── index.html         # Compiler web application (FerraX IDE)
├── LICENSE            # Apache 2.0 License
├── NOTICE             # Third-party attributions (Qiskit)
├── README.md          # This file
```

---

# Technologies Used

* Qiskit: Open-source framework by IBM for quantum computing. FerraX uses it as the simulation engine and code generator.
* JavaScript / HTML5 / CSS3: Interactive user interface and circuit rendering with SVG.
* Canvas API: Advanced 3D rendering of the Bloch Sphere.
* Font Awesome: Interface iconography.

---

# License and Attribution

* Source code: FerraX IDE and the Text4q compiler are licensed under the Apache License 2.0.
  See the [LICENSE](LICENSE) file for full terms.

* Third-party software: This product includes software components developed by third parties:

  * Qiskit ([https://qiskit.org](https://qiskit.org)) — Copyright 2017–2024 IBM Corporation
    Used under the Apache License 2.0.

  Full attribution details can be found in the [NOTICE] file.

---

# Educational Purpose Disclaimer

FerraX IDE is an educational tool.

* Designed to facilitate learning and experimentation with quantum programming concepts.
* Simulations and visualizations may have limitations or contain errors.
* It should not be used for scientific research, commercial development, or any critical purpose without thorough and independent verification.
* This software is distributed “AS IS,” without warranties of any kind, as stated in Section 7 of the Apache License 2.0.

---

# Contributions and Contact

Did you find a bug, have an idea for a new feature, or want to help translate Text4q into more languages?

1. Report bugs or suggest improvements via [Issues](([https://github.com/FerraXIDE](https://github.com/FerraXIDE)).
2. Contribute code: Fork the repository and create a Pull Request.
3. Direct contact:

   Author: Gabriel De Jesús Sánchez Ferra
   GitHub: [https://github.com/FerraXIDE](https://github.com/FerraXIDE)

---

# Acknowledgments

* To my dear family who has always supported me in everything I have done
* To IBM Qiskit for their incredible open-source framework.
* To the Zapotec, Maya, Nahuatl and all language communities for inspiring the inclusion of indigenous languages.
* To all educators and students who help grow quantum computing.

---

# Project Status

Current version: 1.0.0-beta
License: Apache 2.0
Last updated: 2026

