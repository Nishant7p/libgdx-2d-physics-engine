# libGDX 2D Physics Engine Game

A modular 2D physics-based projectile game built with Java, libGDX, and LWJGL. It implements rigid-body inspired mechanics, collision detection, object health modelling, and structured game-state management using object-oriented design.

The goal was not just to recreate a familiar gameplay concept, but to build a clean, extensible 2D physics interaction system from scratch.

[Watch the gameplay demo](https://youtu.be/1h-ZgEZ_d2w)

---

## Project objective

Design and implement a structured 2D projectile physics system that can:

- Simulate projectile motion
- Handle real-time collision detection
- Manage entity health and destruction logic
- Support modular entity behavior
- Keep the game architecture scalable

The focus was on system design, physics logic, and extensibility rather than gameplay replication alone.

---

## Why this project

It demonstrates low-level game systems design, modular physics abstraction, and real-time collision modelling. Those skills carry over to systems programming, simulation, and performance-sensitive software.

It applies core object-oriented principles:

- Encapsulation: entity state (health, position, velocity) is managed internally and exposed through controlled interfaces.
- Abstraction: physics, collision handling, and rendering are separated into modular layers.
- Inheritance: entity hierarchies (Birds, Pigs, Blocks) share common structure while extending specialized behavior.
- Polymorphism: runtime behavior varies by entity type during collision and damage resolution.

New mechanics, entities, or physics rules can be added without large refactors.

---

## System architecture

[UML class diagram](https://lucid.app/lucidchart/929197c6-6168-4dd4-9f11-6cb24bc80eff/edit)

The architecture is modular, with clear separation of responsibilities.

- Entity layer: Birds, Pigs (small, medium, large), Blocks
- Physics engine layer: projectile motion, velocity and gravity, collision boundaries
- Damage and health system: tiered durability, direct-collision elimination, impact damage
- Rendering layer: sprites, frame updates, state transitions
- Game state manager: level state, entity lifecycle, win and loss logic

---

## Physics and gameplay mechanics

### Projectile motion
Birds follow simulated projectile motion governed by velocity and gravity. The trajectory is computed at runtime.

### Collision detection
A bounding-box collision system detects impacts between:

- Bird and Pig
- Bird and Block
- Pig and Ground

### Health and damage model

- Small Pig: eliminated on ground impact.
- Medium Pig: higher durability, needs a block or direct collision.
- Large Pig: highest durability, needs sustained or direct collision.
- Direct bird collision: instantly eliminates pigs.
- Blocks: take damage only from bird impact, and do not self-destruct under gravity, for consistent gameplay.

---

## Tech stack

- Language: Java
- Game framework: libGDX
- Rendering backend: LWJGL
- Build system: Gradle
- Testing: JUnit

The separation between core logic and the platform-specific launcher keeps the project portable and dependencies clean.

---

## How to run

Because of GitHub's 100 MB upload limit, some build artifacts are not stored in the repository.

1. Clone the repository.
2. Place the required distribution files in `lwjgl/build/distributions`.
3. Place the generated JAR file in `lwjgl/build/libs`.
4. Open the project in IntelliJ IDEA.
5. Run the LWJGL launcher configuration.

---

## Testing

- JUnit tests run through Gradle.
- Unit tests cover collision and damage logic.

---

## Engineering highlights

- Modular entity hierarchy.
- Custom collision and damage system.
- Structured game-state lifecycle management.
- Object-oriented abstraction throughout.
- Physics realism balanced against gameplay constraints.
- UML architecture designed before implementation.

---

## Future improvements

- Impulse-based physics
- Dynamic block structural integrity
- Level editor
- Multi-level progression
- Performance tuning for large object counts

---

## Author

Nishant Tomer, B.Tech CSAM, IIIT-Delhi.
