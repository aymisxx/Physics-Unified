# Unit 00: Prerequisites

**Introduction to Physics & Physics and Mathematics**  
*Original revision notes following Chapters 1–2 of H. C. Verma, Concepts of Physics, Volume 1*

> **Purpose.** Establish the language, measurement conventions and mathematical machinery required for the rest of the physics course. These are independently written study notes, not a transcription of the textbook. Section numbers follow HCV to make cross-referencing easy.
>
> **Notation.** Equations intended for display are enclosed in `$$ ... $$`, compatible with GitHub Markdown math rendering. Unless specified otherwise, quantities use SI units.

## Roadmap

| Part | HCV chapter | Focus |
|---|---|---|
| **I** | **1. Introduction to Physics** | Physical laws, units, dimensions, estimation and the structure of matter |
| **II** | **2. Physics and Mathematics** | Vectors, differentiation, integration, significant figures and measurement errors |

**Learning sequence**

```text
Nature and observation
       |
       v
Physical quantities --> Units and dimensions --> Dimensional consistency
       |                                            |
       v                                            v
Scalars and vectors --> Vector operations --> Mathematical models
                                                /          \
                                               v            v
                                         Derivatives     Integrals
                                               \            /
                                                v          v
                                       Measurement and uncertainty
                                                |
                                                v
                                       Kinematics (Chapter 3)
```

---

# Part I: Introduction to Physics

## 1.1 What Is Physics?

Physics seeks general principles that describe and predict natural phenomena. Observations are the starting point: a falling object, the Moon's orbit and ocean tides may appear unrelated, but a small set of laws can describe all three.

A useful picture of scientific reasoning is **observation → hypothesis → prediction → test → revision**. A model is valuable when it explains existing measurements and makes successful predictions. If new observations disagree with it, we investigate the assumptions, range of validity or the model itself.

**Important distinctions**

- A **physical observation** records what happens.
- A **physical law** summarizes a pattern or relation supported by evidence.
- A **model** uses idealizations to describe a physical system.
- A **prediction** is what the model says should occur under specified conditions.

A law is not made true by an authority or by mathematical elegance. Nature remains the test.

## 1.2 Physics and Mathematics

Mathematics makes physical relationships compact and allows quantitative predictions. Consider the magnitude of the gravitational attraction of two point masses separated by distance `r`:

$$
F\propto\frac{m_1m_2}{r^2}.
$$

In a complete model, the proportionality becomes an equation involving the gravitational constant:

$$
F=G\frac{m_1m_2}{r^2}.
$$

Mathematics expresses the physical rule; it does not replace the physical meaning or the assumptions behind it. For example, calculus can combine the contributions of many small mass elements to calculate the net attraction exerted by an extended body.

**Working principle:** first identify the physical system and assumptions; then select the mathematics that describes them.

## 1.3 Units

### Physical quantities and measurements

A measurement compares an unknown quantity with a chosen standard. It contains a **numerical value** and a **unit**:

$$
\text{Physical quantity}=(\text{number})\times(\text{unit}).
$$

Thus, `5 m` and `500 cm` represent the same length. Changing the unit changes the number, not the measured length.

### Fundamental and derived quantities

A set of fundamental quantities is chosen so that its members are independent and other quantities can be expressed using them.

The seven SI base quantities are:

| Base quantity | SI unit | Symbol |
|---|---|---|
| Length | metre | m |
| Mass | kilogram | kg |
| Time | second | s |
| Electric current | ampere | A |
| Thermodynamic temperature | kelvin | K |
| Amount of substance | mole | mol |
| Luminous intensity | candela | cd |

Derived units come from combinations of base units:

$$
[\text{speed}] = \mathrm{m\,s^{-1}},\qquad
[\text{acceleration}] = \mathrm{m\,s^{-2}}.
$$

$$
1\,\mathrm{N}=1\,\mathrm{kg\,m\,s^{-2}},
\qquad
1\,\mathrm{J}=1\,\mathrm{kg\,m^2\,s^{-2}}.
$$

Plane and solid angles use the named units **radian (`rad`)** and **steradian (`sr`)**, respectively.

### Why standards matter

A useful standard should be internationally agreed upon, stable, and reproducible. The General Conference on Weights and Measures (CGPM) coordinates the internationally agreed measurement system.

### Common SI prefixes

