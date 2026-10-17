# Unit 02: Mechanics II

**Gravitation → Simple Harmonic Motion → Fluid Mechanics → Mechanical Properties of Matter**  
*Original revision notes following Chapters 11–14 of H. C. Verma, Concepts of Physics, Volume 1*

> **Purpose.** Extend the mechanics of particles and rigid bodies to inverse-square gravity, oscillatory systems, fluid statics and flow, and the response of real materials to loads, free surfaces and viscosity. Build each law from its physical assumptions, then connect it to methods for solving problems. These are independently written study notes, not a transcription of HCV. Numbering follows its theory sections for cross-referencing.
>
> **Notation.** All display mathematics uses `$$ ... $$` for GitHub rendering. Vector quantities use arrows. Unless specified otherwise, use SI units, idealized models and inertial frames. The symbol $g$ denotes local gravitational acceleration, $G$ universal gravitation, $\rho$ mass density, $\eta$ dynamic viscosity and $S$ surface tension. A sign convention and control volume should always be defined before a derivation.

## Roadmap

| Part | HCV chapter | Central ideas |
|---|---|---|
| **I** | **11. Gravitation** | Inverse-square attraction, gravitational potential and field, shells and spheres, satellites and escape |
| **II** | **12. Simple Harmonic Motion** | Restoring forces, oscillator equations, energy, pendulums, superposition, damping and resonance |
| **III** | **13. Fluid Mechanics** | Fluid pressure, buoyancy, accelerating liquids, flow, continuity and Bernoulli's equation |
| **IV** | **14. Some Mechanical Properties of Matter** | Elastic stress–strain response, surface tension, capillarity, viscosity, Poiseuille and Stokes flow |

**Learning sequence**

```text
Newton's laws + work-energy + angular momentum
                        |
                        v
           Universal gravitation (Ch. 11)
          /               |              \
         v                v               v
  Fields & potentials   Satellites    Escape/binding
         |
         v
 Linear restoring force -> Oscillations (Ch. 12)
                        |
                        v
       Continuous matter: fluids (Ch. 13)
           /                        \
          v                          v
    Pressure / buoyancy       Flow / energy balance
           \                        /
            v                      v
           Real material response (Ch. 14)
               /               \
              v                 v
        Elasticity      Interfaces / viscosity
```

---

# Part I: Gravitation

Newton's universal gravitation connects terrestrial free fall and celestial motion through a single interaction. Compared with the near-Earth approximation of constant $g$, this chapter retains how force and potential change with distance.

## 11.1 Historical Introduction

Kepler distilled extensive astronomical observations into three regularities: planets follow ellipses with the Sun at one focus; the Sun-to-planet radius vector sweeps equal areas in equal times; and the square of orbital period scales with the cube of the orbit's semimajor axis. Newton connected these laws to the acceleration of a falling body.

For a nearly circular orbit, the inward acceleration is

$$
a_c=\frac{v^2}{r}=\frac{4\pi^2r}{T^2}.
$$

If an orbiting object twice as far away requires only one-quarter as much inward acceleration, an inverse-square model becomes plausible. Newton's major unification was to treat the Moon and a falling object as subjects of the same dynamical laws.

For point masses $m_1,m_2$ with separation $r$,

$$
\boxed{F=G\frac{m_1m_2}{r^2}},
$$

with gravitational attraction directed along their line of centers. In vector notation, if $\vec r=\vec r_2-\vec r_1$, the force on mass 2 due to mass 1 is

$$
\boxed{\vec F_{2\leftarrow1}=-\frac{Gm_1m_2}{r^3}\vec r}.
$$

The minus sign records attraction toward mass 1. The forces on the two masses are equal and opposite. Gravitational interactions of many particles are added by **superposition**.

**Dimensional check:**

$$
[G]=\frac{[F]r^2}{m_1m_2}=M^{-1}L^3T^{-2}.
$$

The point-mass equation also describes the force between two nonoverlapping spherically symmetric bodies, evaluated at their centers.

## 11.2 Measurement of Gravitational Constant $G$

A **Cavendish-type torsion balance** makes gravitational attraction between laboratory masses measurable. Two small masses $m$ at the ends of a light horizontal rod are attracted by nearby larger masses $M$. The rod rotates, twisting a thin suspension fiber.

For an ideal geometry with two equal forces $F$ acting perpendicular to a rod of length $l$,

$$
\tau_g=2F\frac l2=Fl=\frac{GMml}{r^2}.
$$

If $\kappa$ is the torsional stiffness and $\theta$ the angular displacement from the fiber's untwisted equilibrium,

$$
\tau_{\mathrm{fiber}}=\kappa\theta,
\qquad
\boxed{G=\frac{\kappa\theta r^2}{Mml}}.
$$

A reflected light beam magnifies tiny angular changes. The fiber stiffness can be obtained from its torsional oscillation period, $T=2\pi\sqrt{I/\kappa}$, where $I$ is the apparatus moment of inertia. Real measurements require geometric corrections and careful isolation from disturbances.

A useful reference value is

$$
\boxed{G\approx6.67\times10^{-11}\ \mathrm{N\,m^2\,kg^{-2}}}.
$$

Do not confuse the universal constant $G$ with the location-dependent acceleration $g$.

## 11.3 Gravitational Potential Energy

An attractive inverse-square force stores potential energy in the configuration of two masses. For separation $r$ and the convention $U(\infty)=0$,

$$
F_r=-\frac{GMm}{r^2},
\qquad
U(r)-U(\infty)=-\int_{\infty}^{r}F_r\,dr.
$$

Consequently,

$$
\boxed{U(r)=-\frac{GMm}{r}}.
$$

Two essential interpretations:

- $U$ is **negative** because bringing initially distant attracting masses together releases energy.
- Raising the mass outward increases $U$ toward zero, even though its numerical value remains negative.

For motion between $r_1$ and $r_2$,

$$
\boxed{\Delta U=GMm\left(\frac1{r_1}-\frac1{r_2}\right)}.
$$

The gravitational work is $W_g=-\Delta U$. Near Earth's surface, $r=R+h$ with $h\ll R$, a first-order expansion gives

$$
U(R+h)-U(R)\simeq\frac{GMm}{R^2}h=mgh,
\qquad g=\frac{GM}{R^2}.
$$

Thus $mgh$ is a local approximation to the general inverse-square potential difference.

## 11.4 Gravitational Potential

**Gravitational potential** is potential energy **per unit test mass**:

$$
\boxed{V(\vec r)=\frac{U(\vec r)}m},
\qquad [V]=L^2T^{-2}=\mathrm{J\,kg^{-1}}.
$$

For a point source mass $M$,

$$
\boxed{V(r)=-\frac{GM}{r}}.
$$

Potential is a scalar. It is easier to add contributions from a collection of masses than it is to add the corresponding force vectors:

$$
V(\vec r)=-G\sum_i\frac{M_i}{|\vec r-\vec r_i|}.
$$

