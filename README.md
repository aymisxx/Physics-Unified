# Physics Unified

**A structured, equation-first collection of physics theory and revision notes, organized around H. C. Verma's _Concepts of Physics_ (Volumes 1 and 2).**

From units and vectors to Newtonian mechanics, waves, electromagnetism, quantum phenomena, and special relativity, this repository brings the **47-chapter theory sequence** into **seven connected Markdown units**.

The aim is not to memorize an encyclopedia of formulas. It is to understand the physical model behind each equation, derive it from clearly stated assumptions, and know when it applies.

> **Status:** Theory notes completed for **47 / 47 chapters** across **both volumes**. The notes are independently written study companions, **not** a transcription of the books or an official H. C. Verma resource.

## Contents

| Unit | Notes | HCV chapters | Coverage | Volume |
|:---:|---|:---:|---|:---:|
| 00 | [Prerequisites](chapters/00-Prerequisites.md) | 1–2 | Physical quantities, SI units, dimensions, vectors, calculus, and measurement | 1 |
| 01 | [Mechanics I](chapters/01-Mechanics-I.md) | 3–10 | Kinematics, forces, Newton's laws, friction, circular motion, energy, momentum, and rotation | 1 |
| 02 | [Mechanics II](chapters/02-Mechanics-II.md) | 11–14 | Gravitation, simple harmonic motion, fluid mechanics, and mechanical properties of matter | 1 |
| 03 | [Waves and Optics](chapters/03-Waves-and-Optics.md) | 15–22 | String and sound waves, wave optics, geometrical optics, instruments, spectra, and photometry | 1 |
| 04 | [Heat and Thermodynamics](chapters/04-Heat-and-Thermodynamics.md) | 23–28 | Temperature, kinetic theory, calorimetry, thermodynamic laws, gas heat capacities, and heat transfer | 2 |
| 05 | [Electricity and Magnetism](chapters/05-Electricity-and-Magnetism.md) | 29–40 | Electric fields, circuits, magnetic phenomena, induction, AC, and electromagnetic waves | 2 |
| 06 | [Modern Physics](chapters/06-Modern-Physics.md) | 41–47 | Electron physics, wave–particle duality, atomic models, X-rays, semiconductors, nuclear physics, and relativity | 2 |

**Volume 1:** Units 00–03, Chapters 1–22  
**Volume 2:** Units 04–06, Chapters 23–47

## Repository structure

```text
Physics-Unified/
├── README.md
└── chapters/
    ├── 00-Prerequisites.md
    ├── 01-Mechanics-I.md
    ├── 02-Mechanics-II.md
    ├── 03-Waves-and-Optics.md
    ├── 04-Heat-and-Thermodynamics.md
    ├── 05-Electricity-and-Magnetism.md
    └── 06-Modern-Physics.md
```

Each file is a self-contained **unit**, while its internal parts preserve the corresponding HCV chapter and section order. This makes it possible to study an entire domain in sequence or jump directly to a topic alongside the textbook.

## How the notes are written

Each unit is organized around a consistent learning structure:

1. **Conceptual roadmap:** What the unit covers and how its ideas connect.
2. **Theory by textbook section:** Physical intuition, definitions, governing principles, and relevant experiments.
3. **Mathematical development:** Derivations, dimensional checks, assumptions, and useful limiting cases.
4. **Worked examples:** Independently constructed problems that connect concepts to calculations.
5. **Consolidated formula sheet:** A quick reference after the theory has been understood.
6. **Misconceptions and diagnostic checks:** Common interpretation errors, hidden assumptions, and sign-convention traps.
7. **Active-recall questions:** Prompts for testing understanding without looking at the notes.

Some notes include **clearly identified extensions** or modern terminology to connect introductory physics to later study. These should not be confused with the exact scope of the textbook.

### Notation and rendering

- Written in **GitHub Flavored Markdown**.
- Display mathematics uses GitHub-supported `$$ ... $$` delimiters; inline mathematics uses `$ ... $`.
- **SI units** are the default unless a different system is explicitly specified.
- Vector signs, coordinate systems, reference frames, and thermodynamic conventions are specified where they matter.

For example, the same second law can be written for a particle as

$$
\sum \vec{F}=m\vec{a},
$$

or, more generally, in terms of momentum as

$$
\sum \vec{F}_{\mathrm{ext}}=\frac{d\vec{p}}{dt}.
$$

The notes aim to explain **why** a particular formulation is valid, not merely display it.

## Suggested study workflow

```text
Observe the phenomenon
        ↓
Define the system and assumptions
        ↓
Identify governing principles
        ↓
Derive the mathematical relation
        ↓
Check units, signs, and limiting cases
        ↓
Solve examples and textbook exercises
        ↓
Review formula sheets and active-recall questions
```

**For a first pass**, read the corresponding HCV section alongside the notes. Try to reconstruct the derivations and sketch the physical setup before looking at equations.

**For problem practice**, work through the original textbook's examples and exercises independently. Use the notes to diagnose conceptual gaps rather than as an answer key.

**For revision**, begin with the formula sheet and active-recall questions. Return to the full theory only for concepts that cannot yet be explained confidently.

## Scope and attribution

This repository follows the **chapter structure and broad theory progression** of:

> H. C. Verma, _Concepts of Physics_, Volume 1 and Volume 2.

The explanations, supplementary derivations, integrated examples, and revision prompts are **independently written**. This project does **not** reproduce the textbook in full, provide a complete solution manual, or replace its original diagrams and experiments. Consult the books themselves for authoritative figures, exact problem statements, and the author's original presentation.

This is an **independent educational project** and is not affiliated with or endorsed by H. C. Verma or the publisher. As with any set of personal study notes, equations and examples should be checked against their assumptions and primary references before being used in consequential calculations.

**47 chapters · 2 volumes · 7 units · One continuous study of physics.**

---