| Factor | Prefix | Symbol | Factor | Prefix | Symbol |
|---:|---|:---:|---:|---|:---:|
| 10¹⁸ | exa | E | 10⁻¹ | deci | d |
| 10¹⁵ | peta | P | 10⁻² | centi | c |
| 10¹² | tera | T | 10⁻³ | milli | m |
| 10⁹ | giga | G | 10⁻⁶ | micro | µ |
| 10⁶ | mega | M | 10⁻⁹ | nano | n |
| 10³ | kilo | k | 10⁻¹² | pico | p |
| 10² | hecto | h | 10⁻¹⁵ | femto | f |
| 10¹ | deka | da | 10⁻¹⁸ | atto | a |

For example:

$$
1\,\mathrm{mm}=10^{-3}\,\mathrm{m},\qquad
1\,\mathrm{\mu F}=10^{-6}\,\mathrm{F}.
$$

**Attention:** upper- and lower-case letters matter. `M` (mega) and `m` (milli) differ by a factor of a billion.

## 1.4 Definitions of Base Units

Modern SI definitions fix the numerical values of selected physical constants. HCV's edition incorporates the definitions that took effect in May 2019.

| Unit | Defining reference | Fixed defining value |
|---|---|---|
| Second (`s`) | Caesium-133 hyperfine transition frequency | $\Delta\nu_{\mathrm{Cs}}=9\,192\,631\,770\,\mathrm{Hz}$ |
| Metre (`m`) | Speed of light in vacuum | $c=299\,792\,458\,\mathrm{m\,s^{-1}}$ |
| Kilogram (`kg`) | Planck constant | $h=6.62607015\times10^{-34}\,\mathrm{J\,s}$ |
| Ampere (`A`) | Elementary charge | $e=1.602176634\times10^{-19}\,\mathrm{C}$ |
| Kelvin (`K`) | Boltzmann constant | $k_{\mathrm B}=1.380649\times10^{-23}\,\mathrm{J\,K^{-1}}$ |
| Mole (`mol`) | Avogadro constant | $N_{\mathrm A}=6.02214076\times10^{23}\,\mathrm{mol^{-1}}$ |
| Candela (`cd`) | Luminous efficacy of specified monochromatic radiation | $K_{\mathrm{cd}}=683\,\mathrm{lm\,W^{-1}}$ |

For the candela definition, the radiation frequency is fixed at **540 × 10¹² Hz**. These constants connect standards to reproducible physical phenomena instead of relying on particular manufactured objects.

## 1.5 Dimension

The **dimension** of a physical quantity specifies how it depends on chosen base quantities. In mechanics, we usually use:

- `M`: mass
- `L`: length
- `T`: time

A dimension is different from a unit. The dimension of speed is the same whether speed is expressed in metres per second or kilometres per hour.

Starting with force as mass multiplied by acceleration:

$$
F=ma,
\qquad
[a]=LT^{-2},
$$

we obtain

$$
[F]=MLT^{-2}.
$$

Likewise, energy has dimensions

$$
[E]=[mv^2]=ML^2T^{-2}.
$$

The pure numerical coefficient in kinetic energy does not affect its dimensions:

$$
K=\frac12 mv^2
\quad\Longrightarrow\quad
[K]=ML^2T^{-2}.
$$

### Small dimensional reference table

| Quantity | Defining relation | Dimensions |
|---|---|---|
| Area | length × length | $L^2$ |
| Volume | length³ | $L^3$ |
| Velocity | displacement / time | $LT^{-1}$ |
| Acceleration | velocity / time | $LT^{-2}$ |
| Force | mass × acceleration | $MLT^{-2}$ |
| Momentum | mass × velocity | $MLT^{-1}$ |
| Work/energy | force × distance | $ML^2T^{-2}$ |
| Power | energy / time | $ML^2T^{-3}$ |
| Pressure | force / area | $ML^{-1}T^{-2}$ |
| Density | mass / volume | $ML^{-3}$ |
| Gravitational constant | force × distance² / mass² | $M^{-1}L^3T^{-2}$ |

**Check:** the symbol in square brackets means *dimensions of*, not numerical magnitude.

## 1.6 Uses of Dimension

### A. Checking dimensional homogeneity

Every term added, subtracted or equated in a physical equation must have compatible dimensions. For constant acceleration, consider

$$
x=ut+\frac12 at^2.
$$

Here

$$
[x]=L,\qquad [ut]=(LT^{-1})T=L,
$$

$$
[at^2]=(LT^{-2})T^2=L.
$$

All three terms are lengths, so the equation **passes** this dimensional test.