For continuous matter with a volume mass density $\rho(\vec r')$,

$$
\boxed{V(\vec r)=-G\int\frac{\rho(\vec r')\,d^3r'}{|\vec r-\vec r'|}}.
$$

A potential difference is physically significant: the field's work per unit mass from $A$ to $B$ is $V(A)-V(B)$.

## 11.5 Calculation of Gravitational Potential

Choose a small mass element $dm$, calculate its potential and integrate. The scalar nature of $V$ simplifies symmetric geometries.

### A. Uniform ring: potential on its axis

Let a thin ring have mass $M$, radius $a$ and center at the origin. A point on its axis is distance $z$ from the center. Every element of the ring is the same distance $\sqrt{a^2+z^2}$ from that point. Thus

$$
\boxed{V(z)=-\frac{GM}{\sqrt{a^2+z^2}}}.
$$

The symmetry reduces an integral over all mass elements to multiplication by total mass.

### B. Thin spherical shell

For a uniformly distributed thin shell of radius $R$ and mass $M$,

$$
\boxed{V(r)=\begin{cases}
-GM/r, & r\ge R,\\
-GM/R, & 0\le r\le R.
\end{cases}}
$$

The potential inside is constant, not zero. The shell produces no gravitational field in its empty interior, because the spatial derivative of a constant is zero.

### C. Uniform solid sphere

For mass $M$, radius $R$ and uniform density, the sphere can be assembled from thin spherical shells. The result is

$$
\boxed{V(r)=\begin{cases}
-GM/r, & r\ge R,\\
-\dfrac{GM}{2R^3}(3R^2-r^2), & r\le R.
\end{cases}}
$$

At the center, $V(0)=-3GM/(2R)$. The two expressions agree at $r=R$.

**Strategy:** identify whether observation point lies outside, inside or on the material. Shell theorems do not license replacing every nonspherical mass distribution by a point mass.

## 11.6 Gravitational Field

The gravitational field $\vec g(\vec r)$ is the force experienced **per unit test mass**:

$$
\boxed{\vec g=\frac{\vec F}{m}},
\qquad [g]=LT^{-2}=\mathrm{N\,kg^{-1}}.
$$

For a point mass $M$,

$$
\boxed{\vec g(\vec r)=-\frac{GM}{r^2}\hat r}.
$$

The gravitational field is a vector: sum field contributions componentwise. The acceleration of a freely moving small test mass equals the local field when gravity is the only force. **Potential** and **field** are properties of the source configuration; a test mass is not part of their definitions.

## 11.7 Relation between Gravitational Field and Potential

An infinitesimal change in potential along a displacement $d\vec r$ satisfies

$$
dV=-\vec g\cdot d\vec r.
$$

Thus

$$
\boxed{\vec g=-\vec\nabla V},
\qquad
\boxed{g_r=-\frac{dV}{dr}\ \text{in radial symmetry}}.
$$

The gravitational field points in the direction of the fastest decrease of potential. A constant potential surface has no tangential component of gravitational field, making it an **equipotential**.

**Check:** if $V=-GM/r$, then $dV/dr=GM/r^2$ and $g_r=-GM/r^2$, inward as expected.

The potential difference between two positions is

$$
\boxed{V_B-V_A=-\int_A^B\vec g\cdot d\vec r}.
$$

This integral is path-independent for Newtonian gravity from fixed sources.

## 11.8 Calculation of Gravitational Field

Two complementary methods are available:

1. Add vector contributions $d\vec g$ using symmetry, or
2. Calculate the scalar potential $V$ and then take $-\vec\nabla V$.

### Ring on its axis

Differentiating the ring potential gives

$$
\boxed{g_z(z)=-\frac{GMz}{(a^2+z^2)^{3/2}}}.
$$

At its center, the net field is zero even though potential is negative. At $z\gg a$, the field approaches $-GM/z^2$.

### Thin spherical shell

$$
\boxed{\vec g(r)=\begin{cases}
-\dfrac{GM}{r^2}\hat r,&r>R,\\
\vec0,&r<R.
\end{cases}}
$$

The field jumps across an ideal infinitesimally thin massive surface; the potential remains continuous. At the shell itself, the two one-sided limits differ.

### Uniform solid sphere

Only the mass enclosed within radius $r$ contributes to the net field there:

$$
M_{\mathrm{enc}}(r)=M\frac{r^3}{R^3}.
$$

Hence

$$
\boxed{\vec g(r)=\begin{cases}
-\dfrac{GM}{r^2}\hat r,&r\ge R,\\
-\dfrac{GM}{R^3}\,r\hat r,&r\le R.
\end{cases}}
$$

Unlike the exterior inverse-square field, the magnitude inside a uniform solid sphere is **linear in $r$**. This result assumes a constant density; a realistic planetary density profile changes it.

## 11.9 Variation in the Value of $g$

For a spherical Earth of radius $R$ and mass $M$, the surface gravitational acceleration is $g_0=GM/R^2$.

### A. Altitude

At height $h$ above the surface,

$$
\boxed{g(h)=g_0\left(\frac{R}{R+h}\right)^2}.
$$

When $h\ll R$, the binomial approximation gives

$$
\boxed{g(h)\simeq g_0\left(1-\frac{2h}{R}\right)}.
$$

### B. Depth in an ideal uniform Earth

At depth $d$, the radial distance from Earth's center is $r=R-d$. For uniform density,

$$
\boxed{g(d)=g_0\left(1-\frac{d}{R}\right)}.
$$

The formula is **not** a universal depth law for a nonuniform Earth.

### C. Rotation and latitude

In Earth's rotating frame, part of the apparent weight is offset by centrifugal acceleration. At the equator for a spherical model,

$$
\boxed{g_{\mathrm{app,eq}}=\frac{GM}{R^2}-\omega_E^2R}.
$$

At the pole the centrifugal contribution vanishes. At intermediate latitudes, the centrifugal term is not generally collinear with the radial gravitational field; the apparent gravity vector is their vector sum. Earth's oblateness and varying density also influence measured $g$.

## 11.10 Planets and Satellites

For a satellite mass $m$ in a **circular orbit** of radius $r$ around a much heavier body $M$, gravity provides centripetal force:

$$
\frac{GMm}{r^2}=\frac{mv^2}{r}.
$$

Therefore

$$
\boxed{v=\sqrt{\frac{GM}{r}}},
\qquad
\boxed{T=2\pi\sqrt{\frac{r^3}{GM}}}.
$$

For circular motion,

$$
K=\frac12mv^2=\frac{GMm}{2r},
\qquad
U=-\frac{GMm}{r}.
$$

Their sum is

$$
\boxed{E_{\mathrm{orbit}}=-\frac{GMm}{2r}}.
$$

The negative total energy identifies a bound orbit. A higher circular orbit has **larger** (less negative) total energy but **smaller** orbital speed.

A geostationary satellite must have a circular equatorial prograde orbit whose period equals Earth's sidereal rotation period. Merely choosing an orbit with a 24-hour period is not by itself sufficient for the satellite to remain above one point on the surface.

## 11.11 Kepler's Laws

**First law:** an ideal two-body bound gravitational orbit is an ellipse with the attracting body at a focus.

**Second law:** equal areas are swept in equal times. Central gravitational force implies zero torque about the attracting body's center:

$$
\vec\tau=\vec r\times\vec F=0
\quad\Longrightarrow\quad
\vec L=m\vec r\times\vec v=\text{constant}.
$$

Since a small swept area obeys $dA/dt=L/(2m)$,

$$
\boxed{\frac{dA}{dt}=\frac{L}{2m}=\text{constant}}.
$$

**Third law:** for an orbit with semimajor axis $a$,

$$
\boxed{T^2=\frac{4\pi^2a^3}{G(M+m)}}.
$$

For $M\gg m$, the denominator is approximately $GM$. The circular-orbit expression follows by setting $a=r$.

## 11.12 Weightlessness in a Satellite

A person inside an orbiting spacecraft is not outside Earth's gravity. Gravity accelerates both the spacecraft and the person almost identically, so the **normal reaction** between person and floor may be approximately zero.

An apparent weight indicated by a scale is the supporting contact force. Under ideal common free fall,

$$
\boxed{N\approx0\quad\text{even while}\quad g\ne0}.
$$

Gravitational gradients, rotation of the spacecraft, atmospheric drag and maneuvering can generate small residual accelerations. The useful diagnostic is **relative acceleration**, not the existence or absence of gravity.

## 11.13 Escape Velocity

Release a mass $m$ at radius $R$ with speed $v_e$. The minimum ideal speed for it to reach infinity with zero terminal speed follows from conservation of mechanical energy:

$$
\frac12mv_e^2-\frac{GMm}{R}=0.
$$

Thus

$$
\boxed{v_e=\sqrt{\frac{2GM}{R}}=\sqrt{2g_0R}}.
$$

The result does not depend on the escaping object's mass. For the same starting radius, escape speed is $\sqrt2$ times circular-orbit speed.

**Assumptions:** Newtonian gravity, no atmospheric resistance or propulsion after release, negligible rotation effects and negligible influence of other celestial bodies. A rocket need not instantaneously acquire $v_e$ to escape; sustained thrust can provide energy gradually.

## 11.14 Gravitational Binding Energy

A self-gravitating object's **binding energy** is the positive external energy required to disperse its mass to infinity from its assembled state. In Newtonian theory, it is the magnitude of its negative gravitational self-energy.

As a uniform sphere of total radius $R$ is assembled shell by shell, an added shell of mass $dm$ at radius $r$ gains potential energy

$$
dU=-\frac{GM(r)}{r}\,dm.
$$

With $\rho=3M/(4\pi R^3)$, $M(r)=4\pi\rho r^3/3$ and $dm=4\pi\rho r^2dr$,

$$
U=-\frac{16\pi^2G\rho^2}{3}\int_0^Rr^4dr
=-\frac{3GM^2}{5R}.
$$

Therefore

$$
\boxed{E_{\mathrm{bind}}=\frac{3GM^2}{5R}}\qquad\text{(uniform sphere).}
$$

For a nonuniform density profile the numerical factor changes. This is gravitational binding energy, not nuclear binding energy.

## 11.15 Black Holes

The Newtonian escape-speed argument becomes suggestive if one formally imposes $v_e=c$:

$$
\sqrt{\frac{2GM}{R}}=c
\quad\Longrightarrow\quad
\boxed{R_s=\frac{2GM}{c^2}}.
$$

This gives the Schwarzschild radius, but the **physical description of a black hole requires general relativity**. Light is not a Newtonian projectile with a rest mass, and the event horizon is a causal boundary of spacetime rather than merely the surface of a compact star whose Newtonian escape speed exceeds $c$.

The matching radius is a useful introductory bridge; it must not be mistaken for a complete derivation of black-hole physics.

## 11.16 Inertial and Gravitational Mass

**Inertial mass** appears in Newton's second law and measures resistance to acceleration:

$$
\vec F=m_i\vec a.
$$

**Gravitational mass** describes coupling to a gravitational field:

$$
\vec F_g=m_g\vec g.
$$

If only gravity acts,

$$
\vec a=\frac{m_g}{m_i}\vec g.
$$

Experimentally, inertial and gravitational mass are proportional with the same ratio for different materials; units can be chosen so that $m_g=m_i$. This explains the near-universality of free-fall acceleration when non-gravitational forces are negligible, and motivates the equivalence principle.

## 11.17 Possible Changes in the Law of Gravitation

The inverse-square law has a large domain of experimental success, but scientific laws remain testable. Measurements can search for departures from Newton's model, especially at extreme distances or in high-precision situations.

Possible interpretations of an apparent discrepancy include an unmodeled experimental effect, a source-mass distribution different from the assumed one, relativistic corrections or genuinely new physics. One may phenomenologically test an extra short-range term, for example

$$
V(r)=-\frac{GM}{r}\left(1+\alpha e^{-r/\lambda}\right),
$$

where $\alpha$ is a dimensionless hypothetical coupling and $\lambda$ a hypothetical length scale. **This is an illustrative beyond-HCV parameterization, not an established correction to the law.**

Newtonian gravity remains the reference model for the rest of this unit except where explicitly qualified.

### Part I: Key takeaways

- Gravity is an attractive inverse-square interaction between mass elements; spherical symmetry simplifies it enormously.
- $V$ is a scalar gravitational potential; $\vec g=-\vec\nabla V$ is a vector field.
- Inside a uniform thin shell, the field vanishes but potential does not; inside a uniform solid sphere, field strength grows linearly with radius.
- Satellites are in free fall. Circular orbital energy is negative and higher circular orbits have lower speeds.
- Escape energy, binding energy and black-hole heuristics solve different physical questions.

---
# Part II: Simple Harmonic Motion

A system with a **stable equilibrium** can oscillate about it when displaced. Simple harmonic motion (SHM) is the special case in which the restoring acceleration is proportional to displacement and directed toward equilibrium. It supplies the basic model for more complicated vibrations.

## 12.1 Simple Harmonic Motion

Let $x$ denote signed displacement from equilibrium. A particle executes SHM if

$$
\boxed{\frac{d^2x}{dt^2}=-\omega^2x},
\qquad\omega>0.
$$

Equivalently, if the mass is $m$ and a net restoring force is $F=-kx$,

$$
\boxed{m\ddot x+kx=0},
\qquad
\boxed{\omega=\sqrt{\frac{k}{m}}}.
$$

The proportionality is essential. A force that merely points toward equilibrium is **restoring**, but is not necessarily *linear* and therefore does not always produce exact SHM.

**Physical picture:** displace a spring-loaded cart to the right; its restoring force and acceleration point left. When the cart crosses equilibrium, the restoring force momentarily vanishes but the cart moves fastest. The force then reverses as the cart passes through.

## 12.2 Qualitative Nature of Simple Harmonic Motion

Take the oscillator released from its rightmost displacement $x=A$:

| Position | Displacement | Velocity | Acceleration |
|---|---|---|---|
| Right extreme | $+A$ | $0$ | Maximum toward left |
| Equilibrium | $0$ | Maximum toward left | $0$ |
| Left extreme | $-A$ | $0$ | Maximum toward right |
| Equilibrium, return | $0$ | Maximum toward right | $0$ |

The displacement, velocity and acceleration change continuously. **Equilibrium is not a resting point** for an oscillating mass; it is the point of zero restoring force.

An undamped ideal oscillator repeatedly trades kinetic and potential energies without changing its maximum displacement. In real systems, dissipation slowly removes oscillation energy.

## 12.3 Equation of Motion of a Simple Harmonic Motion

Solve

$$
\ddot x+\omega^2x=0.
$$

Because differentiation twice reverses the sign of sine and cosine,

$$
\boxed{x(t)=A\cos(\omega t+\phi)}
$$

is a general nontrivial solution with amplitude $A\ge0$ and phase constant $\phi$. Its derivatives are

$$
\boxed{v(t)=-A\omega\sin(\omega t+\phi)},
$$

$$
\boxed{a(t)=-A\omega^2\cos(\omega t+\phi)=-\omega^2x(t)}.
$$

For initial data $x(0)=x_0$ and $v(0)=v_0$,

$$
x_0=A\cos\phi,
\qquad
v_0=-A\omega\sin\phi,
$$

so

$$
\boxed{A=\sqrt{x_0^2+\left(\frac{v_0}{\omega}\right)^2}}.
$$

Determine $\phi$ using *both* sine and cosine information, for example with an appropriate quadrant-aware inverse tangent. A single equation for $\tan\phi$ can give the wrong quadrant.

**Alternative derivation of speed-position relation:**

$$
v^2=A^2\omega^2\sin^2(\omega t+\phi)
=\omega^2(A^2-x^2),
$$

hence

$$
\boxed{v=\pm\omega\sqrt{A^2-x^2}}.
$$

The sign depends on direction of travel.

## 12.4 Terms Associated with Simple Harmonic Motion

- **Mean or equilibrium position:** the stable location at which net restoring force is zero.
- **Displacement $x$:** signed distance from equilibrium.
- **Amplitude $A$:** greatest magnitude of displacement in a cycle.
- **Angular frequency $\omega$:** phase advance per unit time, in rad/s.
- **Phase $\omega t+\phi$:** state of the oscillation within a cycle.
- **Period $T$:** time taken to repeat the same state of displacement and motion direction.
- **Frequency $f$:** number of complete cycles per second.

Their relations are

$$
\boxed{\omega=2\pi f=\frac{2\pi}{T}},
\qquad
\boxed{T=2\pi\sqrt{\frac{m}{k}}}\ \text{for a spring-mass oscillator}.
$$

Extremal magnitudes:

$$
\boxed{v_{\max}=A\omega},
\qquad
\boxed{a_{\max}=A\omega^2}.
$$

For *ideal linear SHM*, period does not depend on amplitude. Changing amplitude changes maximum speed and energy, not $T$.

### Vertical spring and effective stiffness

For a vertical mass-spring system, define displacement $y$ from its shifted static equilibrium $y_0=mg/k$. The gravitational force cancels the spring force associated with $y_0$, leaving

$$
m\ddot y=-ky
\quad\Longrightarrow\quad
\boxed{T=2\pi\sqrt{m/k}}.
$$

For massless ideal springs, parallel springs have $k_{\mathrm{eq}}=k_1+k_2$ and series springs have $1/k_{\mathrm{eq}}=1/k_1+1/k_2$. The spring configuration changes the oscillator frequency through its effective stiffness.

## 12.5 Simple Harmonic Motion as a Projection of Circular Motion

Let a point move in uniform circular motion of radius $A$ with angular speed $\omega$. Its coordinate along a fixed diameter is

$$
x=A\cos(\omega t+\phi).
$$

Thus the projection performs SHM, even though the original particle moves in a circle with constant speed.

The geometry explains why the oscillator moves slowly near a turning point and rapidly around the mean position. The **reference circle** is a mathematical construction, not an assertion that the actual spring mass is secretly traveling in a circle.

Two orthogonal projections, $x=A\cos\omega t$ and $y=A\sin\omega t$, can reconstruct circular motion when their amplitudes match.

## 12.6 Energy Conservation in Simple Harmonic Motion

The restoring force $F=-kx$ is conservative with potential energy, measured from equilibrium,

$$
\boxed{U(x)=\frac12kx^2=\frac12m\omega^2x^2}.
$$

Kinetic energy follows from the speed-position relation:

$$
K=\frac12mv^2=\frac12m\omega^2(A^2-x^2).
$$

Adding them,

$$
\boxed{E=K+U=\frac12kA^2=\frac12m\omega^2A^2}.
$$

At an extreme, $K=0$ and $U=E$. At equilibrium, $U=0$ and $K=E$. At $|x|=A/\sqrt2$, the energies are equal.

**Graphical interpretation:** plot the horizontal total-energy line $E$ over the parabolic potential $U(x)$. Allowed positions satisfy $E\ge U(x)$; turning points occur where $E=U$.

## 12.7 Angular Simple Harmonic Motion

Rotational oscillators obey an analogous relationship. If $\theta$ is angular displacement from a stable equilibrium, $I$ is rotational inertia about a fixed axis, and $\kappa$ the angular restoring stiffness,

$$
\tau=-\kappa\theta,
\qquad
I\ddot\theta=\tau.
$$

Therefore

$$
\boxed{\ddot\theta+\frac{\kappa}{I}\theta=0},
\qquad
\boxed{T=2\pi\sqrt{\frac{I}{\kappa}}}.
$$

The angular amplitude is measured in radians. Its energy is

$$
\boxed{E=\frac12I\dot\theta^2+\frac12\kappa\theta^2}.
$$

The translation-to-rotation correspondence is $x\leftrightarrow\theta$, $m\leftrightarrow I$, $F\leftrightarrow\tau$, $k\leftrightarrow\kappa$.

## 12.8 Simple Pendulum

Consider a small bob of mass $m$ on a light, inextensible string of length $l$, moving in a vertical plane. Use angular displacement $\theta$ from the vertically downward position.

The tension acts radially and produces no torque about the suspension point. The tangential gravitational force is $-mg\sin\theta$:

$$
ml^2\ddot\theta=-mgl\sin\theta,
$$

or

$$
\boxed{\ddot\theta+\frac{g}{l}\sin\theta=0}.
$$

This is nonlinear. For **small angles expressed in radians**, $\sin\theta\simeq\theta$, giving

$$
\ddot\theta+\frac gl\theta\simeq0.
$$

Hence

$$
\boxed{\omega\simeq\sqrt{\frac gl}},
\qquad
\boxed{T\simeq2\pi\sqrt{\frac lg}}.
$$

The small-angle period is independent of bob mass and approximately independent of amplitude. At larger amplitudes, period increases; the exact motion is not SHM.

For energy relative to the lowest point,

$$
\boxed{E=\frac12ml^2\dot\theta^2+mgl(1-\cos\theta)}.
$$

This energy equation remains valid for the ideal pendulum even when the small-angle approximation fails.

**Common trap:** tension is generally not $mg\cos\theta$ during motion, because there is radial acceleration:

$$
T_{\mathrm{string}}-mg\cos\theta=m\frac{v^2}{l}.
$$

## 12.9 Physical Pendulum

A rigid body suspended about a horizontal pivot can oscillate under gravity. Let $I_O$ be its moment of inertia about the pivot and $d$ the distance from pivot to center of mass.

The gravitational torque is

$$
\tau=-mgd\sin\theta.
$$

At small angular displacement,

$$
I_O\ddot\theta+mgd\theta\simeq0,
$$

so

$$
\boxed{T=2\pi\sqrt{\frac{I_O}{mgd}}}.
$$

Define an **equivalent simple-pendulum length** $l_{\mathrm{eq}}=I_O/(md)$ so the same expression becomes $T=2\pi\sqrt{l_{\mathrm{eq}}/g}$.

Use $I_O=I_{\mathrm{CM}}+md^2$ when the parallel-axis theorem applies. The result requires the pivot to be fixed and the oscillation amplitude sufficiently small.

## 12.10 Torsional Pendulum

A rigid body attached to a fiber twisted about a vertical axis experiences a restoring torque approximated by $\tau=-\kappa\theta$, with $\kappa$ the torque per radian.

$$
\boxed{I\ddot\theta+\kappa\theta=0},
\qquad
\boxed{T=2\pi\sqrt{\frac{I}{\kappa}}}.
$$

Unlike a simple pendulum, this oscillator does not need a gravitational restoring torque; its restoring energy is stored in elastic twisting of the fiber. For small, reversible twists, the relationship between torque and angle is linear.

A torsion balance used to measure $G$ is also a torsional oscillator when released.

## 12.11 Composition of Two Simple Harmonic Motions

Superposition means adding displacements that act along the same coordinate, or analyzing the trajectory produced by oscillations along perpendicular coordinates.

### A. Same direction, same frequency

Let

$$
x_1=A_1\cos(\omega t+\phi_1),
\qquad
x_2=A_2\cos(\omega t+\phi_2).
$$

The sum has the same angular frequency:

$$
x=x_1+x_2=A\cos(\omega t+\phi).
$$

Writing $\delta=\phi_2-\phi_1$ and adding phase vectors gives

$$
\boxed{A=\sqrt{A_1^2+A_2^2+2A_1A_2\cos\delta}}.
$$

In phase ($\delta=0$), $A=A_1+A_2$; opposite phase ($\delta=\pi$), $A=|A_1-A_2|$; a phase difference of $\pi/2$ gives $A=\sqrt{A_1^2+A_2^2}$.

This is a vector-addition problem in the *phase plane*, even though the physical displacements lie on one line.

### B. Same direction, slightly different frequencies

For two equal amplitudes $A$,

$$
x=A\cos\omega_1t+A\cos\omega_2t.
$$

Using a trigonometric identity,

$$
\boxed{x=2A\cos\left(\frac{\omega_1-\omega_2}{2}t\right)
\cos\left(\frac{\omega_1+\omega_2}{2}t\right)}.
$$

The rapid oscillation is modulated by a slowly varying envelope. Its **beat frequency** is $|f_1-f_2|$, where beats are counted as envelope maxima in magnitude. The total signal is generally not exact single-frequency SHM.

### C. Perpendicular directions, same frequency

For

$$
x=A\cos\omega t,
\qquad
y=B\cos(\omega t+\delta),
$$

eliminate time to obtain

$$
\boxed{\frac{x^2}{A^2}+\frac{y^2}{B^2}
-\frac{2xy}{AB}\cos\delta=\sin^2\delta}.
$$

Different phase relationships produce different paths:

- $\delta=0$ or $\pi$: straight-line oscillation.
- $\delta=\pm\pi/2$: an ellipse aligned with the axes.
- $A=B$ and $\delta=\pm\pi/2$: circular motion.

These paths are simple examples of **Lissajous figures**. For unlike frequency ratios, more elaborate closed or nonclosed patterns appear.

## 12.12 Damped Harmonic Motion

Real oscillators lose energy to friction, fluid resistance or internal material dissipation. A common model treats damping force as proportional to velocity:

$$
\boxed{m\ddot x+b\dot x+kx=0},
\qquad b>0.
$$

Define

$$
\omega_0=\sqrt{\frac{k}{m}},
\qquad
\gamma=\frac{b}{2m}.
$$

For **underdamping** ($\gamma<\omega_0$),

$$
\boxed{x(t)=Ae^{-\gamma t}\cos(\omega_dt+\phi)},
\qquad
\boxed{\omega_d=\sqrt{\omega_0^2-\gamma^2}}.
$$

The envelope decays exponentially. For **critical damping**, $b=2\sqrt{mk}$ and the system returns toward equilibrium without oscillating, as fast as possible within this linear model for a conventional return response. For **overdamping**, $b>2\sqrt{mk}$ and the return is nonoscillatory with slower long-time behavior.

Mechanical energy is not conserved:

$$
E=\frac12m\dot x^2+\frac12kx^2,
\qquad
\boxed{\frac{dE}{dt}=-b\dot x^2\le0}.
$$

The term on the right is the instantaneous rate of mechanical energy dissipation. Damping and driving must not be conflated.

## 12.13 Forced Oscillation and Resonance

An external periodic force can continuously supply energy to a damped oscillator. A simple model is

$$
\boxed{m\ddot x+b\dot x+kx=F_0\cos\Omega t}.
$$

After the transient dies away, the steady-state motion is at the **driving frequency** $\Omega$, not generally the undamped natural frequency $\omega_0$:

$$
x_{\mathrm{ss}}=X\cos(\Omega t-\delta).
$$

The steady-state amplitude and phase lag are

$$
\boxed{X(\Omega)=\frac{F_0}{\sqrt{(k-m\Omega^2)^2+b^2\Omega^2}}},
$$

$$
\boxed{\tan\delta=\frac{b\Omega}{k-m\Omega^2}}
\qquad\text{(choose the physically correct quadrant).}
$$

For sufficiently light damping ($b^2<2mk$), the *displacement-amplitude* maximum occurs at

$$
\boxed{\Omega_{\mathrm{res}}=\sqrt{\omega_0^2-\frac{b^2}{2m^2}}}.
$$

In the weak-damping limit this is close to $\omega_0$. There is no displacement-amplitude peak at positive frequency for sufficiently strong damping, and other resonance definitions (for velocity or absorbed power) can peak at different frequencies.

Near resonance, each cycle can add energy efficiently. Damping limits the steady-state response. Resonance is not a source of free energy: the energy comes from the driver.

### Part II: Key takeaways

- **SHM criterion:** acceleration must be $-\omega^2x$ for displacement measured from equilibrium.
- A harmonic oscillator alternates between kinetic and potential energy; total mechanical energy is fixed only if damping and driving are absent.
- Pendulums are approximately harmonic at small angular amplitudes; simple and physical pendulums have different inertia models.
- SHM superposition explains phase effects, beats and Lissajous trajectories.
- Damping changes transient motion; periodic forcing selects steady-state frequency and produces a finite resonant response.

---
# Part III: Fluid Mechanics

A fluid continuously deforms when subjected to shear stress. Fluids include liquids and gases. Much of introductory fluid mechanics begins with ideal fluids, then adds physical effects such as viscosity when ideal theory becomes insufficient.

## 13.1 Fluids

A solid can sustain a static shear deformation; a fluid cannot sustain a nonzero shear stress in static equilibrium. The fluid continues to deform (flow) while shear stress persists.

Useful macroscopic properties:

$$
\boxed{\rho=\frac{dm}{dV}}\qquad\text{(mass density)},
$$

$$
\boxed{P=\frac{dF_n}{dA}}\qquad\text{(normal pressure)}.
$$

Density is measured in $\mathrm{kg\,m^{-3}}$, and pressure in pascals, $1\,\mathrm{Pa}=1\,\mathrm{N\,m^{-2}}$.

**Model distinctions:** a *fluid at rest* has no velocity relative to its container; a *steady flow* can move while field quantities at a fixed point remain unchanged with time. An *incompressible* model treats density as constant for a fluid parcel; real liquids are approximately incompressible in many settings, while gases may not be.

## 13.2 Pressure in a Fluid

Consider a small horizontal fluid slab of cross-sectional area $A$ and thickness $dz$. In hydrostatic equilibrium, the upward force from pressure below balances pressure above and the slab's weight:

$$
P(z)A-P(z+dz)A-\rho gA\,dz=0.
$$

If $z$ increases upward,

$$
\boxed{\frac{dP}{dz}=-\rho g}.
$$

For uniform density and constant $g$, integration gives

$$
\boxed{P(h)=P_{\mathrm{surface}}+\rho gh},
$$

where $h$ denotes **depth below** the surface. At a given depth in a connected, static fluid of uniform density, pressure is the same independent of container shape.

Pressure is a scalar and acts normal to the surface of a small immersed element. The *pressure force* is directional:

$$
d\vec F=-P\hat n\,dA,
$$

where $\hat n$ is the outward normal of the chosen fluid control volume.

## 13.3 Pascal's Law

A change of pressure imposed on a confined static fluid is transmitted through it, aside from any hydrostatic variations caused by height.

For an ideal hydraulic device with piston areas $A_1$ and $A_2$ at equal fluid level,

$$
\frac{F_1}{A_1}=\frac{F_2}{A_2}
\quad\Longrightarrow\quad
\boxed{\frac{F_2}{F_1}=\frac{A_2}{A_1}}.
$$

Mechanical advantage does not create work. For nearly incompressible fluid,

$$
A_1\Delta x_1=A_2\Delta x_2,
$$

so, ideally,

$$
F_1\Delta x_1=F_2\Delta x_2.
$$

The larger force travels the smaller distance. Hydraulic jacks, presses and brakes apply this principle under constraints imposed by losses and structural limits.

## 13.4 Atmospheric Pressure and Barometer

Atmospheric pressure is exerted by the weight of air above a location. For a column of mercury with density $\rho_{\mathrm{Hg}}$ whose upper end is approximately vacuum, a barometer satisfies

$$
\boxed{P_{\mathrm{atm}}=\rho_{\mathrm{Hg}}gh}.
$$

At sea level, a standard atmospheric pressure is approximately

$$
\boxed{1\ \mathrm{atm}\simeq1.013\times10^5\ \mathrm{Pa}\simeq760\ \mathrm{mmHg}}.
$$

For a fluid manometer, pressure differences relate to differences in liquid-column elevations. Apply the hydrostatic equation separately in each continuous fluid and compare points at the same horizontal level where appropriate.

**Absolute versus gauge pressure:**

$$
\boxed{P_{\mathrm{gauge}}=P_{\mathrm{absolute}}-P_{\mathrm{atmosphere}}}.
$$

A negative gauge reading does not imply negative absolute pressure. Pressure changes with altitude because the atmosphere has a nonuniform density and finite temperature profile.

## 13.5 Archimedes' Principle

Pressure is greater on the lower surfaces of a submerged object than on its upper surfaces. Integrating the pressure forces gives a net upward **buoyant force** equal to the weight of the displaced fluid:

$$
\boxed{F_B=\rho_f gV_{\mathrm{displaced}}}.
$$

A compact derivation can be obtained by imagining a volume of fluid occupying the object's location. The surrounding fluid would support that volume's weight in static equilibrium; replacing it with an object leaves the same net hydrostatic pressure force for the same displaced volume.

For an object of mass $m$, the apparent weight when immersed and supported from above is

$$
\boxed{W_{\mathrm{apparent}}=mg-F_B}.
$$

A freely floating object in vertical equilibrium obeys

$$
mg=\rho_f gV_{\mathrm{submerged}}.
$$

If it has uniform density $\rho_b$ and total volume $V_b$,

$$
\boxed{\frac{V_{\mathrm{submerged}}}{V_b}=\frac{\rho_b}{\rho_f}}\quad\text{(floating body).}
$$

This ratio is meaningful only for a floating equilibrium and $\rho_b\le\rho_f$; a denser unrestrained object sinks instead. The buoyancy rule assumes hydrostatic surrounding fluid and negligible additional forces such as surface tension.

## 13.6 Pressure Difference and Buoyant Force in Accelerating Fluids

In a container accelerating with constant acceleration $\vec a_0$, a coordinate frame fixed to the container introduces the uniform pseudo acceleration $-\vec a_0$. The fluid can be **at rest relative to the container** even though the system is accelerating in an inertial frame.

Define an effective acceleration field

$$
\boxed{\vec g_{\mathrm{eff}}=\vec g-\vec a_0}.
$$

For relative hydrostatic equilibrium,

$$
\boxed{\vec\nabla P=\rho\vec g_{\mathrm{eff}}}.
$$

**Example: horizontal acceleration.** Let $x$ point along container acceleration $a_0$ and $z$ point upward. Then

$$
\frac{\partial P}{\partial x}=-\rho a_0,
\qquad
\frac{\partial P}{\partial z}=-\rho g.
$$

On the atmospheric-pressure free surface, $dP=0$ gives

$$
-\rho a_0\,dx-\rho g\,dz=0
\quad\Longrightarrow\quad
\boxed{\frac{dz}{dx}=-\frac{a_0}{g}}.
$$

The free surface rises opposite the direction of acceleration. The net pressure-induced buoyancy is opposite to effective gravity, with magnitude $\rho_fV|\vec g_{\mathrm{eff}}|$ for a fully submerged object in the ideal uniform-field setting.

**Vertical acceleration:** when the container accelerates upward with magnitude $a_0$, effective downward gravity becomes $g+a_0$. Downward acceleration lowers effective gravity; in free fall it vanishes in the ideal model.

## 13.7 Flow of Fluids

To describe fluid motion, assign velocity $\vec v(\vec r,t)$ to each location and time. A **streamline** is a curve everywhere tangent to the instantaneous local velocity field.

A **streamtube** consists of streamlines forming its lateral boundary. Under ideal steady flow, fluid does not cross the sides of a streamtube. Particles in steady motion travel along stationary streamlines; for unsteady flow, streamlines at an instant need not coincide with actual particle trajectories.

Three distinct descriptions must be kept separate:

- **Steady versus unsteady:** whether local fields change with time.
- **Laminar versus turbulent:** whether the flow is orderly or has irregular fluctuations and mixing.
- **Compressible versus incompressible:** whether density variations of moving parcels matter.

Flow rate through a cross section is

$$
\boxed{Q=\int_A\vec v\cdot\hat n\,dA}.
$$

For one-dimensional approximately uniform flow, $Q=Av$.

## 13.8 Steady and Turbulent Flow

A **steady** flow satisfies $\partial\vec v/\partial t=0$ at each fixed point, with similar steady conditions for other relevant flow properties. A steady flow can have nonzero acceleration because fluid moving through different positions may change speed or direction.

The material acceleration is

$$
\boxed{\frac{D\vec v}{Dt}=\frac{\partial\vec v}{\partial t}+(\vec v\cdot\vec\nabla)\vec v}.
$$

The second term, **convective acceleration**, remains even when the first term vanishes.

**Turbulence** involves fluctuating eddies and nonlinear transport. A turbulent flow can be statistically steady even though its instantaneous velocity fluctuates. Introductory Bernoulli and continuity problems commonly adopt smooth, steady-flow idealizations.

## 13.9 Irrotational Flow of an Incompressible and Nonviscous Fluid

Three idealizations are often invoked together:

1. **Incompressible:** fluid parcel density stays constant, often approximated by constant $\rho$ everywhere.
2. **Nonviscous (inviscid):** shear stresses due to molecular viscosity are neglected.
3. **Irrotational:** the velocity field has zero curl where it is smooth.

For irrotational flow,

$$
\boxed{\vec\nabla\times\vec v=\vec0}.
$$

In a simply connected region this permits a velocity potential $\Phi$ with $\vec v=\vec\nabla\Phi$. Combined with incompressibility ($\vec\nabla\cdot\vec v=0$),

$$
\boxed{\nabla^2\Phi=0}.
$$

These vector-calculus expressions extend HCV's introductory treatment and help explain why ideal flow fields can be computed from a potential. Inviscid flow need not be irrotational, and irrotational flow need not be steady.

## 13.10 Equation of Continuity

Mass cannot disappear in a flow passage. During a short interval $\Delta t$, mass crossing a uniform inlet section is

$$
\Delta m_{\mathrm{in}}=\rho_1A_1v_1\Delta t.
$$

For **steady flow through one streamtube** with no side leakage,

$$
\boxed{\rho_1A_1v_1=\rho_2A_2v_2}.
$$

For constant density,

$$
\boxed{A_1v_1=A_2v_2=Q}.
$$

A narrower section means greater speed **only** under the stated steady incompressible conditions and appropriate area-averaging.

The differential conservation of mass is

$$
\boxed{\frac{\partial\rho}{\partial t}+\vec\nabla\cdot(\rho\vec v)=0}.
$$

For an incompressible constant-density field, this reduces to $\vec\nabla\cdot\vec v=0$.

## 13.11 Bernoulli's Equation

For steady, inviscid, incompressible flow along a streamline under gravity, pressure work, kinetic energy and gravitational potential energy exchange with one another.

### Derivation from a moving fluid element

Suppose a volume $\Delta V$ enters a region at pressure $P_1$, speed $v_1$ and elevation $z_1$, and leaves at $P_2$, speed $v_2$ and elevation $z_2$.

Net pressure work is

$$
W_P=P_1\Delta V-P_2\Delta V=(P_1-P_2)\Delta V.
$$

The change in kinetic and gravitational potential energies of mass $\Delta m=\rho\Delta V$ is

$$
\Delta E=\frac12\rho\Delta V(v_2^2-v_1^2)
+\rho\Delta Vg(z_2-z_1).
$$

Equating work to energy change and dividing by $\Delta V$,

$$
\boxed{P+\frac12\rho v^2+\rho gz=\text{constant along a streamline}}.
$$

Terms have units of pressure or energy per unit volume. Dividing by $\rho g$ gives **head form**:

$$
\boxed{\frac{P}{\rho g}+\frac{v^2}{2g}+z=\text{constant}}.
$$

Pressure head, velocity head and elevation head all have units of length.

**Applicability matters.** The standard Bernoulli relation excludes significant viscous dissipation, pumps or turbines within the compared segment, and large density changes. Across different streamlines, a single Bernoulli constant generally requires further conditions such as irrotational flow.

**Pressure misconception:** faster local flow can accompany lower static pressure along a suitable streamline at the same elevation, but speed alone does not determine pressure in an arbitrary moving fluid.

## 13.12 Applications of Bernoulli's Equation

### A. Horizontal converging tube

For elevations equal at stations 1 and 2,

$$
P_1+\frac12\rho v_1^2=P_2+\frac12\rho v_2^2,
$$

so

$$
\boxed{P_1-P_2=\frac12\rho(v_2^2-v_1^2)}.
$$

If $A_2<A_1$ in steady incompressible flow, continuity predicts $v_2>v_1$ and hence $P_2<P_1$ under ideal assumptions. This is the principle behind a **Venturi meter**.

### B. Torricelli's law

For a large open reservoir with a small outlet a vertical distance $h$ below the nearly stationary upper free surface, both surface and outlet are at atmospheric pressure. Bernoulli then gives

$$
\boxed{v_{\mathrm{exit}}\simeq\sqrt{2gh}}.
$$

The result assumes negligible tank-surface speed and negligible head loss; real discharge is altered by nozzle geometry and viscosity.

### C. Pitot-style speed measurement

At equal elevation, a fluid brought nearly to rest at a stagnation point gives

$$
P_{\mathrm{stag}}-P_{\mathrm{static}}=\frac12\rho v^2,
$$

hence

$$
\boxed{v=\sqrt{\frac{2(P_{\mathrm{stag}}-P_{\mathrm{static}})}{\rho}}}.
$$

Compressibility corrections matter when gas velocities are sufficiently high.

### D. Atomizers, aspirators and other devices

A pressure difference associated with fast-moving fluid can draw a secondary fluid through a narrow opening. A nozzle may also accelerate fluid at the expense of pressure energy. Device performance depends on geometry and losses, so the ideal calculation is a first approximation rather than a universal engineering formula.

### Part III: Key takeaways

- Hydrostatic pressure changes with vertical position according to $dP/dz=-\rho g$.
- Archimedes' law is the net consequence of a pressure gradient across a displaced volume.
- In an accelerating container, substitute effective gravity when describing relative hydrostatic equilibrium.
- Continuity enforces **mass conservation**; Bernoulli describes **mechanical energy conservation** under specific ideal-flow assumptions.
- Real flows may require viscous head-loss models, compressible-flow theory and careful measurement of mean versus local velocity.

---
# Part IV: Some Mechanical Properties of Matter

Real materials deform and flow because of intermolecular interactions. This chapter connects microscopic forces to macroscopic measurable quantities: elastic moduli, tension at liquid surfaces and resistance to motion within fluids.

## 14.1 Molecular Structure of a Material

Matter consists of atoms and molecules with interactions that are **repulsive at very short separation** and **attractive over an appropriate range**. A simplified pair potential $U(r)$ has a minimum at an equilibrium separation $r_0$.

Since force is related to potential by

$$
\boxed{F_r=-\frac{dU}{dr}},
$$

a small change $x=r-r_0$ about a stable minimum produces, to first order,

$$
U(r)\simeq U(r_0)+\frac12k_{\mathrm{mol}}x^2,
\qquad
F_r\simeq-k_{\mathrm{mol}}x.
$$

This local nearly linear restoring behavior helps explain elasticity and the appearance of harmonic approximations. Macroscopic properties additionally depend on collective geometry, temperature, defects and the arrangement of molecules.

**Important distinction:** the molecular picture motivates bulk laws but does not make one macroscopic elastic constant universal for every material or every deformation.

## 14.2 Elasticity

A material is **elastic** if it tends to recover its original shape or dimensions upon removal of an applied deforming load. An irreversible change remaining after unloading is called **plastic deformation**.

- **Elastic deformation:** unloading approximately restores the original configuration.
- **Plastic deformation:** a permanent set remains after unloading.
- **Ideal Hookean behavior:** the relevant stress is proportional to the corresponding small strain.

Elasticity does **not** mean a material is easy to stretch. A high Young's modulus means a large force per area is required for a given small longitudinal strain; rubber can often recover from much greater strain than a metal, even though its Young's modulus is much smaller.

## 14.3 Stress

**Stress** describes the intensity of internal force transmitted across a surface. At the elementary level, it is force per unit area:

$$
\boxed{\sigma=\frac{F}{A}},
\qquad
[\sigma]=ML^{-1}T^{-2}=\mathrm{Pa}.
$$

Distinguish the direction of the force relative to the surface:

- **Longitudinal tensile stress:** pulls and elongates a rod.
- **Longitudinal compressive stress:** pushes and shortens a rod.
- **Shear stress:** acts parallel to a material cross section and changes angles.
- **Bulk or volume stress:** pressure acting from all directions, changing volume.

In general three-dimensional continuum mechanics, stress is a tensor rather than a single scalar. Here the formulas assume the simple loading patterns shown in HCV.

A wire under axial tension $F$ has average longitudinal stress $\sigma=F/A$ provided the loading is sufficiently uniform and bending can be ignored.

## 14.4 Strain

**Strain** measures deformation relative to an original dimension and is usually dimensionless.

**Longitudinal strain:**

$$
\boxed{\varepsilon_{\ell}=\frac{\Delta L}{L_0}}.
$$

**Volume strain:**

$$
\boxed{\varepsilon_V=\frac{\Delta V}{V_0}}.
$$

**Shear strain:** for a small angular deformation $\gamma$ in radians,

$$
\boxed{\gamma\simeq\tan\gamma=\frac{\Delta x}{h}}.
$$

The signs of longitudinal and volume strains indicate extension and contraction according to convention. Small-strain formulas should not be used uncritically for very large deformations.

## 14.5 Hooke's Law and the Moduli of Elasticity

Within the approximately linear elastic region, **stress is proportional to strain**. The proportionality depends on loading type and material.

### A. Young's modulus

For uniform uniaxial longitudinal loading,

$$
\boxed{Y=\frac{\text{longitudinal stress}}{\text{longitudinal strain}}
=\frac{F/A}{\Delta L/L_0}
=\frac{FL_0}{A\Delta L}}.
$$

Thus

$$
\boxed{\Delta L=\frac{FL_0}{AY}}.
$$

For a wire of original length $L_0$, cross-sectional area $A$ and material modulus $Y$, the effective axial spring constant is $k=YA/L_0$.

### B. Shear modulus (modulus of rigidity)

For simple shear,

$$
\boxed{G_s=\frac{\tau}{\gamma}},
$$

where $\tau=F_{\parallel}/A$ is shear stress and $\gamma\simeq\Delta x/h$ is shear strain. The subscript on $G_s$ avoids confusion with the **gravitational** constant $G$ and the **viscosity** coefficient $\eta$.

### C. Bulk modulus and compressibility

For a positive rise in hydrostatic pressure $\Delta P$ producing a negative volume change,

$$
\boxed{B=-\frac{\Delta P}{\Delta V/V_0}},
$$

or in the infinitesimal form,

$$
\boxed{B=-V\frac{dP}{dV}}.
$$

The **compressibility** is

$$
\boxed{\beta=\frac1B=-\frac1V\frac{dV}{dP}}.
$$

Young's, shear and bulk moduli have dimensions of pressure, while compressibility has dimensions $\mathrm{Pa^{-1}}$.

### D. Poisson's ratio

An axially stretched rod generally becomes thinner transversely. Poisson's ratio is

$$
\boxed{\nu=-\frac{\text{transverse strain}}{\text{longitudinal strain}}}.
$$

For small strains in an **isotropic linear elastic** material, the constants are related:

$$
\boxed{Y=2G_s(1+\nu)},
\qquad
\boxed{Y=3B(1-2\nu)}.
$$

These relationships are additional useful elasticity identities and require the stated isotropy/linearity assumptions. They are not freely applicable to nonlinear rubber behavior or anisotropic crystals.

## 14.6 Relation between Longitudinal Stress and Strain

A stress-strain graph for a typical ductile metal can contain several regions.

| Region or landmark | Interpretation |
|---|---|
| **Proportional limit** | Stress and strain approximately obey a straight line; Young's modulus is its slope. |
| **Elastic limit** | Unloading still approximately restores the initial length, even if the curve is not perfectly linear. |
| **Plastic region** | Unloading leaves a permanent deformation. |
| **Fracture** | The specimen breaks. |

Elastic limit, yield point, ultimate tensile strength and breaking stress need not coincide in real tests.

For rubber-like materials, stress is often nonlinear even over recoverable large strains. Loading and unloading curves may be different, a behavior known as **elastic hysteresis**. Energy dissipated per unit volume over a stress-strain cycle is the area enclosed by the loop:

$$
\boxed{w_{\mathrm{loss}}=\oint\sigma\,d\varepsilon}.
$$

The sign is set by the traversal convention; the positive enclosed area gives dissipated energy per unit volume.

Materials do not become more elastic merely because they deform more easily. **Modulus**, **recoverability** and **strength** describe distinct properties.

## 14.7 Elastic Potential Energy of a Strained Body

An initially unstressed Hookean wire extended by $x$ has tension

$$
F(x)=\frac{YA}{L_0}x=kx.
$$

Slowly stretching it from $0$ to $\Delta L$ stores work:

$$
U=\int_0^{\Delta L}F(x)\,dx
=\frac12k(\Delta L)^2.
$$

Thus

$$
\boxed{U=\frac12\frac{YA}{L_0}(\Delta L)^2=\frac12F\Delta L}.
$$

Divide by the original volume $AL_0$ to obtain **elastic energy per unit volume**:

$$
\boxed{u=\frac12\sigma\varepsilon=\frac{\sigma^2}{2Y}=\frac12Y\varepsilon^2}.
$$

This simple form assumes uniaxial linear elasticity. In nonlinear elastic loading, the stored work is found from the area under the appropriate loading curve, with due allowance for hysteresis and irreversible dissipation.

## 14.8 Determination of Young's Modulus in Laboratory

A long uniform wire under a measured load allows Young's modulus to be inferred from its extension. If a hanging mass $m$ produces tension approximately $F=mg$ after equilibrium,

$$
\boxed{Y=\frac{mgL_0}{A\Delta L}}.
$$

For a circular wire of diameter $d$, $A=\pi d^2/4$, giving

$$
\boxed{Y=\frac{4mgL_0}{\pi d^2\Delta L}}.
$$

**Measurement procedure in principle:** measure wire length and diameter, apply a safe known load, allow oscillations to settle, determine extension, then repeat with several loads to estimate a slope. In a **Searle-type apparatus**, a reference wire helps compensate for common support movement and environmental effects.

Useful experimental safeguards:

- Stay below the elastic limit so repeated loading does not produce permanent extension.
- Use a uniform, straight specimen; bending or slack corrupts the uniaxial model.
- The diameter is especially important because area varies as $d^2$.
- If $\Delta L$ is very small, measurement resolution and temperature changes can dominate.

For small independent measurement uncertainties, approximate fractional propagation is

$$
\left(\frac{\delta Y}{Y}\right)^2\simeq
\left(\frac{\delta F}{F}\right)^2+
\left(\frac{\delta L_0}{L_0}\right)^2+
\left(2\frac{\delta d}{d}\right)^2+
\left(\frac{\delta(\Delta L)}{\Delta L}\right)^2.
$$

This uncertainty relation is an extra measurement-analysis extension, assuming small uncorrelated uncertainties.

## 14.9 Surface Tension

Molecules at a liquid surface experience a different arrangement of neighbors from molecules in the bulk. Creating surface area generally requires energy. The surface exhibits an effective **tension per unit length** along a line in the surface:

$$
\boxed{S=\frac{F}{l}},
\qquad [S]=MT^{-2}=\mathrm{N\,m^{-1}}.
$$

For a soap film spanning a sliding wire of length $l$, there are **two air-liquid surfaces**, so the total pull is

$$
\boxed{F=2Sl}\qquad\text{(two surfaces).}
$$

For a single liquid-air interface along the same line, the ideal pull is $F=Sl$.

Surface tension tends to minimize free surface area under applicable constraints. A small freely suspended drop tends toward a sphere because a sphere has the least surface area for a given enclosed volume. Gravity can distort larger drops.

Surface tension depends on fluid composition, temperature, impurities and the materials on either side of an interface.

## 14.10 Surface Energy

Surface tension can also be expressed in energy units. For an isothermal reversible increase in interface area $dA$ at constant surface tension,

$$
\boxed{dU_{\mathrm{surface}}=S\,dA},
\qquad
\boxed{S=\frac{dU}{dA}}.
$$

Here the relevant quantity is the reversible surface-energy or surface-free-energy cost under the specified conditions. For a soap film with two faces, an increase in its geometric face area by $dA_{\mathrm{face}}$ creates $2dA_{\mathrm{face}}$ of total interface.

### Breaking a drop into smaller drops

A drop of radius $R$ divides into $n$ identical droplets of radius $r$. Conserving volume gives

$$
\frac43\pi R^3=n\frac43\pi r^3
\quad\Longrightarrow\quad
\boxed{r=Rn^{-1/3}}.
$$

The total new liquid-air area is

$$
A_f=n(4\pi r^2)=4\pi R^2n^{1/3}.
$$

Thus

$$
\boxed{\Delta U=4\pi SR^2(n^{1/3}-1)}.
$$

Breaking up a drop **increases** area and costs surface energy; coalescence of small drops usually releases surface energy.

## 14.11 Excess Pressure Inside a Drop

A curved interface can sustain a pressure difference. For a spherical liquid drop of radius $R$ surrounded by gas, a reversible increase $dR$ changes its volume and surface area by

$$
dV=4\pi R^2\,dR,
\qquad
dA=8\pi R\,dR.
$$

The pressure difference $\Delta P=P_{\mathrm{inside}}-P_{\mathrm{outside}}$ does work $\Delta P\,dV$ against the surface-energy change $S\,dA$. Equating,

$$
\Delta P(4\pi R^2\,dR)=S(8\pi R\,dR).
$$

Therefore

$$
\boxed{\Delta P_{\mathrm{drop}}=\frac{2S}{R}}.
$$

For a smaller drop made of the same liquid with the same surface tension, the required excess internal pressure is greater.

## 14.12 Excess Pressure in a Soap Bubble

A thin spherical soap bubble has an **inner** and an **outer** liquid-air surface. The total surface-energy change for a small expansion is twice that of one interface:

$$
dU\simeq2S(8\pi R\,dR).
$$

Equating to pressure work gives

$$
\boxed{\Delta P_{\mathrm{soap\ bubble}}=\frac{4S}{R}}.
$$

Compare carefully:

| Configuration | Curved interfaces | Ideal excess pressure |
|---|---:|---|
| Liquid droplet in air | One | $2S/R$ |
| Gas bubble in a liquid | One | $2S/R$ |
| Thin soap bubble in air | Two | $4S/R$ |

This is the spherical special case of the **Young-Laplace** pressure-jump relationship. It assumes surface tension is uniform and effects of finite film thickness and gravity are negligible.

## 14.13 Contact Angle

When a liquid surface meets a solid boundary, it generally forms a **contact angle** $\theta$, measured through the liquid between the solid surface and the tangent to the liquid interface.

- $\theta<90^\circ$: the liquid generally wets the surface, giving a concave meniscus in an ordinary narrow vertical tube.
- $\theta>90^\circ$: the liquid tends not to wet the surface, giving a convex meniscus.
- The specific value depends on the solid, liquid, surrounding gas and surface cleanliness.

The equilibrium contact angle reflects the competition between solid-vapor, solid-liquid and liquid-vapor interfacial energies. An ideal equilibrium relation is

$$
\boxed{\gamma_{SV}-\gamma_{SL}=\gamma_{LV}\cos\theta},
$$

where $\gamma$ denotes the appropriate interfacial free energy per unit area. This is Young's contact-angle equation and assumes a well-defined equilibrium contact line on an ideal solid surface.

Real surfaces may display advancing and receding contact angles because of pinning and hysteresis.

## 14.14 Rise of Liquid in a Capillary Tube

Put a narrow vertical tube of inner radius $r$ into a liquid. At the contact perimeter $2\pi r$, the vertical component of surface-tension force is

$$
F_{S,z}=2\pi rS\cos\theta.
$$

Balancing against the weight of the liquid column raised by height $h$ relative to the external level,

$$
2\pi rS\cos\theta=\rho g(\pi r^2h).
$$

Thus

$$
\boxed{h=\frac{2S\cos\theta}{\rho gr}}.
$$

A positive $h$ means capillary rise; a negative $h$ describes depression for a nonwetting liquid. The inverse dependence on tube radius makes the effect stronger in narrower tubes.

**Assumptions:** narrow tube, equilibrium, approximate cylindrical column, negligible end effects and an appropriate contact angle. For very narrow pores and real porous materials, geometry and wetting history complicate the formula.

## 14.15 Viscosity

Viscosity expresses a fluid's resistance to relative sliding motion between neighboring fluid layers. For a simple **Newtonian fluid**, shear stress is proportional to the velocity gradient:

$$
\boxed{\tau=\eta\frac{dv_x}{dy}},
$$

where $\eta$ is the coefficient of **dynamic viscosity**:

$$
\boxed{\eta=\frac{F/A}{dv_x/dy}},
\qquad
[\eta]=ML^{-1}T^{-1}=\mathrm{Pa\,s}.
$$

For two parallel plates separated by gap $h$, lower plate fixed and upper plate sliding at speed $v$ with an approximately linear velocity profile,

$$
\boxed{F=\eta A\frac{v}{h}}.
$$

**Distinguish viscosity from static friction:** viscosity depends on a fluid velocity gradient; dry Coulomb friction is modeled using contact normal force and friction coefficients. A Newtonian viscous force commonly depends on speed, whereas dry friction often does not over a broad sliding-speed range.

The **kinematic viscosity** is $\nu=\eta/\rho$, with units $\mathrm{m^2\,s^{-1}}$. This $\nu$ is unrelated to the Poisson's ratio symbol also often written $\nu$; context matters.

## 14.16 Flow through a Narrow Tube: Poiseuille's Equation

Consider steady, fully developed laminar flow of a Newtonian incompressible fluid through a long straight circular tube of radius $a$ and length $L$. A pressure difference $\Delta P=P_{\mathrm{in}}-P_{\mathrm{out}}>0$ drives motion.

In equilibrium of axial forces on a cylindrical fluid core of radius $r$, the pressure force $\Delta P\pi r^2$ balances viscous shear over the lateral area $2\pi rL$:

$$
\Delta P\pi r^2=\eta\left(-\frac{dv}{dr}\right)2\pi rL.
$$

Therefore

$$
\frac{dv}{dr}=-\frac{\Delta P}{2\eta L}r.
$$

Integrate and impose no-slip $v(a)=0$:

$$
\boxed{v(r)=\frac{\Delta P}{4\eta L}(a^2-r^2)}.
$$

The velocity is maximum on the axis and decreases parabolically to zero at the wall. Integrating across rings of area $dA=2\pi r\,dr$,

$$
Q=\int_0^av(r)2\pi r\,dr,
$$

so the **Hagen-Poiseuille law** is

$$
\boxed{Q=\frac{\pi a^4\Delta P}{8\eta L}}.
$$

The average speed is $\bar v=Q/(\pi a^2)$ and $v_{\max}=2\bar v$.

**Fourth-power sensitivity:** doubling the radius at fixed pressure drop, length and viscosity gives sixteen times the ideal flow rate. This depends on maintaining laminar, fully developed, Newtonian flow; the formula cannot be extended blindly to turbulent or strongly entrance-dominated flow.

## 14.17 Stokes' Law

When a small sphere of radius $r$ moves slowly through a viscous fluid, the fluid resists its motion. In the **creeping-flow** regime, Stokes' law gives the drag magnitude

$$
\boxed{F_D=6\pi\eta rv}.
$$

Drag points **opposite** the sphere's velocity relative to the surrounding fluid. Conditions include a low particle Reynolds number, approximately spherical rigid particle, Newtonian continuum fluid, and boundaries sufficiently distant that wall effects are small.

The linear dependence on $v$ contrasts with the approximately quadratic drag common at much higher Reynolds numbers.

## 14.18 Terminal Velocity

Release a solid sphere of radius $r$ and density $\rho_s$ in a fluid of density $\rho_f$ and viscosity $\eta$. If the sphere falls, its downward weight, upward buoyancy and upward viscous drag give

$$
\frac43\pi r^3\rho_sg
-\frac43\pi r^3\rho_fg
-6\pi\eta rv=m\frac{dv}{dt}.
$$

At **terminal velocity** $v_t$, acceleration is zero:

$$
\frac43\pi r^3(\rho_s-\rho_f)g=6\pi\eta rv_t.
$$

Thus

$$
\boxed{v_t=\frac{2r^2(\rho_s-\rho_f)g}{9\eta}}.
$$

If $\rho_s<\rho_f$, the signed terminal motion is upward rather than downward. For a slowly descending sphere, terminal speed grows as $r^2$ under the Stokes assumptions.

The velocity approaches its limiting value exponentially in the ideal constant-coefficient model:

$$
\boxed{v(t)=v_t(1-e^{-t/\tau})},
\qquad
\boxed{\tau=\frac{m}{6\pi\eta r}},
$$

when released from rest with an initially stationary fluid and with appropriate terminal-velocity conditions. For very small particles, Brownian motion and other effects may also matter.

## 14.19 Measuring Coefficient of Viscosity by Stokes' Method

The falling-sphere method determines $\eta$ by measuring the terminal speed of a small sphere through a liquid.

For a sphere of diameter $2r$ traveling a known distance $s$ between marks in time $t$ *after terminal motion has been established*,

$$
v_t=\frac{s}{t}.
$$

Rearrange the preceding terminal-speed equation:

$$
\boxed{\eta=\frac{2r^2(\rho_s-\rho_f)g}{9v_t}}.
$$

**Experimental sequence:** measure particle radius and density, control fluid temperature, release sphere gently away from vessel walls, allow a settling distance, time its travel across a central measurement section, and repeat for several spheres or trials.

**Potential errors:** wall proximity, finite liquid depth, uncertain radius, temperature-dependent viscosity, a particle that has not reached terminal motion, air bubbles adhering to the sphere, and Reynolds numbers too high for Stokes drag.

Since $\eta\propto r^2/v_t$, a small fractional radius error can have a comparatively large influence on calculated viscosity.

## 14.20 Critical Velocity and Reynolds Number

Viscous effects compete with fluid inertia. Their relative importance can be estimated by the **Reynolds number**:

$$
\boxed{\mathrm{Re}=\frac{\rho vL_c}{\eta}=\frac{vL_c}{\nu}},
$$

where $L_c$ is a characteristic length. For flow through a circular pipe, a common choice is diameter $D=2a$ and $v$ is mean speed:

$$
\boxed{\mathrm{Re}_D=\frac{\rho\bar vD}{\eta}}.
$$

A pipe-flow transition to turbulence often occurs around a Reynolds number of order $10^3$, commonly quoted near $2000$–$2300$ for idealized experiments. The actual transition depends on disturbances, pipe roughness and inlet conditions. **There is no single universal critical Reynolds number for every flow geometry.**

One may estimate a geometry-dependent critical speed from

$$
\boxed{v_c\sim\frac{\mathrm{Re}_c\eta}{\rho L_c}}.
$$

Low Reynolds number means viscous effects dominate relative to inertia; high Reynolds number means inertia becomes more important, but does not by itself prove turbulent behavior in every physical configuration.

### Part IV: Key takeaways

- **Elasticity** concerns recoverable deformation; **modulus** measures resistance to a specified small strain.
- Elastic energy in a Hookean solid is obtained by integrating force over extension, or stress over strain.
- Liquid interfaces require surface energy. A spherical drop has pressure jump $2S/R$, and a two-sided soap bubble has $4S/R$.
- Capillary rise results from the vertical component of surface-tension force and depends on contact angle.
- Viscosity resists velocity gradients. Poiseuille's law describes slow laminar pipe flow; Stokes' law describes low-Re drag around a sphere.
- Verify Reynolds number and geometry before applying any viscous-flow formula.

---
# Consolidated Formula Sheet

This section is a **revision index**, not a replacement for the derivations. Every expression depends on the corresponding physical model. Before applying an equation, identify the system, coordinate orientation, relevant geometry and approximation.

## Gravitation (Chapter 11)

| Topic | Main result | Applicability |
|---|---|---|
| Newtonian attraction | $F=Gm_1m_2/r^2$ | Point masses or suitable exterior spherical symmetry |
| Gravitational potential energy | $U=-GMm/r$ | Point masses, zero at infinity |
| Point-source potential | $V=-GM/r$ | Outside a spherical source |
| Field-potential relation | $\vec g=-\vec\nabla V$ | Conservative static gravitational field |
| Spherical-shell interior | $\vec g=0$, $V=-GM/R$ | Uniform thin shell |
| Solid-sphere interior | $g(r)=GMr/R^3$ inward | Uniform density |
| Gravity at altitude | $g(h)=g_0[R/(R+h)]^2$ | Spherical source |
| Gravity at depth | $g(d)=g_0(1-d/R)$ | Uniform-density source |
| Circular orbital speed | $v=\sqrt{GM/r}$ | Circular orbit, $M\gg m$ |
| Circular orbital period | $T=2\pi\sqrt{r^3/(GM)}$ | Circular orbit, $M\gg m$ |
| Circular orbital energy | $E=-GMm/(2r)$ | Newtonian circular orbit |
| Kepler's third law | $T^2=4\pi^2a^3/[G(M+m)]$ | Isolated Newtonian two-body orbit |
| Escape speed | $v_e=\sqrt{2GM/R}$ | Ideal initial launch at radius $R$ |
| Uniform-sphere binding energy | $E_b=3GM^2/(5R)$ | Uniform sphere assembled quasistatically |
| Schwarzschild radius | $R_s=2GM/c^2$ | Relativistic result; Newtonian argument is heuristic only |

## Simple Harmonic Motion (Chapter 12)

**Linear oscillator and kinematics:**

$$
\boxed{\ddot x+\omega^2x=0},\quad
\boxed{x=A\cos(\omega t+\phi)},\quad
\boxed{v=-A\omega\sin(\omega t+\phi)}.
$$

$$
\boxed{a=-\omega^2x},\quad
\boxed{\omega=2\pi f=\frac{2\pi}{T}},\quad
\boxed{v^2=\omega^2(A^2-x^2)}.
$$

$$
\boxed{E=\frac12mv^2+\frac12kx^2=\frac12kA^2}.
$$

| Oscillator | Angular frequency | Small-amplitude period |
|---|---|---|
| Horizontal or vertical linear spring | $\sqrt{k/m}$ | $2\pi\sqrt{m/k}$ |
| Simple pendulum | $\sqrt{g/l}$ | $2\pi\sqrt{l/g}$ |
| Physical pendulum | $\sqrt{mgd/I_O}$ | $2\pi\sqrt{I_O/(mgd)}$ |
| Torsional pendulum | $\sqrt{\kappa/I}$ | $2\pi\sqrt{I/\kappa}$ |

**Composition and nonideal oscillators:**

$$
\boxed{A_{\mathrm{resultant}}=\sqrt{A_1^2+A_2^2+2A_1A_2\cos\delta}}
\quad\text{(equal frequency, same axis)}.
$$

$$
\boxed{\omega_d=\sqrt{\frac{k}{m}-\left(\frac{b}{2m}\right)^2}}
\quad\text{(underdamped linear oscillator)}.
$$

$$
\boxed{X(\Omega)=\frac{F_0}{\sqrt{(k-m\Omega^2)^2+b^2\Omega^2}}}
\quad\text{(steady forced response)}.
$$

## Fluid Mechanics (Chapter 13)

$$
\boxed{\frac{dP}{dz}=-\rho g},\qquad
\boxed{P=P_0+\rho gh}\quad\text{(constant-density hydrostatics)}.
$$

$$
\boxed{F_B=\rho_f gV_{\mathrm{displaced}}},\qquad
\boxed{\vec\nabla P=\rho(\vec g-\vec a_0)}\quad\text{(accelerating-frame hydrostatics)}.
$$

$$
\boxed{\rho_1A_1v_1=\rho_2A_2v_2},\qquad
\boxed{A_1v_1=A_2v_2}\quad\text{(steady incompressible flow)}.
$$

$$
\boxed{P+\frac12\rho v^2+\rho gz=\mathrm{constant}}
\quad\text{(steady, inviscid, incompressible, along streamline)}.
$$

$$
\boxed{v_{\mathrm{exit}}\simeq\sqrt{2gh}},\qquad
\boxed{v_{\mathrm{Pitot}}=\sqrt{\frac{2\Delta P}{\rho}}}.
$$

## Mechanical Properties of Matter (Chapter 14)

| Property | Equation | Assumptions and notes |
|---|---|---|
| Axial stress | $\sigma=F/A$ | Uniform axial load |
| Longitudinal strain | $\varepsilon=\Delta L/L_0$ | Small-deformation measure |
| Young's modulus | $Y=FL_0/(A\Delta L)$ | Linear uniaxial elasticity |
| Wire elongation | $\Delta L=FL_0/(AY)$ | Hookean, uniform wire |
| Shear modulus | $G_s=\tau/\gamma$ | Linear elastic shear |
| Bulk modulus | $B=-\Delta P/(\Delta V/V)$ | Small volume changes |
| Poisson's ratio | $\nu=-\varepsilon_\perp/\varepsilon_\parallel$ | Axial loading |
| Elastic energy density | $u=\sigma\varepsilon/2$ | Uniaxial linear elasticity |
| Soap-film force | $F=2Sl$ | Two free surfaces |
| Drop pressure jump | $\Delta P=2S/R$ | One spherical interface |
| Soap-bubble pressure jump | $\Delta P=4S/R$ | Two spherical interfaces |
| Capillary height | $h=2S\cos\theta/(\rho gr)$ | Static narrow tube |
| Newtonian shear stress | $\tau=\eta\,dv/dy$ | Newtonian fluid |
| Poiseuille flow | $Q=\pi a^4\Delta P/(8\eta L)$ | Laminar, fully developed, straight round tube |
| Stokes drag | $F_D=6\pi\eta rv$ | Low Reynolds number, distant walls |
| Stokes terminal speed | $v_t=2r^2(\rho_s-\rho_f)g/(9\eta)$ | Sphere, creeping flow |
| Reynolds number | $\mathrm{Re}=\rho vL_c/\eta$ | Choose flow-specific characteristic length |

**Dimensional cross-checks:**

$$
\boxed{[Y]=[G_s]=[B]=ML^{-1}T^{-2}},
$$

$$
\boxed{[S]=MT^{-2}},\qquad
\boxed{[\eta]=ML^{-1}T^{-1}},\qquad
\boxed{[\mathrm{Re}]=1}.
$$

---

# Integrated Worked Examples

These independently constructed examples apply the chapter theory without copying HCV's exercise statements. The methods and checks matter more than memorizing the final values.

## Example A: Gravity far above Earth

**Problem.** At what height above the surface of a spherical Earth does gravitational acceleration become one-quarter of its surface value?

Use $g(h)=g_0R^2/(R+h)^2$:

$$
\frac{g(h)}{g_0}=\frac{R^2}{(R+h)^2}=\frac14.
$$

Taking the positive square root,

$$
\frac{R}{R+h}=\frac12\quad\Longrightarrow\quad\boxed{h=R}.
$$

**Check:** the distance from Earth's center has doubled to $2R$, so the inverse-square gravitational field is quartered. The height is **one Earth radius**, not one-quarter of a radius.

## Example B: Gravitational field at a ring's axis

**Problem.** A uniform thin ring of radius $a$ and mass $M$ produces field magnitude

$$
g(z)=\frac{GMz}{(a^2+z^2)^{3/2}},\qquad z\ge0.
$$

Find where the axial field magnitude is maximum.

Differentiate:

$$
\frac{dg}{dz}=GM\left[(a^2+z^2)^{-3/2}-3z^2(a^2+z^2)^{-5/2}\right].
$$

Setting the numerator to zero gives

$$
a^2+z^2-3z^2=0
\quad\Longrightarrow\quad
\boxed{z=\frac{a}{\sqrt2}}.
$$

At $z=0$, the field vanishes by symmetry; at large $z$ it also approaches zero. The interior critical point is the maximum.

## Example C: Start an SHM from position and velocity

**Problem.** A mass-spring oscillator has angular frequency $\omega=5\,\mathrm{rad\,s^{-1}}$. At $t=0$, its displacement is $x_0=0.030\,\mathrm m$ and velocity is $v_0=-0.20\,\mathrm{m\,s^{-1}}$. Find amplitude, phase and period using $x=A\cos(\omega t+\phi)$.

First,

$$
A=\sqrt{x_0^2+(v_0/\omega)^2}
=\sqrt{0.030^2+(-0.040)^2}.
$$

Therefore

$$
\boxed{A=0.050\,\mathrm m}.
$$

At $t=0$, $\cos\phi=x_0/A=0.6$. Since $v_0=-A\omega\sin\phi<0$, we need $\sin\phi=0.8>0$, so $\phi$ lies in the first quadrant:

$$
\boxed{\phi\simeq0.927\,\mathrm{rad}},\qquad
\boxed{T=\frac{2\pi}{5}\simeq1.26\,\mathrm s}.
$$

**Lesson:** both initial displacement and initial velocity are needed to determine phase unambiguously.

## Example D: Uniform rod as a physical pendulum

**Problem.** A thin uniform rod of length $L=0.90\,\mathrm m$ pivots freely about one end. Find its small-oscillation period with $g=9.81\,\mathrm{m\,s^{-2}}$.

For a uniform rod about the endpoint, $I_O=mL^2/3$, and its center of mass is at $d=L/2$. Hence

$$
T=2\pi\sqrt{\frac{I_O}{mgd}}
=2\pi\sqrt{\frac{mL^2/3}{mgL/2}}
=2\pi\sqrt{\frac{2L}{3g}}.
$$

Numerically,

$$
\boxed{T\simeq1.55\,\mathrm s}.
$$

A point mass at the rod's end would have a different moment of inertia and therefore a different period.

## Example E: A floating block

**Problem.** A uniform block of density $600\,\mathrm{kg\,m^{-3}}$ floats in water of density $1000\,\mathrm{kg\,m^{-3}}$. What fraction of its volume lies below the waterline?

At floating equilibrium, weight equals buoyancy:

$$
\rho_bVg=\rho_fV_{\mathrm{submerged}}g.
$$

Therefore

$$
\boxed{\frac{V_{\mathrm{submerged}}}{V}=\frac{600}{1000}=0.60}.
$$

The result means **60% of its volume** is immersed, not that 60% of its mass is below the surface in any independent sense. Its orientation depends on geometry and stability.

## Example F: Pressure and speed in a constriction

**Problem.** Water of density $1000\,\mathrm{kg\,m^{-3}}$ flows steadily through a horizontal ideal tube. The inlet area is four times the outlet area. If inlet speed is $2\,\mathrm{m\,s^{-1}}$, find outlet speed and the ideal pressure difference.

Continuity yields

$$
A_1v_1=A_2v_2
\quad\Longrightarrow\quad
\boxed{v_2=4v_1=8\,\mathrm{m\,s^{-1}}}.
$$

Bernoulli at equal elevations gives

$$
P_1-P_2=\frac12\rho(v_2^2-v_1^2)
=\frac12(1000)(64-4).
$$

Thus

$$
\boxed{P_1-P_2=3.0\times10^4\,\mathrm{Pa}=30\,\mathrm{kPa}}.
$$

The pressure *drops* toward the constriction in this ideal model. A real tube includes energy losses, requiring additional pressure head.

## Example G: Elongation of a wire

**Problem.** A uniform wire has length $1.0\,\mathrm m$, cross-sectional area $1.0\,\mathrm{mm^2}$ and Young's modulus $2.0\times10^{11}\,\mathrm{Pa}$. Find extension under a steady $100\,\mathrm N$ tensile load within the linear elastic range.

Convert area:

$$
A=1.0\,\mathrm{mm^2}=1.0\times10^{-6}\,\mathrm{m^2}.
$$

Use

$$
\Delta L=\frac{FL}{AY}
=\frac{100\times1.0}{(10^{-6})(2.0\times10^{11})}.
$$

Hence

$$
\boxed{\Delta L=5.0\times10^{-4}\,\mathrm m=0.50\,\mathrm{mm}}.
$$

The result is conditional on Hookean behavior and the stated uniform area.

## Example H: Pressure jump across a soap bubble

**Problem.** A thin soap bubble of radius $2.0\,\mathrm{mm}$ has surface tension $S=0.030\,\mathrm{N\,m^{-1}}$. What is its ideal excess internal pressure?

For a two-interface soap film,

$$
\Delta P=\frac{4S}{R}=\frac{4(0.030)}{2.0\times10^{-3}},
$$

so

$$
\boxed{\Delta P=60\,\mathrm{Pa}}.
$$

A **single-interface** liquid drop of the same radius and surface tension would have only $30\,\mathrm{Pa}$ of excess pressure.

## Example I: Capillary rise of water

**Problem.** Water with surface tension $S=0.072\,\mathrm{N\,m^{-1}}$ rises inside a clean, perfectly wetting capillary of radius $r=0.50\,\mathrm{mm}$. Approximate the rise using $\rho=1000\,\mathrm{kg\,m^{-3}}$ and $g=9.81\,\mathrm{m\,s^{-2}}$.

For $\theta\simeq0$, $\cos\theta\simeq1$:

$$
h=\frac{2S\cos\theta}{\rho gr}
\simeq\frac{2(0.072)}{1000(9.81)(0.50\times10^{-3})}.
$$

Therefore

$$
\boxed{h\simeq0.0294\,\mathrm m\simeq2.94\,\mathrm{cm}}.
$$

The radius must be entered in meters; using diameter in place of radius produces a factor-of-two error.

## Example J: Stokes terminal speed and regime check

**Problem.** A small sphere has radius $r=1.0\,\mathrm{mm}$ and density $3000\,\mathrm{kg\,m^{-3}}$. It falls through a liquid with density $1000\,\mathrm{kg\,m^{-3}}$ and dynamic viscosity $1.0\,\mathrm{Pa\,s}$. Estimate terminal speed and check the particle Reynolds number using diameter as length.

Stokes terminal-speed formula gives

$$
v_t=\frac{2r^2(\rho_s-\rho_f)g}{9\eta}
=\frac{2(10^{-3})^2(2000)(9.81)}{9(1.0)}.
$$

Thus

$$
\boxed{v_t\simeq4.36\times10^{-3}\,\mathrm{m\,s^{-1}}}.
$$

Check whether the slow-flow hypothesis is self-consistent:

$$
\mathrm{Re}=\frac{\rho_fv_t(2r)}{\eta}
=\frac{1000(4.36\times10^{-3})(2\times10^{-3})}{1.0}.
$$

Hence

$$
\boxed{\mathrm{Re}\simeq8.7\times10^{-3}\ll1}.
$$

A creeping-flow approximation is plausible. Rechecking the nondimensional regime is part of the solution, not an optional afterthought.

---

# Common Misconceptions and Diagnostic Questions

| Misconception | Correct principle |
|---|---|
| "The gravitational potential must be zero where the gravitational field is zero." | Inside a spherical shell, field is zero but potential is a negative constant. |
| "A satellite floats because Earth's gravitational pull is negligible." | An orbiting satellite and its occupants are in approximately common free fall. |
| "An object needs continuous thrust to maintain a circular orbit." | Gravity itself continuously changes velocity direction. Real satellites need maneuvers only for disturbances, transfers or maintenance. |
| "Objects in a higher circular orbit travel faster." | Circular orbital speed scales as $r^{-1/2}$ for a fixed central mass. |
| "Escape speed is the same as speed for any possible trajectory to space." | It is an ideal minimum **initial unpowered** speed from a given radius. |
| "Every restoring force produces SHM." | Exact SHM requires restoring acceleration proportional to signed displacement. |
| "Acceleration is zero at a spring oscillator's extreme." | It has maximum magnitude there; velocity is zero. |
| "A simple pendulum is perfectly harmonic at every angle." | Its exact restoring torque contains $\sin\theta$; small-angle linearization produces approximate SHM. |
| "Resonance always occurs at precisely the undamped natural frequency." | Damping shifts the displacement-amplitude peak, and different response measures have different peak conditions. |
| "Pressure acts only downward inside a fluid." | Hydrostatic pressure acts normal to any small oriented surface element. |
| "A floating body displaces its own volume of liquid." | It displaces a volume whose **weight** equals the body's weight. |
| "Incompressibility means fluid speed cannot change." | It constrains density, not velocity; continuity can require acceleration through a constriction. |
| "Steady flow means fluid acceleration is zero." | Convective acceleration can be nonzero in a steady but spatially varying flow. |
| "Bernoulli applies to every high-speed flow." | Its simple form relies on restrictive steady, inviscid and incompressible streamline assumptions. |
| "Steel is less elastic than rubber because steel stretches less." | Modulus, elastic recovery and strain-to-failure measure different material behaviors. |
| "Young's modulus equals force divided by extension." | It is stress divided by strain; geometry matters. |
| "A soap bubble and liquid drop both have $2S/R$ pressure jump." | A thin soap bubble has two interfaces, giving $4S/R$. |
| "Capillary action always makes the liquid rise." | Contact angle determines whether the liquid rises or is depressed. |
| "Poiseuille flow rate doubles when tube radius doubles." | Under its assumptions, flow rate varies as radius to the fourth power. |
| "Stokes drag works for any size and speed of sphere." | It requires creeping-flow conditions and appropriate boundaries. |
| "Reynolds number alone guarantees turbulence." | Transition depends on geometry, disturbances and boundary conditions as well as Reynolds number. |

---

# Active-Recall Checkpoints

Attempt these from memory, then verify the derivations above. A convincing response must explain the **assumptions**, not just reproduce the formula.

### Chapter 11: Gravitation

1. Explain what Newton unified by placing terrestrial and celestial motion under the same law.
2. Derive the dimensions of $G$ from the gravitational force equation.
3. Why do the forces on two gravitating masses have equal magnitude although their accelerations differ?
4. Describe how a torsion balance can be used to measure $G$ and which quantities must be measured.
5. Derive $U=-GMm/r$ using the zero-at-infinity convention.
6. Explain why potential is negative outside an isolated positive mass.
7. How does gravitational potential differ from gravitational potential energy?
8. Derive gravitational potential on the axis of a uniform circular ring.
9. Distinguish potential and field inside a uniformly massive thin spherical shell.
10. Explain the linear variation of field strength inside a uniform solid sphere.
11. Obtain $\vec g=-\vec\nabla V$ from the work done by a conservative force.
12. Derive the small-altitude approximation of $g(h)$ and state its range of applicability.
13. Explain the dependence of apparent weight on Earth's rotation and latitude.
14. Derive circular orbital speed, period and total orbital energy from Newton's laws.
15. Derive Kepler's equal-areas law from conservation of angular momentum.
16. Why does orbital speed decrease when circular orbit radius increases?
17. Describe the conditions for a geostationary orbit.
18. Why is a spacecraft occupant apparently weightless while Earth's gravitational field remains nonzero?
19. Derive the ideal escape speed and distinguish it from the requirements of a powered rocket.
20. Derive the gravitational binding energy of a uniform sphere by assembling shells.
21. Explain what the Newtonian escape-speed analogy for a black hole fails to capture.
22. Why is equality of inertial and gravitational mass significant?

### Chapter 12: Simple Harmonic Motion

23. What distinguishes exact SHM from arbitrary oscillatory motion?
24. Derive the general sinusoidal solution from $m\ddot x=-kx$.
25. Recover SHM amplitude from arbitrary initial position and velocity.
26. Derive the speed-position relation $v^2=\omega^2(A^2-x^2)$.
27. Explain which of speed, acceleration and restoring force is greatest at equilibrium and at the turning points.
28. Show how the projection of uniform circular motion generates SHM.
29. Derive the total mechanical energy and its division into kinetic and potential forms.
30. Why does gravitational acceleration not alter the period of an ideal vertical mass-spring oscillator?
31. Derive the small-angle period of a simple pendulum, explicitly identifying the approximation.
32. Distinguish a simple pendulum, a physical pendulum and a torsional pendulum.
33. Derive the period of a uniform rod oscillating about a point at its end.
34. Derive the amplitude of two same-frequency SHMs using their phase difference.
35. Under what conditions does two-dimensional SHM trace a circle rather than an ellipse or straight line?
36. Explain beats and distinguish beat frequency from the two carrier frequencies.
37. Derive the energy-dissipation rate for a linearly damped oscillator.
38. Distinguish underdamped, critically damped and overdamped motion.
39. Explain why a driven oscillator eventually follows the driving frequency.
40. State when maximum steady displacement occurs and why damping is needed for a finite response.

### Chapter 13: Fluid Mechanics

41. Why can a fluid be in mechanical equilibrium under pressure but not under a sustained static shear stress?
42. Derive hydrostatic pressure variation from the forces acting on a thin fluid slab.
43. Explain the meaning of gauge pressure and absolute pressure.
44. Use Pascal's law and volume conservation to prove that a hydraulic press does not amplify energy.
45. Derive a barometer's pressure reading from a column of liquid.
46. Derive Archimedes' law by comparing an immersed object with the fluid it displaces.
47. What determines the submerged volume fraction of a floating solid?
48. Explain how a fluid free surface tilts in a horizontally accelerating tank.
49. Distinguish a streamline, a pathline, a steady flow and a turbulent flow.
50. What is the meaning of convective acceleration in a steady flow?
51. Derive the steady one-dimensional continuity equation using mass conservation.
52. When is $A_1v_1=A_2v_2$ valid and when must density be included?
53. Derive Bernoulli's equation from pressure work and energy change of a fluid element.
54. Explain the roles of pressure head, velocity head and elevation head.
55. Obtain Torricelli's law and identify the approximations involved.
56. Explain how a Venturi meter obtains information about speed from pressure variation.
57. Describe at least three situations where direct use of ideal Bernoulli theory would be misleading.

### Chapter 14: Some Mechanical Properties of Matter

58. Explain how an intermolecular potential minimum produces an approximate restoring force for small deformations.
59. Distinguish stress, strain, stiffness, strength, elasticity and plasticity.
60. Derive Young's modulus for a stretched uniform wire and explain the role of length and cross section.
61. Define shear modulus, bulk modulus, compressibility and Poisson's ratio.
62. Sketch a qualitative ductile-metal stress-strain curve and label its important regions.
63. How does hysteresis appear in a loading-unloading experiment, and what does the loop area represent?
64. Derive the elastic energy stored in a Hookean wire and its energy density.
65. Outline a laboratory method to measure Young's modulus and identify the main sources of error.
66. Why does a soap film pull a sliding wire with force $2Sl$ instead of $Sl$?
67. Derive the relationship between surface tension and surface energy.
68. Why does breaking a large droplet into many small droplets require energy?
69. Derive the excess pressure inside a liquid drop from a change in radius.
70. Explain the factor-of-two difference between a soap bubble and a liquid droplet.
71. Define contact angle precisely and explain how it affects capillary rise or depression.
72. Derive the capillary rise formula from the balance of vertical forces.
73. Explain dynamic viscosity using shear stress and fluid velocity gradient.
74. Derive the parabolic velocity profile and flow rate in Poiseuille flow.
75. Why does a small change in tube radius dramatically change Poiseuille flow rate?
76. State the low-Reynolds-number conditions of Stokes' law and explain its drag direction.
77. Derive terminal speed of a falling sphere including weight, buoyancy and viscous drag.
78. Describe how a falling-sphere viscosity experiment can fail if the test vessel is too narrow.
79. Form the Reynolds number from density, velocity, characteristic length and viscosity; show it is dimensionless.
80. Explain why critical Reynolds number is not the same for all geometries.

---

## Source and scope

- **Primary source:** H. C. Verma, *Concepts of Physics*, Volume 1.
- **Chapter 11:** *Gravitation*, textbook pp. **203–228** (PDF pp. **213–238**).
- **Chapter 12:** *Simple Harmonic Motion*, textbook pp. **229–257** (PDF pp. **239–267**).
- **Chapter 13:** *Fluid Mechanics*, textbook pp. **258–276** (PDF pp. **268–286**).
- **Chapter 14:** *Some Mechanical Properties of Matter*, textbook pp. **277–302** (PDF pp. **287–312**).
- All **62 HCV theory-section headings**, **11.1–14.20**, are represented in their original order. The conceptual explanations, mathematical treatments, worked examples and revision questions are independently authored and condensed rather than copied verbatim.
- **Scope distinction:** vector-calculus formulations, the illustrative modified-gravity potential, elasticity-constant identities, uncertainty propagation, and selected engineering qualifications are explicitly supplementary context. HCV's introductory sequence and physical level remain the organizing basis.
- **Previous unit:** *Mechanics I*, Chapters 3–10.
- **Next unit:** Chapters 15–17, *Waves*.
