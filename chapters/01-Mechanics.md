# Unit 01: Mechanics-I

**Rest and Motion: Kinematics → Rotational Mechanics**  
*Original revision notes following Chapters 3–10 of H. C. Verma, Concepts of Physics, Volume 1*

> **Purpose.** Build a continuous account of classical mechanics: describe motion, identify interactions, apply Newton's laws, handle friction and curved trajectories, use energy and momentum, and finally analyze the rotation of extended bodies. These are independently written study notes, not a transcription of the textbook. Section numbers follow HCV for cross-referencing.
>
> **Notation.** Display equations use `$$ ... $$` for GitHub Markdown math rendering. Vector quantities carry arrows; unit vectors carry hats. SI units are assumed unless stated otherwise. State the reference frame, system boundary, and sign convention before solving a problem.

## Roadmap

| Part | HCV chapter | Focus |
|---|---|---|
| **I** | **3. Rest and Motion: Kinematics** | Position, velocity, acceleration, projectiles and frames |
| **II** | **4. The Forces** | Fundamental interactions and their everyday manifestations |
| **III** | **5. Newton's Laws of Motion** | Inertia, free-body diagrams, dynamics, action-reaction and pseudo forces |
| **IV** | **6. Friction** | Contact-force components, static/kinetic friction and measurements |
| **V** | **7. Circular Motion** | Angular variables, radial acceleration, turns and noninertial descriptions |
| **VI** | **8. Work and Energy** | Work-energy theorem, conservative forces and mechanical energy |
| **VII** | **9. Centre of Mass, Linear Momentum, Collision** | Systems, impulses, rockets and collision mechanics |
| **VIII** | **10. Rotational Mechanics** | Torque, inertia, angular momentum, rolling and coupled translation-rotation |

**Learning sequence**

```text
Reference frame → Position / velocity / acceleration
                            |
                            v
                 Identify physical forces
                            |
                            v
                Free-body diagram + ΣF = ma
                      /             \
                     v               v
           Friction / constraints   Circular paths
                     \               /
                      v             v
                   Work and energy
                            |
                            v
                Momentum and collisions
                            |
                            v
               Torque and rigid-body rotation
                            |
                            v
                       Rolling motion
```

---

# Part I: Rest and Motion: Kinematics

Kinematics describes *how* bodies move without first asking *why* they move. Dynamics, beginning in Chapter 5, supplies the forces responsible for that motion.

## 3.1 Rest and Motion

A body's position and motion have meaning only relative to a **chosen frame of reference**. A book resting on a train seat is at rest relative to the carriage but moves relative to the track. Neither description contradicts the other.

Specify an origin, axes and a clock. A particle's position can be represented by

$$
\vec r(t)=x(t)\hat i+y(t)\hat j+z(t)\hat k.
$$

If all three coordinates remain constant, the particle is at rest in that frame; otherwise it is in motion. The choice of frame simplifies the problem, but not every frame permits Newton's laws to be used without modifications.

**Useful idealization:** a *particle* is a body whose size and orientation can be neglected for the question being studied. The same car can be modeled as a particle when studying its journey and as a rigid body when studying a skid or rollover.

## 3.2 Distance and Displacement

**Distance** is the total length of the actual path traversed. It is a nonnegative scalar. **Displacement** is the directed change between final and initial positions:

$$
\Delta\vec r=\vec r_f-\vec r_i.
$$

In Cartesian coordinates,

$$
|\Delta\vec r|=\sqrt{(x_f-x_i)^2+(y_f-y_i)^2+(z_f-z_i)^2}.
$$

Distance depends on the path; displacement depends only on the endpoints. Thus

$$
\boxed{\text{Distance travelled}\ge |\text{displacement}|.}
$$

**Example:** Walking around a semicircle of radius `R` gives distance `πR` but displacement magnitude `2R`. Walking a full circle produces a positive distance `2πR` and zero net displacement.

## 3.3 Average Speed and Instantaneous Speed

The **average speed** over an interval is total path length divided by elapsed time:

$$
\boxed{v_{\mathrm{speed,avg}}=\frac{s_{\mathrm{total}}}{\Delta t}.}
$$

For the cumulative distance function `s(t)`, the **instantaneous speed** is

$$
\boxed{v_{\mathrm{speed}}=\lim_{\Delta t\to0}\frac{\Delta s}{\Delta t}=\frac{ds}{dt}.}
$$

A distance-time graph has instantaneous slope equal to speed, provided `s` is cumulative path length. The average speed of an outward-and-return journey is generally **not** the arithmetic average of the outward and return speeds unless the corresponding times are equal.

**Worked example:** Travel equal distances `d` at speeds `v_1` and `v_2`. The total time is `d/v_1+d/v_2`, so

$$
\boxed{v_{\mathrm{avg}}=\frac{2d}{d/v_1+d/v_2}=\frac{2v_1v_2}{v_1+v_2}.}
$$

## 3.4 Average Velocity and Instantaneous Velocity

Velocity is a vector; its average depends on **displacement**, not distance:

$$
\boxed{\vec v_{\mathrm{avg}}=\frac{\Delta\vec r}{\Delta t}.}
$$

The instantaneous velocity is

$$
\boxed{\vec v=\lim_{\Delta t\to0}\frac{\Delta\vec r}{\Delta t}=\frac{d\vec r}{dt}.}
$$

Its Cartesian form is

$$
\vec v=\frac{dx}{dt}\hat i+\frac{dy}{dt}\hat j+\frac{dz}{dt}\hat k,
\qquad
\text{speed}=|\vec v|.
$$

The velocity vector is tangent to a smooth trajectory at the particle's instantaneous position. Its magnitude equals instantaneous speed, but *average speed* and the *magnitude of average velocity* need not agree.

**Example:** On a closed lap, net displacement and average velocity are zero, although average speed is positive.

## 3.5 Average Acceleration and Instantaneous Acceleration

Acceleration measures how velocity changes with time:

$$
\boxed{\vec a_{\mathrm{avg}}=\frac{\vec v_f-\vec v_i}{t_f-t_i},
\qquad
\vec a=\frac{d\vec v}{dt}=\frac{d^2\vec r}{dt^2}.}
$$

Acceleration is not simply the rate of change of **speed**. A particle in uniform circular motion has constant speed but a continuously changing velocity direction; hence its acceleration is nonzero.

For one-dimensional signed motion, velocity and acceleration with the same sign imply increasing speed; opposite signs imply decreasing speed. A negative acceleration does **not** automatically mean slowing down.

## 3.6 Motion in a Straight Line

Take the `x` axis along the line of motion. In general,

$$
 v_x=\frac{dx}{dt},\qquad a_x=\frac{dv_x}{dt}=\frac{d^2x}{dt^2}.
$$

### Constant-acceleration equations

If acceleration `a` is constant and the initial velocity is `u`, integration gives

$$
\frac{dv}{dt}=a
\quad\Longrightarrow\quad
\boxed{v=u+at}.
$$

A second integration gives

$$
\boxed{x-x_0=ut+\frac12at^2}.
$$

Eliminate time using

$$
 a=\frac{dv}{dt}=\frac{dv}{dx}\frac{dx}{dt}=v\frac{dv}{dx}.
$$

Then

$$
\int_u^v v\,dv=\int_{x_0}^x a\,dx
\quad\Longrightarrow\quad
\boxed{v^2=u^2+2a(x-x_0)}.
$$

A fourth useful expression, valid for constant acceleration, is

$$
\boxed{x-x_0=\frac{u+v}{2}\,t}.
$$

These are **signed component equations**; preserve the chosen positive direction. They do not apply in this simple form if acceleration varies with time.

### Vertical motion under gravity

Take positive `y` upward, with gravitational acceleration `a_y=-g` near Earth's surface:

$$
 v_y=u_y-gt,
\qquad
 y-y_0=u_yt-\frac12gt^2,
\qquad
 v_y^2=u_y^2-2g(y-y_0).
$$

For an upward throw from `y_0`, the velocity is zero momentarily at maximum height:

$$
\boxed{t_{\mathrm{up}}=\frac{u_y}{g},
\qquad H=\frac{u_y^2}{2g}.}
$$

The downward acceleration persists at the top even while the instantaneous vertical velocity vanishes.

### Interpreting graphs

| Graph | Slope | Signed area under curve |
|---|---|---|
| Position vs. time | Velocity | Not a standard kinematic quantity |
| Velocity vs. time | Acceleration | Displacement |
| Acceleration vs. time | Rate of change of acceleration | Change in velocity |
| Speed vs. time | Rate of change of speed | Distance travelled |

For a velocity-time graph, portions below the time axis contribute **negative displacement**, not negative distance.

### General variable acceleration

When `a` is not constant, revert to calculus:

$$
 v(t)=v(t_0)+\int_{t_0}^{t}a(\tau)\,d\tau,
$$

$$
 x(t)=x(t_0)+\int_{t_0}^{t}v(\tau)\,d\tau.
$$

## 3.7 Motion in a Plane

For two-dimensional motion,

$$
\vec r=x\hat i+y\hat j,
\qquad
\vec v=v_x\hat i+v_y\hat j,
\qquad
\vec a=a_x\hat i+a_y\hat j.
$$

Analyze each component separately. If acceleration is **constant as a vector**, then

$$
\boxed{\vec v=\vec u+\vec at},
$$

$$
\boxed{\vec r=\vec r_0+\vec ut+\frac12\vec at^2}.
$$

Equivalently, apply the one-dimensional constant-acceleration equations independently along `x` and `y`. The particle follows a straight path only under appropriate alignment of velocity and acceleration; otherwise its path curves.

## 3.8 Projectile Motion

A projectile near Earth's surface, with negligible air resistance and constant `g`, has zero horizontal acceleration and downward vertical acceleration. Let initial speed be `u`, launch angle `θ` above horizontal, and initial coordinates `(0,0)`:

$$
 u_x=u\cos\theta,\qquad u_y=u\sin\theta.
$$

Its parametric motion is

$$
\boxed{x=u\cos\theta\,t},
\qquad
\boxed{y=u\sin\theta\,t-\frac12gt^2}.
$$

Thus

$$
 v_x=u\cos\theta,
\qquad
 v_y=u\sin\theta-gt.
$$

Eliminate `t` to find the trajectory:

$$
\boxed{y=x\tan\theta-\frac{gx^2}{2u^2\cos^2\theta}}.
$$

The path is parabolic under these assumptions.

### Launch and landing at equal heights

The nonzero time for return to launch height is

$$
\boxed{T=\frac{2u\sin\theta}{g}.}
$$

At maximum height `v_y=0`:

$$
\boxed{H=\frac{u^2\sin^2\theta}{2g}}.
$$

Horizontal range is

$$
\boxed{R=u\cos\theta\,T=\frac{u^2\sin2\theta}{g}}.
$$

Consequences: complementary angles have equal ranges for fixed speed and equal launch/landing heights; the ideal maximum range occurs at `45°`. These results are not generally valid for unequal heights, appreciable aerodynamic drag, or spatially varying gravity.

### Launch from an elevated position

With initial height `h` above the landing level,

$$
0=h+u\sin\theta\,t-\frac12gt^2.
$$

The physical positive root is

$$
\boxed{t_{\mathrm{flight}}=\frac{u\sin\theta+\sqrt{u^2\sin^2\theta+2gh}}{g}},
$$

and horizontal distance is `u cosθ` multiplied by that flight time. Do not use the equal-height range formula here.

**Worked example:** A ball leaves ground at `20 m/s`, `30°` above horizontal with `g=10 m/s²`:

$$
T=\frac{2(20)(1/2)}{10}=2\,\mathrm{s},
\quad
H=\frac{(20)^2(1/2)^2}{2(10)}=5\,\mathrm{m},
$$

$$
R=\frac{(20)^2\sin60^\circ}{10}
=20\sqrt3\,\mathrm{m}\approx34.6\,\mathrm{m}.
$$

## 3.9 Change of Frame

For two reference frames `S` and `S′`, where the origin of `S′` is at position `\vec R(t)` relative to `S` and axes remain parallel,