**Critical limitation:** passing the test does **not** prove an equation is correct. Replacing `1/2` with `7` leaves its dimensions unchanged but generally destroys its physical validity.

### B. Converting units

If a quantity has dimensions

$$
[Q]=M^aL^bT^c,
$$

its unit-conversion factor is the product of the conversion factors for mass, length and time raised to the corresponding powers.

For pressure:

$$
[P]=ML^{-1}T^{-2}.
$$

Since `1 kg = 10³ g` and `1 m = 10² cm`,

$$
1\,\mathrm{Pa}
=1\,\mathrm{kg\,m^{-1}\,s^{-2}}
=10\,\mathrm{g\,cm^{-1}\,s^{-2}}
=10\,\mathrm{dyn\,cm^{-2}}.
$$

Similarly,

$$
1\,\mathrm{J}=10^7\,\mathrm{erg}.
$$

### C. Deducing the form of a relation

Suppose the period `T_p` of a small-angle simple pendulum depends on its length `l`, bob mass `m` and gravitational acceleration `g`. Assume a product of powers:

$$
T_p=kl^am^bg^c,
$$

where `k` is dimensionless. Comparing dimensions,

$$
T=M^bL^{a+c}T^{-2c}.
$$

Equating exponents gives

$$
b=0,\qquad a+c=0,\qquad -2c=1.
$$

Therefore,

$$
a=\frac12,\qquad b=0,\qquad c=-\frac12,
$$

and the dependence is

$$
\boxed{T_p=k\sqrt{\frac{l}{g}}}.
$$

The reasoning predicts that the period is independent of bob mass and grows with the square root of length. **Dimensional analysis cannot determine `k`.** For an ideal small-angle pendulum, further physics gives `k = 2π`.

### D. Limits of dimensional analysis

1. It cannot determine pure numerical factors such as `1/2` or `2π`.
2. It cannot by itself identify which physical variables should enter a model.
3. It cannot generally reconstruct a sum of different terms from a single guessed product.
4. If there are more unknown exponents than independent dimensional equations, the powers may not be uniquely determined.

**Mental model:** dimensional analysis is a powerful consistency filter, not a complete theory of the system.

## 1.7 Order of Magnitude

Physics spans enormous ranges of size, mass and time. Scientific notation expresses a positive number as

$$
Q=a\times10^n,\qquad 1\le a<10.
$$

An **order-of-magnitude estimate** captures the approximate power of ten rather than fine numerical detail. HCV rounds the coefficient to `1` or `10` to estimate a nearby power of ten.

For a rough count of people in a circular area, divide the area available by the approximate space occupied by each person:

$$
N\approx\frac{\pi R^2}{A_{\mathrm{person}}}.
$$

Using a field radius of `800 m` and about `0.25 m²` per seated person,

$$
N\approx\frac{\pi(800)^2}{0.25}
\approx8\times10^6
\sim10^7.
$$

This estimate ignores aisles, obstacles and crowd-safety constraints. It is an **order-of-magnitude calculation**, not a seating plan.

**Good estimating practice:** write the formula, identify dominant quantities, round sensible inputs and check the resulting units.

## 1.8 The Structure of World

Matter that appears continuous at everyday scales has microscopic structure:

```text
Everyday objects
    --> molecules
         --> atoms
              --> electrons and atomic nuclei
                   --> protons, neutrons and other particles
```

The historical development of atomic physics revealed that proton, neutron and electron are not the entire inventory of nature. HCV emphasizes that classical descriptions useful for macroscopic objects do not automatically extend to atoms, nuclei or elementary particles.

**Scale matters.** A "particle" in classical mechanics is often an idealized object whose dimensions are negligible for the problem at hand. It need not be a fundamental particle; a dust grain can be modeled as a point particle when its internal structure does not matter.

### Part I: Key takeaways

- Physics discovers testable patterns in nature; mathematics provides a way to express and use them.
- Physical quantities require well-defined units.
- Dimensions describe the type of quantity, independent of the chosen units.
- Dimensional consistency can reject incorrect expressions but cannot establish their correctness.
- Order-of-magnitude reasoning is useful whenever precise inputs are unavailable or unnecessary.

---

# Part II: Physics and Mathematics

## 2.1 Vectors and Scalars

A **scalar** is specified by magnitude (with units, when applicable) and follows ordinary scalar addition. Examples include mass, temperature, time and energy.

A **vector** has magnitude and direction **and obeys vector addition**. Examples include displacement, velocity, force, momentum and electric field.

