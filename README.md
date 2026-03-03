# libGDX 2D Physics Engine Game

A modular 2D physics-based projectile game developed using **Java, libGDX, and LWJGL**.  
This project demonstrates custom implementation of rigid-body inspired mechanics, collision detection systems, object health modelling, and structured game-state management using Object-Oriented Design principles.

The goal of this project was not just to recreate a popular gameplay concept, but to architect a clean, extensible 2D physics interaction system from scratch.

---

## 🎯 Project Objective

To design and implement a structured 2D projectile physics system capable of:

- Simulating projectile motion
- Handling real-time collision detection
- Managing entity health and destruction logic
- Supporting modular entity behavior
- Maintaining scalable game architecture

The emphasis was placed on system design, physics logic, and extensibility rather than only gameplay replication.

---
## Why This Project

This project demonstrates low-level game systems design, modular physics abstraction, and real-time collision modelling — skills transferable to systems programming, simulation design, and performance-critical software engineering.

It also applies core Object-Oriented Programming (OOP) principles including:

- **Encapsulation** – Entity state (health, position, velocity) is internally managed and protected through controlled interfaces.
- **Abstraction** – Physics logic, collision handling, and rendering are separated into modular layers.
- **Inheritance** – Entity hierarchies (Birds, Pigs, Blocks) share common structure while extending specialized behaviors.
- **Polymorphism** – Runtime behavior varies based on entity type during collision and damage resolution.

The architecture emphasizes maintainability, extensibility, and clear separation of concerns — allowing new mechanics, entities, or physics rules to be integrated without large-scale refactoring.

## 🎥 Gameplay Demo

Watch the demo here:  
https://youtu.be/1h-ZgEZ_d2w

---

## 🏗 System Architecture

UML Class Diagram:  
https://lucid.app/lucidchart/929197c6-6168-4dd4-9f11-6cb24bc80eff/edit

The architecture follows a modular OOP approach with separation of responsibilities:

### Core Components

- **Entity Layer**
  - Birds
  - Pigs (Small, Medium, Large)
  - Blocks
- **Physics Engine Layer**
  - Projectile motion calculations
  - Velocity and gravity simulation
  - Collision boundary detection
- **Damage & Health System**
  - Tiered durability modelling
  - Direct collision elimination rules
  - Impact-based damage system
- **Rendering Layer**
  - Sprite handling
  - Frame updates
  - State transitions
- **Game State Manager**
  - Level state
  - Entity lifecycle tracking
  - Win/Loss evaluation logic

The system was designed to ensure extensibility — new entities or mechanics can be integrated without major architectural refactoring.

---

## 🧠 Physics & Gameplay Mechanics

### Projectile Motion
Birds follow simulated projectile motion governed by velocity and gravity parameters. The trajectory logic is computed dynamically at runtime.

### Collision Detection
A bounding-box collision detection system was implemented to determine impact between:

- Bird ↔ Pig
- Bird ↔ Block
- Pig ↔ Ground

### Health & Damage Model

- **Small Pig**
  - Eliminated on ground impact.
- **Medium Pig**
  - Higher durability.
  - Requires block or direct collision impact.
- **Large Pig**
  - Highest durability.
  - Requires sustained or direct collision impact.
- **Direct Bird Collision**
  - Instantly eliminates pigs.
- **Blocks**
  - Take damage only from bird impact.
  - Do not self-destruct due to gravity for controlled gameplay consistency.

Gameplay decisions were made intentionally to maintain logical clarity and balance while keeping the physics system stable.

---

## 🛠 Technology Stack

- **Language:** Java  
- **Game Framework:** libGDX  
- **Rendering Backend:** LWJGL  
- **Build System:** Gradle  
- **Testing:** JUnit  

---

The separation between core logic and platform-specific launcher ensures portability and cleaner dependency management.

---

## ▶ How To Run

Due to GitHub’s 100MB upload limit, certain build artifacts are not directly stored in the repository.

### Steps:

1. Clone the repository.
2. Ensure required distribution files are placed inside:
   lwjgl/build/distributions
3. Place generated JAR file inside:
   lwjgl/build/libs
4. Open the project in IntelliJ IDEA.
5. Run the LWJGL launcher configuration.

---

## 🧪 Testing

- JUnit testing support integrated via Gradle configuration.
- Unit tests verify collision and damage logic consistency.

---

## 📈 Engineering Highlights

- Designed modular entity hierarchy.
- Implemented custom collision and damage system.
- Built structured game-state lifecycle management.
- Applied object-oriented abstraction principles.
- Balanced physics realism with gameplay constraints.
- Designed UML architecture before implementation.

---

## 📚 Key Learning Outcomes

- Real-time physics simulation design
- Collision system implementation
- Game entity abstraction
- Health-based object modelling
- Modular system architecture
- Rendering pipeline integration with libGDX
- Practical Gradle configuration and dependency handling

---

## 🔮 Future Improvements

- Advanced impulse-based physics integration
- Dynamic block structural integrity modelling
- Level editor system
- Multi-level progression engine
- Performance optimization for large object counts

---

## 👨‍💻 Author

**Nishant Tomer**  
B.Tech (CSAM), IIIT Delhi  
Systems Engineering & AI Enthusiast  

---

This project represents a hands-on implementation of structured physics modelling within a real-time interactive environment.