$$
\boxed{\vec r_{P/S}=\vec R+\vec r_{P/S'}}.
$$

Differentiate:

$$
\boxed{\vec v_{P/S}=\vec V_{S'/S}+\vec v_{P/S'}},
$$

$$
\boxed{\vec a_{P/S}=\vec A_{S'/S}+\vec a_{P/S'}}.
$$

Thus relative velocity of bodies `A` and `B` is

$$
\boxed{\vec v_{A/B}=\vec v_{A/S}-\vec v_{B/S}}.
$$

When the two frames have constant relative velocity, their measured accelerations agree. An accelerating frame needs special treatment (Chapter 5); rotating frames require additional terms and are outside this simple translation formula.

**Worked example:** A swimmer heads directly across a river with water-relative velocity `3 m/s` while the current is `4 m/s` downstream. Relative to the bank,

$$
\vec v=(4\hat i+3\hat j)\,\mathrm{m/s},
\qquad |\vec v|=5\,\mathrm{m/s}.
$$

The swimmer's *heading* and *actual track* differ because velocities combine vectorially.

### Part I: Key takeaways

- Motion is always specified relative to a frame.
- **Distance/speed** are scalar; **displacement/velocity/acceleration** are vector quantities.
- Constant-acceleration formulas are special cases of derivative and integral relations.
- Projectile motion separates into independent horizontal and vertical components.
- A change of frame changes reported positions and velocities and may change accelerations if the frames accelerate relative to one another.

---

# Part II: The Forces

## 4.1 Introduction

A force is an **interaction** exerted by one body on another. Identify both the *agent* applying the force and the *object* receiving it. A force is a vector; concurrent forces add vectorially:

$$
\boxed{\vec F_{\mathrm{net}}=\sum_i\vec F_i}.
$$

The SI unit of force is the newton:

$$
1\,\mathrm{N}=1\,\mathrm{kg\,m\,s^{-2}}.
$$

Interactions involve pairs of equal and opposite forces on **different** bodies, developed formally in Chapter 5. HCV groups forces into gravitational, electromagnetic, nuclear and weak interactions.

## 4.2 Gravitational Force

Two point masses attract one another:

$$
\boxed{F=G\frac{m_1m_2}{r^2}},
$$

where `r` is their separation and approximately

$$
G=6.67\times10^{-11}\,\mathrm{N\,m^2\,kg^{-2}}.
$$

The force acts along the line joining the masses. For spherically symmetric masses whose distributions do not overlap, their gravitational interaction is the same as if their masses were concentrated at their centers.

Near Earth, writing Earth's mass as `M` and radius as `R_E`,

$$
g=\frac{GM}{R_E^2},
\qquad
\boxed{\vec F_g=m\vec g},
$$

with `g≈9.8 m/s²` directed toward Earth. The gravitational field `g` is not the universal constant `G`.

**Scale insight:** gravitational attraction between small everyday objects is extremely weak; gravity from an astronomical body is commonly the significant gravitational contribution.

## 4.3 Electromagnetic (EM) Force

Stationary charges obey Coulomb's inverse-square force law:

$$
\boxed{F=\frac{1}{4\pi\varepsilon_0}\frac{|q_1q_2|}{r^2}},
$$

$$
\frac{1}{4\pi\varepsilon_0}\approx9.0\times10^9\,\mathrm{N\,m^2\,C^{-2}}.
$$

Like charges repel and unlike charges attract. Charge and current interactions also produce magnetic effects. Electromagnetic interactions account for much of the binding and resistance observed in ordinary materials.

### Everyday manifestations of electromagnetic force

- **Normal contact force:** perpendicular component of the force between contacting surfaces. Its magnitude is determined by the *dynamics*, not automatically by `mg`.
- **Friction:** tangential component of contact force that resists slipping or its tendency.
- **Tension:** a taut string/rope transmits a pull along its local direction; an ideal flexible string does not push.
- **Elastic force:** deformed materials exert restoring forces. For an ideal linear spring along an axis,

$$
\boxed{F_x=-kx}.
$$

The minus sign means restoring force opposes displacement from the natural equilibrium position. Such macroscopic laws summarize many underlying electromagnetic interactions between constituent particles.

## 4.4 Nuclear Forces

The strong nuclear interaction binds nucleons in the atomic nucleus despite electrostatic proton-proton repulsion. HCV describes the effective **nuclear force** as very strong but short-ranged, significant over nuclear distances rather than ordinary macroscopic separations.

**Important distinction:** the attractive nuclear force between nucleons is a residual manifestation of the strong interaction; it is not described by a universal Coulomb-style inverse-square law at these separations.

## 4.5 Weak Forces

Weak interactions are responsible for processes such as beta decay and certain transformations of elementary particles. They are important in nuclear and particle phenomena but do not normally enter the direct calculation of familiar contact-force mechanics.

## 4.6 Scope of Classical Physics

The physics in subsequent mechanics chapters largely treats objects that are sufficiently large and slow for a classical description to be useful. At atomic scales quantum descriptions are required, and near light speed relativistic corrections are significant.

**Operational lesson:** the validity of a mathematical model depends on scale and assumptions, not just algebraic consistency.

### Part II: Key takeaways

- A force always has a source and a receiving body.
- Gravity and electromagnetic interactions explain the forces most often drawn on a macroscopic free-body diagram.
- Contact forces may be resolved into normal and tangential components.
- A simple force law is an idealization within a specified physical regime.

---

# Part III: Newton's Laws of Motion

## 5.1 First Law of Motion

A body remains at rest or continues moving with uniform velocity along a straight line unless acted on by a nonzero resultant external force. The first law identifies **inertial frames**, in which free particles do not spontaneously accelerate.

$$
\boxed{\sum\vec F_{\mathrm{external}}=0\ \Longrightarrow\ \vec v=\text{constant}.}
$$

The implication is **not** that zero net force means zero velocity. Rest and constant nonzero velocity are equally compatible with zero resultant force.

## 5.2 Second Law of Motion

For a particle of constant mass, the resultant force determines its acceleration:

$$
\boxed{\sum\vec F_{\mathrm{external}}=m\vec a}.
$$

In Cartesian components,

$$
\sum F_x=ma_x,\qquad \sum F_y=ma_y,\qquad \sum F_z=ma_z.
$$

Mass is a measure of inertia: with the same resultant force, a larger mass accelerates less. The more general statement for a system uses momentum and will be developed in Chapter 9:

$$
\sum\vec F_{\mathrm{external}}=\frac{d\vec p}{dt},
$$

with suitable system and momentum accounting.

### Free-body-diagram method

1. **Choose exactly one body or system.** Draw a boundary around it.
2. **Choose an inertial frame** whenever practical; define signed axes.
3. **Draw every external force acting *on* that chosen body.** Label its source.
4. **Resolve vectors** into components. Do not introduce an extra force merely because the body moves.
5. **Apply** `ΣF_x=ma_x`, `ΣF_y=ma_y`, and constraints.
6. **Check signs, units and limiting cases** before reporting the result.

### Example: block pulled on a smooth horizontal table

With a horizontal pull `F` and no friction,

$$
N-mg=0,\qquad F=ma.
$$

Hence

$$
\boxed{N=mg,\qquad a=\frac{F}{m}}.
$$

If the force is inclined upward through angle `θ`, the vertical balance changes:

$$
N+F\sin\theta-mg=0
\quad\Longrightarrow\quad
\boxed{N=mg-F\sin\theta},
$$

provided the block remains in contact with the table. Thus `N=mg` is **not** universal.

## 5.3 Working with Newton's First and Second Law

The equations work best when combined with geometry and idealized constraints.

### Blocks on a frictionless incline

For inclination `θ`, choose one axis down the plane and another perpendicular to it. Gravity resolves into `mg sinθ` down the plane and `mg cosθ` into the plane. With no other forces,

$$
\boxed{ma=mg\sin\theta\ \Longrightarrow\ a=g\sin\theta},
$$

$$
\boxed{N=mg\cos\theta}.
$$

### Ideal strings, pulleys and connected masses

A light inextensible string imposes geometric relations between the motions of connected bodies. With a **massless string and frictionless, massless pulley**, the tension is uniform along a continuous string.

For an ideal two-mass Atwood machine with `m_2>m_1`, take `m_2` downward and `m_1` upward:

$$
m_2g-T=m_2a,
\qquad T-m_1g=m_1a.
$$

Adding gives

$$
\boxed{a=\frac{m_2-m_1}{m_1+m_2}g},
\qquad
\boxed{T=\frac{2m_1m_2}{m_1+m_2}g}.
$$

A movable pulley or massive pulley requires its own acceleration constraints and/or torque equation. Never impose equal accelerations without verifying the string geometry.

### Equilibrium and constrained motion

For a body known to have zero acceleration,

$$
\boxed{\sum\vec F=0}.
$$

For contact at a surface, an ideal normal reaction maintains the nonpenetration constraint. Its magnitude follows from the force balances; it is not a force with a predetermined magnitude.

## 5.4 Newton's Third Law of Motion

If body `A` exerts a force on body `B`, `B` exerts an equal and opposite force on `A`:

$$
\boxed{\vec F_{A\to B}=-\vec F_{B\to A}}.
$$

The two forces act on **different bodies**. They therefore cannot be canceled on the *same* body's free-body diagram.

**Example:** The floor pushes up on a person; the person pushes down on the floor. A person's weight (Earth acting on person) and the normal force (floor acting on person) are *not* a third-law pair.

When summing equations across an appropriate multi-body system, internal action-reaction pairs cancel in the total force balance, leaving external forces to determine center-of-mass motion.

## 5.5 Pseudo Forces

Newton's second law in its ordinary form is formulated for an **inertial frame**. Suppose a frame `S′` translates without rotation but accelerates at `\vec a_0` relative to an inertial frame `S`:

$$
\vec a_{P/S}=\vec a_{P/S'}+\vec a_0.
$$

Substitute into the inertial-frame force law:

$$
\sum\vec F_{\mathrm{real}}=m(\vec a_{P/S'}+\vec a_0).
$$

Rearrange into a Newton-like law as observed from `S′`:

$$
\boxed{\sum\vec F_{\mathrm{real}}+\vec F_{\mathrm{pseudo}}=m\vec a_{P/S'}},
\qquad
\boxed{\vec F_{\mathrm{pseudo}}=-m\vec a_0}.
$$

A pseudo force accounts for using an accelerating frame; it is not an additional physical interaction with another body.

**Example: accelerating elevator.** For a passenger of mass `m` standing on the floor, taking upward acceleration of the elevator as `a`:

$$
N-mg=ma \quad\Longrightarrow\quad \boxed{N=m(g+a)}.
$$

If the elevator accelerates downward at magnitude `a`, then `N=m(g-a)` while contact persists. A downward acceleration of `g` gives `N=0`, the ideal free-fall condition.

Rotating frames require additional inertial terms and are treated only selectively later in this unit.

## 5.6 The Horse and the Cart

A horse pulls a cart, and the cart pulls the horse backward with equal force. Why can the assembly accelerate? The internal rope forces cancel in the combined horse-cart system; the ground exerts an **external forward static-friction force** on the horse's hooves. Resistive forces on the cart oppose motion.

For the entire horse-cart system,

$$
\boxed{F_{\mathrm{ground\ on\ horse}}-F_{\mathrm{resistance}}=(m_h+m_c)a}.
$$

The third law does **not** prevent acceleration. It says interaction forces come in body-to-body pairs, not that every body's net force is zero.

## 5.7 Inertia

Inertia is the tendency to preserve velocity in an inertial frame. **Mass** quantifies translational inertia: more mass requires more force to achieve the same acceleration.

A passenger leans forward when a bus brakes because the passenger's body initially tends to retain its forward velocity. A seat belt supplies the force needed to reduce that velocity.

### Part III: Key takeaways

- Zero net force preserves **velocity**, not necessarily rest.
- Define system, axes, actual interactions and constraints before writing equations.
- Third-law forces act on different bodies; internal forces cancel only after forming a suitable combined system.
- Pseudo forces are computational terms associated with noninertial frames.
- A constraint force such as tension or the normal reaction is solved from the system's dynamics.

---
# Part IV: Friction

## 6.1 Friction as the Component of Contact Force

The net contact force between two surfaces may be resolved into a normal component `N` and a tangential component `f`:

$$
\boxed{\vec F_{\mathrm{contact}}=\vec N+\vec f},
\qquad
\vec N\cdot\vec f=0.
$$

The **normal reaction** prevents interpenetration; the **frictional component** opposes the *relative sliding* or *tendency to slide* of the two surfaces. The frictional force does not necessarily oppose the object's velocity relative to the ground.

For example, while walking forward, a foot pushes the ground backward and static friction from the ground pushes the foot forward. Friction can therefore propel an object, even though it opposes slipping at the interface.

## 6.2 Kinetic Friction

When two surfaces actually slide relative to one another, the usual approximate law for dry kinetic friction is

$$
\boxed{f_k=\mu_kN},
$$

where `μ_k` is the dimensionless **coefficient of kinetic friction**. The direction is opposite the relative tangential sliding velocity.

The law is an empirical approximation for many rigid dry surfaces under ordinary conditions; it is not an exact universal property of every contact, especially in lubrication, highly deformable materials or rate-dependent friction.

### Sliding block on a horizontal floor

A block of mass `m` sliding with no applied horizontal force experiences friction `μ_kmg` opposite the motion:

$$
ma=-\mu_kmg\quad\Longrightarrow\quad\boxed{a=-\mu_kg}.
$$

If its initial velocity along `+x` is `u`, it stops after

$$
0=u^2-2\mu_kgd
\quad\Longrightarrow\quad
\boxed{d=\frac{u^2}{2\mu_kg}}.
$$

This assumes the block remains sliding until it stops, `μ_k` and `g` are constant, and no additional horizontal forces act.

## 6.3 Static Friction

Static friction acts between surfaces that are **not sliding** relative to one another. Its magnitude is whatever is required to maintain no slip, up to a limiting value:

$$
\boxed{|f_s|\le\mu_sN}.
$$

Here `μ_s` is the coefficient of static friction. At impending slip,

$$
\boxed{|f_{s,\max}|=\mu_sN}.
$$

**Crucial distinction:** do not automatically set `f_s=μ_sN`. That equality holds only at the limiting condition, not for every body at rest.

**Example: horizontal block.** If a stationary block is pushed with horizontal force `F`, static friction may adjust to `f_s=F` while `F≤μ_smg`. If the applied force exceeds the limiting value, the block starts sliding in the ideal Coulomb model, after which kinetic friction applies.

### Block at rest on a rough incline

A block on an inclined plane at angle `θ` has downhill component `mg sinθ` and normal reaction `mg cosθ`. To remain stationary, friction must act **uphill** with

$$
f_s=mg\sin\theta.
$$

The no-slip criterion is

$$
mg\sin\theta\le\mu_smg\cos\theta
\quad\Longrightarrow\quad
\boxed{\tan\theta\le\mu_s}.
$$

The **angle of repose** `θ_c` satisfies

$$
\boxed{\tan\theta_c=\mu_s}.
$$

Above this angle, a static configuration is not sustainable under this model.

## 6.4 Laws of Friction

HCV presents approximate experimentally motivated rules for solid contact:

- During sliding, kinetic friction has approximate magnitude `μ_kN`.
- In static contact, friction is self-adjusting with the bound `|f_s|≤μ_sN`.
- For many material pairs and loading conditions, `μ_s>μ_k`, although this is not a universal law.
- Under ordinary dry-contact conditions, friction is approximately independent of the *apparent* contact area for a fixed normal load.

**Direction algorithm:** first infer which way the surfaces would move *relative to each other* if tangential friction were absent. Friction acts to oppose that slipping tendency. Solve the equations, then check whether the assumed direction and friction bound were consistent.

### Pulling versus pushing a block

A force `F` at angle `θ` **above** the horizontal reduces the normal force:

$$
N=mg-F\sin\theta.
$$

A force at angle `θ` **below** horizontal increases it:

$$
N=mg+F\sin\theta.
$$

If sliding occurs, horizontal acceleration during an upward pull is

$$
\boxed{a=\frac{F\cos\theta-\mu_k(mg-F\sin\theta)}{m}}.
$$

The normal-force expression assumes contact is maintained and there is no vertical acceleration. This is why inclined pulls and pushes produce different frictional resistance.

## 6.5 Understanding Friction at Atomic Level

Real contact occurs at many microscopic surface asperities, not across the entire visible contact area. Surface irregularities deform, adhere and interact through electromagnetic forces. Increasing the normal load generally increases the amount and strength of actual microscopic contact, helping explain why friction often grows with `N`.

The fact that kinetic friction is **often** approximately independent of apparent contact area does not mean microscopic area or surface chemistry is irrelevant. Real surfaces can depart substantially from the simplest Coulomb model.

**Physical insight:** friction converts organized mechanical motion into internal energy of the bodies and their surroundings. Energy is not destroyed when a sliding block slows; mechanical energy is transferred into other forms.

## 6.6 A Laboratory Method to Measure Friction Coefficient

HCV outlines two basic measurement approaches.

### A. Horizontal-table method

Connect a block on a horizontal plank to a hanging mass by a light string over a pulley. Increase the hanging load until slipping is about to begin. Under the ideal assumptions of negligible pulley friction and negligible string mass, the horizontal friction force at threshold equals the hanging weight:

$$
f_{s,\max}\approx m_hg,
\qquad N=m_bg.
$$

Thus an approximate estimate is

$$
\boxed{\mu_s\approx\frac{m_h}{m_b}}.
$$

For a block already sliding at constant speed, balance forces to estimate `μ_k`. If it accelerates, include `ma` for both masses instead of assuming the string tension equals hanging weight.

### B. Inclined-table method

Raise one end of the plank slowly until the block *just* begins to slide. At the threshold,

$$
mg\sin\theta_c=\mu_smg\cos\theta_c
\quad\Longrightarrow\quad
\boxed{\mu_s=\tan\theta_c}.
$$

A sliding-body measurement can instead estimate `μ_k` by measuring its acceleration down the incline:

$$
a=g(\sin\theta-\mu_k\cos\theta)
\quad\Longrightarrow\quad
\boxed{\mu_k=\frac{g\sin\theta-a}{g\cos\theta}}.
$$

**Experimental practice:** repeat readings, record angles and uncertainties, and distinguish the **onset of slip** from sustained sliding. Ideal pulley and rigid-surface assumptions can dominate experimental error.

### Part IV: Key takeaways

- Static friction is an **inequality** until the contact reaches impending slip.
- The normal reaction depends on applied forces, geometry and acceleration.
- Determine friction direction from the *relative tendency to slip*, not from global motion.
- Real friction is a surface-interaction phenomenon approximated by simple useful laws.

---

# Part V: Circular Motion

## 7.1 Angular Variables

For a particle traveling along a circle of radius `r`, its position can be described by angular coordinate `θ` (measured in radians). Arc length and angular displacement satisfy

$$
\boxed{s=r\theta}
$$

when `s` is a signed arc displacement and `θ` the corresponding signed angle. Angular velocity and angular acceleration are

$$
\boxed{\omega=\frac{d\theta}{dt}},
\qquad
\boxed{\alpha=\frac{d\omega}{dt}=\frac{d^2\theta}{dt^2}}.
$$

For constant `α`, angular kinematic equations mirror straight-line motion:

$$
\boxed{\omega=\omega_0+\alpha t},
$$

$$
\boxed{\theta-\theta_0=\omega_0t+\frac12\alpha t^2},
$$

$$
\boxed{\omega^2-\omega_0^2=2\alpha(\theta-\theta_0)}.
$$

Angular quantities are conventionally assigned a sign for clockwise/counterclockwise motion about a chosen axis; angular velocity can also be represented as an axial vector.

For uniform circular motion,

$$
\boxed{T=\frac{2\pi}{|\omega|}},
\qquad
\boxed{f=\frac1T=\frac{|\omega|}{2\pi}}.
$$

## 7.2 Unit Vectors along the Radius and the Tangent

At angle `θ` in the `xy` plane, define outward radial and increasing-angle tangential unit vectors:

$$
\hat e_r=\cos\theta\,\hat i+\sin\theta\,\hat j,
$$

$$
\hat e_\theta=-\sin\theta\,\hat i+\cos\theta\,\hat j.
$$

These unit vectors rotate as the particle moves:

$$
\boxed{\frac{d\hat e_r}{dt}=\omega\hat e_\theta},
\qquad
\boxed{\frac{d\hat e_\theta}{dt}=-\omega\hat e_r}.
$$

The basis itself changing with time is the central geometric reason circular motion has radial acceleration even at constant speed.

## 7.3 Acceleration in Circular Motion

For a fixed-radius circle,

$$
\vec r=r\hat e_r.
$$

Differentiate once:

$$
\vec v=r\omega\hat e_\theta,
\qquad
\boxed{v=r|\omega|}.
$$

Differentiate again:

$$
\boxed{\vec a=-r\omega^2\hat e_r+r\alpha\hat e_\theta}.
$$

Thus acceleration has two perpendicular components:

$$
\boxed{a_r=-\frac{v^2}{r}=-r\omega^2},
\qquad
\boxed{a_t=r\alpha=\frac{dv_{\mathrm{speed}}}{dt}\ \text{(with consistent direction)}}.
$$

The inward radial component is often called **centripetal acceleration**. Its magnitude is

$$
\boxed{a_c=\frac{v^2}{r}=r\omega^2}.
$$

The total acceleration magnitude for a fixed radius is

$$
\boxed{|\vec a|=\sqrt{(r\omega^2)^2+(r\alpha)^2}}.
$$

For uniform circular motion, `α=0` but `a_c` remains nonzero.

## 7.4 Dynamics of Circular Motion

In an inertial frame, the inward radial acceleration must come from the inward component of **actual forces**:

$$
\boxed{\sum F_{\mathrm{radial,in}}=m\frac{v^2}{r}}.
$$

**Centripetal force is not a new fifth kind of force.** It is a description of the *net inward force*. Depending on the system, it may be supplied by tension, gravity, friction, normal force or a combination.

### Mass on a string in a horizontal circle

When the string itself supplies the entire inward force,

$$
\boxed{T=\frac{mv^2}{r}}.
$$

If the string breaks, the mass initially continues along its instantaneous tangent, not radially outward, in the inertial frame.

### Conical pendulum

For a bob rotating in a horizontal circle on a string of length `\ell` at an angle `θ` from vertical, radius `r=\ell\sin\theta`. With tension `T_s`,

$$
T_s\cos\theta=mg,
\qquad
T_s\sin\theta=\frac{mv^2}{r}.
$$

Divide the equations:

$$
\boxed{\tan\theta=\frac{v^2}{rg}}.
$$

Then use `r=\ell sinθ` to find the angular speed.

### Vertical circular motion

At the lowest point of a mass attached to a string,

$$
T_{\mathrm{bottom}}-mg=\frac{mv_{\mathrm{bottom}}^2}{r}.
$$

At the top, if inward is downward,

$$
T_{\mathrm{top}}+mg=\frac{mv_{\mathrm{top}}^2}{r}.
$$

Therefore,

$$
\boxed{T_{\mathrm{top}}=\frac{mv_{\mathrm{top}}^2}{r}-mg}.
$$

A **string cannot push**. To remain taut at the top, `T_top≥0`, requiring

$$
\boxed{v_{\mathrm{top}}^2\ge gr}.
$$

This is a minimum-speed condition for taut circular motion, not a statement that all vertical-circle trajectories maintain fixed speed.

## 7.5 Circular Turnings and Banking of Roads

### Level road

Static friction must supply the inward force for a car turning on a level road:

$$
\frac{mv^2}{r}\le\mu_smg.
$$

Hence the no-skid speed limit of this ideal model is

$$
\boxed{v\le\sqrt{\mu_srg}}.
$$

The mass cancels in the simple model, but real tire behavior is more complex than constant-`μ` Coulomb friction.

### Banked road without friction

For bank angle `θ` measured from horizontal, the normal force has vertical and horizontal components:

$$
N\cos\theta=mg,
\qquad
N\sin\theta=\frac{mv^2}{r}.
$$

Thus

$$
\boxed{\tan\theta=\frac{v^2}{rg}},
\qquad
\boxed{v=\sqrt{rg\tan\theta}}.
$$

This is the **design speed** at which no lateral friction is needed. At other speeds, friction may act uphill or downhill along the bank; its direction cannot be assumed in advance.

### Worked example

A car follows a level curve of radius `50 m` with `μ_s=0.40` and `g=10 m/s²`:

$$
v_{\max}=\sqrt{0.40\times50\times10}
=\sqrt{200}\approx14.1\,\mathrm{m/s}.
$$

The result assumes level road, no aerodynamic/other lateral forces and adequate tire-road static friction.

## 7.6 Centrifugal Force

An object moving in a circle needs inward acceleration in an inertial frame. An observer in a uniformly rotating frame can instead describe the body using an apparent outward **centrifugal force**:

$$
\boxed{\vec F_{\mathrm{cf}}=m\omega^2r\,\hat e_r}
$$

for the radial distance `r` from the rotation axis. This is a pseudo-force term, not an outward interaction applied by another body.

In a rotating frame, other inertial terms, including Coriolis contributions for relative motion, may also be needed. The simple outward centrifugal term alone does not describe every rotating-frame problem.

**Frame comparison:**

- Inertial-frame observer: net **inward real force** produces circular acceleration.
- Corotating observer: body may appear stationary because real forces plus appropriate pseudo forces balance.

Never count both a radial net force `mv²/r` **and** an additional real centrifugal force in one inertial-frame free-body diagram.

## 7.7 Effect of Earth's Rotation on Apparent Weight

Because Earth rotates, a point on its surface (away from the poles) moves in a circle about Earth's rotation axis. Let Earth's angular rate be `Ω`, terrestrial latitude `λ`, and spherical Earth radius `R_E`. The distance to the rotation axis is approximately

$$
r_\perp=R_E\cos\lambda.
$$

A stationary object in the Earth-fixed frame has the centrifugal pseudo acceleration

$$
\boxed{\vec a_{\mathrm{cf}}=\Omega^2r_\perp\hat e_\perp},
$$

pointing outward from the rotation axis. The effective gravitational acceleration is the vector combination

$$
\boxed{\vec g_{\mathrm{eff}}=\vec g_{\mathrm{grav}}+\vec a_{\mathrm{cf}}}.
$$

On an idealized spherical Earth the centrifugal effect is greatest at the equator and vanishes at the poles. At the equator,

$$
\boxed{g_{\mathrm{eff}}\approx g_{\mathrm{grav}}-\Omega^2R_E}.
$$

At general latitudes the centrifugal vector is **not exactly opposite** the gravitational vector, so simply subtracting `Ω²R_E cosλ` from `g` as scalar magnitudes would be incorrect. Earth's nonspherical shape and nonuniform gravity add further real-world effects.

The reading of a scale at rest with the Earth is related to the supporting normal force and this effective gravity, rather than gravitational attraction alone.

### Part V: Key takeaways

- `a_c=v²/r` is an **acceleration requirement**, not an independent force.
- Uniform circular motion has changing velocity even at constant speed.
- Tangential acceleration changes speed; radial acceleration changes direction.
- Friction, tension, gravity or normal forces can supply centripetal acceleration.
- Outward centrifugal effects belong to an accelerating/rotating reference-frame description.

---

# Part VI: Work and Energy

## 8.1 Kinetic Energy

For a particle of mass `m` moving at speed `v`, the translational kinetic energy is

$$
\boxed{K=\frac12mv^2}.
$$

Kinetic energy is a scalar, nonnegative quantity. Its value depends on the chosen inertial frame because measured speed depends on the frame. Its SI unit is the joule:

$$
1\,\mathrm J=1\,\mathrm{N\,m}=1\,\mathrm{kg\,m^2\,s^{-2}}.
$$

## 8.2 Work and Work-Energy Theorem

For a constant force `\vec F` and displacement `\Delta\vec r`, work done by that force is

$$
\boxed{W=\vec F\cdot\Delta\vec r=F\,\Delta r\cos\theta}.
$$

Positive work tends to increase the particle's kinetic energy, negative work tends to decrease it, and perpendicular force does zero instantaneous work.

### Deriving the theorem

Use Newton's second law and the definition of work:

$$
dW=\vec F\cdot d\vec r
=m\frac{d\vec v}{dt}\cdot\vec v\,dt.
$$

Since

$$
\vec v\cdot d\vec v=\frac12d(v^2),
$$

it follows that

$$
dW=d\left(\frac12mv^2\right).
$$

Integrating over the motion,

$$
\boxed{W_{\mathrm{net}}=K_f-K_i=\Delta K}.
$$

This **work-energy theorem** is valid for a particle even when net force varies with position or time, provided forces and work are properly defined.

## 8.3 Calculation of Work Done

When force changes along the path, divide the motion into infinitesimal displacements:

$$
\boxed{W=\int_{\mathcal C}\vec F\cdot d\vec r}.
$$

In one-dimensional motion,

$$
\boxed{W=\int_{x_i}^{x_f}F_x(x)\,dx}.
$$

The signed area under an `F_x`-versus-`x` curve equals the work done in the corresponding interval.

### Uniform gravitational force near Earth's surface

Taking height `y` upward,

$$
\vec F_g=-mg\hat j,
\qquad
\boxed{W_g=-mg(y_f-y_i)}.
$$

Gravity does positive work when the object goes downward and negative work when it goes upward.

### Work done by a spring

For `F_x=-kx`,

$$
W_s=\int_{x_i}^{x_f}-kx\,dx
=\boxed{\frac12k(x_i^2-x_f^2)}.
$$

Compression and extension store spring energy; a restoring spring does positive work as it returns toward its natural length.

### Instantaneous power

Power is the rate of doing work:

$$
\boxed{P=\frac{dW}{dt}=\vec F\cdot\vec v}.
$$

Average power over an interval is total work divided by elapsed time. The SI unit is the watt, `1 W=1 J/s`.

## 8.4 Work-Energy Theorem for a System of Particles

For a collection of particles, add the work-energy relations of all particles:

$$
\boxed{\Delta K_{\mathrm{total}}=W_{\mathrm{external}}+W_{\mathrm{internal}}}.
$$

Here

$$
K_{\mathrm{total}}=\sum_i\frac12m_i v_i^2.
$$

**Subtle point:** internal forces cancel in the total **force** balance as action-reaction pairs, but their **works** need not cancel because the forces act through different particle displacements. Internal interactions may convert kinetic energy into spring energy, thermal energy or other internal forms.

For an ideal rigid body, internal constraint forces do no net work on the allowed rigid-body motion. For deformable systems, internal work generally matters.

## 8.5 Potential Energy

Potential energy is associated with the **configuration of a system of interacting bodies**, not ordinarily an isolated particle without its environment. A gravitational potential-energy change belongs to the Earth-object system; an elastic potential-energy change belongs to the deformed spring system.

For a conservative force, define the change in potential energy as minus the work done by that force:

$$
\boxed{U_f-U_i=-W_{\mathrm{conservative}}}.
$$

Only changes in potential energy have direct mechanical significance; the zero level of `U` may be selected conveniently.

## 8.6 Conservative and Nonconservative Forces

A force is **conservative** when its work between two positions is independent of the path. Equivalently, work over a closed path is zero:

$$
\boxed{\oint\vec F_c\cdot d\vec r=0}.
$$

Examples in the usual mechanical idealizations include gravitational and ideal-spring forces. Sliding friction is generally nonconservative: its work depends on the traversed path length.

For a conservative force in one dimension,

$$
\boxed{F_x=-\frac{dU}{dx}}.
$$

In three dimensions,

$$
\boxed{\vec F=-\nabla U},
$$

where a well-defined potential function exists on the relevant domain. The force points toward decreasing potential energy, but equilibrium can occur at stationary points of `U`.

## 8.7 Definition of Potential Energy and Conservation of Mechanical Energy

Separate conservative and nonconservative work:

$$
\Delta K=W_c+W_{nc},
\qquad W_c=-\Delta U.
$$

Therefore

$$
\boxed{\Delta(K+U)=W_{nc}}.
$$

If no nonconservative work changes the mechanical energy of the chosen system,

$$
\boxed{K_i+U_i=K_f+U_f}.
$$

The total `E_mech=K+U` is then constant. This statement requires a careful system boundary and suitable assumptions; merely having a conservative force present is not sufficient if other agents do work.

### Worked example: body sliding down a smooth slope

A body starts from rest at vertical height `h` and reaches the bottom without friction. Energy conservation gives

$$
mgh=\frac12mv^2
\quad\Longrightarrow\quad
\boxed{v=\sqrt{2gh}}.
$$

The speed does not depend on mass or the precise shape of the frictionless track, provided the body stays on the track and no other work or energy transfers intervene.

## 8.8 Change in the Potential Energy in a Rigid-Body Motion

In a uniform gravitational field, the total gravitational potential energy of a rigid body of mass `M` depends on the height of its center of mass:

$$
\boxed{U_g=Mg y_{\mathrm{CM}}+C}.
$$

Consequently,

$$
\boxed{\Delta U_g=Mg\,\Delta y_{\mathrm{CM}}}.
$$

A rigid body's complicated shape does not prevent use of this compact expression for its gravitational-energy change. This is especially valuable when analyzing rolling or rotating objects whose constituent particles follow different paths.

## 8.9 Gravitational Potential Energy

### Uniform field near Earth

For modest height changes,

$$
\boxed{U_g=mgy+C}.
$$

### General inverse-square gravity

At distance `r` from the center of a spherically symmetric mass `M`, choose `U(∞)=0`. Because gravitational force is attractive,

$$
\boxed{U_g(r)=-\frac{GMm}{r}}.
$$

The negative sign indicates that work must be supplied to separate the bound masses from a finite separation to infinity.

**Do not interchange blindly:** `mgh` is a local approximation for small height changes near the surface; `-GMm/r` is the central-force potential used over large changes in `r` (its fuller study occurs in Chapter 11).

## 8.10 Potential Energy of a Compressed or Extended Spring

For a spring obeying Hooke's law, select zero potential at natural length `x=0`:

$$
\boxed{U_s=\frac12kx^2}.
$$

Compression and extension store the same energy for equal `|x|` within the linear spring model.

The total mechanical energy of an ideal horizontal mass-spring system is

$$
\boxed{E=\frac12mv^2+\frac12kx^2=\text{constant}}.
$$

At maximum extension, speed momentarily vanishes and energy is fully elastic; at equilibrium, spring potential is minimum and speed is largest. This prepares the ground for harmonic motion in Chapter 12.

## 8.11 Different Forms of Energy: Mass-Energy Equivalence

Mechanical energy is only part of a system's energy. Electrical, thermal, chemical, nuclear and other forms can participate in transformations. When friction reduces mechanical energy, a corresponding transfer typically increases internal energy and/or energy in the surroundings.

The relation

$$
\boxed{E_0=mc^2}
$$

connects rest mass and rest energy in relativity. It does not mean that ordinary Newtonian kinetic-energy problems require replacing `K=mv²/2` at low speed. The full relativistic treatment is reserved for later physics.

**General energy-conservation principle:** energy is transferred or converted between forms; accounting for a sufficiently inclusive system preserves total energy even if mechanical energy is not conserved.

### Part VI: Key takeaways

- Work is force integrated along displacement; its sign follows the force's projection along motion.
- Net work changes kinetic energy, even when force varies.
- Internal forces can do nonzero work on a system of particles.
- Conservative forces admit potential-energy descriptions; nonconservative work changes `K+U`.
- Choosing the **system** and identifying energy transfers are as essential as manipulating equations.

---
# Part VII: Centre of Mass, Linear Momentum, Collision

## 9.1 Centre of Mass

For particles of masses `m_i` at positions `\vec r_i`, the **center of mass** (CM) is the mass-weighted average position:

$$
\boxed{\vec R_{\mathrm{CM}}=\frac{\sum_i m_i\vec r_i}{\sum_i m_i}}.
$$

Define total mass `M=Σm_i`. Then

$$
\boxed{M\vec R_{\mathrm{CM}}=\sum_i m_i\vec r_i}.
$$

For two particles along a line,

$$
\boxed{x_{\mathrm{CM}}=\frac{m_1x_1+m_2x_2}{m_1+m_2}}.
$$

The CM lies closer to the more massive particle. It can lie outside the material of a hollow or concave body, so it need not coincide with a point occupied by matter.

### Worked example

A `2 kg` particle is at `x=0` and a `6 kg` particle is at `x=4 m`:

$$
x_{\mathrm{CM}}=\frac{2(0)+6(4)}{2+6}=3\,\mathrm m.
$$

The result is three-quarters of the way from the lighter particle toward the heavier one.

## 9.2 Centre of Mass of Continuous Bodies

For a continuous mass distribution, replace the discrete sum with an integral:

$$
\boxed{\vec R_{\mathrm{CM}}=\frac1M\int\vec r\,dm}.
$$

For a thin rod of linear density `λ(x)`, `dm=λ(x)dx`; for a planar lamina, `dm=σ(x,y)dA`; for a three-dimensional body, `dm=ρ(x,y,z)dV`.

$$
x_{\mathrm{CM}}=\frac{\int x\,dm}{\int dm},
\quad
y_{\mathrm{CM}}=\frac{\int y\,dm}{\int dm},
\quad
z_{\mathrm{CM}}=\frac{\int z\,dm}{\int dm}.
$$

### Symmetry before integration

A uniform rod has its CM at its midpoint. A uniform circular ring, disk or sphere has its CM at the geometric center. Reflection symmetries often determine one or more CM coordinates without calculation.

### Worked example: nonuniform rod

A rod occupies `0≤x≤L` with `λ(x)=Cx` for constant positive `C`. Then

$$
M=\int_0^L Cx\,dx=\frac12CL^2,
$$

$$
x_{\mathrm{CM}}=\frac1M\int_0^L x(Cx)\,dx
=\frac{CL^3/3}{CL^2/2}
=\boxed{\frac{2L}{3}}.
$$

The CM shifts toward the end with higher linear mass density.

## 9.3 Motion of the Centre of Mass

For a system of fixed total mass `M`, differentiate the CM definition:

$$
\boxed{\vec V_{\mathrm{CM}}=\frac{\sum_i m_i\vec v_i}{M}}.
$$

A second differentiation gives

$$
\boxed{M\vec A_{\mathrm{CM}}=\sum_i m_i\vec a_i}.
$$

Apply Newton's law to each constituent and add. Internal action-reaction forces cancel pairwise, leaving

$$
\boxed{M\vec A_{\mathrm{CM}}=\sum\vec F_{\mathrm{external}}}.
$$

This powerful relation holds for a fixed-mass system even when the bodies move relative to one another, collide or deform. Its validity does not require the whole system to be rigid.

**Interpretation:** external forces control center-of-mass motion, while internal interactions control how the components move relative to the CM.

## 9.4 Linear Momentum and Its Conservation Principle

For a particle, linear momentum is

$$
\boxed{\vec p=m\vec v}.
$$

For a system,

$$
\boxed{\vec P=\sum_i m_i\vec v_i=M\vec V_{\mathrm{CM}}}.
$$

The net external force is the time rate of change of total momentum:

$$
\boxed{\frac{d\vec P}{dt}=\sum\vec F_{\mathrm{external}}}.
$$

Hence if the net external force is zero,

$$
\boxed{\vec P=\text{constant}}.
$$

If the external force in one direction vanishes, momentum **in that direction** is conserved, even if forces act in other directions.

**Example:** Two skaters push one another apart on nearly frictionless ice. Their individual momenta change in opposite directions, but total momentum remains constant if horizontal external impulse is negligible.

## 9.5 Rocket Propulsion

A rocket accelerates by expelling propellant. The rocket and exhausted gas exchange momentum internally; the whole rocket-plus-propellant system conserves momentum in the absence of external forces.

Let `m` be the remaining rocket mass, `v` its velocity in an inertial frame and `u_e` the **speed of exhaust relative to the rocket**, directed backward along its axis. With `dm<0` for mass lost in time `dt`, the ideal rocket's velocity change is

$$
\boxed{m\,dv=-u_e\,dm}.
$$

For constant exhaust speed, integration from initial mass `m_0` to final mass `m_f` yields the **ideal rocket equation**:

$$
\int_{v_0}^{v_f}dv=-u_e\int_{m_0}^{m_f}\frac{dm}{m}
\quad\Longrightarrow\quad
\boxed{\Delta v=u_e\ln\left(\frac{m_0}{m_f}\right)}.
$$

This assumes motion aligned with the thrust, no external forces over the idealized maneuver, and constant effective exhaust speed. With gravity and drag, the actual change of velocity must additionally account for those effects.

For propellant mass flow rate `\dot m_p>0`, the ideal thrust magnitude is

$$
\boxed{F_{\mathrm{thrust}}=u_e\dot m_p}.
$$

**Conceptual pitfall:** a rocket does not need air to push against; it pushes expelled propellant backward and receives an equal-and-opposite force. Exhaust moving backward *relative to the rocket* need not move backward in every inertial frame.

## 9.6 Collision

A **collision** is an interaction during which bodies exchange a substantial impulse over a relatively short interval. When external impulse is negligible over that interval, total system momentum is approximately conserved:

$$
\boxed{\sum\vec p_{\mathrm{before}}=\sum\vec p_{\mathrm{after}}}.
$$

Kinetic energy behaves differently depending on the collision type:

- **Elastic collision:** total kinetic energy and momentum are conserved.
- **Inelastic collision:** momentum is conserved for an isolated system, while total kinetic energy changes into other forms.
- **Perfectly inelastic collision:** the bodies stick together and share a common velocity immediately afterward.

In any collision, energy conservation applies to the *full* system, but translational kinetic energy need not be conserved.

## 9.7 Elastic Collision in One Dimension

Let initial velocities be `u_1,u_2` and final velocities `v_1,v_2` for masses `m_1,m_2`, all signed along the collision line. Momentum conservation gives

$$
m_1u_1+m_2u_2=m_1v_1+m_2v_2.
$$

Kinetic-energy conservation gives

$$
\frac12m_1u_1^2+\frac12m_2u_2^2
=\frac12m_1v_1^2+\frac12m_2v_2^2.
$$

Combining these yields the **relative-speed reversal** condition for a nontrivial one-dimensional elastic encounter:

$$
\boxed{v_1-v_2=-(u_1-u_2)}.
$$

Solving gives

$$
\boxed{v_1=\frac{m_1-m_2}{m_1+m_2}u_1+\frac{2m_2}{m_1+m_2}u_2},
$$

$$
\boxed{v_2=\frac{2m_1}{m_1+m_2}u_1+\frac{m_2-m_1}{m_1+m_2}u_2}.
$$

### Important limiting cases

**Equal masses:** if `m_1=m_2`, the particles exchange their velocities:

$$
\boxed{v_1=u_2,\qquad v_2=u_1}.
$$

**Stationary heavy target:** for `m_2≫m_1` with `u_2=0`, the lighter particle approximately reverses direction.

**Stationary light target:** for `m_1≫m_2` with `u_2=0`, the massive projectile changes speed only slightly, while the lighter target receives a speed approaching twice the projectile's initial speed.

## 9.8 Perfectly Inelastic Collision in One Dimension

If masses `m_1,m_2` move together at shared velocity `v` immediately after impact,

$$
m_1u_1+m_2u_2=(m_1+m_2)v.
$$

Therefore

$$
\boxed{v=\frac{m_1u_1+m_2u_2}{m_1+m_2}}.
$$

The initial kinetic energy is generally larger than the translational kinetic energy after the sticking event. The decrease is

$$
\boxed{K_i-K_f=\frac12\frac{m_1m_2}{m_1+m_2}(u_1-u_2)^2}.
$$

The factor

$$
\boxed{\mu=\frac{m_1m_2}{m_1+m_2}}
$$

is the **reduced mass**. This result shows that kinetic-energy loss depends on relative speed, not on the observer's choice of constant-velocity inertial frame.

### Worked example

A `2 kg` cart at `6 m/s` sticks to a stationary `4 kg` cart:

$$
v=\frac{2(6)+4(0)}{2+4}=2\,\mathrm{m/s}.
$$

Before collision,

$$
K_i=\frac12(2)(6^2)=36\,\mathrm J.
$$

After collision,

$$
K_f=\frac12(6)(2^2)=12\,\mathrm J.
$$

Thus `24 J` of translational kinetic energy is converted to other forms while total momentum is conserved.

## 9.9 Coefficient of Restitution

The **coefficient of restitution** `e` compares the relative speed of separation to the relative speed of approach **along the line of impact**:

$$
\boxed{e=\frac{\text{relative separation speed}}{\text{relative approach speed}}}.
$$

For a one-dimensional collision with body 1 approaching body 2 so that `u_1>u_2`, and the bodies separating after impact,

$$
\boxed{e=\frac{v_2-v_1}{u_1-u_2}}.
$$

Typical ideal cases:

| Collision | Coefficient | Consequence |
|---|---:|---|
| Perfectly elastic | `e=1` | Relative speed of separation equals approach speed |
| Ordinary partially inelastic | `0<e<1` | Reduced relative speed after impact |
| Perfectly inelastic in 1D | `e=0` | No relative separation along impact direction immediately afterward |

For the simple passive collision models in the text, `0≤e≤1`. Some energetic or specially actuated impacts can exhibit values outside that interval, but these are not captured by the standard passive model.

Combine restitution and momentum conservation to solve for the final velocities in a nonelastic collision without incorrectly imposing conservation of kinetic energy.

## 9.10 Elastic Collision in Two Dimensions

Momentum conservation is vectorial. For two colliding particles,

$$
\boxed{m_1\vec u_1+m_2\vec u_2=m_1\vec v_1+m_2\vec v_2}.
$$

For an elastic collision,

$$
\boxed{\frac12m_1u_1^2+\frac12m_2u_2^2
=\frac12m_1v_1^2+\frac12m_2v_2^2}.
$$

Resolve momentum into `x` and `y` equations, then use the kinetic-energy relation and any specified outgoing angles or contact geometry. Conservation laws alone may not uniquely determine an arbitrary two-dimensional outcome without more information.

### Equal masses, one initially stationary

If `m_1=m_2=m` and `\vec u_2=0`, momentum implies

$$
\vec u_1=\vec v_1+\vec v_2.
$$

Kinetic-energy conservation requires

$$
u_1^2=v_1^2+v_2^2.
$$

Square the vector momentum equation:

$$
u_1^2=v_1^2+v_2^2+2\vec v_1\cdot\vec v_2.
$$

Comparing gives

$$
\boxed{\vec v_1\cdot\vec v_2=0}.
$$

Thus **when both outgoing speeds are nonzero**, the two outgoing velocity vectors are perpendicular in this special ideal case.

## 9.11 Impulse and Impulsive Force

An impulse is the time integral of force:

$$
\boxed{\vec J=\int_{t_i}^{t_f}\vec F\,dt}.
$$

Using the momentum form of Newton's second law,

$$
\boxed{\vec J=\Delta\vec p}.
$$

For a constant or average force over impact duration `Δt`,

$$
\boxed{\vec F_{\mathrm{avg}}=\frac{\Delta\vec p}{\Delta t}}.
$$

The unit of impulse is `N·s`, equivalently `kg·m/s`. A very large impact force can occur over a short time and still produce a finite impulse.

**Safety interpretation:** for a specified momentum change, increasing the stopping time decreases the *average* required force. This is a central physical principle behind cushioning and impact-management systems, though peak forces also depend on the detailed force-time profile.

### Part VII: Key takeaways

- The center of mass is a mass-weighted position; its acceleration depends only on **external net force** for a fixed-mass system.
- Total momentum is conserved when net external impulse vanishes.
- Collisions conserve momentum under isolation, but not necessarily translational kinetic energy.
- Rockets gain momentum by transferring momentum to exhaust; the expelled mass must be accounted for.
- Coefficient of restitution describes relative normal separation/approach speeds, not the ratio of individual speeds.

---

# Part VIII: Rotational Mechanics

## 10.1 Rotation of a Rigid Body about a Given Fixed Line

A **rigid body** idealization treats distances between all its particles as constant. Under rotation about a fixed axis, every constituent particle traces a circle centered on that axis. All particles share the same angular displacement, angular velocity and angular acceleration, though their **linear** speeds and accelerations depend on their distance from the axis.

A body that translates and rotates simultaneously requires a more general analysis, developed at the end of this chapter.

## 10.2 Kinematics

A particle at perpendicular distance `r_\perp` from a fixed rotation axis has

$$
\boxed{v=r_\perp|\omega|},
\qquad
\boxed{a_t=r_\perp\alpha},
\qquad
\boxed{a_r=r_\perp\omega^2}.
$$

Here `a_r` denotes inward radial-acceleration **magnitude**. The angular variables for all points of a rigid body are common, while `v`, `a_t` and `a_r` vary with `r_\perp`.

For constant angular acceleration,

$$
\boxed{\omega=\omega_0+\alpha t},
$$

$$
\boxed{\Delta\theta=\omega_0t+\frac12\alpha t^2},
$$

$$
\boxed{\omega^2=\omega_0^2+2\alpha\Delta\theta}.
$$

A full revolution corresponds to `2π` radians. **Angular acceleration is not radial acceleration**: `α` describes change of angular speed, whereas the radial component exists even with constant `ω`.

## 10.3 Rotational Dynamics

Translation responds to resultant force; rotation responds to resultant torque about an axis. A force acting through an axis can change a body's support loads without producing a torque about that axis.

Rigid-body dynamics requires the distribution of mass, not just total mass. A ring and disk with the same mass and radius do not respond identically to a given torque because they have different mass moments of inertia.

## 10.4 Torque of a Force about the Axis of Rotation

The torque of a force about a chosen point `O` is the vector

$$
\boxed{\vec\tau_O=\vec r\times\vec F},
$$

where `\vec r` extends from `O` to the point of application. Torque magnitude is

$$
\boxed{\tau=rF\sin\phi=F\ell_\perp},
$$

with `\ell_\perp` the perpendicular distance from the axis to the force's line of action (the **moment arm**). In the fixed-axis model, use the component of torque along that axis, with an agreed positive rotation direction.

Torque has SI units `N·m`, which are dimensionally the same as energy units but describe a distinct physical quantity; torque and work are not interchangeable scalars.

## 10.5 Torque and Angular Acceleration (Γ = Iα)

Consider particles of a rigid body rotating about a fixed axis. A particle `m_i` at distance `r_i` has tangential acceleration `r_iα`. Its tangential force requirement is `m_i r_iα`, giving a torque contribution `m_i r_i²α` about the axis. Summing contributions yields

$$
\tau_{\mathrm{net}}=\sum_i m_i r_i^2\alpha.
$$

Define **moment of inertia** about the specified axis:

$$
\boxed{I=\sum_i m_ir_i^2=\int r_\perp^2\,dm}.
$$

For fixed-axis rotation of a rigid body about a stationary axis,

$$
\boxed{\tau_{\mathrm{net,axis}}=I\alpha}.
$$

HCV uses `Γ` as a symbol for torque, so its `Γ=Iα` is the same physical statement.

**Important:** moment of inertia depends on the *axis*, not only the body. The relation `τ=Iα` in this simple scalar form requires the specified fixed-axis model; general three-dimensional rigid-body rotation needs a tensor description and additional terms.

## 10.6 Bodies in Equilibrium

A rigid body in static equilibrium must satisfy both the **force balance** and the **torque balance**:

$$
\boxed{\sum\vec F=0},
\qquad
\boxed{\sum\vec\tau_O=0}.
$$

The second equation can be written about any reference point `O` once force balance holds. Conveniently choose a point through which unknown support forces pass, causing their torque contributions to vanish.

### Example: uniform horizontal beam

A uniform beam of mass `M` and length `L` is supported at its two ends, `A` and `B`, with upward reactions `N_A,N_B`. Its weight acts at the midpoint:

$$
N_A+N_B=Mg.
$$

Torque balance about `A` gives

$$
N_BL-Mg\frac L2=0
\quad\Longrightarrow\quad
\boxed{N_B=\frac{Mg}{2}=N_A}.
$$

In an accelerating rigid-body problem, zero net force is not enough to imply zero angular acceleration, nor is zero net torque enough to imply zero linear acceleration.

## 10.7 Bending of a Cyclist on a Horizontal Turn

A cyclist turning on a level road leans inward to balance the turning effects associated with gravity and the horizontal ground reaction. In the cyclist's accelerating frame, one may use an outward pseudo force at the center of mass and require zero net torque about the tire-road contact region.

For center-of-mass height `h`, horizontal offset `x` and lean angle `θ` measured from the vertical,

$$
\tan\theta=\frac{x}{h}.
$$

In the ideal steady-turn model, balancing moments gives

$$
mg\,x=\frac{mv^2}{r}\,h
\quad\Longrightarrow\quad
\boxed{\tan\theta=\frac{v^2}{rg}}.
$$

The angle increases with the square of speed and decreases as turning radius increases. The simple model neglects steering geometry, tire deformation, gyroscopic effects and transient lean dynamics.

## 10.8 Angular Momentum

For a particle about a reference point `O`, angular momentum is

$$
\boxed{\vec L_O=\vec r\times\vec p=\vec r\times m\vec v}.
$$

Its magnitude is `L=mvr sinφ`, where `φ` is the angle between position and momentum. Angular momentum depends on the chosen origin, unlike linear momentum.

Differentiate:

$$
\frac{d\vec L_O}{dt}=\frac{d\vec r}{dt}\times\vec p+\vec r\times\frac{d\vec p}{dt}.
$$

For a particle with `\vec p=m\vec v`, the first term vanishes because `\vec v×m\vec v=0`. Thus, about a point fixed in an inertial frame,

$$
\boxed{\frac{d\vec L_O}{dt}=\vec\tau_O}.
$$

For a multi-particle system under standard internal central-force assumptions, internal torques cancel and

$$
\boxed{\frac{d\vec L_{\mathrm{system},O}}{dt}=\sum\vec\tau_{\mathrm{external},O}}.
$$

## 10.9 Angular Momentum and Angular Velocity (L = Iω)

For a particle rotating about an axis at radius `r`, with speed `v=rω`, its angular momentum component along the axis is `mr²ω`. For a rigid body rotating about a fixed **principal/symmetry axis** (or when considering the component *along the rotation axis*),

$$
L_{\mathrm{axis}}=\left(\sum_i m_ir_i^2\right)\omega.
$$

Therefore

$$
\boxed{L_{\mathrm{axis}}=I_{\mathrm{axis}}\omega}.
$$

**Clarification:** the full three-dimensional angular-momentum vector need not be parallel to the angular-velocity vector for an arbitrary body's rotation. The scalar relation is reliable for the specified axis component and the textbook's fixed-axis treatment.

## 10.10 Conservation of Angular Momentum

If the resultant external torque about the chosen fixed point or axis is zero,

$$
\boxed{\vec L=\text{constant}}
$$

or, for the axis component in the rigid-body axis model,

$$
\boxed{I_i\omega_i=I_f\omega_f}.
$$

**Example:** A spinning person pulls their arms inward, reducing rotational inertia. If external torque about the vertical axis is negligible, angular speed increases.

**Do not confuse conservation of angular momentum with conservation of kinetic energy.** If `L` is constant,

$$
K_{\mathrm{rot}}=\frac{L^2}{2I}.
$$

Reducing `I` increases rotational kinetic energy; the person supplies the required energy by doing internal muscular work.

## 10.11 Angular Impulse

Integrate the torque-angular-momentum relation over a time interval:

$$
\boxed{\vec J_{\mathrm{angular}}=\int_{t_i}^{t_f}\vec\tau\,dt=\Delta\vec L}.
$$

For a constant torque about a fixed axis,

$$
\boxed{\tau\,\Delta t=\Delta L_{\mathrm{axis}}}.
$$

This is the rotational counterpart of linear impulse:

$$
\boxed{\int\vec F\,dt=\Delta\vec p}.
$$

The larger the moment arm of an impact, the greater the angular impulse about the chosen axis for the same force-time history.

## 10.12 Kinetic Energy of a Rigid Body Rotating About a Given Axis

Every constituent particle has speed `v_i=r_iω` about the axis, so

$$
K=\sum_i\frac12m_i(r_i\omega)^2
=\frac12\omega^2\sum_i m_ir_i^2.
$$

Hence

$$
\boxed{K_{\mathrm{rot}}=\frac12I\omega^2}.
$$

Unlike the translational term `mv²/2`, rotational kinetic energy depends on the body's mass distribution about the given axis. Two bodies of equal mass and angular speed can have different rotational energies.

## 10.13 Power Delivered and Work Done by a Torque

For a small angular displacement `dθ` about a fixed axis, work done by the torque component along that axis is

$$
\boxed{dW=\tau\,d\theta}.
$$

Thus

$$
\boxed{W=\int_{\theta_i}^{\theta_f}\tau(\theta)\,d\theta}.
$$

Instantaneous rotational power is

$$
\boxed{P=\tau\omega}.
$$

Combine `τ=Iα` with the fixed-axis kinematic relation `α=ω(dω/dθ)` for constant `I`:

$$
W_{\mathrm{net}}=\int_{\omega_i}^{\omega_f}I\omega\,d\omega
=\boxed{\frac12I\omega_f^2-\frac12I\omega_i^2}.
$$

This is the **rotational work-energy theorem** in the fixed-axis model.

## 10.14 Calculation of Moment of Inertia

Moment of inertia about a chosen axis is

$$
\boxed{I=\int r_\perp^2\,dm}.
$$

Mass farther from the axis contributes disproportionately through the `r²` factor. A body with the same total mass but with more mass near its outer boundary has greater rotational inertia about that axis.

### Standard results

| Uniform body | Axis | Moment of inertia |
|---|---|---|
| Point mass `m` | Distance `r` from axis | $mr^2$ |
| Thin ring or hoop, radius `R` | Symmetry axis perpendicular to plane | $MR^2$ |
| Thin ring or hoop, radius `R` | Diameter within plane | $\tfrac12MR^2$ |
| Uniform disk, radius `R` | Symmetry axis perpendicular to plane | $\tfrac12MR^2$ |
| Uniform disk, radius `R` | Diameter within plane | $\tfrac14MR^2$ |
| Thin uniform rod, length `L` | Perpendicular through center | $\tfrac1{12}ML^2$ |
| Thin uniform rod, length `L` | Perpendicular through end | $\tfrac13ML^2$ |
| Uniform solid cylinder, radius `R` | Longitudinal symmetry axis | $\tfrac12MR^2$ |
| Uniform hollow thin cylinder, radius `R` | Longitudinal symmetry axis | $MR^2$ |
| Uniform solid sphere, radius `R` | Diameter | $\tfrac25MR^2$ |
| Thin spherical shell, radius `R` | Diameter | $\tfrac23MR^2$ |

Each expression applies to the specified shape and axis. A thick-walled cylinder, nonuniform rod or eccentric axis generally requires a new calculation.

### Derivation: uniform thin rod about its center

Place the rod along `x` from `-L/2` to `L/2`. Linear density is `λ=M/L`, so `dm=λ dx`:

$$
I=\int_{-L/2}^{L/2}x^2\frac{M}{L}\,dx
=\frac{M}{L}\left[\frac{x^3}{3}\right]_{-L/2}^{L/2}.
$$

Thus

$$
\boxed{I=\frac1{12}ML^2}.
$$

### Derivation: uniform disk about central perpendicular axis

Take concentric rings of radius `r` and thickness `dr`. With surface density `σ=M/(πR²)`,

$$
dm=2\pi r\sigma\,dr.
$$

Therefore

$$
I=\int_0^R r^2(2\pi r\sigma\,dr)
=2\pi\sigma\int_0^R r^3\,dr.
$$

Hence

$$
\boxed{I=\frac12MR^2}.
$$

## 10.15 Two Important Theorems on Moment of Inertia

### Parallel-axis theorem

If `I_CM` is the moment of inertia about an axis through the center of mass and `I_O` is the moment of inertia about a **parallel** axis at perpendicular distance `d`, then

$$
\boxed{I_O=I_{\mathrm{CM}}+Md^2}.
$$

To understand this, write each particle's position relative to the shifted axis as its CM-relative position plus the CM offset. When summed, the cross term vanishes because positions relative to the CM have zero mass-weighted sum.

**Example: rod about an endpoint**

$$
I_{\mathrm{end}}=\frac1{12}ML^2+M\left(\frac L2\right)^2
=\boxed{\frac13ML^2}.
$$

### Perpendicular-axis theorem

For a **planar lamina**, choose mutually perpendicular `x` and `y` axes **in the plane**, with `z` perpendicular to the plane through their intersection. Then

$$
\boxed{I_z=I_x+I_y}.
$$

This follows because each element satisfies `r_z²=x²+y²`. It generally cannot be applied directly to an arbitrary three-dimensional solid.

**Example: uniform thin circular disk**

Symmetry gives `I_x=I_y`, so

$$
\frac12MR^2=I_x+I_y=2I_x
\quad\Longrightarrow\quad
\boxed{I_x=I_y=\frac14MR^2}.
$$

## 10.16 Combined Rotation and Translation

A freely moving rigid body need not rotate about an axis fixed in space. Its motion can be decomposed into:

1. Translation of the center of mass.
2. Rotation relative to its center of mass.

For a point `P` of the rigid body,

$$
\boxed{\vec v_P=\vec V_{\mathrm{CM}}+\vec\omega\times\vec r_{P/\mathrm{CM}}}.
$$

The velocity of `P` is therefore the vector sum of CM translation and the velocity caused by rotation about the CM. This is a kinematic decomposition; it does not claim the body is literally made of two separate moving systems.

For planar motion, a point with zero instantaneous velocity may be used as an **instantaneous center** for velocity analysis, but it is not automatically a fixed pivot for computing accelerations or torques.

## 10.17 Rolling

A wheel or cylinder **rolls without slipping** when the point of contact has zero instantaneous velocity relative to the ground. For radius `R`,

$$
\boxed{v_{\mathrm{CM}}=R\omega},
\qquad
\boxed{a_{\mathrm{CM}}=R\alpha}
$$

for motion along a straight surface with consistent signs, fixed radius and the rolling constraint maintained.

If the center translates by distance `s` while the wheel rotates by `θ`, then

$$
\boxed{s=R\theta}.
$$

A topmost point of a rolling wheel has instantaneous speed `2v_CM` relative to the ground, while the point at the bottom has speed zero.

**Why static friction can act:** although the contacting point has zero relative velocity in ideal no-slip rolling, static friction may be required to enforce the rolling constraint or produce angular acceleration. Under ideal rolling on a stationary rigid surface, static friction does no instantaneous work at the stationary contact point.

### Rolling down an incline

For a rigid body of mass `M`, radius `R`, and central moment of inertia `I_CM`, take downhill as positive. Force and torque balances are

$$
Mg\sin\theta-f=Ma,
$$

$$
fR=I_{\mathrm{CM}}\alpha,
\qquad a=R\alpha.
$$

Eliminate `f` and `α`:

$$
\boxed{a=\frac{g\sin\theta}{1+I_{\mathrm{CM}}/(MR^2)}}.
$$

And the required static friction magnitude is

$$
\boxed{f=\frac{I_{\mathrm{CM}}}{R^2}a}.
$$

For ordinary bodies released from rest rolling downhill in this model, friction points **up** the plane. After solving, verify that `|f|≤μ_sN`; otherwise the no-slip assumption fails.

### Comparative rolling accelerations

| Body | `I_CM/(MR²)` | Acceleration down incline |
|---|---:|---|
| Solid sphere | `2/5` | $(5/7)g\sin\theta$ |
| Solid cylinder or disk | `1/2` | $(2/3)g\sin\theta$ |
| Hollow thin sphere | `2/3` | $(3/5)g\sin\theta$ |
| Thin ring | `1` | $(1/2)g\sin\theta$ |

Under the same ideal rolling conditions, the body with smaller normalized rotational inertia accelerates faster.

## 10.18 Kinetic Energy of a Body in Combined Rotation and Translation

For each particle of a rigid body, decompose its velocity into CM translation and CM-relative rotation. Sum kinetic energies:

$$
K=\frac12\sum_i m_i\left|\vec V_{\mathrm{CM}}+\vec v_i'\right|^2.
$$

The mixed term vanishes because

$$
\sum_i m_i\vec v_i'=0.
$$

Thus for planar rigid-body motion,

$$
\boxed{K=\frac12MV_{\mathrm{CM}}^2+\frac12I_{\mathrm{CM}}\omega^2}.
$$

For rolling without slip, substitute `V_CM=Rω`:

$$
\boxed{K=\frac12\left(M+\frac{I_{\mathrm{CM}}}{R^2}\right)V_{\mathrm{CM}}^2}.
$$

### Rolling-energy derivation

A body starts from rest at a vertical height `h` and rolls down without energy loss. Potential-energy decrease equals translational plus rotational kinetic energy:

$$
Mgh=\frac12Mv^2+\frac12I_{\mathrm{CM}}\frac{v^2}{R^2}.
$$

Therefore

$$
\boxed{v=\sqrt{\frac{2gh}{1+I_{\mathrm{CM}}/(MR^2)}}}.
$$

This agrees with the acceleration-based analysis for rolling down a uniform straight incline from rest.

## 10.19 Angular Momentum of a Body in Combined Rotation and Translation

Angular momentum about an origin `O` separates into orbital angular momentum of the CM and intrinsic angular momentum about the CM:

$$
\boxed{\vec L_O=\vec R_{\mathrm{CM}/O}\times M\vec V_{\mathrm{CM}}+\vec L_{\mathrm{CM}}}.
$$

For planar rigid-body motion about a principal axis normal to the plane,

$$
\boxed{\vec L_O=\vec R_{\mathrm{CM}/O}\times M\vec V_{\mathrm{CM}}+I_{\mathrm{CM}}\vec\omega}.
$$

The first term represents motion of the CM around `O`, while the second describes rotation about the CM. The decomposition helps avoid wrongly equating `L_O` with `I_CMω` when the entire body is translating.

### Example: rolling wheel, angular momentum about ground contact point

At a chosen instant, for a rolling wheel with contact point `C` and `\vec R_{\mathrm{CM}/C}` upward while `\vec V_CM` is forward, the orbital and spin angular momenta point in the same sense for ordinary forward rolling. Their magnitudes add:

$$
|L_C|=MRV_{\mathrm{CM}}+I_{\mathrm{CM}}\omega.
$$

Using `V_CM=Rω`,

$$
\boxed{|L_C|=(MR^2+I_{\mathrm{CM}})|\omega|}.
$$

This is an *instantaneous angular-momentum expression*. A material point on the wheel that coincides with contact at one instant does not remain the contact point later, so care is required when using time derivatives of angular momentum about a moving point.

## 10.20 Why Does a Rolling Sphere Slow Down?

An ideal rigid sphere on an ideal rigid horizontal plane can roll without loss at constant speed. Real spheres eventually slow due to **rolling resistance** and other dissipative effects.

One important cause is deformation of the sphere and supporting surface. The pressure distribution under a rolling sphere may become asymmetric, shifting the resultant normal reaction ahead of the vertical line through the center and creating a torque that opposes rotation.

For an effective forward contact-force shift `b`, the resisting moment can be approximated as

$$
\boxed{\tau_{\mathrm{resist}}\approx Nb}.
$$

The actual resistance depends on material deformation, surface condition and other losses. It is not equivalent to assuming the sphere continuously slips under the ordinary kinetic-friction law.

**Final distinction:**

- **Sliding friction:** surfaces slip relative to one another; mechanical energy is usually dissipated at the interface.
- **Ideal static friction in pure rolling:** prevents slipping and need not perform work at a stationary point of contact.
- **Rolling resistance:** arises from real deformation and dissipation, and can slow a sphere even without gross slipping.

### Part VIII: Key takeaways

- Torque is the rotational influence of a force about a specified point/axis.
- Moment of inertia depends on both **mass distribution and axis choice**.
- For a fixed-axis rigid-body model, `τ=Iα` and `K_rot=Iω²/2`.
- Angular momentum changes only through the net external torque about the chosen reference.
- Combined motion decomposes into CM translation plus rotation about the CM.
- Rolling without slip couples `v_CM` and `ω`; rotational inertia determines how energy divides between translation and rotation.

---
# Consolidated Formula Sheet

The equations below are reference formulas, **not substitutes for identifying a system and checking assumptions**. Verify that the prerequisites in the surrounding chapters apply before using a result.

## Kinematics and frame changes (Chapter 3)

| Topic | Main result | Validity / warning |
|---|---|---|
| Average velocity | $\vec v_{avg}=\Delta\vec r/\Delta t$ | Displacement, not distance |
| Instantaneous velocity | $\vec v=d\vec r/dt$ | Defined for differentiable position |
| Acceleration | $\vec a=d\vec v/dt$ | Vector change, including direction |
| Constant acceleration | $v=u+at$ | Signed 1D components |
| Constant acceleration | $x-x_0=ut+\tfrac12at^2$ | `a` constant |
| Constant acceleration | $v^2=u^2+2a(x-x_0)$ | `a` constant |
| Gravity near surface | $a_y=-g$ | Upward `y` positive |
| Relative velocity | $\vec v_{A/B}=\vec v_{A/S}-\vec v_{B/S}$ | Translation between frames |

**Projectiles:**

$$
\boxed{x=u\cos\theta\,t,\qquad y=u\sin\theta\,t-\frac12gt^2}.
$$

$$
\boxed{T=\frac{2u\sin\theta}{g},\quad
H=\frac{u^2\sin^2\theta}{2g},\quad
R=\frac{u^2\sin2\theta}{g}}.
$$

The three latter formulas assume equal launch/landing height, constant gravity and negligible drag.

## Forces, laws of motion and friction (Chapters 4–6)

$$
\boxed{\sum\vec F_{\mathrm{ext}}=m\vec a},
\qquad
\boxed{\vec F_{A\to B}=-\vec F_{B\to A}}.
$$

$$
\boxed{F_g=G\frac{m_1m_2}{r^2}},
\quad
\boxed{\vec F_g=m\vec g},
\quad
\boxed{F_s=-kx}.
$$

$$
\boxed{|f_s|\le\mu_sN},
\qquad
\boxed{f_k=\mu_kN},
\qquad
\boxed{\tan\theta_{\mathrm{repose}}=\mu_s}.
$$

$$
\boxed{\vec F_{\mathrm{pseudo}}=-m\vec a_0}
\quad \text{(translating, nonrotating accelerating frame).}
$$

## Circular motion (Chapter 7)

$$
\boxed{\omega=\frac{d\theta}{dt}},
\qquad
\boxed{\alpha=\frac{d\omega}{dt}},
\qquad
\boxed{v=r|\omega|}.
$$

$$
\boxed{a_c=\frac{v^2}{r}=r\omega^2},
\qquad
\boxed{a_t=r\alpha},
\qquad
\boxed{\sum F_{\mathrm{in}}=\frac{mv^2}{r}}.
$$

$$
\boxed{v_{\mathrm{level,max}}=\sqrt{\mu_srg}},
\qquad
\boxed{\tan\theta_{\mathrm{bank}}=\frac{v^2}{rg}}.
$$

## Work and energy (Chapter 8)

$$
\boxed{W=\int\vec F\cdot d\vec r},
\qquad
\boxed{P=\vec F\cdot\vec v},
\qquad
\boxed{W_{\mathrm{net}}=\Delta K}.
$$

$$
\boxed{K=\frac12mv^2},
\qquad
\boxed{U_g=mgh+C},
\qquad
\boxed{U_s=\frac12kx^2}.
$$

$$
\boxed{\vec F_c=-\nabla U},
\qquad
\boxed{\Delta(K+U)=W_{nc}}.
$$

$$
\boxed{K_i+U_i=K_f+U_f}
\quad\text{when nonconservative work is zero.}
$$

## Systems, momentum and collisions (Chapter 9)

$$
\boxed{\vec R_{\mathrm{CM}}=\frac1M\sum m_i\vec r_i},
\qquad
\boxed{\vec P=M\vec V_{\mathrm{CM}}}.
$$

$$
\boxed{\sum\vec F_{\mathrm{ext}}=\frac{d\vec P}{dt}},
\qquad
\boxed{\vec J=\Delta\vec P}.
$$

$$
\boxed{\Delta v_{\mathrm{rocket}}=u_e\ln\left(\frac{m_0}{m_f}\right)}
\quad\text{(ideal, constant-exhaust-speed rocket).}
$$

$$
\boxed{m_1u_1+m_2u_2=m_1v_1+m_2v_2}
\quad\text{(isolated 1D collision).}
$$

$$
\boxed{e=\frac{v_2-v_1}{u_1-u_2}}
\quad\text{(specified 1D approach/separation convention).}
$$

$$
\boxed{v_{\mathrm{stick}}=\frac{m_1u_1+m_2u_2}{m_1+m_2}}.
$$

## Rotational mechanics (Chapter 10)

$$
\boxed{\vec\tau=\vec r\times\vec F},
\qquad
\boxed{I=\int r_\perp^2\,dm},
\qquad
\boxed{\tau_{\mathrm{axis}}=I_{\mathrm{axis}}\alpha}.
$$

$$
\boxed{\vec L_O=\vec r\times\vec p},
\qquad
\boxed{\frac{d\vec L_O}{dt}=\vec\tau_O},
\qquad
\boxed{L_{\mathrm{axis}}=I_{\mathrm{axis}}\omega}.
$$

$$
\boxed{K_{\mathrm{rot}}=\frac12I\omega^2},
\qquad
\boxed{W_{\mathrm{rot}}=\int\tau\,d\theta},
\qquad
\boxed{P_{\mathrm{rot}}=\tau\omega}.
$$

$$
\boxed{I_O=I_{\mathrm{CM}}+Md^2},
\qquad
\boxed{I_z=I_x+I_y\ \text{(planar lamina)}}.
$$

$$
\boxed{\vec v_P=\vec V_{\mathrm{CM}}+\vec\omega\times\vec r_{P/\mathrm{CM}}}.
$$

$$
\boxed{K_{\mathrm{rigid}}=\frac12MV_{\mathrm{CM}}^2+\frac12I_{\mathrm{CM}}\omega^2}.
$$

$$
\boxed{v_{\mathrm{CM}}=R\omega},
\qquad
\boxed{a_{\mathrm{roll}}=\frac{g\sin\theta}{1+I_{\mathrm{CM}}/(MR^2)}}.
$$

## Dimensional and sign-consistency checks

| Quantity | Dimensions | SI unit |
|---|---|---|
| Velocity | $LT^{-1}$ | m/s |
| Acceleration | $LT^{-2}$ | m/s² |
| Force | $MLT^{-2}$ | N |
| Linear momentum | $MLT^{-1}$ | kg·m/s |
| Impulse | $MLT^{-1}$ | N·s |
| Work/energy | $ML^2T^{-2}$ | J |
| Power | $ML^2T^{-3}$ | W |
| Torque | $ML^2T^{-2}$ | N·m |
| Moment of inertia | $ML^2$ | kg·m² |
| Angular momentum | $ML^2T^{-1}$ | kg·m²/s |
| Angular speed | $T^{-1}$ | rad/s |
| Angular acceleration | $T^{-2}$ | rad/s² |

**Remember:** equal dimensions do not imply identical physics. Torque and energy share dimensions but represent different concepts.

---

# Integrated Worked Examples

These original examples deliberately combine multiple chapters, as the later HCV exercises often do.

## Example A: Block slides and compresses a spring

**Problem.** A block of mass `m` enters a horizontal rough region at speed `u` and compresses a spring of stiffness `k`. The kinetic friction coefficient on the horizontal surface is `μ_k`. Find the maximum compression `x` if the block remains in sliding contact throughout compression.

**System:** block + spring + Earth. At maximum compression, block speed is zero. Kinetic friction transfers mechanical energy out of the block-spring mechanical subsystem.

$$
\frac12mu^2=\frac12kx^2+\mu_kmgx.
$$

Rearrange as a quadratic:

$$
kx^2+2\mu_kmgx-mu^2=0.
$$

Choose the physically nonnegative root:

$$
\boxed{x=\frac{-\mu_kmg+\sqrt{\mu_k^2m^2g^2+kmu^2}}{k}}.
$$

**Checks:** as `μ_k→0`, this becomes `x=u√(m/k)`. Greater friction reduces compression. If the spring starts elsewhere or other forces act, the energy equation changes.

## Example B: A car rounds a curve and then brakes

**Problem.** A car of mass `m` travels at speed `v` on a level circular road of radius `r`, then exits the curve onto a straight, level road and brakes with a maximum friction coefficient `μ`. Analyze the two phases separately.

**Turning phase:** static tire-road friction supplies inward acceleration:

$$
\frac{mv^2}{r}\le\mu mg
\quad\Longrightarrow\quad
\boxed{v\le\sqrt{\mu rg}}.
$$

**Straight braking phase:** assume friction-limited constant deceleration of magnitude `μg`, with wheel-road interaction sufficient to realize that force:

$$
0=v^2-2\mu gd
\quad\Longrightarrow\quad
\boxed{d=\frac{v^2}{2\mu g}}.
$$

These are **different constraints** in two separate phases. During simultaneous turning and braking, lateral and longitudinal tire force demands compete, and using both friction maxima independently is generally incorrect.

## Example C: Ballistic pendulum

**Problem.** A small projectile of mass `m` at speed `u` embeds in a stationary pendulum bob of mass `M`. Together they rise by height `h`. Determine the projectile speed, assuming negligible external horizontal impulse *during impact* and negligible mechanical losses *during the subsequent swing*.

**Stage 1, impact:** mechanical energy is not conserved because the impact is perfectly inelastic, but horizontal momentum is approximately conserved:

$$
mu=(M+m)V
\quad\Longrightarrow\quad
V=\frac{mu}{M+m}.
$$

**Stage 2, swing:** after impact, mechanical energy is conserved under the swing assumptions:

$$
\frac12(M+m)V^2=(M+m)gh
\quad\Longrightarrow\quad
V=\sqrt{2gh}.
$$

Combine stages:

$$
\boxed{u=\frac{M+m}{m}\sqrt{2gh}}.
$$

**Lesson:** conservation laws depend on the **stage and system**. Momentum through impact and energy through the later swing are not interchangeable.

## Example D: A disk rolls downhill

**Problem.** A uniform solid disk rolls from rest down an incline of angle `θ` through a vertical drop `h`, without slipping. Find its linear acceleration and speed after the drop.

For a solid disk,

$$
I_{\mathrm{CM}}=\frac12MR^2.
$$

From the rotational and translational balances,

$$
\boxed{a=\frac{g\sin\theta}{1+1/2}=\frac23g\sin\theta}.
$$

From energy conservation,

$$
Mgh=\frac12Mv^2+\frac12\left(\frac12MR^2\right)\frac{v^2}{R^2}
=\frac34Mv^2.
$$

Hence

$$
\boxed{v=\sqrt{\frac{4gh}{3}}}.
$$

The acceleration and energy methods agree. The pure-rolling assumption must still satisfy the available static-friction bound.

---

# Common Misconceptions and Diagnostic Questions

| Misconception | Correct principle |
|---|---|
| "Velocity is zero at the top, so acceleration is zero." | At the top of a projectile's arc, vertical velocity can vanish while gravitational acceleration remains downward. |
| "Negative acceleration means slowing down." | It means acceleration along the negative chosen axis; the effect on speed depends on velocity direction. |
| "A moving body must have a net forward force." | Constant-velocity motion needs zero net force in an inertial frame. |
| "Normal reaction always equals weight." | It is set by normal-direction dynamics and other forces. |
| "Friction always opposes the body's velocity." | Friction opposes relative slipping or its tendency at the contact. |
| "Static friction is always μsN." | That is a limiting magnitude; static friction generally adjusts below it. |
| "Centripetal force is separate from tension/friction/gravity." | It describes the net inward component of actual forces. |
| "Centrifugal force is real in every reference frame." | It appears as a pseudo force in a rotating-frame formulation. |
| "Mechanical energy is conserved in every collision." | An isolated collision conserves momentum; kinetic energy is conserved only for elastic collisions. |
| "Internal forces never affect energy." | Internal forces can do work when constituent particles displace differently. |
| "Same momentum means same kinetic energy." | Momentum scales as `mv`, kinetic energy as `mv²/2`. |
| "Torque depends only on force magnitude." | It also depends on the moment arm and chosen reference axis. |
| "A body's moment of inertia is a single fixed number." | It changes when the reference axis changes. |
| "Angular momentum always points along angular velocity." | The full vectors need not align for general 3D rigid bodies. |
| "Static friction can never be involved in rolling." | It may be required to enforce no slip and produce angular acceleration. |
| "A wheel's bottom point has zero acceleration if it has zero speed." | Zero instantaneous speed at contact does not imply zero acceleration of that material point. |

---

# Active-Recall Checkpoints

Try these *without* looking at the formula sheet. Where possible, derive a result rather than recalling it from memory.

### Chapter 3: Kinematics

1. Explain why a book can be at rest in one frame and in motion in another.
2. Construct a path for which total distance is positive but net displacement is zero.
3. Why can average speed differ from the magnitude of average velocity?
4. Derive the velocity and position equations for constant acceleration using calculus.
5. Derive the relation between `v²`, `u²`, acceleration and displacement without explicitly using time.
6. Explain why a projectile's velocity is horizontal at its highest point but its acceleration is not zero.
7. Derive the ideal projectile's trajectory equation from its `x(t)` and `y(t)` components.
8. Under which assumptions are complementary launch angles guaranteed to give equal horizontal ranges?
9. Derive the relative-velocity formula for two observers related by a nonrotating translating frame.

### Chapters 4–5: Forces and Newton's laws

10. For a normal force, identify the *agent*, *recipient*, and direction of application.
11. What distinguishes a gravitational force from a normal or frictional contact force at a microscopic level?
12. Why is it useful to isolate a body before drawing force vectors?
13. Explain why an action-reaction pair does not cancel in a single body's free-body diagram.
14. Derive the acceleration of a two-mass Atwood machine and state its idealizations.
15. Why is `N=mg` not always valid for a block on a horizontal surface?
16. Derive the pseudo-force expression for a frame translating with acceleration `a_0`.
17. Resolve the horse-cart paradox by treating the horse and cart as one system.

### Chapter 6: Friction

18. What determines the actual magnitude of static friction below impending slip?
19. How do you choose the direction of friction for a contact that has no sliding?
20. Derive the angle-of-repose relation for a block on a rough incline.
21. Explain why pulling upward on a block can lower sliding resistance relative to pushing downward.
22. Describe two laboratory methods to estimate friction coefficients and their main assumptions.

### Chapters 7–8: Circular motion, work and energy

23. Derive radial acceleration by differentiating the rotating radial unit vector.
24. Why does uniform circular motion require a resultant force even at constant speed?
25. Derive the friction-limited turning-speed formula for a car on a level curve.
26. How does bank angle modify the need for lateral friction?
27. What is the distinction between centripetal acceleration and centrifugal pseudo force?
28. Derive the work-energy theorem from Newton's second law.
29. Explain how an internal force can do work yet cancel from the total force of a system.
30. Derive spring potential energy from Hooke's law.
31. What condition makes potential energy depend only on endpoints rather than path?
32. How do you test whether mechanical energy, rather than total energy, is conserved?

### Chapters 9–10: Systems and rotation

33. Derive center-of-mass position for a collection of discrete particles.
34. Demonstrate that internal forces cancel in the total momentum balance of a fixed-mass system.
35. Why is momentum conserved during an approximately isolated collision even when kinetic energy is not?
36. Derive the final shared velocity of two bodies in a perfectly inelastic collision.
37. Show why equal-mass, elastic two-dimensional collisions with one initially stationary particle give perpendicular outgoing velocities (when both are nonzero).
38. Explain the meaning and units of impulse.
39. Explain why a rocket can propel itself in vacuum and derive the logarithm in the ideal rocket equation.
40. Derive moment of inertia of a uniform rod about its midpoint using an integral.
41. Why does shifting a rotation axis away from the center of mass increase moment of inertia for parallel axes?
42. Derive the rotational kinetic-energy formula from the kinetic energies of constituent particles.
43. Describe a process in which angular momentum is conserved but rotational kinetic energy changes.
44. What are the separate conditions for translation and rotation equilibrium of a rigid body?
45. Derive the rolling-without-slipping acceleration down an incline.
46. How can a wheel have zero instantaneous speed at its lowest point while its top point moves at twice the CM speed?
47. Explain how rolling resistance can slow a sphere even without kinetic sliding friction.
48. For a rolling disk, explain why `K` contains both translational and rotational terms.

---

## Source and scope

- **Primary source:** H. C. Verma, *Concepts of Physics*, Volume 1.
- **Chapter 3:** *Rest and Motion: Kinematics*, textbook pp. 31–55 (PDF pp. 41–65).
- **Chapter 4:** *The Forces*, textbook pp. 56–63 (PDF pp. 66–73).
- **Chapter 5:** *Newton's Laws of Motion*, textbook pp. 64–84 (PDF pp. 74–94).
- **Chapter 6:** *Friction*, textbook pp. 85–100 (PDF pp. 95–110).
- **Chapter 7:** *Circular Motion*, textbook pp. 101–117 (PDF pp. 111–127).
- **Chapter 8:** *Work and Energy*, textbook pp. 118–138 (PDF pp. 128–148).
- **Chapter 9:** *Centre of Mass, Linear Momentum, Collision*, textbook pp. 139–165 (PDF pp. 149–175).
- **Chapter 10:** *Rotational Mechanics*, textbook pp. 166–202 (PDF pp. 176–212).
- The sequence and principal subjects follow HCV sections **3.1–10.20**. Explanations and integrated examples are independently written and condensed for revision rather than transcribed. Derivations, qualifications, and additional examples sometimes elaborate on the book's introductory treatment; where a formula requires an idealization, that assumption is stated.
- **Next:** Chapter 11, *Gravitation*.