The final condition matters. A conventional electric current along a wire has an associated direction of flow, but it is not treated as a vector under the triangle law of addition.

### Geometric meaning

Represent a vector by an arrow. Its length on the diagram is proportional to magnitude; the arrowhead marks direction.

If a ball moves at `3 m/s` along a tube while the tube moves at `4 m/s` perpendicular to the tube, the ball's velocity relative to the room is the vector sum:

$$
|\vec v|=\sqrt{3^2+4^2}=5\,\mathrm{m\,s^{-1}}.
$$

The resultant direction relative to the `3 m/s` direction satisfies

$$
\tan\theta=\frac43.
$$

## 2.2 Equality of Vectors

Two vectors of the **same physical kind** are equal when both magnitude and direction are equal. Translating an arrow without rotating or resizing it does not change the vector it represents.

$$
\vec A=\vec B
\quad\Longleftrightarrow\quad
|\vec A|=|\vec B|\ \text{and their directions agree}.
$$

For free-vector calculations, the arrow's location is unimportant. Physical applications may impose additional information about *where* a force acts; that information is not encoded in the free vector alone.

## 2.3 Addition of Vectors

### Triangle and parallelogram rules

For the triangle rule, place the tail of `B` at the head of `A`; the arrow from the first tail to the final head is the resultant. Equivalently, draw both arrows from one origin and take the parallelogram diagonal.

For magnitudes `a` and `b` with angle `θ` between them,

$$
\boxed{|\vec a+\vec b|=\sqrt{a^2+b^2+2ab\cos\theta}}.
$$

This follows by resolving `b` parallel and perpendicular to `a`:

$$
R_x=a+b\cos\theta,\qquad R_y=b\sin\theta,
$$

$$
R^2=R_x^2+R_y^2=a^2+b^2+2ab\cos\theta.
$$

The angle `α` measured from `a` toward `b` obeys

$$
\boxed{\tan\alpha=\frac{b\sin\theta}{a+b\cos\theta}}.
$$

For complete quadrant handling, check the signs of both components instead of relying on the inverse tangent alone.

**Useful special cases**

| Relationship | Magnitude of resultant |
|---|---|
| Same direction | $a+b$ |
| Opposite directions | $|a-b|$ |
| Perpendicular | $\sqrt{a^2+b^2}$ |
| Equal magnitudes `A`, angle `θ` | $2A\cos(\theta/2)$ |

For two equal vectors with `0 ≤ θ ≤ 180°`, the resultant bisects their angle (except when they cancel exactly and have no resultant direction).

## 2.4 Multiplication of a Vector by a Number

Multiplying a vector by a scalar `k` changes its magnitude by `|k|`. Its direction is preserved when `k > 0` and reversed when `k < 0`.

$$
\vec b=k\vec a,\qquad |\vec b|=|k|\,|\vec a|.
$$

If `\hat u` is a unit vector in the direction of `\vec a`,

$$
\vec a=a\hat u,\qquad |\hat u|=1.
$$

## 2.5 Subtraction of Vectors

Subtracting a vector means adding its reverse:

$$
\boxed{\vec a-\vec b=\vec a+(-\vec b)}.
$$

The squared magnitude of the difference is

$$
|\vec a-\vec b|^2=a^2+b^2-2ab\cos\theta.
$$

**Example:** two vectors of magnitude `5` at `60°` give

$$
|\vec a+\vec b|=5\sqrt3,\qquad
|\vec a-\vec b|=5.
$$

## 2.6 Resolution of Vectors

A vector can be decomposed into components along perpendicular coordinate axes. In two dimensions,

$$
\vec a=a_x\hat i+a_y\hat j,
$$

with

$$
a_x=a\cos\theta,\qquad a_y=a\sin\theta
$$

when `θ` is measured counterclockwise from the positive `x` axis.

In three dimensions,

$$
\boxed{\vec a=a_x\hat i+a_y\hat j+a_z\hat k}.
$$

If `α`, `β`, `γ` are the angles with the positive coordinate axes, then

$$
a_x=a\cos\alpha,\quad
a_y=a\cos\beta,\quad
a_z=a\cos\gamma.
$$

Consequently,

$$
a=\sqrt{a_x^2+a_y^2+a_z^2},
$$

$$
\cos^2\alpha+\cos^2\beta+\cos^2\gamma=1.
$$

Vector addition reduces to ordinary addition of corresponding components:

$$
\vec R=\vec a+\vec b
=(a_x+b_x)\hat i+(a_y+b_y)\hat j+(a_z+b_z)\hat k.
$$

