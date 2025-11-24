# Automatic Deductive Verification of Event Sequence Properties

This repository contains the [KeY](https://key-project.org) extension for reasoning about event sequence properties.

## Experiment Reproduction
1. Clone the repo:
    ```sh
    git clone https://github.com/KIT-TVA/event-sequences.git
    ```
2. Open this project in [IntelliJ](https://www.jetbrains.com/de-de/idea/download).
3. In the topbar, select `Current File -> Edit Configurations...`
4. Create a new Gradle configuration and enter `key.ui:run` as a command.
5. Execute the newly created configuration to start KeY.
6. Select `File -> Load...`
7. Navigate to `key/key.ui/examples/eventSequences` to find systems used for evaluation.
8. Select a Java source file that contains event sequences, e.g., `Mail/src/Client.java`.
9. Select a proof target by prefix:
    - BASE --- functional contract.
    - ESV --- (E)vent (S)sequence (V)iolation; unsafe implementation that violates an event sequence.
    - SEC --- (Sec)ure; Safe implementation that does not violate an event sequence.
10. Select `Java verif. std.` as Proof Search Strategy and increase `Max. Rule Applications` to `1M`.
11. Navigate to `Options -> Settings -> Taclet Options` and enable the radio box for `events`.
12. Run the proof.

## License Remark
```
This is the KeY project - Integrated Deductive Software Design
Copyright (C) 2001-2011 Universität Karlsruhe, Germany
						Universität Koblenz-Landau, Germany
						and Chalmers University of Technology, Sweden
Copyright (C) 2011-2024 Karlsruhe Institute of Technology, Germany
						Technical University Darmstadt, Germany
						Chalmers University of Technology, Sweden

The KeY system is protected by the GNU General Public License.
See LICENSE.TXT for details.
```
