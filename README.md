# CMSC425 - Game Programming

Welcome to my repository for ```CMSC425 - Game Programming``` at the ```University of Maryland, College Park```. This repository includes a summary and the grade received for the homeworks and projects that I completed throughout this course. Due to university policies, the code for these projects is not publicly available. If you are an employer or have a legitimate request to view the code, please contact me directly.

## Projects 

### Project 1: **A Small Unity Project**
**Description:**  
- Created a simple Unity scene featuring a 3D cube.
- Implemented material swapping using C# and Unity’s input system.
- Cube starts with a red material at position (0, 0, 0).
- On each spacebar press:
  - The cube's material toggles between red and blue.
  - The cube's position alternates between (0, 0, 0) and (-2, 0, 0).
- Utilized `MeshRenderer` and `Transform` components to control visuals and positioning.

**Grade:** 2/2 

--- 

### Project 2: **Mesh Coding**
**Description:**  
- Implemented three C\# scripts: `Reshape`, `Pulsate`, and `Oscillate`, with each attached to its corresponding cylinder.
- **Reshape**:
  - Shrinks the top of the cylinder by 50% and expands the bottom by 50%.
  - Manually adjusts all vertex normals (without `Mesh.RecalculateNormals`) to ensure correct shading on the sloped sides.
- **Pulsate**:
  - Scales the cylinder in and out in the XZ-plane while keeping all Y-coordinates unchanged.
  - Uses a sine function to animate the pulsation, completing one full cycle per second.
- **Oscillate**:
  - Alternates growth and shrinkage between the top and bottom halves of the cylinder in the XZ-plane.
  - When the top grows, the bottom shrinks, and vice versa.
  - Includes manual normal computation for accurate lighting during deformation.
- All scripts modify the cylinder's existing mesh via `GetComponent<MeshFilter>().mesh`, updating vertex and normal arrays directly.

**Grade:** 6/6

---

### Project 3: **Robotic Arm**
**Description:**  
- Constructed a fully articulated robotic arm in Unity using a hierarchical prefab-based structure (base -> joints -> arms -> fingers -> fingertips).
- Implemented a reusable `Transformer` component to apply smooth, continuous local rotations and translations based on user input.
  - Supported both forward and reverse movement using Left Shift as a modifier.
  - Configured multiple `Transformer` instances across the arm hierarchy to control vertical movement, base rotation, joint rotation, and fingertip articulation.
- Rigged the arm so that:
  - The upper joint rotates the entire arm structure around the central column.
  - The first arm segment swings independently while a counter-rotating segment preserves the wrist's orientation.
  - The hand and all finger joints open and close with coordinated rotations of varying speeds.
- Built a functional gripping system using physics colliders, triggers, and rigidbodies.
  - Implemented the `BeGripped` script to detect when all three fingertips simultaneously contact a target object.
  - When gripped, the object becomes a child of the hand, allowing it to be lifted, carried, and placed elsewhere.
- Calibrated the arm's motion so it can pick up a cube on the plane and accurately drop it onto a nearby box through a combination of joint rotations and translations.
- Used quaternions throughout to ensure smooth rotational behavior and avoid gimbal issues.

**Grade:** 

---

### Project 4: **Inchworm**  
**Description:**  
- Developed a robotic inchworm animation system in Unity using coroutines, input handling, and hierarchical transform manipulation.
- Implemented a `Mover` script that animates a four-phase locomotion cycle:
  1. Shrinking the body while moving the head downward toward the tail.
  2. Flopping horizontally into the target square while extending the body.
  3. Retracting the tail toward the head in the new square.
  4. Rising back to a vertical stance with the body fully extended.
- Designed a keystroke queue system using `List<KeyCode>` and `WaitUntil` to buffer arrow key inputs, enabling smooth sequential movement even with rapid key presses.
- Utilized `Mathf.Lerp` and `Vector3.Lerp` within a coroutine loop to achieve frame-rate-independent, smooth scaling and translation of the inchworm's body and head.
- Wrote a unified `Inch` coroutine that handles both growing and shrinking animations without conditional branching inside the loop, by computing start and end values beforehand based on the sign of the input parameter.
- Managed parent/child transform relationships to correctly animate the head's local position and the body's local scale independently, preserving the visual integrity of the inchworm model.
- Implemented boundary checking to prevent the inchworm from moving outside the dynamically generated checkerboard, ensuring valid grid positions based on configurable `rows` and `cols` parameters.
- Exposed `secondsPerStep` in the Unity Inspector for runtime adjustment of animation speed without recompilation.

**Grade:**

---

### Final Project: **Slime Game**
**Description:**  
- **NOTE: This project is located in another repository, as there are incremental updates.**
- Collaborated with a team to design and develop a roguelike dungeon crawler in Unity where player progression is tied to knowledge rather than persistent gear or stats.
- Architected a **procedural level generation system** that assembles hand-crafted cavern rooms and tunnels into a randomized maze-like cave network, ensuring unique layouts on every playthrough.
- Implemented a **research and dissection system** that allows players to study enemy corpses, unlocking permanent attack and defense bonuses against specific enemy types stored in a persistent bestiary.
- Developed a **stamina-based combat system** featuring light/heavy attacks, critical strikes, splash damage for certain weapons, and AI enemies with detection ranges and predictive aiming.
- Created a **slime enemy type** with recursive splitting behavior—upon death, slimes divide into smaller variants with dynamically scaled stats.
- Built a **tiered weapon system** supporting melee and ranged weapons across rarity levels (Rusty, Sharpened, Enchanted), each with distinct stat distributions encouraging loadout experimentation.
- Designed and implemented a **consumable potion system** (Speed, Damage, Health boosts) with inventory management, random drops from enemies and destructible crates, and strategic resource allocation.
- Developed a **tech tree UI** with branching upgrade nodes for stat customization, enabling varied build paths across runs.
- Created a **bestiary UI** that displays accumulated research data including enemy lore, visual references, and combat bonuses gained through dissections.
- Implemented **dynamic UI elements** including player health/stamina bars, floating damage numbers with color/size variations for critical hits, and semi-translucent interaction pop-ups for items and corpses.
- Integrated **atmospheric lighting** using handheld torches and environmental light sources to create pockets of visibility and tension during exploration.
- Added **audio feedback** with ambient music and contextual sound cues for combat, level-ups, and interactions to enhance player immersion.
- Incorporated **special interactables** such as destructible crates, loot chests, and mimic enemies disguised as chests to add environmental hazards and rewards.
- Designed a **death screen statistics display** showing run metrics (damage dealt, enemies killed by type, max level reached, etc.) to encourage replayability and personal goal-setting.

**Grade:** 

---

## Disclaimer

**## CONTACT ME IF YOU WOULD LIKE TO SEE THE CODE, UNDER UNIVERSITY RULES I AM NOT ALLOWED TO POST PUBLICLY ON HERE**

If you are interested in reviewing the code or have any questions related to the projects, please reach out to me directly.