**Worked example:** a `10.5 N` force inclined at `37°` to the vertical has vertical component

$$
F_y=10.5\cos37^\circ\approx8.4\,\mathrm N.
$$

The sign of a component depends on the selected positive axis.

## 2.7 Dot Product or Scalar Product of Two Vectors

The dot product is a **scalar**:

$$
\boxed{\vec a\cdot\vec b=ab\cos\theta}.
$$

Interpretation: multiply the magnitude of one vector by the component of the other **along** it.

For Cartesian components,

$$
\boxed{\vec a\cdot\vec b=a_xb_x+a_yb_y+a_zb_z}.
$$

This follows because the unit vectors obey

$$
\hat i\cdot\hat i=\hat j\cdot\hat j=\hat k\cdot\hat k=1,
$$

$$
\hat i\cdot\hat j=\hat j\cdot\hat k=\hat k\cdot\hat i=0.
$$

### Properties and physics connection

$$
\vec a\cdot\vec b=\vec b\cdot\vec a,
$$

$$
\vec a\cdot(\vec b+\vec c)=\vec a\cdot\vec b+\vec a\cdot\vec c.
$$

The dot product is zero for nonzero perpendicular vectors. Work done by a constant force over a displacement is

$$
W=\vec F\cdot\vec s=Fs\cos\theta.
$$

For an upward force of `12 N` and a downward displacement of `2 m`,

$$
W=(12)(2)\cos180^\circ=-24\,\mathrm J.
$$

The negative sign means the force component opposes the displacement.

## 2.8 Cross Product or Vector Product of Two Vectors

The cross product is a **vector** perpendicular to the plane of its two inputs:

$$
\boxed{|\vec a\times\vec b|=ab\sin\theta}.
$$

Its direction follows the **right-hand rule**. Reversing the order reverses the direction:

$$
\vec a\times\vec b=-\vec b\times\vec a.
$$

For a right-handed Cartesian system,

$$
\hat i\times\hat j=\hat k,\quad
\hat j\times\hat k=\hat i,\quad
\hat k\times\hat i=\hat j.
$$

Reversed pairs have a minus sign, while the cross product of a basis vector with itself vanishes.

### Component formula

For

$$
\vec a=(a_x,a_y,a_z),\qquad \vec b=(b_x,b_y,b_z),
$$

we obtain

$$
\boxed{\begin{aligned}
\vec a\times\vec b={}&(a_yb_z-a_zb_y)\hat i\\
&+(a_zb_x-a_xb_z)\hat j\\
&+(a_xb_y-a_yb_x)\hat k.
\end{aligned}}
$$

The cross product is distributive:

$$
\vec a\times(\vec b+\vec c)
=\vec a\times\vec b+\vec a\times\vec c.
$$

But it is **not generally associative**:

$$
\vec a\times(\vec b\times\vec c)
\ne(\vec a\times\vec b)\times\vec c.
$$

It vanishes for parallel vectors. Its magnitude is greatest when the inputs are perpendicular. A later mechanics application is torque:

$$
\vec\tau=\vec r\times\vec F.
$$

This torque formula is a forward reference, not a separate topic developed in HCV Chapter 2.

### Zero vector

A zero vector has magnitude zero and no definite direction:

$$
\vec a+(-\vec a)=\vec0,\qquad
\vec a+\vec0=\vec a,
$$

$$
\vec a\times\vec0=\vec0.
$$

## 2.9 Differential Calculus: Derivative as a Rate Measurer

Suppose `y = f(x)`. Over a finite change,

$$
\text{average rate of change}=\frac{\Delta y}{\Delta x}.
$$

The **instantaneous** rate is the limiting slope:

$$
\boxed{\frac{dy}{dx}=
\lim_{\Delta x\to0}\frac{f(x+\Delta x)-f(x)}{\Delta x}}.
$$

Graphically, this is the slope of the tangent to the graph at the chosen point. Positive derivative means a locally increasing function; negative derivative means a locally decreasing function.

### Derivative from first principles

For the area of a square,

$$
A=L^2.
$$

If its side increases by `ΔL`,

$$
\Delta A=(L+\Delta L)^2-L^2
=2L\Delta L+(\Delta L)^2.
$$

Therefore,

$$
\frac{\Delta A}{\Delta L}=2L+\Delta L
\quad\Longrightarrow\quad
\boxed{\frac{dA}{dL}=2L}.
$$

### Common derivatives

