
# ⚡ Logic-Simulator: OOP Desktop Circuit Designer

![Status](https://img.shields.io/badge/status-active-brightgreen)
![Language](https://img.shields.io/badge/language-C++-blue)
![Platform](https://img.shields.io/badge/platform-Windows-lightgrey)

---

## 🌟 Overview

Logic-Simulator is a modern desktop application for designing, simulating, and analyzing digital logic circuits. Built in C++ with a strong focus on Object-Oriented Programming (OOP), it provides an intuitive GUI for creating circuits using a variety of logic gates and tools. This project was developed as a college assignment to demonstrate advanced OOP and GUI programming skills.

---

## ✨ Features

- Drag-and-drop logic gate placement (AND, OR, NOT, NAND, NOR, XOR, XNOR)
- Connect gates visually and simulate outputs in real time
- Copy, delete, and move one or multiple gates
- Save/load circuit designs
- Undo/redo actions
- Circuit validation and error highlighting
- User-friendly GUI with custom graphics

---

## 🛠️ Technologies Used

- C++ (core logic)
- OOP design patterns (Factory, Command, Observer)
- Custom graphics library (CMUgraphicsLib)
- Windows desktop application

---

## 🧠 Design & Architecture

### How We Thought About the Project

- **Modularity:** Each gate is a class derived from a common `Gate` base, allowing easy extension and maintenance.
- **Command Pattern:** Actions like copy, delete, and connect are implemented as commands, enabling undo/redo and clean separation of concerns.
- **Observer Pattern:** The GUI observes changes in the circuit model and updates the display automatically.
- **Factory Pattern:** Gate creation is handled by a factory, simplifying the addition of new gate types.
- **Separation of Concerns:** GUI, simulation logic, and data management are separated into distinct modules for clarity and scalability.

### Project Flow

1. **User Interaction:** The user selects gates and places them on the canvas using drag-and-drop.
2. **Circuit Construction:** Gates are connected via wires; the system checks for valid connections and updates the model.
3. **Simulation:** When the user runs the simulation, the app propagates signals through the gates and displays outputs.
4. **Editing:** Users can copy, delete, or move gates, with all actions tracked for undo/redo.
5. **Persistence:** Circuits can be saved to and loaded from files for future editing.

### Why These Design Choices?

- **OOP:** Enables extensibility (add new gates/features easily), maintainability, and code reuse.
- **GUI:** Makes circuit design accessible and interactive, ideal for learning and prototyping.
- **Patterns:** Command and Observer patterns simplify complex user interactions and state management.

---

## 📁 File Explanations

| File/Folder         | Purpose |
|---------------------|---------|
| `main.cpp`          | Application entry point, initializes GUI and main loop |
| `ApplicationManager.*` | Manages overall app state, user actions, and circuit data |
| `Actions/`          | Contains command classes for user actions (AddGate, DeleteGate, Connect, etc.) |
| `Components/`       | Gate classes (AND, OR, NOT, etc.), wire classes, and circuit elements |
| `GUI/`              | GUI rendering, user input handling, and graphics |
| `CMUgraphicsLib/`   | Custom graphics library for drawing and interaction |
| `Circuits examples/`| Sample circuit files for testing and demonstration |
| `Images/`           | Icons and graphics assets |
| `README.md`         | Project documentation |

---

## 💡 Example Usage

```cpp
#include "ApplicationManager.h"

ApplicationManager app;
app.addGate("AND", 100, 200);
app.addGate("OR", 300, 200);
app.connectGates(1, 2);
app.simulate();
std::cout << "Output: " << app.getGateOutput(2) << std::endl;
```

---

## 📦 Getting Started

1. **Clone the repository:**
    ```bash
    git clone https://github.com/<your-username>/Logic-Simulator-main.git
    cd Logic-Simulator-main
    ```
2. **Open the project in Visual Studio (or compatible IDE)**
3. **Build and run the solution:**
    - Open `graphics_prj.sln` and build.
    - Run the application and start designing circuits!

---

## 👤 License

- Licensed under the MIT License

---

## 🤝 Contributing

Contributions, suggestions, and feedback are welcome! Feel free to fork the repo, open issues, or submit pull requests.

---

## 📝 Notes

- This project is for educational purposes and demonstrates best practices in OOP and GUI programming.
- Designed for learning, experimentation, and extension.

---

> **Design. Simulate. Learn. ⚡**
