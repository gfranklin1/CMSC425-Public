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

### Project 4: ****  
**Description:**  


**Grade:**

---

### Project 5: ****
**Description:**


**Grade:**


---

## Disclaimer

**## CONTACT ME IF YOU WOULD LIKE TO SEE THE CODE, UNDER UNIVERSITY RULES I AM NOT ALLOWED TO POST PUBLICLY ON HERE**

If you are interested in reviewing the code or have any questions related to the projects, please reach out to me directly.