| Function | Derivative |
|---|---|
| $x^n$ | $nx^{n-1}$ |
| $\sin x$ | $\cos x$ |
| $\cos x$ | $-\sin x$ |
| $\tan x$ | $\sec^2x$ |
| $\cot x$ | $-\csc^2x$ |
| $\sec x$ | $\sec x\tan x$ |
| $\csc x$ | $-\csc x\cot x$ |
| $e^x$ | $e^x$ |
| $\ln x$ | $1/x$ |

Angles in calculus formulas are expressed in radians.

### Differentiation rules

For constant `c` and differentiable functions `u(x)` and `v(x)`:

$$
\frac{d(cu)}{dx}=c\frac{du}{dx},
\qquad
\frac{d(u+v)}{dx}=\frac{du}{dx}+\frac{dv}{dx}.
$$

$$
\boxed{\frac{d(uv)}{dx}=u\frac{dv}{dx}+v\frac{du}{dx}}
$$

$$
\boxed{\frac{d}{dx}\left(\frac uv\right)=
\frac{v\,du/dx-u\,dv/dx}{v^2}}.
$$

The chain rule is

$$
\boxed{\frac{dy}{dx}=\frac{dy}{du}\frac{du}{dx}}.
$$

**Example:**

$$
\frac{d}{dx}(e^x\sin x)
=e^x(\cos x+\sin x).
$$

## 2.10 Maxima and Minima

At a smooth **interior** local maximum or minimum, the graph's tangent is horizontal (provided the derivative exists):

$$
\frac{dy}{dx}=0.
$$

The second-derivative test distinguishes common cases:

$$
\left.\frac{d^2y}{dx^2}\right|_{x=x_0}<0
\quad\Longrightarrow\quad\text{local maximum},
$$

$$
\left.\frac{d^2y}{dx^2}\right|_{x=x_0}>0
\quad\Longrightarrow\quad\text{local minimum}.
$$

These tests are sufficient when their conditions hold, not necessary for every extremum. Endpoints and nondifferentiable points must be handled separately.

**Example: maximum height in vertical motion.** With upward initial velocity `u` and constant downward acceleration `g`,

$$
h(t)=ut-\frac12gt^2,
$$

$$
\frac{dh}{dt}=u-gt.
$$

Setting this to zero gives the time at maximum height:

$$
\boxed{t_{\mathrm{top}}=\frac ug}.
$$

Because the second derivative is negative,

$$
\frac{d^2h}{dt^2}=-g<0,
$$

the stationary point is a maximum.

## 2.11 Integral Calculus

Integration describes **accumulation**. If `y = f(x)` is nonnegative on an interval, the area under its graph can be approximated by many narrow rectangular strips:

$$
I_N=\sum_{i=1}^{N}f(x_i)\,\Delta x,
\qquad \Delta x=\frac{b-a}{N}.
$$

Taking narrower and more numerous strips gives the definite integral:

$$
\boxed{\int_a^b f(x)\,dx
=\lim_{N\to\infty}\sum_{i=1}^{N}f(x_i)\,\Delta x}.
$$

More generally, the definite integral is a **signed accumulation**; regions below the horizontal axis contribute negatively.

### Antiderivatives and the fundamental relationship

If `F'(x) = f(x)`, then

$$
\boxed{\int_a^b f(x)\,dx=F(b)-F(a)}.
$$

The indefinite integral is a family of antiderivatives:

$$
\int f(x)\,dx=F(x)+C.
$$

The arbitrary constant `C` disappears in a definite integral.

**Example:** for `f(x)=x`,

$$
\int_a^b x\,dx
=\left[\frac{x^2}{2}\right]_a^b
=\frac{b^2-a^2}{2}.
$$

This agrees with the elementary area of a trapezium under the straight line `y=x` (for a suitable nonnegative interval).

### Common integrals

| Integrand | Antiderivative (plus constant `C`) |
|---|---|
| $x^n\ (n\ne-1)$ | $\dfrac{x^{n+1}}{n+1}$ |
| $1/x$ | $\ln|x|$ |
| $\sin x$ | $-\cos x$ |
| $\cos x$ | $\sin x$ |
| $\sec^2x$ | $\tan x$ |
| $\csc^2x$ | $-\cot x$ |
| $\sec x\tan x$ | $\sec x$ |
| $\csc x\cot x$ | $-\csc x$ |
| $1/(x^2+a^2)$ | $\dfrac1a\tan^{-1}(x/a)\ (a>0)$ |
| $1/\sqrt{a^2-x^2}$ | $\sin^{-1}(x/a)\ (a>0)$ |

