# SYSTEM SPECIFICATION: LEARNING TERMINAL v1.0
## [ PROJECT: RETRO-EDUCATIONAL INTERFACE FOR EARLY LEARNERS ]

### 1. VISION & PHILOSOPHY
The **Learning Terminal** is a high-contrast, distraction-free educational environment designed specifically for toddlers (Ages 2-4). It replaces modern UI "clutter" with a 1980s monochrome CRT aesthetic.

**Core Goal:** Strip away complex animations, multi-color palettes, and small icons to provide a focused, tactile experience where the educational content is the brightest thing on the screen.

---

### 2. VISUAL SPECIFICATIONS (THE AESTHETIC)
The interface must emulate a vintage computer terminal:
*   **Palette:** Absolute Black (`#000000`) background with High-Intensity Green (`#33FF33`) text.
*   **Typography:** Monospace fonts only (Courier, Consolas, or similar). All text is forced to UPPERCASE to mimic early system BIOS.
*   **CRT Effects:** 
    *   **Scanlines:** Horizontal darkening lines to simulate low-resolution monitors.
    *   **Static Display:** No jarring flicker or refresh animations.
    *   **Glow:** CSS text-shadow on all elements to simulate light bleed on glass.
*   **Borders:** Sections are defined using box-drawing characters (═, ║, ╗, etc.) rather than rounded modern containers.

---

### 3. USER EXPERIENCE (UX) FOR TODDLERS
Modern design is often too "busy" for 3-year-olds. The Terminal follows these strict UX rules:
*   **Massive Touch Targets:** Buttons are oversized boxes.
*   **Single-Task Focus:** One question per screen. No sidebars, no ads, no navigation menus during gameplay.
*   **Immediate Feedback:** Every tap produces a visual reaction.
*   **Success Reinforcement:** Correct answers trigger a centered "GREAT JOB!" box. The transition is calm and does not involve flashing.

---

### 4. FUNCTIONAL MODULES (THE GAMES)

#### A. SPELLING MODULE (SEQUENTIAL LOGIC)
*   **Objective:** Identify and select letters in the correct order to form a word.
*   **Logic:**
    1.  Display a target word (e.g., "CAT") in a low-intensity green.
    2.  The "active" letter is underlined.
    3.  User must find the matching letter from 4 large options (1 correct, 3 distractors).
    4.  Correct tap: Letter turns high-intensity green; underline moves to next letter, and 4 new options are generated.
    5.  Completion: Full-screen success flash, then load a new word.

#### B. COUNTING MODULE (QUANTITY RECOGNITION)
*   **Objective:** Count objects and map them to a numerical symbol.
*   **Logic:**
    1.  Display 1–5 large icons (●) in a centered box.
    2.  Provide 3 large numerical options below.
    3.  Correct tap: Match quantity to number.
    4.  Completion: Full-screen success flash, then randomize count.

#### C. ADDITION MODULE (BASIC ARITHMETIC)
*   **Objective:** Solve single-digit addition problems.
*   **Logic:**
    1.  Equation format: `X + Y = ?`
    2.  Operands (X and Y) are limited to 1–3 to keep the sum ≤ 6.
    3.  Provide 3 numerical options for the sum.
    4.  Completion: Full-screen success flash, then generate new problem.

---

### 5. FEEDBACK LOOPS
*   **Correct Action:** 1000ms "GREAT JOB!" overlay + State Reset.
*   **Incorrect Action:** No harsh buzzers or "Wrong" icons. The system simply does not advance, encouraging the child to keep trying until they hit the right target.
*   **Navigation:** A "RETURN TO MENU" button is always available at the bottom of games, but is styled smaller than game buttons to prevent accidental taps.

---

### 6. TECHNICAL STACK SPIRIT
*   **State Management:** Minimalist. The app tracks the current mode and progress within a specific game loop.
*   **Rendering:** CSS-heavy. The "look" is achieved through global filters and linear gradients rather than heavy image assets.
*   **Responsive:** Must scale to fill 100% of the viewport (optimized for tablet/iPad usage).
