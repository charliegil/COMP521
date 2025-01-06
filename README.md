## 1. Simple Game in Unity

In this first project, I reacquainted myself with Unity by creating a single-level first-person shooter. The objective is to reach the temple, destroy a weak pillar using a gun, and use the fallen pillar pieces to cross a river and reach the goal.

**Notable Features:**
- Player controller for movement and view direction.
- Projectile system with collision detection.
- Dynamic spawning of game objects (e.g., pillar pieces falling into the river).
- Simple UI for win/lose messages.
- Out-of-bounds constraints to keep the player within the playable area.

---

## 2. Collision Detection and Resolution

In this simulation, balloons spawn randomly and float upwards with natural movement, influenced by random gusts of wind. A harpoon launcher at the top, controlled by arrow keys and spacebar, allows the player to launch harpoons to pop balloons upon direct collision. Balloons respond to various collisions, including with terrain, other balloons, and projectiles.

**Notable Features:**
- Custom collision detection and resolution system.
- Autonomous balloon movement with wind influence, managed by a Game Manager that handles spawning and despawning.
- Harpoon controller for launching at balloons using arrow keys and spacebar.

**Simulation in Action**

![Collision Simulation Video](https://github.com/user-attachments/assets/15164dd7-3a75-462d-90e3-91b79218943e)

**Next Steps:**
- Add sprites to enhance visuals.
- Resolve remaining bugs in collision resolution.
- Animate balloon spawning.
- Add sound effects (e.g., wind, balloon popping).

---

## 3. Pathfinding

This simulation replicates a large library setting where robots move discretely on a grid, while humans move continuously. Robots fetch and replace books, avoid obstacles, and interact with benches around the building. Both types of agents avoid collisions, seek the shortest paths, and handle dynamic obstacles.

**Notable Features:**
- **Discrete Movement**: Implemented a dynamic grid based on the environment's size and obstacles. Nodes containing obstacles are marked as unwalkable.
- **Continuous Movement**: Built a waypoint graph dynamically, placing waypoints based on obstacle layout.
- **Pathfinding**: Developed A* pathfinding from scratch, modified for both discrete and continuous movements.
- **Robot Behavior**: Follow paths, avoid collisions with dynamic agents, and re-path when necessary.
- **Human Behavior**: Detect deadlocks, follow paths, and re-path as needed.

### Discrete Pathfinding and Movement
![Discrete Pathfinding Video](https://github.com/user-attachments/assets/7e675670-ebaa-4aa4-b0c2-7ee3d18c9ae4)

### Continuous Pathfinding and Movement
![Continuous Pathfinding Video](https://github.com/user-attachments/assets/25060655-c26d-4c78-9c91-6e210c8e8256)

### Simulation with Multiple Agents
Running with five humans and five robots.

![Multiple Agents Simulation Video](https://github.com/user-attachments/assets/41900457-dba9-4c36-b6c5-5acd9be3ee83)

---

## 4. HTN Frogger

In this project, I implemented an AI for a frog navigating through traffic, inspired by the classic game Frogger. The frog must avoid vehicles, leap to safety, and potentially eat flies to gain the ability to jump. The AI uses Hierarchical Task Network (HTN) planning, allowing the frog to decide whether to jump forward, retreat, or leap over traffic based on the current game state.

**Notable Features:**
- **HTN AI**: The frog's decision-making is controlled by an HTN planner, which selects tasks based on the game state. Tasks are broken down into composite and primitive actions.
- **Traffic Simulation**: Vehicles move across the screen in alternating directions, with random speeds and spawn points. The frog must navigate through these lanes while avoiding collisions.
- **Fly Interaction**: The frog can eat flies to gain the ability to perform a vertical leap, avoiding traffic below.
- **Dynamic Difficulty**: The number of vehicles and their speed can be adjusted to create varying challenge levels.
- **Game State Representation**: The planner tracks and uses the world state to make decisions.

### Level Layout
<img width="647" alt="Screenshot 2025-01-06 at 14 49 27" src="https://github.com/user-attachments/assets/0681c5d7-45e3-4a18-96ce-5fc50877e9ae" />