### Integration rules

$$
\int cf(x)\,dx=c\int f(x)\,dx,
$$

$$
\int[f(x)+g(x)]\,dx
=\int f(x)\,dx+\int g(x)\,dx.
$$

If `F'(x)=f(x)` and `c ≠ 0`, then

$$
\int f(cx)\,dx=\frac1c F(cx)+C.
$$

**Example:**

$$
\begin{aligned}
\int_3^6(2x^2+3x+5)\,dx
&=\left[\frac23x^3+\frac32x^2+5x\right]_3^6\\
&=181.5.
\end{aligned}
$$

### Why calculus belongs in physics

- **Differentiate** position to obtain velocity and velocity to obtain acceleration.
- **Integrate** velocity to obtain displacement and force over distance to obtain work in suitable one-dimensional situations.
- Always check the meaning and units of the differential, limits and integrand.

These are applications that will be developed in later chapters, especially kinematics.

## 2.12 Significant Digits

Every experimental measurement has finite precision. The reported digits ordinarily include the digits resolved by the instrument plus **one estimated (uncertain) final digit**.

Example: an object measured on a scale with millimetre markings might be reported as **10.46 cm**, where the last digit represents a finer visual estimate.

### Counting significant digits

| Written value | Significant digits | Reason |
|---|---:|---|
| `0.0023` | 2 | Leading zeros only locate the decimal point |
| `1.0023` | 5 | Zeros inside significant digits count |
| `6 × 10²` | 1 | Only `6` is stated precisely |
| `6.0 × 10²` | 2 | Trailing decimal zero is significant |
| `6.00 × 10²` | 3 | Both written decimal zeros are significant |

A bare number such as `600` may be ambiguous without information about how it was measured. Scientific notation makes the intended precision explicit.

**Least count** is the smallest marked or directly resolvable division of an instrument; it helps determine meaningful reporting precision.

## 2.13 Significant Digits in Calculations

### Multiplication and division

A calculated result should ordinarily retain the **smallest significant-figure count** among the measured input quantities.

Example:

$$
\frac{25.2\times1374}{33.3}
=1039.783\ldots
\approx1.04\times10^3
$$

The result is reported with **three significant figures**, the smallest count among the inputs.

### Addition and subtraction

Precision is constrained by the **least precise decimal place**, not simply by the smallest number of significant digits.

Example:

$$
24.36+0.0623+256.2=280.6223
\approx280.7.
$$

Because `256.2` is given only to tenths, the final sum is reported to tenths.

### Rounding

HCV uses the **round-to-even** convention for an exact trailing `5` in the rounding position:

- Next digit smaller than `5`: keep the retained digit.
- Next digit greater than `5`: increase the retained digit.
- Exact halfway case: choose the retained result whose final digit is even.

For three significant digits:

| Original number | Rounded value |
|---|---|
| `15462` | `15500` |
| `14.745` | `14.7` |
| `14.750` | `14.8` |
| `14.650 × 10¹²` | `14.6 × 10¹²` |

**Practical note:** preserve more digits during intermediate calculations and round when reporting the final result to avoid unnecessary rounding error.

## 2.14 Errors in Measurement

Measurements can differ from the desired value for several reasons:

- **Systematic sources:** a miscalibrated or unsuitable instrument, a consistent procedural bias, or a modeling assumption.
- **Human mistakes:** reading or recording an instrument incorrectly.
- **Random variation:** uncontrollable fluctuations that shift repeated observations in different directions.

Detecting and fixing an identifiable bias is different from estimating scatter across repeated trials.

### Repeated measurements and mean

For `N` measurements `x₁, x₂, ..., xₙ`, the arithmetic mean is

$$
\boxed{\bar x=\frac1N\sum_{i=1}^N x_i}.
$$

HCV defines a measure of scatter using

$$
\boxed{\sigma=\sqrt{\frac1N\sum_{i=1}^N(x_i-\bar x)^2}}.
$$

Here `σ` measures the spread of individual observations around their average, with the denominator `N` as presented in the textbook.

### HCV's repeated-measurement example

Ten reported measurements of a concave mirror's focal length (in cm) are:

`25.4, 25.2, 25.6, 25.1, 25.3, 25.2, 25.5, 25.4, 25.3, 25.7`.

For these data,

$$
\bar f=25.37\,\mathrm{cm}\approx25.4\,\mathrm{cm},
$$

and, using HCV's definition,

$$
\sigma\approx0.18\,\mathrm{cm}\approx0.2\,\mathrm{cm}.
$$

A compact report of the mean and observational scatter is

$$
\boxed{\bar f=25.4\,\mathrm{cm},\qquad \sigma\approx0.2\,\mathrm{cm}}.
$$

> **Statistical clarification (beyond the textbook):** HCV discusses intervals such as `mean ± 1.96σ` for a 95% chance of containing the true value. That statement is **not a generally valid 95% confidence interval for the population mean** when `σ` is the standard deviation of the individual readings. Under the usual independent, approximately normal-measurement model, uncertainty in the *mean* instead scales with the standard error, roughly `s/√N`, and an appropriate critical factor. The spread of observations and the uncertainty of their estimated mean are different concepts.

### Precision, accuracy and uncertainty

- **Precision** concerns how closely repeated readings cluster.
- **Accuracy** concerns agreement with an appropriate reference or accepted value.
- **Uncertainty** expresses the limited knowledge of the quantity being measured.

A cluster of repeatable measurements may still be biased. Taking more readings can reduce random uncertainty in their mean, but cannot automatically remove systematic error.

---

# Consolidated Formula Sheet

## Measurement, mechanics and dimensions

$$
[v]=LT^{-1},\quad [a]=LT^{-2},\quad [F]=MLT^{-2},
$$

$$
[p]=MLT^{-1},\quad [E]=ML^2T^{-2},\quad [P]=ML^2T^{-3}.
$$

$$
[F/A]=ML^{-1}T^{-2},\qquad
[G]=M^{-1}L^3T^{-2}.
$$

## Vector operations

$$
\vec a=a_x\hat i+a_y\hat j+a_z\hat k,
\qquad
a=\sqrt{a_x^2+a_y^2+a_z^2}.
$$

$$
|\vec a\pm\vec b|^2=a^2+b^2\pm2ab\cos\theta.
$$

$$
\vec a\cdot\vec b=ab\cos\theta=a_xb_x+a_yb_y+a_zb_z.
$$

$$
|\vec a\times\vec b|=ab\sin\theta.
$$

## Calculus

$$
\frac{dy}{dx}=\lim_{\Delta x\to0}\frac{\Delta y}{\Delta x},
\qquad
\int_a^b f(x)\,dx=F(b)-F(a).
$$

$$
\frac{d}{dx}x^n=nx^{n-1},
\qquad
\int x^n\,dx=\frac{x^{n+1}}{n+1}+C\quad(n\ne-1).
$$

## Repeated observations

$$
\bar x=\frac1N\sum_{i=1}^{N}x_i,
\qquad
\sigma=\sqrt{\frac1N\sum_{i=1}^{N}(x_i-\bar x)^2}.
$$

---

# Active-Recall Checkpoints

Try answering these without opening the notes.

1. Why is mathematics necessary but not sufficient for doing physics?
2. What is the difference between a unit and a dimension?
3. Can a dimensionally correct equation still be physically wrong? Give an example.
4. Why does dimensional analysis fail to determine the factor `2π` in a pendulum's period?
5. Why is electric current through a wire not classified as a vector in this treatment?
6. Derive the magnitude of the sum of two vectors separated by an angle `θ`.
7. Explain the difference between the dot product and the cross product, including their physical interpretations.
8. Why can the cross product change sign when its operands are reversed?
9. Derive `d(L²)/dL` directly from a small increment `ΔL`.
10. Explain differentiation as a limiting rate and integration as accumulated contributions.
11. When finding an extremum, why is checking only that the first derivative vanishes sometimes insufficient?
12. How does scientific notation remove ambiguity about significant zeros?
13. Why do multiplication and addition follow different significant-figure rules?
14. What does standard deviation measure, and how is it different from uncertainty in the mean?

---

## Source and scope

- **Primary source:** H. C. Verma, *Concepts of Physics*, Volume 1.
- **Chapter 1:** *Introduction to Physics*, textbook pp. 1–11 (PDF pp. 11–21).
- **Chapter 2:** *Physics and Mathematics*, textbook pp. 12–30 (PDF pp. 22–40).
- The sequence and principal topics follow HCV Sections **1.1–1.8** and **2.1–2.14**. Explanations are newly written and condensed for revision. Some clarifying remarks and later-application examples are explicitly identified where relevant.
- **Next:** Chapter 3, *Rest and Motion: Kinematics*.

---