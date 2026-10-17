# Unit 05: Electricity and Magnetism

**Electric Field and Potential → Gauss's Law → Capacitors → Electric Current → Thermal and Chemical Effects → Magnetic Fields → Permanent Magnets → Magnetic Matter → Electromagnetic Induction → Alternating Current → Electromagnetic Waves**  
*Original revision notes following Chapters 29–40 of H. C. Verma, Concepts of Physics, Volume 2*

> **Purpose.** Develop a coherent chain from stationary charges through currents, magnetic phenomena, induction, AC circuits, and finally electromagnetic waves. The sequence and numbered theory headings follow HCV; the explanations, worked examples, and recall prompts are independently written. These notes complement, rather than replace, the textbook's diagrams and exercises.
>
> **Notation and conventions.** SI units throughout. A vector has an arrow, e.g. $\vec E$; magnitudes are $E=|\vec E|$. $k_e=1/(4\pi\varepsilon_0)$, $\varepsilon_0$ is vacuum permittivity, and $\mu_0$ is vacuum permeability. $V$ means electric potential or voltage, while $U$ is potential energy; $q$ denotes electric charge; $Q$ can denote an aggregate charge; $I$ is current. $\Phi_E$ and $\Phi_B$ denote electric and magnetic flux. For sinusoidal circuits $i_0$ and $V_0$ are peak values, whereas $I$ and $V$ without subscript are ordinarily RMS values. Unless stated otherwise, magnetostatic and electrostatic results assume time-independent sources. **Every displayed equation uses `$$ ... $$` for GitHub rendering.**
>
> **Source fidelity.** The uploaded volume's table of contents has typographic numbering mistakes in Chapter 39 (it lists §39.5 as §39.6 and §39.10 as §38.10). The notes use the correctly sequenced §39.1–§39.12 headings from the chapter text, and identify assumptions when a concise model does not apply generally.

## Roadmap

| Part | HCV chapter | Central ideas |
|---|---|---|
| **I** | **29. Electric Field and Potential** | Charge, Coulomb interaction, fields, voltage, dipoles, conductors |
| **II** | **30. Gauss's Law** | Flux, solid angle, symmetry, charge distributions, grounding |
| **III** | **31. Capacitors** | Capacitance networks, dielectrics, stored electric energy, high voltage |
| **IV** | **32. Electric Current in Conductors** | Drift, resistance, Kirchhoff circuits, instruments, RC dynamics |
| **V** | **33. Thermal and Chemical Effects of Electric Current** | Joule heating, thermoelectric effects, electrolysis, cells |
| **VI** | **34. Magnetic Field** | Lorentz force, helical motion, force and torque on conductors |
| **VII** | **35. Magnetic Field due to a Current** | Biot–Savart, Ampère's law, wires, loops, solenoids, toroids |
| **VIII** | **36. Permanent Magnets** | Magnetic dipoles, terrestrial field, magnetometers and galvanometers |
| **IX** | **37. Magnetic Properties of Matter** | Magnetization, susceptibility, permeability, hysteresis |
| **X** | **38. Electromagnetic Induction** | Faraday–Lenz law, motional emf, inductance, LR transients |
| **XI** | **39. Alternating Current** | Generators, RMS, phasors, impedance, resonance, transformers |
| **XII** | **40. Electromagnetic Waves** | Displacement current, Maxwell equations, wave propagation, radiation |

**Conceptual dependency map**

```text
Electric charge + Coulomb force
              |
              v
        Electric field -----> Electric potential
              |                        |
              v                        v
       Gauss's law             Capacitance + energy
              |                        |
              +----------+-------------+
                         v
              Charge transport (current)
                         |
             +-----------+-----------+
             v                       v
        Circuit laws          Magnetic field of currents
                                     |
                             Matter + magnetic dipoles
                                     |
                                     v
                              Changing magnetic flux
                                     |
                                     v
                              Induction and AC
                                     |
                                     v
                       Maxwell's time-dependent fields
                                     |
                                     v
                             Electromagnetic waves
```

---

# Part I: Electric Field and Potential

Electrostatics replaces the idea of a mysterious force acting across a distance with an operational field: a charge establishes an electric field, and a second charge experiences a force in it. Potential then packages the same conservative field information into a scalar.

## 29.1 What Is Electric Charge?

Electrical charge is a property of matter responsible for electric interactions. Positive and negative charges have opposite effects on a test charge; like signs repel and unlike signs attract. In ordinary matter, positively charged protons and negatively charged electrons balance approximately, making objects neutral overall. Charging by friction or contact generally **transfers electrons** rather than creating charge.

Charge is **additive**, **conserved** in an isolated system, and **quantized**:

$$
\boxed{q=ne,\qquad e\simeq1.602\times10^{-19}\ \mathrm C,\quad n\in\mathbb Z.}
$$

On macroscopic scales charge steps are extremely small, so treating charge as a continuous density is often justified. A positively charged conductor usually has an electron deficit, not an excess of protons moving through the metal.

## 29.2 Coulomb's Law

For two ideal point charges at rest separated by distance $r$ in vacuum, the magnitude of their mutual force is

$$
\boxed{F=\frac{1}{4\pi\varepsilon_0}\frac{|q_1q_2|}{r^2}=k_e\frac{|q_1q_2|}{r^2}.}
$$

For a vector displacement $\vec r_{12}=\vec r_2-\vec r_1$, the force **on charge 2 due to charge 1** is

$$
\boxed{\vec F_{2\leftarrow1}=k_e\frac{q_1q_2}{|\vec r_{12}|^3}\vec r_{12}.}
$$

The sign of $q_1q_2$ handles attraction or repulsion automatically. Coulomb's law is an inverse-square law, and forces from different source charges **superpose vectorially**. The point-charge approximation requires separations large compared with charge-distribution size; a material medium introduces additional polarization and requires care.

**Superposition for a collection:**

$$
\vec F=\sum_j\vec F_j;\qquad \vec F=\int d\vec F\quad\text{for continuous charge.}
$$

## 29.3 Electric Field

The electric field is defined using a sufficiently small positive test charge:

$$
\boxed{\vec E(\vec r)=\lim_{q_t\to0}\frac{\vec F}{q_t}.}
$$

The limit indicates that the test charge should not appreciably rearrange the sources. A point charge $Q$ at $\vec r_0$ creates

$$
\vec E(\vec r)=k_eQ\frac{\vec r-\vec r_0}{|\vec r-\vec r_0|^3}.
$$

Thus $\vec F=q\vec E$; for negative $q$, force is antiparallel to $\vec E$. Field units are $\mathrm{N/C}=\mathrm{V/m}$. For charge density $\rho(\vec r')$,

$$
\vec E(\vec r)=k_e\int\rho(\vec r')\frac{\vec r-\vec r'}{|\vec r-\vec r'|^3}\,d^3r'.
$$

The field is a property of the source configuration, independent of whether a test charge is present.

## 29.4 Lines of Electric Force

An **electric field line** is an imaginary curve everywhere tangent to $\vec E$. Lines leave positive source charges and terminate on negative charges or at infinity. Their local density schematically represents field strength; field lines **never cross** because a nonzero field has one direction at a point.

Field-line diagrams help establish symmetry, but the number of lines drawn is an artistic convention, not a physical count. In electrostatics, field lines cannot form closed loops because the electrostatic field is conservative.

## 29.5 Electric Potential Energy

Electrostatic interactions are conservative. For a charge $q$ moving from $A$ to $B$,

$$
W_{A\to B}^{\rm field}=\int_A^Bq\vec E\cdot d\vec l=-\Delta U.
$$

For two point charges separated by $r$, choosing zero energy at infinite separation,

$$
\boxed{U(r)=k_e\frac{q_1q_2}{r}.}
$$

Unlike force magnitude, $U$ carries a sign. Opposite-sign charges have **negative** interaction energy relative to infinity; positive energy must be supplied to separate them quasistatically to infinity. For assemblies, count each distinct pair only once:

$$
U_{\rm assembly}=\sum_{i<j}k_e\frac{q_iq_j}{r_{ij}}.
$$

## 29.6 Electric Potential

Electric potential is potential energy **per unit charge** in an electrostatic field:

$$
\boxed{V=\frac{U}{q},\qquad V_B-V_A=-\int_A^B\vec E\cdot d\vec l.}
$$

Potential is a **scalar**, while field is a vector. Its SI unit is volt $1\ \mathrm V=1\ \mathrm{J/C}$. Only potential differences have an unavoidable experimental significance: the zero level can be chosen conveniently.

A particle's change in potential energy is $\Delta U=q\Delta V$. Positive charges naturally move toward lower $V$ if released; negative charges accelerate toward higher $V$. Distinguish the **sign of potential** from its physical ability to do work.

## 29.7 Electric Potential due to a Point Charge

With $V(\infty)=0$ for a localized point charge,

$$
\boxed{V(r)=k_e\frac{Q}{r}.}
$$

For multiple point charges, add potentials **algebraically**:

$$
V(\vec r)=k_e\sum_i\frac{q_i}{|\vec r-\vec r_i|}.
$$

For continuous distributions,

$$
V(\vec r)=k_e\int\frac{dq}{|\vec r-\vec r'|}.
$$

This scalar integral is often much easier to evaluate than the three components of $\vec E$. Differentiating afterward recovers the field.

## 29.8 Relation between Electric Field and Potential

For a small displacement $d\vec l$,

$$
dV=-\vec E\cdot d\vec l.
$$

In Cartesian coordinates,

$$
\boxed{\vec E=-\nabla V=-\left(\frac{\partial V}{\partial x}\hat x+\frac{\partial V}{\partial y}\hat y+\frac{\partial V}{\partial z}\hat z\right).}
$$

For a one-dimensional field $E_x=-dV/dx$. Equipotential surfaces are everywhere perpendicular to electrostatic field lines wherever $\vec E\ne0$. No electrostatic work is done moving a charge *along* an equipotential. For a constant field parallel to the $x$-axis, $\Delta V=-E_x\Delta x$.

**Important:** A point of zero $V$ need not have zero $\vec E$ (nor conversely). The field depends on the *gradient*, not on the absolute value of the potential.

## 29.9 Electric Dipole

A dipole consists of equal and opposite charges separated by vector $\vec d$ **from negative to positive**. Its dipole moment is

$$
\boxed{\vec p=q\vec d,\qquad [p]=\mathrm{C\,m}.}
$$

At distances $r\gg d$, its leading potential is

$$
V(\vec r)\simeq k_e\frac{\vec p\cdot\hat r}{r^2}=k_e\frac{p\cos\theta}{r^2}.
$$

Two important dipole-field directions, in the far-field approximation, are

$$
E_{\rm axial}\simeq k_e\frac{2p}{r^3},\qquad E_{\rm equatorial}\simeq k_e\frac{p}{r^3},
$$

where the equatorial field is opposite to $\vec p$. Compared with a monopole's $r^{-2}$ field, a dipole's leading field falls as $r^{-3}$; the positive and negative source contributions partly cancel.

## 29.10 Torque on an Electric Dipole Placed in an Electric Field

In a **uniform** external field, the equal and opposite forces on a dipole cancel in translation but generally produce a torque:

$$
\boxed{\vec\tau=\vec p\times\vec E,\qquad |\tau|=pE\sin\theta.}
$$

The torque turns $\vec p$ toward $\vec E$. A nonuniform field can also produce a net force; the zero-net-force result is restricted to a uniform field. For a small fixed dipole in a slowly varying field,

$$
\vec F\simeq\nabla(\vec p\cdot\vec E).
$$

The last expression is an additional useful approximation, not a replacement for directly summing forces when the dipole is large.

## 29.11 Potential Energy of a Dipole Placed in a Uniform Electric Field

If the torque aligns the dipole, its potential energy decreases. Integrating $\tau=-dU/d\theta$ gives

$$
\boxed{U=-\vec p\cdot\vec E=-pE\cos\theta,}
$$

with the conventional additive constant zero. Stable equilibrium: $\theta=0$ (lowest $U$). Unstable equilibrium: $\theta=\pi$ (highest $U$). The two configurations have zero torque, but very different stability.

## 29.12 Conductors, Insulators and Semiconductors

**Conductors** contain mobile carriers capable of rearranging in response to an electric field. In metals the mobile carriers are primarily electrons. **Insulators** strongly restrict free-charge transport but polarize in a field. **Semiconductors** have conductivity sensitive to temperature, doping, and illumination; detailed electronic-device behavior is treated later in the book.

Electrostatic induction redistributes charges in a conductor without requiring physical charge transfer from the inducing object. Contact charging, friction charging, and induction charging are distinct procedures.

## 29.13 The Electric Field inside a Conductor

In **electrostatic equilibrium**, a bulk conductor has no sustained internal electric field:

$$
\boxed{\vec E_{\rm conductor}=0,\qquad V_{\rm conductor}=\text{constant}.}
$$

Otherwise free charges would continue accelerating and rearranging. Any excess net charge resides on the surface for an isolated conductor in electrostatic equilibrium. Immediately outside a conductor's surface,

$$
E_{\perp,\rm outside}=\frac{\sigma}{\varepsilon_0}
$$

if the field immediately inside is zero; the tangential external component vanishes. Surface charge tends to concentrate near sharply curved regions. **Exception to remember:** a conductor carrying steady current may have a **nonzero internal electric field**; it is not an electrostatic-equilibrium configuration.

---

# Part II: Gauss's Law

Gauss's law gives a global constraint on electric fields. It is always true in classical electrostatics, but it becomes an efficient method for *calculating* $E$ only when geometry supplies enough symmetry.

## 30.1 Flux of an Electric Field through a Surface

For a small oriented surface $d\vec A=\hat n\,dA$, electric flux is

$$
d\Phi_E=\vec E\cdot d\vec A=E\cos\theta\,dA.
$$

The total flux through an open surface is $\int\vec E\cdot d\vec A$, with a specified surface normal. For a **closed** surface, the normal is conventionally outward:

$$
\boxed{\Phi_E=\oint_S\vec E\cdot d\vec A.}
$$

Flux is **signed** and has SI unit $\mathrm{N\,m^2/C}$. It measures net field crossing an oriented surface, not a count of charge particles or the amount of field *stored* within the region.

## 30.2 Solid Angle

Solid angle is the three-dimensional analogue of plane angle. An area element $dA$ observed at distance $r$, with normal making angle $\theta$ with the line of sight, subtends

$$
\boxed{d\Omega=\frac{dA\cos\theta}{r^2}.}
$$

Its unit is the steradian (sr); a complete sphere subtends $4\pi$ sr. The radial field of a point charge produces flux $k_eq\,d\Omega$ through an element, making the $4\pi$ in Gauss's law natural.

## 30.3 Gauss's Law and Its Derivation from Coulomb's Law

For charge $q$ at the center of a sphere of radius $r$,

$$
\Phi_E=E(4\pi r^2)=\left(k_e\frac{q}{r^2}\right)(4\pi r^2)=\frac{q}{\varepsilon_0}.
$$

The cancellation of $r^2$ reflects the inverse-square force law. Using oriented solid angle and superposition generalizes the statement to arbitrary closed surfaces and charge distributions:

$$
\boxed{\oint_S\vec E\cdot d\vec A=\frac{Q_{\rm enclosed}}{\varepsilon_0}.}
$$

**No symmetry is required for the law itself.** Exterior charges can contribute to $\vec E$ at every point on the surface, but they contribute **zero net closed-surface flux**. The enclosed charge is an algebraic sum.

## 30.4 Applications of Gauss's Law

**Method:** (1) infer field direction from symmetry, (2) choose a closed Gaussian surface on which $E$ is constant or its normal component vanishes, (3) calculate flux, and (4) set flux to $Q_{\rm enc}/\varepsilon_0$.

**Infinite line, uniform linear charge density $\lambda$.** A coaxial cylinder radius $r$, length $L$ gives

$$
E(2\pi rL)=\frac{\lambda L}{\varepsilon_0}\quad\Longrightarrow\quad
\boxed{E=\frac{|\lambda|}{2\pi\varepsilon_0r}.}
$$

Field is radially outward for positive $\lambda$ and inward for negative $\lambda$.

**Infinite uniformly charged nonconducting sheet, density $\sigma$.** A pillbox gives

$$
2EA=\frac{\sigma A}{\varepsilon_0}\quad\Longrightarrow\quad
\boxed{|E|=\frac{|\sigma|}{2\varepsilon_0}.}
$$

**Infinite conducting surface.** Because the interior field is zero, a pillbox crossing one conducting face gives $|E_{\rm outside}|=|\sigma|/\varepsilon_0$ for the **local surface charge density**. Do not confuse this with the two-sided infinite nonconducting sheet result.

## 30.5 Spherical Charge Distributions

For a **spherically symmetric** distribution, choose a concentric spherical Gaussian surface:

$$
\boxed{E(r)=\frac{1}{4\pi\varepsilon_0}\frac{|Q_{\rm enc}(r)|}{r^2}.}
$$

- **Thin uniformly charged spherical shell:** $E=0$ everywhere inside; outside $E$ equals that of a point charge at the center.
- **Uniform solid insulating sphere** of radius $R$ and charge $Q$: $Q_{\rm enc}=Q(r^3/R^3)$ for $r<R$, so

$$
\boxed{E(r)=\begin{cases}k_e|Q|r/R^3,&0\le r<R,\\k_e|Q|/r^2,&r\ge R.\end{cases}}
$$

- **Spherical conducting shell:** field is zero in the conductor material in electrostatic equilibrium. In an empty spherical cavity with no internal charge, field vanishes. With a charge inside the cavity, induced surface charges matter, and the cavity field need not vanish.

Potential for a thin shell (reference $V(\infty)=0$) is continuous:

$$
V(r)=\begin{cases}k_eQ/R,&r\le R,\\k_eQ/r,&r\ge R.\end{cases}
$$

## 30.6 Earthing a Conductor

**Earthing (grounding)** connects a conductor to a large charge reservoir whose potential can be treated as fixed, conventionally zero. Electrons may enter or leave the conductor until its potential matches the ground. Grounding changes the charge configuration; it does **not** mean the conductor necessarily has zero net charge afterward.

An insulated conductor obeys a fixed-net-charge condition; a grounded conductor obeys a fixed-potential condition. Choose the correct boundary condition before solving a charging or induction problem.

---

# Part III: Capacitors

Capacitance quantifies how much charge can be placed on an electrode pair per unit potential difference. Geometry and dielectric materials determine the capacitance; the applied voltage sets the charge in a linear ideal capacitor.

## 31.1 Capacitor and Capacitance

A capacitor comprises two conductors separated by an insulating region. Idealized capacitor electrodes acquire $+Q$ and $-Q$ when connected to a source. Define

$$
\boxed{C=\frac{Q}{V},\qquad [C]=\mathrm F=\mathrm{C/V}.}
$$

Here $Q$ is the **magnitude on one electrode**, not the algebraic sum of both electrode charges. For fixed geometry and a linear dielectric, $C$ is independent of $Q$ and $V$. Capacitance is measured in farads, frequently $\mu\mathrm F$, $\mathrm{nF}$, and $\mathrm{pF}$.

## 31.2 Calculation of Capacitance

**Parallel plates** of area $A$, separation $d$, $d\ll\sqrt A$, in vacuum: treat the central field as uniform and neglect edge fringing. With charge density $\sigma=Q/A$,

$$
E\simeq\frac{\sigma}{\varepsilon_0},\qquad V=Ed=\frac{Qd}{\varepsilon_0 A},
$$

so

$$
\boxed{C\simeq\frac{\varepsilon_0A}{d}.}
$$

**Isolated conducting sphere** of radius $R$, taking infinity as the reference electrode:

$$
\boxed{C=4\pi\varepsilon_0R.}
$$

**Concentric spherical capacitor** with inner radius $a$ and outer radius $b>a$:

$$
\boxed{C=4\pi\varepsilon_0\frac{ab}{b-a}.}
$$

**Long coaxial capacitor**, inner radius $a$, outer radius $b$, length $L\gg b$:

$$
\boxed{C=\frac{2\pi\varepsilon_0L}{\ln(b/a)}.}
$$

These expressions follow from finding $E$ by symmetry and integrating the potential difference, then taking $C=Q/|\Delta V|$.

## 31.3 Combination of Capacitors

**Parallel:** all capacitors share voltage $V$, while electrode charges add:

$$
Q_{\rm total}=\sum_iC_iV\quad\Longrightarrow\quad
\boxed{C_{\rm eq}=\sum_iC_i.}
$$

**Series:** identical charge magnitude appears on each ideal capacitor after charging, while voltage drops add:

$$
V_{\rm total}=\sum_i\frac{Q}{C_i}\quad\Longrightarrow\quad
\boxed{\frac1{C_{\rm eq}}=\sum_i\frac1{C_i}.}
$$

For an isolated intermediate electrode initially uncharged, conservation of charge explains the equal-charge condition. Series connection reduces equivalent capacitance below the smallest member; parallel connection increases it above the largest.

## 31.4 Force between the Plates of a Capacitor

A plate experiences force due to the field of the **other** plate, not its own self-field. For a large-plate vacuum capacitor the other plate's field magnitude is $E_{\rm other}=\sigma/(2\varepsilon_0)$, giving the attraction magnitude

$$
\boxed{F=QE_{\rm other}=\frac{Q^2}{2\varepsilon_0A}=\frac12\varepsilon_0AE^2.}
$$

At fixed $Q$, this follows also from differentiating stored field energy with plate separation. **Caution:** if a battery holds $V$ fixed, account for the work exchanged with the source. Differentiating capacitor energy alone under fixed $V$ can give the wrong force sign.

## 31.5 Energy Stored in a Capacitor and Energy Density in Electric Field

Charging a capacitor requires incremental work $dW=V(q)\,dq=(q/C)\,dq$. Hence

$$
U=\int_0^Q\frac{q}{C}\,dq
\quad\Longrightarrow\quad
\boxed{U=\frac{Q^2}{2C}=\frac12QV=\frac12CV^2.}
$$

For parallel plates, use $C=\varepsilon_0A/d$ and $V=Ed$:

$$
U=\frac12\varepsilon_0E^2(Ad).
$$

The vacuum electrostatic **energy density** therefore is

$$
\boxed{u_E=\frac12\varepsilon_0E^2.}
$$

The energy belongs to the total physical system, and expressing it as field energy makes the extension to general field configurations natural.

## 31.6 Dielectrics

A dielectric is an insulating material whose internal bound charges shift or orient in an applied electric field. **Polarization** means net dipole moment per unit volume:

$$
\vec P=\frac{\text{electric dipole moment}}{\text{volume}}.
$$

For an isotropic, linear dielectric,

$$
\vec P=\varepsilon_0\chi_e\vec E,\qquad
\varepsilon=\varepsilon_0(1+\chi_e)=\kappa\varepsilon_0.
$$

Here $\chi_e$ is electric susceptibility and $\kappa$ is relative permittivity (dielectric constant). Dielectric insertion reduces the net field at fixed free charge, but the outcome depends on the electrical boundary condition.

## 31.7 Parallel-plate Capacitor with a Dielectric

With the plate gap completely filled by a linear dielectric,

$$
\boxed{C=\kappa C_0=\kappa\varepsilon_0\frac{A}{d}.}
$$

**Capacitor isolated ($Q$ fixed):** $V=V_0/\kappa$, $E=E_0/\kappa$, and $U=U_0/\kappa$.

**Capacitor connected to ideal battery ($V$ fixed):** $Q=\kappa Q_0$ and $U=\kappa U_0$ for the capacitor itself; the battery supplies additional energy. Dielectric slabs in layers along the field direction behave as capacitances in series. Slabs partitioning *area* behave as capacitances in parallel (neglect fringing).

## 31.8 An Alternative Form of Gauss's Law

In material media, distinguish **free charge** from polarization's **bound charge**. The displacement field is

$$
\boxed{\vec D=\varepsilon_0\vec E+\vec P.}
$$

Gauss's law for free charge becomes

$$
\boxed{\oint_S\vec D\cdot d\vec A=Q_{\rm free,enclosed}.}
$$

For a linear isotropic dielectric $\vec D=\varepsilon\vec E$. The original $\oint\vec E\cdot d\vec A=Q_{\rm total,enclosed}/\varepsilon_0$ still holds: $Q_{\rm total}$ includes both free and bound charges. Do not confuse the two laws' right-hand sides.

## 31.9 Electric Field due to a Point Charge $q$ Placed in an Infinite Dielectric

For a point free charge embedded in an infinite, uniform, isotropic, linear dielectric, symmetry and the $\vec D$ form of Gauss's law give

$$
4\pi r^2D=q\quad\Longrightarrow\quad
\boxed{\vec E=\frac{q}{4\pi\varepsilon r^2}\hat r.}
$$

This is Coulomb's vacuum field reduced by factor $\kappa$ in the idealized medium. Interfaces, finite dielectric dimensions, nonlinear polarization, and anisotropy invalidate the simple uniform-$\varepsilon$ expression.

## 31.10 Energy in the Electric Field in a Dielectric

For a linear dielectric, the energy density can be written

$$
\boxed{u=\frac12\vec E\cdot\vec D=\frac12\varepsilon E^2.}
$$

The total electrostatic energy is $U=\int u\,dV$ when applicable. The form $\tfrac12\vec E\cdot\vec D$ assumes a linear response built up reversibly from zero field; for nonlinear or history-dependent materials, integrate the constitutive relation instead.

## 31.11 Corona Discharge

Charge accumulates disproportionately near sharply curved conductor surfaces. The enhanced field can ionize surrounding air, enabling localized conduction, glow, or hissing **corona discharge** even without a complete spark across a gap. Corona contributes to transmission-line losses and is exploited in electrostatic equipment. Thresholds depend on air density, geometry, humidity, and surface quality.

## 31.12 High-voltage Generator

An electrostatic generator can transport charge to an insulated terminal, raising its potential approximately according to $V=Q/C$. The Van de Graaff principle uses a moving belt or analogous charge-transport arrangement to deliver charge to a large hollow dome. The dome geometry increases capacitance and reduces extreme local fields compared with a small sharp electrode. Real voltage is limited by leakage, corona, and electrical breakdown, not merely by the ideal $Q/C$ formula.

---

# Part IV: Electric Current in Conductors

Electrostatics concerns charge configurations at equilibrium; circuit theory concerns the transport of charge through materials and the energy transfers associated with that transport. The basic accounting variables are charge, current, potential difference, and resistance.

## 32.1 Electric Current and Current Density

Electric current is the **rate of net charge transport** through a chosen cross-section:

$$
\boxed{I=\frac{dQ}{dt}.}
$$

The SI unit is ampere ($\mathrm A=\mathrm{C/s}$). Conventional current points in the direction of **positive-charge** motion; conduction electrons move opposite to this convention. The local current density $\vec J$ (A/m$^2$) satisfies

$$
\boxed{I=\int_A\vec J\cdot d\vec A.}
$$

For a uniform current-density profile normal to cross-sectional area $A$, $I=JA$. Current is a scalar flow across an **oriented surface**; current density is a vector at a point.

Conservation of charge takes the local form

$$
\boxed{\frac{\partial\rho}{\partial t}+\nabla\cdot\vec J=0.}
$$

Its circuit-level consequence is that, at a junction with negligible charge accumulation, current entering equals current leaving. This continuity relation also reappears in Maxwell's theory.

## 32.2 Drift Speed

In a metallic conductor electrons exhibit rapid random thermal motion even without a current. An applied field adds a much smaller **average drift velocity**. If carrier number density is $n$, carrier charge $q$, and mean velocity $\vec v_d$,

$$
\boxed{\vec J=nq\vec v_d,\qquad I=n|q|Av_d}
$$

for the magnitude of a uniform single-carrier current. For electrons $q=-e$, making $\vec J$ opposite to electron drift. A simple relaxation-time model predicts

$$
\vec v_d=\frac{q\tau}{m}\vec E,
\qquad \sigma=\frac{nq^2\tau}{m},
$$

where $\tau$ is a characteristic momentum-relaxation time. This *Drude model* is a useful extension; it does not describe all the quantum physics of conduction. Electric signals propagate through the circuit much faster than individual electrons drift.

## 32.3 Ohm's Law

For an **ohmic** conductor under fixed physical conditions, voltage is proportional to current:

$$
\boxed{V=IR.}
$$

For a uniform wire of length $\ell$, cross-section $A$, and resistivity $\rho$,

$$
\boxed{R=\rho\frac{\ell}{A},\qquad \vec J=\sigma\vec E,\quad\sigma=\rho^{-1}.}
$$

Dimensions: $[\rho]=\Omega\,\mathrm m$, $[\sigma]=\mathrm{S/m}$. Material resistivity is not the same as geometric resistance. Ohm's law is **empirical and conditional**; diodes, electrolytes, high-field devices, and self-heating elements need not have constant resistance.

## 32.4 Temperature Dependence of Resistivity

In many ordinary metals near a chosen reference temperature $T_0$, resistivity is approximated by

$$
\boxed{\rho(T)\simeq\rho_0[1+\alpha(T-T_0)].}
$$

Here $\alpha$ is a temperature coefficient and the relation holds over a restricted temperature interval. Metallic resistivity often rises with temperature due to enhanced scattering. Semiconductor conductivity can increase with temperature because thermally generated carriers become more numerous. Temperature dependence is material-specific; it is unsafe to apply one sign of $\alpha$ universally.

## 32.5 Battery and emf

A battery uses non-electrostatic forces associated with chemical processes to separate charges. Its **electromotive force** (emf) $\mathcal E$ is the work supplied per unit charge by the source through a complete circuit:

$$
\boxed{\mathcal E=\frac{W_{\rm source}}{q}.}
$$

It is measured in volts despite its historical name. With internal resistance $r$ and external load current $I$, a discharging cell's terminal voltage is

$$
\boxed{V_{\rm terminal}=\mathcal E-Ir.}
$$

When a battery is being charged by an external supply, the sign of its internal drop reverses under the corresponding current convention. An ideal voltage source has zero internal resistance.

## 32.6 Energy Transfer in an Electric Circuit

Charge $dq$ crossing a potential drop $V$ transfers energy $dW=V\,dq$. Hence the **electrical power** delivered across a two-terminal element is

$$
\boxed{P=VI.}
$$

For a resistor, Ohm's law yields

$$
\boxed{P=I^2R=\frac{V^2}{R}.}
$$

These last two equalities require an **ohmic resistor**; $P=VI$ remains the basic lumped-circuit relation for other elements with the passive sign convention. In a circuit energy is transferred between chemical, electrical, thermal, and sometimes mechanical forms. Energy does not travel around a circuit in a little parcel inside a single electron.

## 32.7 Kirchhoff's Laws

**Junction rule (KCL):** sum of signed currents into any node equals zero for a lumped circuit without appreciable charge buildup:

$$
\boxed{\sum_{\rm node}I_k=0.}
$$

**Loop rule (KVL):** algebraic sum of potential changes around a closed loop vanishes in the quasistatic circuit approximation:

$$
\boxed{\sum_{\rm loop}\Delta V=0.}
$$

**Solving a circuit:** (1) mark assumed current arrows; (2) draw loop traversals; (3) entering a resistor along assumed current gives $-IR$ potential change; (4) crossing ideal cell from negative to positive gives $+\mathcal E$; (5) solve simultaneous equations; (6) a negative current means the true direction was opposite to the assumed arrow.

KVL needs qualification when a time-varying magnetic flux threads the circuit; induced emf must be included. One cannot insist that the electrostatic field integral around such a loop vanishes.

## 32.8 Combination of Resistors in Series and Parallel

**Series:** common current $I$, additive drops $V_i=IR_i$:

$$
\boxed{R_{\rm eq}=\sum_iR_i.}
$$

**Parallel:** common voltage $V$, additive branch currents $I_i=V/R_i$:

$$
\boxed{\frac1{R_{\rm eq}}=\sum_i\frac1{R_i}.}
$$

Useful special cases: two parallel resistors $R_1R_2/(R_1+R_2)$; $n$ identical resistors of resistance $R$ give $nR$ in series and $R/n$ in parallel. A voltmeter changes the effective branch resistance and an ammeter changes the series resistance unless they are ideal.

## 32.9 Grouping of Batteries

For $n$ identical cells of emf $\mathcal E$ and internal resistance $r$ in **series** (same orientation),

$$
\mathcal E_{\rm eq}=n\mathcal E,\qquad r_{\rm eq}=nr.
$$

For $n$ identical cells in **parallel** (same polarity),

$$
\mathcal E_{\rm eq}=\mathcal E,\qquad r_{\rm eq}=r/n.
$$

If $n_s$ cells are placed in series in each of $n_p$ identical parallel strings, then

$$
\mathcal E_{\rm eq}=n_s\mathcal E,\qquad r_{\rm eq}=\frac{n_s r}{n_p}.
$$

All formulas assume matched cells and safe equalization currents. Parallel connecting real unequal-emf cells can drive large circulating currents and should not be modeled with naive identical-cell rules.

## 32.10 Wheatstone Bridge

A Wheatstone bridge is a four-resistor network with two series arms joined by a galvanometer between their intermediate nodes. At **balance**, galvanometer current is zero, so the two intermediate points have equal potential.

For resistors $P,Q$ in one branch and $R,S$ in another, with the source across the branch ends and the galvanometer between the midpoints, the balance condition is

$$
\boxed{\frac{P}{Q}=\frac{R}{S}.}
$$

This follows by equating voltage-divider ratios. It is a **null measurement**, useful because the galvanometer's own resistance does not affect the ideal balance condition.

## 32.11 Ammeter and Voltmeter

An **ammeter** measures current and is connected in series; ideally its resistance is $0$. A **voltmeter** measures potential difference and is connected in parallel; ideally its resistance is infinite.

A moving-coil galvanometer with coil resistance $G$ and full-scale current $I_g$ can be converted into an ammeter of full-scale $I$ using a **parallel shunt**

$$
\boxed{S=\frac{I_gG}{I-I_g}.}
$$

For a voltmeter of full-scale voltage $V$, place a **series resistor**

$$
\boxed{R_s=\frac{V}{I_g}-G.}
$$

These equations are based on matching the galvanometer's full-scale coil current. Real instruments have loading errors, accuracy classes, and frequency-response limits.

## 32.12 Stretched-wire Potentiometer

A uniform wire carrying constant current has a nearly uniform voltage gradient $k=V_{AB}/L$, giving a potential drop $V=k\ell$ over length $\ell$. A potentiometer compares unknown emfs by a **null-deflection** method.

At balance, the cell being measured supplies no current through the galvanometer branch, so its emf equals the corresponding wire drop:

$$
\boxed{\mathcal E=k\ell.}
$$

For two cells compared under unchanged wire current,

$$
\boxed{\frac{\mathcal E_1}{\mathcal E_2}=\frac{\ell_1}{\ell_2}.}
$$

To determine internal resistance, compare open-circuit balance length $\ell_0$ with loaded balance length $\ell$ when a known resistor $R$ is connected:

$$
\boxed{r=R\left(\frac{\ell_0}{\ell}-1\right).}
$$

Null methods reduce errors due to drawing current from the tested emf source.

## 32.13 Charging and Discharging of Capacitors

For a series $RC$ circuit driven by constant ideal source $\mathcal E$, KVL yields

$$
\mathcal E=IR+\frac{q}{C},\qquad I=\frac{dq}{dt}.
$$

For an initially uncharged capacitor, integration gives

$$
\boxed{q(t)=C\mathcal E(1-e^{-t/RC}),\qquad I(t)=\frac{\mathcal E}{R}e^{-t/RC}.}
$$

At the instant of switch closure the uncharged ideal capacitor has zero voltage; at long times it approaches source voltage, and current approaches zero. Discharging an initial charge $Q_0$ through $R$ gives

$$
\boxed{q(t)=Q_0e^{-t/RC},\qquad |I(t)|=\frac{Q_0}{RC}e^{-t/RC}.}
$$

The time constant is $\tau=RC$. After one time constant, charging reaches $1-e^{-1}\simeq63.2\%$ of its final change; discharging retains $e^{-1}\simeq36.8\%$. At five time constants, a first-order transient is approximately $99.3\%$ complete.

## 32.14 Atmospheric Electricity

Thundercloud processes separate charge over large spatial regions, creating electric fields and potential differences between clouds and the ground or between different cloud regions. When local air breakdown occurs, a conducting plasma channel forms: **lightning**. Grounding, sharp-tip corona, and large-scale atmospheric electric fields are applications of electrostatic concepts, though cloud charging and discharge are highly dynamic, nonequilibrium processes.

**Scope warning:** A cloud is not accurately modeled as a uniform parallel-plate capacitor except for rough estimates of capacitance, stored energy, or field strength.

---

# Part V: Thermal and Chemical Effects of Electric Current

Current is not merely a charge flow. It can transfer energy to lattice vibrations, drive chemical transformations, or arise from temperature differences. These effects connect electromagnetism to thermodynamics and chemistry.

## 33.1 Joule's Laws of Heating

In an ohmic resistor, instantaneous thermal power converted from electrical energy is $P=I^2R$. For steady current over time $t$,

$$
\boxed{H=I^2Rt=VIt=\frac{V^2}{R}t.}
$$

Here $H$ is energy (joules), not temperature rise. To estimate a temperature rise, add a thermal model such as $H=mc\Delta T$ and account for heat losses. With a time-varying current in fixed $R$, use $H=\int i^2R\,dt$ rather than replacing $i$ by its signed average.

## 33.2 Verification of Joule's Laws

A calorimetric arrangement can surround a resistor with an approximately insulated liquid of known heat capacity. Supply measured $I$ and $V$ for time $t$ and measure the liquid's temperature change. Ideally,

$$
I^2Rt=(mc+C_{\rm vessel})\Delta T.
$$

Experiments vary current, resistance, or time while controlling the other quantities and correcting for heat exchange with surroundings. A resistive heating experiment tests the $I^2Rt$ law only if electrical parameters remain effectively constant during measurement.

## 33.3 Seebeck Effect

When two dissimilar conductors form junctions at different temperatures, a net thermoelectric emf can arise around the loop. The generated voltage is related to **Seebeck coefficients** $S_A$ and $S_B$:

$$
\boxed{\mathcal E_{\rm thermo}\simeq(S_A-S_B)(T_h-T_c)}
$$

if their coefficient difference is nearly constant over the temperature interval. More generally the emf is an integral of the coefficient difference over temperature. A **thermocouple** converts a junction-temperature difference into an electrical signal; it does not measure absolute temperature without a reference-junction calibration.

## 33.4 Peltier Effect

Passing current across a junction of dissimilar materials can absorb or release heat, depending on current direction and material combination. Peltier heat per unit time is proportional to current:

$$
\boxed{\dot Q_P=\Pi_{AB}I,}
$$

where $\Pi_{AB}$ is the Peltier coefficient for the junction and the sign indicates heating or cooling under a chosen orientation. Unlike ordinary Joule heating ($\propto I^2$), reversible Peltier heating changes sign upon reversing current.

## 33.5 Thomson Effect

Even a *single homogeneous conductor* may exchange reversible heat with its surroundings if it carries current along a temperature gradient. With Thomson coefficient $\tau_T$, one common local convention writes the reversible heating rate per unit volume as

$$
\dot q_{\rm Thomson}\propto-\tau_T\,\vec J\cdot\nabla T,
$$

where the overall sign depends on the definition of the coefficient and which direction counts as heat evolved. The key physics is that the effect is linear in current and depends on an internal temperature gradient, unlike junction-localized Peltier heat.

## 33.6 Explanation of Seebeck, Peltier and Thomson Effects

Carriers transport not only electrical charge but also energy and entropy. If carrier populations and energies differ between materials or positions at different temperatures, a net voltage or reversible heat transfer can arise.

A deeper thermodynamic connection is expressed by the **Kelvin relations** for compatible sign conventions:

$$
\boxed{\Pi=ST,\qquad \tau_T=T\frac{dS}{dT}.}
$$

These connections are a brief extension beyond the elementary experimental descriptions. They emphasize that the three effects are not unrelated curiosities: they emerge from coupled heat and charge transport.

## 33.7 Electrolysis

An electrolyte conducts through mobile ions. When a suitable voltage is imposed between immersed electrodes, ions migrate and electrode reactions can transfer material or transform chemical species. **Cations** move toward the cathode and **anions** toward the anode; the labels cathode and anode follow reduction and oxidation processes, not simply fixed positive/negative polarity in every device.

Electrolysis converts electrical energy into chemical change, often with resistive and activation losses. It is important to distinguish the ionic current inside an electrolyte from the electron current in connecting metal wires.

## 33.8 Faraday's Laws of Electrolysis

For an electrode reaction requiring $z$ electrons per product entity, charge $Q$ transfers $Q/(ze)$ entities (ideal current efficiency). Using Avogadro's constant $N_A$ and Faraday's constant $F=N_Ae$:

$$
\boxed{n_{\rm product}=\frac{Q}{zF},\qquad F\simeq9.6485\times10^4\ \mathrm{C/mol}.}
$$

For molar mass $M$, deposited mass is

$$
\boxed{m=\frac{MQ}{zF}=\frac{MIt}{zF}.}
$$

Thus (1) deposited mass is proportional to total charge for a specified reaction, and (2) equal charges deposit masses proportional to their electrochemical equivalents $M/z$. Side reactions and incomplete efficiency reduce actual deposition.

## 33.9 Voltameter or Coulombmeter

An **electrolytic coulombmeter** determines total charge from the known mass of an electrode deposit or consumed material:

$$
\boxed{Q=\frac{mzF}{M}.}
$$

This is a measurement of **charge passed**, not necessarily instantaneous current. If current varies, $Q=\int I\,dt$ and the deposited mass integrates that history. Chemical-purity, current-efficiency, and handling errors matter in laboratory operation.

## 33.10 Primary and Secondary Cells

A **primary cell** uses reactions not designed to be substantially reversed in ordinary use, so it is generally discarded after discharge. A **secondary cell** (rechargeable battery) operates with reactions that can be driven backward by an external electrical supply. Emf, internal resistance, capacity, energy, cycle life, and rate capability are distinct properties; high emf does not guarantee high usable energy.

For a discharging cell, useful terminal behavior is approximated by $V=\mathcal E-Ir$, although realistic electrochemical polarization can make $r$ state- and rate-dependent.

## 33.11 Primary Cells

Classical primary-cell examples include zinc–carbon dry cells and related galvanic cells. A cell's electrolyte and electrode chemistry determine the emf. Practical primary cells are often designed for low cost, shelf stability, and simplicity; performance depends on temperature, discharge rate, storage condition, and composition.

**Chemistry caveat:** The simple textbook phrase “primary = irreversible, secondary = reversible” is a functional classification, not an assertion that actual battery cycles are perfectly thermodynamically reversible.

## 33.12 Secondary Cell: Lead Accumulator

A lead–acid accumulator uses lead, lead dioxide, and sulfuric acid. During discharge, both electrode reactions produce lead sulfate while the electrolyte composition changes. The net discharge reaction is commonly represented by

$$
\boxed{\mathrm{Pb+PbO_2+2H_2SO_4\longrightarrow2PbSO_4+2H_2O}.}
$$

An individual cell has a nominal voltage near $2\ \mathrm V$; several cells in series produce higher pack voltages. Charging drives the overall reaction in reverse, with inefficiencies and possible gas evolution. Lead–acid cells can supply substantial starting current but are heavy; maintenance and safe handling matter because of corrosive acid and lead toxicity.

---

# Part VI: Magnetic Field

Electric and magnetic fields are closely connected, but their mechanical actions differ. Magnetic forces on moving charges are perpendicular to their velocities, and consequently do not by themselves change kinetic energy.

## 34.1 Introduction

A moving charge or a current can experience force in the presence of a magnetic field. Permanent magnets exert torques and forces due to organized microscopic magnetic moments. Magnetic interactions become particularly clear when expressed through a local vector field $\vec B$ rather than through isolated north/south pole bookkeeping.

## 34.2 Definition of Magnetic Field $\vec B$

Experimentally, a charge $q$ moving with velocity $\vec v$ in electric and magnetic fields experiences **Lorentz force**

$$
\boxed{\vec F=q(\vec E+\vec v\times\vec B).}
$$

The magnetic part is $\vec F_B=q\vec v\times\vec B$ with magnitude $|q|vB\sin\theta$. Hence a stationary charge is unaffected by a purely magnetic field; a moving charge parallel to $\vec B$ also has no magnetic deflection. Magnetic field is measured in tesla:

$$
1\ \mathrm T=1\ \frac{\mathrm N}{\mathrm{A\,m}}.
$$

The **right-hand rule** gives $\vec v\times\vec B$ for positive charge; reverse the direction for negative charge.

## 34.3 Relation between Electric and Magnetic Fields

Electric and magnetic fields are not fundamentally unrelated entities. A charge at rest in one inertial frame can be seen moving in another, and the observed electric and magnetic fields then transform into one another. At the level of elementary problems, one commonly uses the Lorentz force with given $\vec E$ and $\vec B$; the full field transformation belongs to special relativity.

In a region with crossed perpendicular uniform fields, a particle can move undeflected when the forces cancel:

$$
q\vec E+q\vec v\times\vec B=0.
$$

For a suitable velocity orientation, the **velocity selector** condition is $v=E/B$. This is a geometric cancellation, not a claim that the fields are identical.

## 34.4 Motion of a Charged Particle in a Uniform Magnetic Field

For velocity perpendicular to a uniform field, magnetic force is centripetal:

$$
|q|vB=\frac{mv^2}{r}\quad\Longrightarrow\quad
\boxed{r=\frac{mv}{|q|B},\quad\omega_c=\frac{|q|B}{m},\quad T_c=\frac{2\pi m}{|q|B}.}
$$

These **nonrelativistic** formulas assume no appreciable radiation loss or collisions. The speed remains constant because

$$
\frac{dK}{dt}=\vec F_B\cdot\vec v=q(\vec v\times\vec B)\cdot\vec v=0.
$$

If velocity has components $v_\perp$ and $v_\parallel$ relative to $\vec B$, the motion is **helical**: a circle at speed $v_\perp$ combined with uniform axial translation at $v_\parallel$. Helix pitch is

$$
\boxed{h=v_\parallel T_c=\frac{2\pi mv_\parallel}{|q|B}.}
$$

## 34.5 Magnetic Force on a Current-carrying Wire

Each drifting carrier experiences magnetic Lorentz force. Summing over carriers in a wire element $d\vec\ell$ gives

$$
\boxed{d\vec F=I\,d\vec\ell\times\vec B.}
$$

For a straight segment of vector length $\vec L$ in a uniform field,

$$
\boxed{\vec F=I\vec L\times\vec B,\quad F=ILB\sin\theta.}
$$

The segment-vector direction follows **conventional current**. In a nonuniform field or curved wire, integrate $I\int d\vec\ell\times\vec B$; replacing the actual geometry by total wire length can be wrong.

## 34.6 Torque on a Current Loop

For a planar loop of area $A$, $N$ turns, carrying current $I$, define the magnetic dipole moment

$$
\boxed{\vec\mu=NIA\,\hat n.}
$$

The right-hand curl rule determines $\hat n$. In a uniform field, opposite sides of a rectangular loop experience forces forming a couple. The result generalizes to other planar loops:

$$
\boxed{\vec\tau=\vec\mu\times\vec B,\qquad U=-\vec\mu\cdot\vec B.}
$$

The net force on a closed current loop in a **uniform** $\vec B$ is zero, but torque can be nonzero. This torque underlies moving-coil instruments and elementary motor models. In a nonuniform field a small dipole may also experience a net force.

---

# Part VII: Magnetic Field due to a Current

A magnetic field may be created by electric currents. In magnetostatics the Biot–Savart law describes contributions from each current element; Ampère's law is often more powerful when symmetry permits.

## 35.1 Biot–Savart Law

For a steady current $I$ in a thin wire, the contribution of a short directed length $d\vec\ell$ to the field at position displaced by $\vec r$ is

$$
\boxed{d\vec B=\frac{\mu_0I}{4\pi}\frac{d\vec\ell\times\hat r}{r^2}.}
$$

Its magnitude is $dB=(\mu_0I/4\pi)(d\ell\sin\theta/r^2)$. Integrate over the current path for the total field:

$$
\vec B(\vec x)=\frac{\mu_0I}{4\pi}\int_C\frac{d\vec\ell\times(\vec x-\vec x')}{|\vec x-\vec x'|^3}.
$$

This is the steady-current thin-wire form; a volume current distribution is treated with $\vec J\,dV$ in place of $I\,d\vec\ell$. Every element's direction matters, so blindly adding magnitudes is unsafe.

## 35.2 Magnetic Field due to Current in a Straight Wire

For an infinitely long straight wire with current $I$, use cylindrical symmetry or integrate the Biot–Savart contributions:

$$
\boxed{B(r)=\frac{\mu_0I}{2\pi r}.}
$$

Direction is tangential to circles centered on the wire, set by the right-hand rule. For a finite straight wire, with perpendicular distance $r$ and signed endpoint angles $\theta_1,\theta_2$ measured from the perpendicular in a common convention,

$$
\boxed{B=\frac{\mu_0I}{4\pi r}(\sin\theta_1+\sin\theta_2)}.
$$

The angle definition must match the physical diagram; other angle conventions give equivalent cosine or difference expressions. The infinite-wire formula emerges when each endpoint tends to $90^\circ$.

## 35.3 Force between Parallel Currents

A long straight wire 1 creates a field $B_1=\mu_0I_1/(2\pi d)$ at a parallel wire 2 a distance $d$ away. The magnetic force per unit length on the second is

$$
\boxed{\frac{F}{L}=I_2B_1=\frac{\mu_0I_1I_2}{2\pi d}.}
$$

Currents in the **same direction attract** and in **opposite directions repel**. The result is idealized for long parallel wires and ignores finite-end corrections. It relates magnetic force to the definition and measurement of current in classical electromagnetism.

## 35.4 Field due to a Circular Current

For a circle of radius $R$ carrying current $I$, on its symmetry axis at distance $x$ from center, transverse contributions cancel. The surviving axial component is

$$
\boxed{B(x)=\frac{\mu_0IR^2}{2(R^2+x^2)^{3/2}}.}
$$

At the center $x=0$,

$$
\boxed{B_0=\frac{\mu_0I}{2R}.}
$$

For $N$ closely spaced turns carrying identical current, multiply the expression by $N$. At $|x|\gg R$, the field decreases as $1/|x|^3$, characteristic of a magnetic dipole. Symmetry is the fastest way to identify the field direction before integration.

## 35.5 Ampere's Law

For steady currents in vacuum, the circulation of $\vec B$ around any closed oriented loop is

$$
\boxed{\oint_C\vec B\cdot d\vec\ell=\mu_0I_{\rm enclosed}.}
$$

The algebraic enclosed current is counted according to the loop orientation by the right-hand convention. Ampère's law is always valid in magnetostatics, but extracting $B$ from the integral requires symmetry. A generic magnetic field cannot be pulled out of the line integral.

When fields vary in time, the law must be amended by Maxwell's displacement-current term; see Chapter 40.

## 35.6 Magnetic Field at a Point due to a Long, Straight Current

Take a circular Amperian loop of radius $r$ centered on a very long straight current-carrying wire. By cylindrical symmetry, $\vec B$ is tangential and has constant magnitude on the loop:

$$
\oint\vec B\cdot d\vec\ell=B(2\pi r)=\mu_0I.
$$

Therefore

$$
\boxed{B=\frac{\mu_0I}{2\pi r}.}
$$

This reproduces the Biot–Savart result with almost no integration. **Watch the applicability:** circular symmetry fails for an off-center, finite, or bent conductor, even though Ampère's law itself remains correct.

## 35.7 Solenoid

A long, tightly wound solenoid with $n=N/L$ turns per unit length produces a nearly uniform interior axial field (away from ends). In vacuum,

$$
\boxed{B_{\rm inside}\simeq\mu_0nI,\qquad B_{\rm far\ outside}\simeq0.}
$$

Choose a rectangular Amperian loop with one long side inside and one outside. Approximate negligible exterior field and negligible contributions from the transverse sides. Then $BL\simeq\mu_0(nL)I$. Real finite solenoids have fringing fields and nonzero exterior fields. Magnetic cores can substantially change the result and may saturate.

## 35.8 Toroid

A toroidal coil is essentially a solenoid bent into a ring. For $N$ turns with current $I$, an Amperian circle of radius $r$ *within the winding region* encloses $NI$:

$$
\boxed{B(r)=\frac{\mu_0NI}{2\pi r}.}
$$

The field follows concentric circles around the torus axis and varies approximately as $1/r$ across the winding cross-section. In an ideal tightly wound toroid, field is negligible in the central hole and far outside. Inserting a linear core changes $\mu_0$ to the appropriate effective permeability, provided the constitutive assumptions hold.

---

# Part VIII: Permanent Magnets

Permanent magnets and classical magnetic measurement techniques provide a bridge between dipole theory and laboratory instrumentation. A bar magnet is approximately a magnetic dipole at distances large compared with its length, while its near field depends on geometry and magnetization.

## 36.1 Magnetic Poles and Bar Magnets

An ordinary bar magnet has recognizable north and south ends. In elementary magnetostatic models one sometimes introduces fictitious **pole strengths** $+m_p$ and $-m_p$ separated by an effective magnetic length $2\ell$ to calculate far fields. This is a mathematical model, not evidence for isolated magnetic monopoles.

Magnetic dipole moment in the pole model is $M=m_p(2\ell)$, directed from the model's south pole toward its north pole. Current-loop magnetic moment $\vec\mu=IA\hat n$ describes the same dipole behavior at large distance. Both represent a magnetic source with zero net magnetic charge.

## 36.2 Torque on a Bar Magnet Placed in a Magnetic Field

A small bar magnet of dipole moment $\vec M$ in an approximately uniform field $\vec B$ experiences

$$
\boxed{\vec\tau=\vec M\times\vec B,\qquad U=-\vec M\cdot\vec B.}
$$

The stable orientation is parallel to the field. For a suspended magnet rotated through a small angle $\theta$,

$$
\tau\simeq-MB\theta.
$$

If the magnet's moment of inertia about its suspension axis is $I_{\rm rot}$, the small-amplitude oscillation period is

$$
\boxed{T=2\pi\sqrt{\frac{I_{\rm rot}}{MB}}.}
$$

This is **angular simple harmonic motion** and becomes inaccurate for large oscillation amplitudes, significant damping, or nonuniform fields.

## 36.3 Magnetic Field due to a Bar Magnet

At distances much larger than magnet size, its field is accurately modeled by a magnetic dipole. With $\hat r$ the observation direction,

$$
\boxed{\vec B(\vec r)=\frac{\mu_0}{4\pi r^3}\left[3(\vec M\cdot\hat r)\hat r-\vec M\right].}
$$

On the **axial line**,

$$
\boxed{B_{\rm axial}\simeq\frac{\mu_0}{4\pi}\frac{2M}{r^3}.}
$$

On the **equatorial line**,

$$
\boxed{B_{\rm equatorial}\simeq\frac{\mu_0}{4\pi}\frac{M}{r^3},}
$$

with direction opposite to the magnetic moment. The axial far-field magnitude is twice the equatorial far-field magnitude at the same $r$. These are **dipole approximations**; a finite bar's near field is not given by these simple expressions.

## 36.4 Magnetic Scalar Potential

In a current-free region, $\nabla\times\vec H=0$ for magnetostatics; one can locally write $\vec H=-\nabla\phi_m$ in a simply connected region. In free space this is equivalent to describing $\vec B$ through a scalar magnetic potential up to a constant factor.

For a dipole, one useful vacuum convention is

$$
\phi_m=\frac{\vec M\cdot\hat r}{4\pi r^2},\qquad \vec H=-\nabla\phi_m,
\qquad \vec B=\mu_0\vec H.
$$

**Key limitation:** a globally single-valued magnetic scalar potential generally cannot be used around current-carrying loops, because the circulation of $\vec H$ can be nonzero. Magnetic scalar potential is a convenient mathematical tool **in regions without free current**, not a claim that the general magnetic field is conservative.

## 36.5 Terrestrial Magnetism

Near a location on Earth's surface, the geomagnetic field is resolved into a **horizontal** component $B_H$ and a vertical component $B_V$. If $I_d$ is the magnetic inclination (dip) measured from the horizontal,

$$
\boxed{B_H=B\cos I_d,\qquad B_V=B\sin I_d,\qquad\tan I_d=\frac{B_V}{B_H}.}
$$

**Declination** is the horizontal angle between geographic north and magnetic north. Inclination is the vertical angle the field makes with the horizontal plane. Their values vary with latitude, longitude, altitude, and time; the magnetic and geographic poles are not identical.

## 36.6 Determination of Dip at a Place

A **dip circle** supports a magnetized needle so that it rotates in a vertical plane. Once aligned with the magnetic meridian, the needle can settle in the direction of Earth's total field, and its angle with the horizontal gives the inclination. Off-meridian orientations and pivot friction can bias a raw reading, so practical methods use reversing and multiple orientations.

If the rotating plane is not aligned with the magnetic meridian and makes azimuth $\alpha$ with it, the effective horizontal component in that plane is $B_H\cos\alpha$; the observed apparent dip $I'$ then satisfies

$$
\tan I'=\frac{B_V}{B_H\cos\alpha}=\frac{\tan I_d}{\cos\alpha}.
$$

Correct alignment is therefore not optional.

## 36.7 Neutral Point

A **neutral point** near a magnet is a location where the magnet's field cancels Earth's horizontal field (or another applied field), so the vector sum vanishes:

$$
\boxed{\vec B_{\rm magnet}+\vec B_H=0.}
$$

For a dipole in a geometry where the two fields are opposed, the cancellation distance often follows $r^3\propto M/B_H$. The required orientation depends on whether the point lies on the magnet's axial or equatorial line. Neutral-point positions are not universal constants of a magnet and must be interpreted with the laboratory geometry.

## 36.8 Tangent Galvanometer

A tangent galvanometer uses a circular coil to create a horizontal magnetic field perpendicular to Earth's horizontal component. At the center of an $N$-turn circular coil of radius $R$,

$$
B_c=\frac{\mu_0NI}{2R}.
$$

A small pivoted magnetic needle aligns with the **resultant** field. If the coil and Earth's horizontal field are perpendicular and the needle deflects by $\theta$,

$$
\tan\theta=\frac{B_c}{B_H}
\quad\Longrightarrow\quad
\boxed{I=\frac{2RB_H}{\mu_0N}\tan\theta.}
$$

The tangent relation requires correct coil alignment, negligible field nonuniformity across the needle, and negligible nearby magnetic disturbances.

## 36.9 Moving-coil Galvanometer

A moving coil of $N$ turns and area $A$ in a radial magnetic field experiences approximately constant-magnitude torque

$$
\tau_B=NIAB,
$$

while a suspension or spring provides restoring torque $\tau_s=c\theta$. At equilibrium,

$$
\boxed{NIAB=c\theta\quad\Longrightarrow\quad\theta=\frac{NAB}{c}I.}
$$

Thus deflection is approximately proportional to current. The **current sensitivity** is $d\theta/dI=NAB/c$. A radial field is valuable because the coil-plane orientation does not introduce a varying $\sin\theta$ factor in normal operation.

## 36.10 Shunt

To measure a current larger than the galvanometer's full-scale value, place a low resistor **in parallel**. The voltage across the shunt $S$ equals that across the coil resistance $G$:

$$
(I-I_g)S=I_gG.
$$

Therefore

$$
\boxed{S=\frac{I_gG}{I-I_g}.}
$$

A well-designed ammeter diverts most current around the sensitive galvanometer coil. Low shunt resistance is desirable to avoid significantly modifying the measured circuit.

## 36.11 Tangent Law of Perpendicular Fields

When two **mutually perpendicular** uniform magnetic fields $B_1$ and $B_2$ act on a free magnetic needle, its equilibrium direction is that of their resultant. If the needle makes angle $\theta$ with the $B_1$ direction,

$$
\boxed{\tan\theta=\frac{B_2}{B_1}.}
$$

The law follows directly from vector addition or balancing magnetic torque. It is the operating principle behind tangent galvanometers and several deflection magnetometers; it fails in the same simple form when the field components are not orthogonal.

## 36.12 Deflection Magnetometer

A deflection magnetometer places a known or unknown magnetic dipole at a measured distance from a small compass needle, so that its horizontal field is transverse to Earth's horizontal field. The needle follows the vector resultant:

$$
\boxed{\tan\theta=\frac{B_{\rm bar,transverse}}{B_H}.}
$$

In a long-distance **axial** dipole arrangement, $B_{\rm bar}\simeq(\mu_0/4\pi)(2M/r^3)$; in an **equatorial** arrangement, $B_{\rm bar}\simeq(\mu_0/4\pi)(M/r^3)$. A finite magnet requires an end-correction or a more detailed field expression. Magnet orientation and measurement location must be checked before choosing the factor 1 or 2.

## 36.13 Oscillation Magnetometer

A small magnetic bar suspended in Earth's approximately uniform horizontal field experiences a restoring torque $-MB_H\sin\theta$. Small-angle dynamics are

$$
I_{\rm rot}\ddot\theta+MB_H\theta=0.
$$

Hence its oscillation period is

$$
\boxed{T=2\pi\sqrt{\frac{I_{\rm rot}}{MB_H}}.}
$$

Time many cycles, average the period, and keep angular amplitudes small. The method determines the combination $MB_H$ if $I_{\rm rot}$ is known, not $M$ and $B_H$ independently.

## 36.14 Determination of $M$ and $B_H$

Combine an **oscillation measurement** with a **deflection measurement**. The oscillation relation yields a product:

$$
\boxed{MB_H=\frac{4\pi^2 I_{\rm rot}}{T^2}.}
$$

A distant-bar deflection measurement yields approximately a ratio, for example for an axial geometry,

$$
\boxed{\frac{M}{B_H}\simeq\frac{4\pi r^3}{2\mu_0}\tan\theta.}
$$

Let $P=MB_H$ and $R=M/B_H$. Solve the two positive quantities as

$$
\boxed{M=\sqrt{PR},\qquad B_H=\sqrt{P/R}.}
$$

This is an instructive example of **experimental identifiability**: neither instrument alone isolates both unknowns, but two independent relationships do. Here $M$ is the magnet's **dipole moment**, not magnetization per unit volume.

## 36.15 Gauss's Law for Magnetism

Magnetic field lines form continuous loops rather than beginning or ending on ordinary isolated magnetic charges. Maxwell's magnetic Gauss law is

$$
\boxed{\oint_S\vec B\cdot d\vec A=0\quad\Longleftrightarrow\quad\nabla\cdot\vec B=0.}
$$

Every closed surface has zero **net magnetic flux**, even if large nonzero flux passes through individual patches. Cutting a bar magnet makes smaller dipoles, not a separate north pole and south pole. This is fully consistent with magnetization and pole-model calculations, which are approximate descriptions of dipole distributions.

---

# Part IX: Magnetic Properties of Matter

Materials respond to magnetic fields by reorganizing microscopic magnetic moments. Three familiar response classes are diamagnetism, paramagnetism, and ferromagnetism, but simple linear laws describe only limited operating regimes.

## 37.1 Magnetization of Materials: Intensity of Magnetization

Magnetization (or intensity of magnetization) is the magnetic dipole moment per unit volume:

$$
\boxed{\vec M=\frac{d\vec\mu}{dV},\qquad [M]=\mathrm{A/m}.}
$$

For a uniformly magnetized specimen, total magnetic moment is $\vec\mu_{\rm total}=\vec M\,V$. Magnetization includes the combined effect of microscopic orbital and spin magnetic moments. Note the symbol conflict: Chapter 36 often denotes the **total bar-magnet dipole moment** by $M$, whereas in this chapter $\vec M$ conventionally denotes a **dipole moment density**.

## 37.2 Paramagnetism, Ferromagnetism and Diamagnetism

- **Diamagnetism:** applied field induces an opposing response; weak negative susceptibility, normally very small.
- **Paramagnetism:** materials with net microscopic moments tend to align with an external field; weak positive susceptibility, often temperature dependent.
- **Ferromagnetism:** exchange interactions produce strongly correlated moments and **domains**, often giving very large, nonlinear, history-dependent magnetization.

A paramagnet generally loses much of its field-induced magnetization when the applied field disappears. A ferromagnet may retain **remanence**, which underlies permanent magnets. Magnetic classification concerns microscopic mechanisms and collective organization, not simply whether a material is attracted or repelled by a hand-held magnet in every geometry.

## 37.3 Magnetic Intensity $\vec H$

In SI electromagnetism, auxiliary magnetic field $\vec H$ separates the response of matter from the total magnetic field $\vec B$:

$$
\boxed{\vec B=\mu_0(\vec H+\vec M).}
$$

$\vec B$ is measured in tesla; $\vec H$ and $\vec M$ are measured in A/m. The source equation in magnetostatics is $\nabla\times\vec H=\vec J_{\rm free}$. Inside matter, $\vec B$ depends on applied free currents, geometry, demagnetizing fields, and magnetization.

## 37.4 Magnetic Susceptibility

A homogeneous isotropic **linear** magnetic material responds as

$$
\boxed{\vec M=\chi_m\vec H.}
$$

$\chi_m$ is dimensionless volume susceptibility. Diamagnets usually have $\chi_m<0$; ordinary paramagnets have $\chi_m>0$. Ferromagnets typically do **not** have a fixed field-independent $\chi_m$ across their useful range, so treating them as perfectly linear can obscure saturation and hysteresis.

## 37.5 Permeability

Combining $\vec M=\chi_m\vec H$ with $\vec B=\mu_0(\vec H+\vec M)$ gives

$$
\boxed{\vec B=\mu\vec H,\qquad\mu=\mu_0(1+\chi_m),\qquad\mu_r=1+\chi_m.}
$$

This relation applies to a linear, isotropic magnetic medium. Relative permeability $\mu_r$ is dimensionless. For nonlinear magnetic materials, $B/H$ and $dB/dH$ may differ, and effective permeability can depend on operating point and magnetic history.

## 37.6 Curie's Law

For an ideal classical paramagnet at sufficiently weak field and away from cooperative phase transitions, the susceptibility often varies inversely with absolute temperature:

$$
\boxed{\chi_m=\frac{C}{T}.}
$$

$C$ is a material-dependent Curie constant. Increasing temperature tends to disorder field-aligned moments. Above the Curie temperature, many ferromagnets instead approximately follow a **Curie–Weiss** form $\chi_m\propto1/(T-T_C)$ under appropriate conditions; this is an added refinement, not identical to simple Curie's law.

## 37.7 Properties of Dia-, Para- and Ferromagnetic Substances

| Property | Diamagnetic | Paramagnetic | Ferromagnetic |
|---|---|---|---|
| Typical susceptibility | Small, negative | Small, positive | Large; nonlinear and variable |
| Relative permeability | Slightly below 1 | Slightly above 1 | Often much larger than 1 |
| Dominant response | Induced moment opposes field | Partial alignment of existing moments | Strong exchange correlations and domains |
| Behavior after field removed | No ordinary remanence | No ordinary remanence | Remanence may remain |
| Temperature trend | Often weak | Often Curie-like | Strong; magnetic ordering can vanish above $T_C$ |

Examples to remember: bismuth is strongly diamagnetic among ordinary substances; aluminum is paramagnetic; iron, cobalt, and nickel are classic ferromagnets under suitable conditions. Real magnetic responses also depend on crystalline structure and phase.

## 37.8 Hysteresis

For ferromagnets, the field response depends on how the material was previously magnetized. Cycling $H$ traces a **hysteresis loop** in the $B$–$H$ plane. The loop reveals:

- **Saturation:** most alignable domains have approached the field direction.
- **Remanence:** residual $B$ when applied $H$ returns to zero.
- **Coercive field:** reversed $H$ needed to reduce $B$ through zero on the appropriate branch.

The energy dissipated per unit volume in a complete quasistatic magnetization cycle equals the signed loop area in the $H$–$B$ plane:

$$
\boxed{w_{\rm loss}=\oint H\,dB,}
$$

interpreted as a positive dissipated energy for the correctly oriented cycle. The loop should not be confused with a reversible constitutive curve; a single number “permeability” may be inadequate.

## 37.9 Soft Iron and Steel

**Soft magnetic materials** are selected for easy magnetization and demagnetization, often with low coercivity and comparatively small hysteresis loss. They are valuable for transformer cores, electromagnets, and inductors. **Hard magnetic materials** resist demagnetization and are useful for permanent magnets; traditional steel examples illustrate this distinction, though modern engineered alloys and rare-earth magnets can be far more capable.

A transformer core should generally be magnetically *soft* rather than strongly remanent. Material choice also considers electrical resistivity, saturation flux density, eddy-current loss, cost, and operating frequency.

---

# Part X: Electromagnetic Induction

Static electric and magnetic fields can be treated separately in many problems, but **time-varying magnetic flux produces an electric circulation**. This is the essential new physical effect behind generators, transformers, inductors, and induction heating.

## 38.1 Faraday's Law of Electromagnetic Induction

Magnetic flux through an oriented surface $S$ is

$$
\boxed{\Phi_B=\int_S\vec B\cdot d\vec A.}
$$

If the **flux linkage** through a circuit of $N$ tightly coupled turns changes, the total induced emf is

$$
\boxed{\mathcal E_{\rm ind}=-N\frac{d\Phi_B}{dt}.}
$$

The negative sign is fixed by orientation conventions and Lenz's law. Flux can change because the field changes, because the circuit's shape or area changes, or because its orientation changes. For a stationary loop, the induced emf can be written as $\oint\vec E\cdot d\vec\ell=-d\Phi_B/dt$; for a moving loop one must include motional contributions, addressed below.

## 38.2 Lenz's Law

The induced current flows in whichever direction causes its **own magnetic effect to oppose the change in flux** responsible for it. It does not necessarily oppose the existing field. For example:

- An *increasing* external flux into the page induces a counteracting flux out of the page.
- A *decreasing* flux into the page induces a compensating flux into the page.

This is a statement of **energy consistency**: if an induced current strengthened its own cause indefinitely, electrical energy could emerge without the required mechanical or field-source work.

A reliable sign procedure: choose a loop normal, decide whether signed external flux is increasing or decreasing, decide the induced field needed to oppose that *change*, then determine current direction by the right-hand rule.

## 38.3 The Origin of Induced emf

There are two useful limiting mechanisms.

**Motional emf:** charges in a moving conductor feel $q\vec v\times\vec B$. The emf along a moving conducting segment is

$$
\boxed{\mathcal E_{\rm motion}=\int_{\rm segment}(\vec v\times\vec B)\cdot d\vec\ell.}
$$

For a straight rod of length $\ell$ moving perpendicular to its length and to uniform $\vec B$,

$$
\boxed{|\mathcal E|=B\ell v.}
$$

The magnetic force on charges leads to charge separation and an internal electric field. In a closed conducting circuit, current flows and mechanical work is required to maintain the motion against electromagnetic reaction forces.

**Transformer emf:** a time-varying $\vec B$ creates a circulating nonconservative electric field even when the circuit is stationary:

$$
\boxed{\oint\vec E\cdot d\vec\ell=-\frac{d\Phi_B}{dt}.}
$$

The unified moving-contour formulation uses $\oint(\vec E+\vec v_{\rm wire}\times\vec B)\cdot d\vec\ell$ and the appropriate time derivative of flux through the moving loop. Do not treat $\mathcal E$ as merely an electrostatic potential difference around a nonconservative loop.

## 38.4 Eddy Current

A changing magnetic flux through an **extended conducting body** can drive circulating currents within the material, called **eddy currents**. Their Joule losses heat the material; their magnetic fields can oppose relative motion between magnet and conductor.

Uses include magnetic braking, induction heating, metal detection, and some damping systems. Unwanted eddy-current losses in transformer cores are reduced by electrically insulated thin laminations or higher-resistivity ferrites. Energy dissipated by eddy currents ultimately comes from the changing field's source or from external mechanical work.

## 38.5 Self-induction

A current in a circuit produces flux through the same circuit. If the linkage is proportional to current in a linear magnetic system, define inductance $L$ by

$$
\boxed{N\Phi_B=LI.}
$$

Then changing current induces a back emf

$$
\boxed{\mathcal E_L=-L\frac{dI}{dt}.}
$$

The SI unit is henry $1\ \mathrm H=1\ \mathrm{V\,s/A}$. For a long air-core solenoid (length $\ell$, $N$ turns, area $A$, negligible fringing),

$$
\boxed{L\simeq\frac{\mu_0N^2A}{\ell}.}
$$

An inductor resists **changes in current**, not steady current itself. In a nonlinear ferromagnetic core, flux linkage need not remain proportional to current, so inductance can depend on operating point.

## 38.6 Growth and Decay of Current in an LR Circuit

For a series $RL$ circuit with ideal source $\mathcal E$ switched on at $t=0$, KVL gives

$$
\mathcal E=L\frac{dI}{dt}+RI.
$$

With $I(0)=0$,

$$
\boxed{I(t)=\frac{\mathcal E}{R}\left(1-e^{-tR/L}\right).}
$$

The **inductive time constant** is

$$
\boxed{\tau_L=\frac{L}{R}.}
$$

When a current $I_0$ circulates through $R$ after the source is removed (with an appropriate closed discharge path),

$$
\boxed{I(t)=I_0e^{-tR/L}.}
$$

At switch-on, a finite inductor with $I(0)=0$ initially opposes the current change; after a long time it behaves like a short circuit in this ideal DC model. A current through an ideal inductor **cannot jump instantaneously** without an unbounded voltage.

## 38.7 Energy Stored in an Inductor

Build up an inductor current gradually. Instantaneous input power associated with field energy is $P=VI=LI(dI/dt)$ in a linear model, so

$$
U_L=\int_0^I Li\,di
\quad\Longrightarrow\quad
\boxed{U_L=\frac12LI^2.}
$$

For a uniform magnetic field in vacuum, magnetic field energy density is

$$
\boxed{u_B=\frac{B^2}{2\mu_0}.}
$$

More generally $u=\int_0^B H(B')\,dB'$ for a reversible material law. Dissipative, hysteretic magnetic media cannot be fully characterized by a single-valued stored-energy function. The field-energy picture is the magnetic analogue of capacitor energy $U_C=\tfrac12CV^2$.

## 38.8 Mutual Induction

Current in circuit 1 can link flux through circuit 2. For linear reciprocal geometries, define mutual inductance $M$:

$$
\boxed{N_2\Phi_{21}=MI_1,\qquad\mathcal E_2=-M\frac{dI_1}{dt}.}
$$

Reciprocity generally gives $M_{12}=M_{21}$ for ordinary linear passive media with consistent winding orientations. The coupling coefficient is

$$
\boxed{k=\frac{|M|}{\sqrt{L_1L_2}},\qquad0\le k\le1.}
$$

$k=1$ represents ideal complete flux coupling, not a typical real transformer. Sign conventions for dot-marked windings determine whether induced voltages aid or oppose one another.

## 38.9 Induction Coil

An induction coil uses a changing primary current to create a large transient secondary emf. Typically the primary has relatively few turns, the secondary many turns, and a magnetic core enhances coupling. A contact interrupter or switching element rapidly changes primary current, and the associated changing flux produces voltage pulses in the secondary:

$$
\mathcal E_s=-N_s\frac{d\Phi}{dt}.
$$

A high turn ratio helps produce high voltage, but insulation, leakage inductance, arcing, core behavior, and switching speed strongly affect real operation. The energy is not created by the turns ratio: it ultimately comes from the primary electrical supply.

---

# Part XI: Alternating Current

Alternating-current theory extends circuit reasoning from constant quantities to periodic ones. Phase becomes essential: a capacitor and an inductor exchange stored energy with a source rather than behaving like ordinary resistors.

## 39.1 Alternating Current

Sinusoidal current is commonly modeled as

$$
\boxed{i(t)=I_0\sin(\omega t+\phi),\qquad \omega=2\pi f=\frac{2\pi}{T}.}
$$

$I_0$ is peak current; $f$ is frequency; $T$ is period; $\phi$ is initial phase. A sinusoidal alternating voltage is similarly $v(t)=V_0\sin(\omega t+\phi_v)$. The signed average of a perfect sinusoid over a complete cycle is zero, but it can still deliver positive time-averaged power to a resistor because $i^2$ remains nonnegative.

## 39.2 AC Generator or AC Dynamo

Consider a coil with $N$ turns and area $A$ rotating at constant angular speed $\omega$ in a uniform field $B$. If its normal initially aligns with the field,

$$
\Phi_B(t)=BA\cos\omega t.
$$

Faraday's law then gives

$$
\boxed{\mathcal E(t)=-N\frac{d\Phi_B}{dt}=NBA\omega\sin\omega t.}
$$

The **peak emf** is $\mathcal E_0=NBA\omega$. A conventional AC generator uses slip rings and brushes to connect the rotating armature to an external circuit; the exact mechanical layout can vary. The generator converts mechanical input power into electromagnetic power, subject to electrical and mechanical losses.

## 39.3 Instantaneous and rms Current

For $i(t)=I_0\sin(\omega t+\phi)$, its signed full-cycle mean is zero. A resistor's mean heating power is instead determined by the mean of $i^2$:

$$
\langle i^2\rangle=\frac{1}{T}\int_0^TI_0^2\sin^2(\omega t+\phi)\,dt=\frac{I_0^2}{2}.
$$

Define **root mean square** current and voltage by

$$
\boxed{I_{\rm rms}=\sqrt{\langle i^2\rangle}=\frac{I_0}{\sqrt2},\qquad V_{\rm rms}=\frac{V_0}{\sqrt2}.}
$$

For a pure resistor, $P_{\rm avg}=I_{\rm rms}^2R$. The $1/\sqrt2$ conversion is for **sinusoids only**; for other waveforms compute RMS directly from the squared waveform.

## 39.4 Simple AC Circuits

**Pure resistor $R$.** Current and voltage are in phase:

$$
i(t)=\frac{V_0}{R}\sin\omega t,\qquad \boxed{Z_R=R.}
$$

**Pure inductor $L$.** With $v=L\,di/dt$, sinusoidal steady state gives

$$
\boxed{X_L=\omega L,\qquad I_0=\frac{V_0}{X_L}.}
$$

Current **lags** applied voltage by $90^\circ$. The inductor alternately stores and returns magnetic energy; ideal time-averaged absorbed power is zero.

**Pure capacitor $C$.** With $i=C\,dv/dt$,

$$
\boxed{X_C=\frac1{\omega C},\qquad I_0=\frac{V_0}{X_C}.}
$$

Current **leads** applied voltage by $90^\circ$. A capacitor has high reactance at low frequencies and low reactance at high frequencies, within the ideal lumped-element regime.

**Memory aid:** *ELI the ICE man* is sometimes used: for **L**, voltage $E$ leads current $I$; for **C**, current $I$ leads voltage $E$. The equations above are the reliable reference when memory aids fail.

## 39.5 Vector Method to Find the Current in an AC Circuit

Sinusoidal steady-state variables at a common $\omega$ can be represented by **phasors**, rotating complex amplitudes or stationary vectors with relative phase angles. In a series $RLC$ circuit, current is common; voltage drops are $IR$ along the current phasor, $IX_L$ at $+90^\circ$, and $IX_C$ at $-90^\circ$.

The total voltage amplitude is therefore the vector sum,

$$
V_0^2=(I_0R)^2+[I_0(X_L-X_C)]^2.
$$

Define impedance magnitude

$$
\boxed{|Z|=\sqrt{R^2+(X_L-X_C)^2},\qquad I_{\rm rms}=\frac{V_{\rm rms}}{|Z|}.}
$$

The phase angle by which source voltage leads current is

$$
\boxed{\tan\phi=\frac{X_L-X_C}{R}.}
$$

If $X_L>X_C$, the circuit is net inductive (current lags); if $X_C>X_L$, it is net capacitive (current leads). Vector addition, rather than scalar voltage summation, is essential.

## 39.6 More AC Circuits

The phasor method covers common two-element arrangements:

- **Series $RL$:** $|Z|=\sqrt{R^2+(\omega L)^2}$ and $\tan\phi=\omega L/R$.
- **Series $RC$:** $|Z|=\sqrt{R^2+1/(\omega C)^2}$ and $\tan\phi=-1/(\omega CR)$.
- **Series $RLC$:** $|Z|=\sqrt{R^2+(\omega L-1/(\omega C))^2}$.

The ideal **series-resonance** frequency occurs when inductive and capacitive reactances cancel:

$$
\boxed{\omega_0=\frac1{\sqrt{LC}},\qquad f_0=\frac1{2\pi\sqrt{LC}}.}
$$

At resonance, $|Z|=R$ and current reaches its peak at fixed applied source voltage. For series resonance the quality factor and approximate half-power bandwidth are

$$
\boxed{Q_{\rm series}=\frac{\omega_0L}{R},\qquad \Delta\omega\simeq\frac{R}{L}.}
$$

Those last relations assume an ideal lumped series $RLC$ model and standard half-power definitions. The capacitor and inductor can have substantial opposing voltages even while the combined reactive voltage vanishes.

## 39.7 Power in AC Circuits

For $v(t)=V_0\sin\omega t$ and $i(t)=I_0\sin(\omega t-\phi)$, multiply and average over a complete cycle:

$$
\langle p\rangle=\frac{V_0I_0}{2}\cos\phi.
$$

In RMS quantities,

$$
\boxed{P_{\rm avg}=V_{\rm rms}I_{\rm rms}\cos\phi=I_{\rm rms}^2R.}
$$

$\cos\phi$ is the **power factor** for a sinusoidal linear circuit. Real power $P$ (W) is not the same as apparent power $S=VI$ (VA). In the same restricted context reactive power is $Q_{\rm reactive}=VI\sin\phi$ (var). A pure ideal $L$ or $C$ has zero mean active power, even while exchanging energy with the source throughout the cycle.

## 39.8 Choke Coil

A **choke** is an inductor used to limit AC current using inductive reactance $X_L=\omega L$, ideally with much less dissipative power than a large series resistor would require. Because current lags voltage, a choke changes power factor and can create voltage drops without equivalent ohmic heating.

A realistic choke has winding resistance, core losses, stray capacitance, and frequency-dependent behavior. It may saturate under large current. Do not substitute an ideal inductor's zero-power statement for a real device's efficiency calculation.

## 39.9 Hot-wire Instruments

A current-carrying thin wire heats by $i^2R$. Its thermal expansion can operate a mechanical pointer, producing a response related approximately to **mean-square current**, so a well-calibrated hot-wire instrument can measure AC as well as DC.

Such instruments historically provided waveform-insensitive indication within thermal and frequency limits. The operating principle is thermal, not a direct measurement of the signed instantaneous current. Slow thermal response and ambient-temperature sensitivity constrain accuracy.

## 39.10 DC Dynamo

A **DC dynamo** is a generator that provides approximately unidirectional output by using a **commutator** rather than two simple slip rings. The induced emf in the rotating armature still reverses internally every half-turn; the commutator reverses the coil's connections at corresponding intervals so the external terminal polarity remains approximately fixed.

The output of a simple single-coil generator is **pulsating**, not perfectly steady DC. Multiple windings and commutator segments reduce ripple. Electrical output power still comes from mechanical input supplied by the shaft.

## 39.11 DC Motor

A motor reverses the generator energy-conversion direction. A current-carrying armature in a magnetic field experiences torque $\vec\tau=\vec\mu\times\vec B$, causing shaft rotation. In a simple brushed DC motor, the **commutator** switches current direction at suitable armature orientations to maintain a useful average torque direction.

As the motor rotates, induction generates a **back emf** opposing the applied voltage. In an elementary steady model,

$$
\boxed{V=E_b+IR,\qquad E_b\propto\omega.}
$$

Ignoring other losses, converted mechanical power is approximately $P_{\rm mech}=E_bI$. At stall $\omega\simeq0$, so back emf is small and current can be large, making thermal and torque limits important.

## 39.12 Transformer

Two windings share a changing magnetic flux in a common core. In an **ideal transformer** (perfect coupling, no winding resistance, leakage or core loss), Faraday's law gives

$$
\boxed{\frac{V_s}{V_p}=\frac{N_s}{N_p}.}
$$

Conservation of average power in the ideal device implies

$$
\boxed{V_pI_p=V_sI_s,\qquad\frac{I_s}{I_p}=\frac{N_p}{N_s}.}
$$

A step-up transformer raises voltage and lowers current for the same ideal power; a step-down transformer does the opposite. Continuous DC does **not** produce the sustained time-varying flux needed for ordinary transformer operation. In real transformers, magnetizing current, copper loss, core hysteresis, eddy currents, leakage, and saturation matter.

---

# Part XII: Electromagnetic Waves

This is the conceptual culmination. Maxwell added the missing time-dependent term to Ampère's law, exposing a mutual coupling: changing magnetic fields create curling electric fields, and changing electric fields can create curling magnetic fields. The field equations permit self-propagating waves in vacuum.

## 40.1 Introduction

A time-varying electromagnetic field can propagate through space even without conducting matter. Light is an electromagnetic phenomenon; radio, infrared, visible, ultraviolet, X-rays, and gamma rays share the same broad classical wave description while differing greatly in frequency and wavelength.

A wave transmits electromagnetic energy and momentum. It does not require charges to be physically carried along the propagation direction as in a conduction current, and vacuum propagation does not require a material medium.

## 40.2 Maxwell's Displacement Current

Consider a charging capacitor. A wire leads conduction current $I$ into a plate, but no free charge crosses the ideal dielectric gap. Applying the magnetostatic form of Ampère's law to different spanning surfaces would produce an apparent contradiction unless a new term accounts for the changing electric field.

For a vacuum gap, define **displacement current**

$$
\boxed{I_D=\varepsilon_0\frac{d\Phi_E}{dt}.}
$$

The generalized Ampère–Maxwell law is

$$
\boxed{\oint_C\vec B\cdot d\vec\ell=\mu_0I_{\rm conduction,enc}+\mu_0\varepsilon_0\frac{d\Phi_E}{dt}.}
$$

For an ideal parallel-plate capacitor $E=Q/(\varepsilon_0A)$, so $\varepsilon_0d(EA)/dt=dQ/dt=I$; the displacement current across the gap matches the conduction current in the wire. **Displacement current is not a flow of physical free charges through the vacuum gap.**

## 40.3 Continuity of Electric Current

Local charge conservation is

$$
\boxed{\nabla\cdot\vec J+\frac{\partial\rho}{\partial t}=0.}
$$

Taking the divergence of $\nabla\times\vec B=\mu_0\vec J+\mu_0\varepsilon_0\partial\vec E/\partial t$ gives

$$
0=\mu_0\left(\nabla\cdot\vec J+\varepsilon_0\frac{\partial}{\partial t}\nabla\cdot\vec E\right).
$$

Using Gauss's law $\nabla\cdot\vec E=\rho/\varepsilon_0$ yields continuity automatically. The displacement-current term is therefore not merely a convenient capacitor trick; it restores **mathematical consistency with charge conservation**.

## 40.4 Maxwell's Equations and Plane Electromagnetic Waves

In vacuum, with total charge density $\rho$ and conduction current density $\vec J$, Maxwell's equations in differential form are

$$
\boxed{\begin{aligned}
\nabla\cdot\vec E&=\frac{\rho}{\varepsilon_0},\\
\nabla\cdot\vec B&=0,\\
\nabla\times\vec E&=-\frac{\partial\vec B}{\partial t},\\
\nabla\times\vec B&=\mu_0\vec J+\mu_0\varepsilon_0\frac{\partial\vec E}{\partial t}.
\end{aligned}}
$$

In a charge-free, current-free region, use the vector identity $\nabla\times(\nabla\times\vec E)=\nabla(\nabla\cdot\vec E)-\nabla^2\vec E$ and substitute Faraday's and Ampère–Maxwell laws. Because $\nabla\cdot\vec E=0$ in the region,

$$
-\nabla^2\vec E=-\mu_0\varepsilon_0\frac{\partial^2\vec E}{\partial t^2}.
$$

Thus

$$
\boxed{\nabla^2\vec E=\mu_0\varepsilon_0\frac{\partial^2\vec E}{\partial t^2},\qquad
\nabla^2\vec B=\mu_0\varepsilon_0\frac{\partial^2\vec B}{\partial t^2}.}
$$

Comparing with a standard wave equation identifies the vacuum propagation speed:

$$
\boxed{c=\frac{1}{\sqrt{\mu_0\varepsilon_0}}\simeq2.998\times10^8\ \mathrm{m/s}.}
$$

A linearly polarized wave traveling in the $+x$ direction can be represented by

$$
\vec E=E_0\hat y\cos(kx-\omega t),\qquad
\vec B=B_0\hat z\cos(kx-\omega t),
$$

where $\omega=ck$, $E_0=cB_0$, and $\vec E\times\vec B$ points along propagation. The fields are **transverse, mutually perpendicular, and in phase** in this vacuum plane-wave model.

## 40.5 Energy Density and Intensity

The electromagnetic energy density in vacuum is the sum of electric and magnetic contributions:

$$
\boxed{u=\frac12\varepsilon_0E^2+\frac{B^2}{2\mu_0}.}
$$

For a vacuum plane wave with $E=cB$, the two contributions are equal:

$$
\boxed{u_E=u_B=\frac12\varepsilon_0E^2,\qquad u=\varepsilon_0E^2.}
$$

The **Poynting vector** gives electromagnetic energy-flow density:

$$
\boxed{\vec S=\frac1{\mu_0}\vec E\times\vec B.}
$$

For a sinusoidal vacuum plane wave, the time-averaged intensity is

$$
\boxed{I=\langle S\rangle=\frac12\varepsilon_0cE_0^2
=\frac{cB_0^2}{2\mu_0}.}
$$

The factor $1/2$ comes from averaging a squared sinusoid. $E_0$ and $B_0$ here are **peak** field amplitudes, not RMS fields.

## 40.6 Momentum

Electromagnetic waves carry momentum as well as energy. For radiation traveling in one direction in vacuum,

$$
\boxed{p_{\rm radiation}=\frac{U}{c}.}
$$

This yields radiation pressure when an absorbing or reflecting surface receives momentum flux. For normally incident radiation of intensity $I$:

$$
\boxed{P_{\rm absorb}=\frac{I}{c},\qquad P_{\rm reflect}=\frac{2I}{c}}
$$

for ideal complete absorption and ideal specular reflection respectively. The second result assumes reversal of the normal momentum component, and real reflectivity and geometry require additional factors. Radiation pressure is tiny in ordinary life but relevant to precision optics and solar sailing.

## 40.7 Electromagnetic Spectrum and Radiation in Atmosphere

All vacuum electromagnetic waves obey

$$
\boxed{c=f\lambda.}
$$

As frequency increases, wavelength decreases. The approximate progression is **radio → microwave → infrared → visible → ultraviolet → X-ray → gamma ray**. Boundaries between categories are conventional and sometimes overlap; wavelength alone does not determine a radiation source's production mechanism.

Earth's atmosphere transmits some spectral bands relatively well (notably much of visible light and selected radio/microwave windows) but strongly absorbs others through molecular transitions and electronic absorption. Ozone is important for ultraviolet attenuation, while water vapour and carbon dioxide absorb many infrared bands. Scattering also redistributes incident sunlight. **An atmosphere is a frequency-selective medium**, not a perfectly transparent shell.

---

# Consolidated Formula Sheet

This is a **recall map**, not a substitute for checking the assumptions stated in the theory sections. Formulas using $\varepsilon$ or $\mu$ as scalar constants assume a suitable homogeneous, isotropic, linear medium. Unless otherwise indicated, $k_e=1/(4\pi\varepsilon_0)$.

## Chapter 29: Electric Field and Potential

| Topic | Principal relation |
|---|---|
| Quantization | $q=ne$ |
| Coulomb magnitude | $F=k_e\lvert q_1q_2\rvert/r^2$ |
| Force on test charge | $\vec F=q\vec E$ |
| Point-charge field | $\vec E=k_eQ\hat r/r^2$ |
| Pair potential energy | $U=k_eq_1q_2/r$ |
| Point-charge potential | $V=k_eQ/r$ |
| Potential difference | $V_B-V_A=-\int_A^B\vec E\cdot d\vec l$ |
| Field-gradient relation | $\vec E=-\nabla V$ |
| Dipole moment | $\vec p=q\vec d$ |
| Dipole energy and torque | $U=-\vec p\cdot\vec E$, $\vec\tau=\vec p\times\vec E$ |

## Chapter 30: Gauss's Law

| Topic | Principal relation |
|---|---|
| Electric flux | $\Phi_E=\oint\vec E\cdot d\vec A$ |
| Gauss's law | $\Phi_E=Q_{\rm enc}/\varepsilon_0$ |
| Infinite line | $E=\lvert\lambda\rvert/(2\pi\varepsilon_0r)$ |
| Infinite insulating sheet | $E=\lvert\sigma\rvert/(2\varepsilon_0)$ |
| Conducting surface, outside | $E_\perp=\sigma/\varepsilon_0$ |
| Uniform solid sphere, inside | $E=k_e\lvert Q\rvert r/R^3$ |
| Spherical shell, inside | $E=0$ |

## Chapter 31: Capacitors

| Topic | Principal relation |
|---|---|
| Definition | $C=Q/V$ |
| Parallel plate | $C=\varepsilon A/d$ |
| Sphere | $C=4\pi\varepsilon_0R$ |
| Spherical capacitor | $C=4\pi\varepsilon_0ab/(b-a)$ |
| Coaxial capacitor | $C=2\pi\varepsilon_0L/\ln(b/a)$ |
| Parallel network | $C_{\rm eq}=\sum C_i$ |
| Series network | $1/C_{\rm eq}=\sum1/C_i$ |
| Field energy | $U=Q^2/(2C)=CV^2/2=QV/2$ |
| Vacuum field density | $u_E=\varepsilon_0E^2/2$ |
| Linear dielectric | $\vec D=\varepsilon_0\vec E+\vec P=\varepsilon\vec E$ |
| Gauss for free charge | $\oint\vec D\cdot d\vec A=Q_{\rm free}$ |

## Chapter 32: Current and Circuits

| Topic | Principal relation |
|---|---|
| Current | $I=dQ/dt$ |
| Current density | $I=\int\vec J\cdot d\vec A$ |
| Drift | $I=n\lvert q\rvert Av_d$ |
| Ohm | $V=IR$ |
| Wire resistance | $R=\rho L/A$ |
| Cell terminal voltage | $V=\mathcal E-Ir$ (discharging) |
| Power | $P=VI=I^2R=V^2/R$ (last forms for an ohmic resistor) |
| Kirchhoff node/loop | $\sum I=0$, $\sum\Delta V=0$ (quasistatic) |
| Resistors: series/parallel | $R_{\rm s}=\sum R_i$, $1/R_{\rm p}=\sum1/R_i$ |
| Wheatstone balance | $P/Q=R/S$ (defined arm arrangement) |
| RC charge/discharge | $q=C\mathcal E(1-e^{-t/RC})$, $q=Q_0e^{-t/RC}$ |
| RC time constant | $\tau_C=RC$ |

## Chapter 33: Heating and Chemical Effects

| Topic | Principal relation |
|---|---|
| Joule heating | $H=I^2Rt$ (constant ohmic $I,R$) |
| Seebeck emf | $\mathcal E\simeq(S_A-S_B)\Delta T$ (nearly constant coefficients) |
| Peltier heating/cooling | $\dot Q_P=\Pi I$ (signed convention) |
| Faraday charge constant | $F=N_Ae$ |
| Deposited mass | $m=MQ/(zF)$ |
| Charge measured by coulombmeter | $Q=mzF/M$ |

## Chapter 34: Magnetic Motion and Torque

| Topic | Principal relation |
|---|---|
| Lorentz force | $\vec F=q(\vec E+\vec v\times\vec B)$ |
| Cyclotron radius and frequency | $r=mv_\perp/(\lvert q\rvert B)$, $\omega_c=\lvert q\rvert B/m$ |
| Magnetic force on wire | $d\vec F=I\,d\vec l\times\vec B$ |
| Loop moment | $\vec\mu=NIA\hat n$ |
| Loop torque and energy | $\vec\tau=\vec\mu\times\vec B$, $U=-\vec\mu\cdot\vec B$ |

## Chapter 35: Current-generated Magnetic Fields

| Topic | Principal relation |
|---|---|
| Biot–Savart | $d\vec B=(\mu_0I/4\pi)(d\vec l\times\hat r)/r^2$ |
| Long straight wire | $B=\mu_0I/(2\pi r)$ |
| Parallel-wire force | $F/L=\mu_0I_1I_2/(2\pi d)$ |
| Circular-loop center | $B=\mu_0NI/(2R)$ |
| Circular-loop axis | $B=\mu_0NIR^2/[2(R^2+x^2)^{3/2}]$ |
| Magnetostatic Ampère | $\oint\vec B\cdot d\vec l=\mu_0I_{\rm enc}$ |
| Long solenoid | $B\simeq\mu_0(N/L)I$ |
| Ideal toroid | $B(r)=\mu_0NI/(2\pi r)$ |

## Chapter 36: Permanent Magnets and Instruments

| Topic | Principal relation |
|---|---|
| Magnetic dipole torque | $\vec\tau=\vec M\times\vec B$ |
| Dipole axial field (far) | $B\simeq(\mu_0/4\pi)(2M/r^3)$ |
| Dipole equatorial field (far) | $B\simeq(\mu_0/4\pi)(M/r^3)$ |
| Horizontal and vertical Earth field | $B_H=B\cos I_d$, $B_V=B\sin I_d$ |
| Tangent galvanometer | $I=2RB_H\tan\theta/(\mu_0N)$ |
| Moving-coil galvanometer | $\theta=NIAB/c$ |
| Galvanometer shunt | $S=I_gG/(I-I_g)$ |
| Oscillating bar magnet | $T=2\pi\sqrt{I_{\rm rot}/(MB_H)}$ |
| No magnetic monopole flux | $\oint\vec B\cdot d\vec A=0$ |

## Chapter 37: Magnetic Matter

| Topic | Principal relation |
|---|---|
| Magnetization | $\vec M=d\vec\mu/dV$ |
| Magnetic auxiliary field | $\vec B=\mu_0(\vec H+\vec M)$ |
| Linear susceptibility | $\vec M=\chi_m\vec H$ |
| Linear permeability | $\mu_r=1+\chi_m$ |
| Curie's law | $\chi_m=C/T$ |
| Hysteresis loss density | $w_{\rm loss}=\oint H\,dB$ (positive cycle orientation) |

## Chapter 38: Electromagnetic Induction

| Topic | Principal relation |
|---|---|
| Magnetic flux | $\Phi_B=\int\vec B\cdot d\vec A$ |
| Faraday–Lenz | $\mathcal E=-N\,d\Phi_B/dt$ |
| Rod motional emf | $\lvert\mathcal E\rvert=B\ell v$ (orthogonal geometry) |
| Self-induction | $\mathcal E_L=-L\,dI/dt$ |
| Long solenoid inductance | $L\simeq\mu_0N^2A/\ell$ |
| LR time constant | $\tau_L=L/R$ |
| LR growth | $I=(\mathcal E/R)(1-e^{-tR/L})$ |
| Magnetic stored energy | $U_L=LI^2/2$ |
| Mutual induction | $\mathcal E_2=-M\,dI_1/dt$ |

## Chapter 39: Alternating Current

| Topic | Principal relation |
|---|---|
| Sinusoid | $i=I_0\sin(\omega t+\phi)$ |
| Frequency | $\omega=2\pi f$ |
| Generator emf | $\mathcal E=NBA\omega\sin\omega t$ |
| RMS amplitudes | $I=I_0/\sqrt2$, $V=V_0/\sqrt2$ |
| Reactance | $X_L=\omega L$, $X_C=1/(\omega C)$ |
| Series impedance magnitude | $\lvert Z\rvert=\sqrt{R^2+(X_L-X_C)^2}$ |
| Phase angle | $\tan\phi=(X_L-X_C)/R$ |
| Series resonance | $\omega_0=1/\sqrt{LC}$ |
| Mean active power | $P=VI\cos\phi=I^2R$ |
| Ideal transformer | $V_s/V_p=N_s/N_p=I_p/I_s$ |

## Chapter 40: Electromagnetic Waves

| Topic | Principal relation |
|---|---|
| Displacement current (vacuum) | $I_D=\varepsilon_0\,d\Phi_E/dt$ |
| Ampère–Maxwell | $\oint\vec B\cdot d\vec l=\mu_0I+\mu_0\varepsilon_0\,d\Phi_E/dt$ |
| Wave speed | $c=(\mu_0\varepsilon_0)^{-1/2}$ |
| Vacuum plane-wave amplitudes | $E_0=cB_0$ |
| Field energy density | $u=\varepsilon_0E^2/2+B^2/(2\mu_0)$ |
| Poynting vector | $\vec S=(\vec E\times\vec B)/\mu_0$ |
| Sinusoidal mean intensity | $I=\varepsilon_0cE_0^2/2$ |
| Radiation pressure | $P_{\rm abs}=I/c$, $P_{\rm refl}=2I/c$ (normal incidence, ideal) |
| Wavelength | $c=f\lambda$ |

---

# Integrated Worked Examples

All examples here are **new calculations** constructed for revision; they are not copied from the textbook. Numerical values are rounded reasonably, and idealizing assumptions are stated. For quick estimates take $k_e\simeq9.0\times10^9\ \mathrm{N\,m^2/C^2}$, $\varepsilon_0\simeq8.85\times10^{-12}\ \mathrm{F/m}$, and $\mu_0\simeq4\pi\times10^{-7}\ \mathrm{H/m}$.

## Example A: Coulomb Force with Opposite Charges (Chapter 29)

**Problem.** Charges $+2.0\ \mu\mathrm C$ and $-3.0\ \mu\mathrm C$ are $0.30\ \mathrm m$ apart. Find force magnitude and direction.

$$
F=k_e\frac{|q_1q_2|}{r^2}=
9.0\times10^9\frac{(2.0\times10^{-6})(3.0\times10^{-6})}{(0.30)^2}
=\boxed{0.60\ \mathrm N}.
$$

The charges **attract**, so forces point toward one another and are equal and opposite. The sign determines the direction; the magnitude calculation uses absolute values.

## Example B: Potential versus Potential Energy (Chapter 29)

**Problem.** A $+5.0\ \mathrm{nC}$ point charge creates a potential at $r=0.20\ \mathrm m$. What is the potential and the energy of a $-2.0\ \mathrm{nC}$ test charge there, with infinity as zero?

$$
V=\frac{k_eQ}{r}=\frac{9.0\times10^9\cdot5.0\times10^{-9}}{0.20}
=\boxed{225\ \mathrm V}.
$$

$$
U=qV=(-2.0\times10^{-9})(225)=\boxed{-4.5\times10^{-7}\ \mathrm J}.
$$

Positive $V$ and negative $U$ are perfectly compatible because the test charge is negative.

## Example C: Gaussian Cylinder Around a Line (Chapter 30)

**Problem.** An extremely long line has $\lambda=4.0\ \mathrm{nC/m}$. Estimate its field $0.10\ \mathrm m$ away.

$$
E=\frac{\lambda}{2\pi\varepsilon_0r}
=\frac{4.0\times10^{-9}}{2\pi(8.85\times10^{-12})(0.10)}
\simeq\boxed{7.2\times10^2\ \mathrm{N/C}}.
$$

The field is radial, outward for this positive line charge. The answer relies on the *effectively infinite line* approximation.

## Example D: Field Inside and Outside a Uniformly Charged Sphere (Chapter 30)

**Problem.** A nonconducting sphere has $Q=1.0\ \mu\mathrm C$, radius $R=0.10\ \mathrm m$, and uniform volume charge density. Find $E$ at $r=0.05\ \mathrm m$ and $0.20\ \mathrm m$.

Inside:

$$
E_{\rm in}=k_e\frac{Qr}{R^3}=9.0\times10^9\frac{10^{-6}(0.05)}{(0.10)^3}
=\boxed{4.5\times10^5\ \mathrm{N/C}}.
$$

Outside:

$$
E_{\rm out}=k_e\frac{Q}{r^2}=9.0\times10^9\frac{10^{-6}}{(0.20)^2}
=\boxed{2.25\times10^5\ \mathrm{N/C}}.
$$

Using the outside point-charge expression **inside** a uniformly charged solid sphere would be incorrect.

## Example E: Parallel-Plate Capacitance and Energy (Chapter 31)

**Problem.** Two large plates have area $0.020\ \mathrm{m^2}$ and separation $1.0\ \mathrm{mm}$ in vacuum. A $100\ \mathrm V$ source charges them. Neglect fringing.

$$
C=\frac{\varepsilon_0A}{d}=\frac{(8.85\times10^{-12})(0.020)}{0.001}
=\boxed{1.77\times10^{-10}\ \mathrm F}.
$$

$$
Q=CV=\boxed{17.7\ \mathrm{nC}},\qquad
U=\frac12CV^2=\boxed{0.885\ \mu\mathrm J}.
$$

Because the voltage is specified, $U=CV^2/2$ is the most direct energy formula.

## Example F: Series Capacitors (Chapter 31)

**Problem.** Capacitors of $6\ \mu\mathrm F$ and $3\ \mu\mathrm F$ are connected in series across $12\ \mathrm V$. Find their charges and voltages.

$$
C_{\rm eq}=\frac{6\cdot3}{6+3}\ \mu\mathrm F=2\ \mu\mathrm F,
\qquad Q=C_{\rm eq}V=\boxed{24\ \mu\mathrm C}.
$$

Each capacitor carries the same **magnitude** of charge. Thus $V_1=Q/C_1=4\ \mathrm V$ and $V_2=Q/C_2=8\ \mathrm V$. Check: $4+8=12\ \mathrm V$.

## Example G: Copper-wire Resistance and Heating (Chapter 32)

**Problem.** A $10\ \mathrm m$ wire of resistivity $1.7\times10^{-8}\ \Omega\mathrm m$ has cross-section $1.0\ \mathrm{mm^2}$. It carries steady $2.0\ \mathrm A$. Find resistance, voltage drop, and dissipated power.

$$
R=\rho\frac{L}{A}=\frac{1.7\times10^{-8}\cdot10}{10^{-6}}=\boxed{0.17\ \Omega}.
$$

$$
V=IR=\boxed{0.34\ \mathrm V},\qquad P=I^2R=4(0.17)=\boxed{0.68\ \mathrm W}.
$$

Temperature changes are neglected; resistivity will change somewhat if the wire heats.

## Example H: Real Battery with Internal Resistance (Chapter 32)

**Problem.** A battery with emf $12\ \mathrm V$ and internal resistance $1.0\ \Omega$ drives a $5.0\ \Omega$ resistor. Find current and terminal voltage.

$$
I=\frac{\mathcal E}{R+r}=\frac{12}{5+1}=\boxed{2.0\ \mathrm A}.
$$

$$
V_{\rm terminal}=\mathcal E-Ir=12-2(1)=\boxed{10\ \mathrm V}.
$$

Check the external resistance receives $IR=2\cdot5=10\ \mathrm V$. The load receives $20\ \mathrm W$ while the battery's internal resistance dissipates $4\ \mathrm W$.

## Example I: The RC Time Constant (Chapter 32)

**Problem.** Charge an initially uncharged $100\ \mu\mathrm F$ capacitor from $10\ \mathrm V$ through $10\ \mathrm{k\Omega}$. What charge is present after one time constant?

$$
\tau=RC=(10^4)(10^{-4})=\boxed{1.0\ \mathrm s}.
$$

$$
q(\tau)=C\mathcal E(1-e^{-1})=(10^{-4})(10)(0.6321)
=\boxed{0.632\ \mathrm{mC}}.
$$

The final charge is $1.00\ \mathrm{mC}$. One time constant is **not** the time to full charge.

## Example J: Wheatstone Balance (Chapter 32)

**Problem.** In an ideal Wheatstone arrangement, one branch has $P=100\ \Omega$ and $Q=200\ \Omega$, while the other contains $R=150\ \Omega$ and unknown $S$. Determine $S$ for zero galvanometer current.

$$
\frac{P}{Q}=\frac{R}{S}\quad\Longrightarrow\quad
S=\frac{QR}{P}=\frac{200\cdot150}{100}=\boxed{300\ \Omega}.
$$

The unknown is determined by a **ratio of resistances**, without needing the supply voltage or galvanometer resistance at exact balance.

## Example K: Joule Heating in a Resistor (Chapter 33)

**Problem.** Current $2.0\ \mathrm A$ flows through a fixed $5.0\ \Omega$ resistor for $60\ \mathrm s$. Find the electrical energy turned into heat.

$$
H=I^2Rt=(2)^2(5)(60)=\boxed{1.20\times10^3\ \mathrm J}.
$$

The resistor's temperature rise cannot be determined until its heat capacity and heat-loss environment are known.

## Example L: Silver Deposition (Chapter 33)

**Problem.** A $0.50\ \mathrm A$ current passes for $20\ \mathrm{min}$ through an electrolytic bath depositing silver with $M=107.9\ \mathrm{g/mol}$ and $z=1$. Assume $100\%$ current efficiency.

$$
Q=It=(0.50)(20\cdot60)=600\ \mathrm C.
$$

$$
m=\frac{MQ}{zF}=\frac{107.9(600)}{96485}\ \mathrm g
\simeq\boxed{0.671\ \mathrm g}.
$$

This is a **Faraday-charge** calculation; the electrolyte resistance is not needed if current and time are already specified.

## Example M: Proton Orbit in a Magnetic Field (Chapter 34)

**Problem.** A proton ($m=1.67\times10^{-27}\ \mathrm{kg}$, $q=1.60\times10^{-19}\ \mathrm C$) enters a uniform $0.50\ \mathrm T$ field at $10^6\ \mathrm{m/s}$, perpendicular to the field. Find radius and period.

$$
r=\frac{mv}{qB}=\frac{1.67\times10^{-27}(10^6)}{(1.60\times10^{-19})(0.50)}
\simeq\boxed{2.09\ \mathrm{cm}}.
$$

$$
T=\frac{2\pi m}{qB}\simeq\boxed{1.31\times10^{-7}\ \mathrm s}.
$$

The period is independent of speed in the **nonrelativistic ideal model**, whereas radius increases with speed.

## Example N: Magnetic Force on a Straight Wire (Chapter 34)

**Problem.** A $0.40\ \mathrm m$ wire carries $3.0\ \mathrm A$ at $90^\circ$ to uniform $B=0.20\ \mathrm T$. Find force magnitude.

$$
F=ILB\sin90^\circ=(3.0)(0.40)(0.20)=\boxed{0.24\ \mathrm N}.
$$

Direction is obtained from current-vector cross field-vector, not from the scalar multiplication.

## Example O: Circular-coil Field (Chapter 35)

**Problem.** A coil with $20$ closely spaced turns has radius $0.10\ \mathrm m$ and carries $0.50\ \mathrm A$. Find the field at its center.

$$
B=\frac{\mu_0NI}{2R}=\frac{(4\pi\times10^{-7})(20)(0.50)}{2(0.10)}
\simeq\boxed{6.28\times10^{-5}\ \mathrm T}.
$$

All turn contributions add along the same axial direction for a tightly wound coil.

## Example P: Long-solenoid Field (Chapter 35)

**Problem.** A long air-core solenoid has $N=1000$ turns over $0.50\ \mathrm m$, carrying $1.0\ \mathrm A$. Neglect end effects.

$$
n=\frac{N}{L}=2000\ \mathrm{turns/m},\qquad
B\simeq\mu_0nI=(4\pi\times10^{-7})(2000)(1)
\simeq\boxed{2.51\ \mathrm{mT}}.
$$

A dense magnetic core would change the magnitude and require a material constitutive model.

## Example Q: Tangent Galvanometer (Chapter 36)

**Problem.** A tangent galvanometer has $N=10$ turns, radius $R=0.10\ \mathrm m$, and is located where $B_H=40\ \mu\mathrm T$. What current produces $45^\circ$ deflection?

$$
I=\frac{2RB_H}{\mu_0N}\tan45^\circ
=\frac{2(0.10)(40\times10^{-6})}{(4\pi\times10^{-7})(10)}
\simeq\boxed{0.637\ \mathrm A}.
$$

At $45^\circ$ the coil field equals the horizontal geomagnetic field in magnitude.

## Example R: Oscillating Bar Magnet (Chapter 36)

**Problem.** A small suspended magnet has rotational inertia $2.0\times10^{-6}\ \mathrm{kg\,m^2}$, dipole moment $0.20\ \mathrm{A\,m^2}$, and Earth-field horizontal component $50\ \mu\mathrm T$. Find the small-angle period.

$$
T=2\pi\sqrt{\frac{I_{\rm rot}}{MB_H}}
=2\pi\sqrt{\frac{2.0\times10^{-6}}{0.20(50\times10^{-6})}}
\simeq\boxed{2.81\ \mathrm s}.
$$

A larger angular excursion lengthens the period slightly compared with the linear small-angle prediction.

## Example S: Magnetic Susceptibility (Chapter 37)

**Problem.** A linear material has $\chi_m=0.002$ in an applied field $H=1000\ \mathrm{A/m}$. Find magnetization, relative permeability, and magnetic field magnitude inside the material assuming the stated homogeneous local $H$.

$$
M=\chi_mH=\boxed{2.0\ \mathrm{A/m}},\qquad\mu_r=1+\chi_m=\boxed{1.002}.
$$

$$
B=\mu_0\mu_rH=(4\pi\times10^{-7})(1.002)(1000)
\simeq\boxed{1.259\ \mathrm{mT}}.
$$

One must distinguish a specified **internal $H$** from an externally imposed field when sample demagnetization is important.

## Example T: Hysteresis Energy per Cycle (Chapter 37)

**Problem.** A measured $B$–$H$ loop encloses a dissipated-energy area of $500\ \mathrm{J/m^3}$ per cycle. A core volume is $2.0\times10^{-4}\ \mathrm{m^3}$ and experiences $50$ complete cycles per second. Estimate hysteresis power loss.

$$
E_{\rm cycle}=500(2.0\times10^{-4})=0.10\ \mathrm J,
\qquad P=50(0.10)=\boxed{5.0\ \mathrm W}.
$$

This is only hysteresis loss. Winding resistance and eddy currents create additional losses.

## Example U: Moving Rod and Magnetic Braking (Chapter 38)

**Problem.** A rod of length $0.30\ \mathrm m$ moves at $5.0\ \mathrm{m/s}$ across $B=0.40\ \mathrm T$ while completing a circuit of total resistance $3.0\ \Omega$. All directions are mutually perpendicular. Find emf, current, magnetic force magnitude, and input mechanical power at steady speed.

$$
\mathcal E=B\ell v=(0.40)(0.30)(5.0)=\boxed{0.60\ \mathrm V}.
$$

$$
I=\mathcal E/R=\boxed{0.20\ \mathrm A},\qquad
F=BI\ell=(0.40)(0.20)(0.30)=\boxed{0.024\ \mathrm N}.
$$

The external mechanical force maintains the speed against the magnetic reaction. Check the power balance:

$$
Fv=0.024(5.0)=0.12\ \mathrm W=I^2R=(0.20)^2(3.0).
$$

## Example V: RL Current Growth (Chapter 38)

**Problem.** A $0.50\ \mathrm H$ inductor and $10\ \Omega$ resistor are in series with a $20\ \mathrm V$ DC source. Find the time constant, current after one time constant, and eventual stored magnetic energy.

$$
\tau=\frac LR=\frac{0.50}{10}=\boxed{0.050\ \mathrm s}.
$$

$$
I(\tau)=\frac{20}{10}(1-e^{-1})=\boxed{1.26\ \mathrm A}.
$$

At steady state $I_\infty=2.0\ \mathrm A$, so

$$
U_{L,\infty}=\frac12LI_\infty^2=\frac12(0.50)(2.0)^2=\boxed{1.0\ \mathrm J}.
$$

## Example W: Impedance and Real Power (Chapter 39)

**Problem.** A series AC circuit has $R=30\ \Omega$, $X_L=40\ \Omega$, and negligible capacitance, with $V_{\rm rms}=100\ \mathrm V$. Determine impedance magnitude, RMS current, power factor, and real power.

$$
|Z|=\sqrt{30^2+40^2}=\boxed{50\ \Omega},\qquad
I=\frac{100}{50}=\boxed{2.0\ \mathrm A}.
$$

$$
\cos\phi=\frac{R}{|Z|}=\boxed{0.60\ \text{(lagging)}},\qquad
P=I^2R=4(30)=\boxed{120\ \mathrm W}.
$$

Apparent power is $VI=200\ \mathrm{VA}$, not $200\ \mathrm W$.

## Example X: Resonance Frequency (Chapter 39)

**Problem.** Find resonance frequency for an ideal series circuit with $L=0.10\ \mathrm H$ and $C=100\ \mu\mathrm F$.

$$
\omega_0=\frac1{\sqrt{LC}}=\frac1{\sqrt{0.10(100\times10^{-6})}}
\simeq\boxed{316\ \mathrm{rad/s}}.
$$

$$
f_0=\frac{\omega_0}{2\pi}\simeq\boxed{50.3\ \mathrm{Hz}}.
$$

Series resistance controls the peak current and resonance sharpness, but does not appear in the ideal reactance-cancellation condition.

## Example Y: Ideal Transformer (Chapter 39)

**Problem.** An ideal transformer converts $240\ \mathrm{V_{rms}}$ to $12\ \mathrm{V_{rms}}$ and supplies $4.0\ \mathrm{A_{rms}}$ to a load. Determine turns ratio and primary current.

$$
\frac{N_s}{N_p}=\frac{V_s}{V_p}=\frac{12}{240}=\boxed{\frac1{20}}.
$$

$$
P_{\rm out}=V_sI_s=12(4)=48\ \mathrm W,
\qquad I_p=\frac{48}{240}=\boxed{0.20\ \mathrm A}.
$$

These are idealized power quantities assuming a resistive load or unity power factor; for a reactive load use appropriate **real or complex power** conservation, including phase.

## Example Z: Intensity of a Plane EM Wave (Chapter 40)

**Problem.** A vacuum sinusoidal plane wave has peak electric field $E_0=100\ \mathrm{V/m}$. Find peak magnetic field and mean intensity.

$$
B_0=\frac{E_0}{c}\simeq\frac{100}{3.00\times10^8}
=\boxed{3.33\times10^{-7}\ \mathrm T}.
$$

$$
I=\frac12\varepsilon_0cE_0^2
\simeq\frac12(8.85\times10^{-12})(3.00\times10^8)(100)^2
=\boxed{13.3\ \mathrm{W/m^2}}.
$$

The intensity would be **twice** this value if peak field were incorrectly substituted into an RMS-field formula without the proper factor.

---

# Common Misconceptions and Diagnostic Questions

1. **“Positive potential means a positive force.”** False. Force depends on $\vec E=-\nabla V$ and the sign of the test charge. A large positive constant potential contributes no electric field.
2. **“A negative potential is physically impossible.”** False. Potential depends on the chosen reference, and potential energy depends on test-charge sign.
3. **“A charge feels force along the electric field regardless of sign.”** Negative charge experiences $\vec F=q\vec E$ antiparallel to $\vec E$.
4. **“Zero Gaussian flux means zero field at every point.”** False. A uniform field through a closed cube has zero net flux even though its field is nonzero.
5. **“Gauss's law works only for symmetric objects.”** The law is universal; symmetry makes field extraction easy.
6. **“A charged conducting object must have a field inside.”** In electrostatic equilibrium, bulk conductor field vanishes; steady current is a different regime.
7. **“Grounding makes a conductor electrically neutral.”** Grounding sets a potential boundary condition and can leave induced net charge.
8. **“A capacitor's charge is the sum of the magnitudes on both plates.”** Standard $Q$ denotes the magnitude on **one** of the two oppositely charged plates.
9. **“A dielectric always reduces capacitor energy.”** It reduces stored energy for fixed charge but raises capacitor energy for fixed voltage; the battery exchanges energy.
10. **“The force on a capacitor plate comes from its own field.”** Use the field of the *other* plate to compute the mechanical force on one plate.
11. **“Current in a wire means electrons travel at the speed of light.”** Individual drift speed is commonly slow; fields and electrical signals propagate much faster.
12. **“Ohm's law applies to every two-terminal electrical device.”** Constant $R$ characterizes a restricted class of conductor behavior.
13. **“An emf is a mechanical force.”** Emf is energy supplied per unit charge, measured in volts.
14. **“The voltage across a battery is always its emf.”** Internal resistance and chemical polarization can shift terminal voltage under load.
15. **“Kirchhoff's loop rule always means $\oint\vec E\cdot d\vec l=0$.”** Time-varying magnetic flux can create nonconservative electric circulation.
16. **“A potentiometer must draw current from the source under test.”** At an ideal null balance, the test-source branch current vanishes.
17. **“Joule heating always means a temperature rise.”** Some energy may escape to surroundings or change phase; temperature needs a thermal model.
18. **“All thermoelectric heating is $I^2R$.”** Peltier and Thomson reversible terms can be **linear** in current and change sign on current reversal.
19. **“Magnetic forces accelerate particles along their velocity.”** Magnetic Lorentz force is perpendicular to instantaneous velocity and does no work.
20. **“A uniform magnetic field produces net force on any closed current loop.”** A closed loop has zero net force in uniform $\vec B$ but may have torque.
21. **“Magnetic field lines start at north and end at south.”** In physical $\vec B$, lines form continuous closed loops; isolated north/south poles are not ordinary measured sources.
22. **“Ampère's law gives $B=\mu_0I/(2\pi r)$ for every wire.”** That expression requires the long-straight-wire symmetry.
23. **“Magnetic moment and magnetization are the same quantity.”** Dipole moment has units $\mathrm{A\,m^2}$; magnetization has units $\mathrm{A/m}$.
24. **“Every ferromagnet has a fixed relative permeability.”** Ferromagnets can be nonlinear, saturating, and hysteretic.
25. **“The induced current opposes the magnetic field.”** Lenz's law says it opposes the *change in flux*, not necessarily the field itself.
26. **“A magnetic field is needed to do work on a moving rod's charges.”** The rod's motion under an external mechanical force supplies the power in a simple motional-emf generator; the magnetic force on a free charge remains perpendicular to its velocity.
27. **“An ideal inductor blocks any current.”** It opposes *change* in current; at steady DC it behaves as a short circuit in the ideal circuit model.
28. **“A pure inductor permanently consumes $VI$ watts of average power.”** Ideal inductors have nonzero instantaneous power but zero cycle-average **active** power.
29. **“An AC current of $10\ \mathrm A$ peak is $10\ \mathrm A$ RMS.”** Sinusoidal RMS current is peak divided by $\sqrt2$.
30. **“The resistor, capacitor, and inductor voltages in series add as ordinary scalar magnitudes.”** AC voltages have phase, so they add as phasors.
31. **“At series resonance all component voltages vanish.”** Reactive voltage drops can be individually large and opposite while net reactance is zero.
32. **“A step-up transformer produces more energy than supplied.”** Ideal voltage gain is balanced by inverse current gain.
33. **“Displacement current is charge flowing through an ideal vacuum capacitor gap.”** It represents a time-varying electric-flux term, not conduction across the gap.
34. **“The electric and magnetic energy densities in a vacuum plane wave oscillate out of phase.”** They are equal **at each point and time** for the traveling wave solution given here.
35. **“Radiation has energy but no momentum.”** Electromagnetic waves transport momentum and exert radiation pressure.
36. **“All electromagnetic radiation passes through the atmosphere equally.”** Atmospheric absorption and scattering depend strongly on wavelength and composition.

**Universal problem-solving protocol**

```text
1. Draw geometry, mark field/current/loop-normal directions.
2. Identify the regime: electrostatic, steady current, magnetostatic, time-varying.
3. Choose control object, Gaussian surface, Amperian loop, or circuit boundary.
4. State idealizations (point source, infinite wire, linear dielectric, ideal battery, ...).
5. Select the correct governing law and sign convention.
6. Derive symbolically, then substitute SI values.
7. Check units, limiting behavior, physical direction, and conservation of energy.
8. If the answer seems wrong, inspect the *assumptions* before adding new formulas.
```

---

# Active-Recall Checkpoints

**Method:** Attempt each question without looking at the notes. Write the governing principle and at least one sentence justifying it before quoting a formula. For calculation prompts, draw the geometry and mark orientation conventions.

### Chapter 29: Electric Field and Potential

1. Distinguish charge conservation from quantization. Is charge continuously divisible in a macroscopic approximation?
2. Derive the vector force on one point charge due to another and explain how charge signs affect direction.
3. What is the operational definition of electric field, and why must the test charge be small?
4. Explain superposition for $\vec E$ and contrast it with scalar superposition for $V$.
5. State three rules for electrostatic field-line diagrams; why can't two lines cross?
6. Starting from work done by a conservative force, derive $\Delta U=-q\int\vec E\cdot d\vec l$.
7. Show why the potential of a point charge varies as $1/r$ rather than $1/r^2$.
8. Explain physically what $\vec E=-\nabla V$ says about the direction of electric force on positive charge.
9. Can potential vanish where electric field does not? Construct an example.
10. Derive the far-field axial and equatorial scaling of an electric dipole and explain the $r^{-3}$ behavior.
11. Explain why a dipole can rotate but not translate in a perfectly uniform field.
12. Distinguish electrostatic equilibrium inside a conductor from the state of a conductor carrying steady DC.

### Chapter 30: Gauss's Law

13. Define oriented electric flux and explain why it can be positive, negative, or zero.
14. Derive the solid angle subtended by a tilted differential area element.
15. Starting from Coulomb's law, derive net flux through a sphere surrounding a point charge.
16. Why do external charges contribute zero *net* flux to a closed Gaussian surface without contributing zero field?
17. Describe the geometric conditions required to pull $E$ outside a Gaussian flux integral.
18. Derive the field of an infinite charged line using a cylindrical Gaussian surface.
19. Derive the field of an infinite nonconducting sheet using a pillbox.
20. Explain the factor-of-two difference between an infinite charged sheet and the field immediately outside a conductor.
21. Derive the electric field inside a uniformly charged **nonconducting** solid sphere.
22. Compare the fields inside a thin charged spherical shell and a uniformly charged solid sphere.
23. Explain why potential remains continuous across a charged spherical shell while the normal field can jump.
24. Explain grounding as a boundary condition and give an example where a grounded conductor is not neutral.

### Chapter 31: Capacitors

25. Define capacitance and justify why it depends on geometry and medium in a linear ideal device.
26. Derive the parallel-plate formula from Gauss's law and a potential integral.
27. Derive the capacitance of an isolated charged conducting sphere.
28. Obtain the capacitance of concentric conducting spheres by integrating the radial electric field.
29. Explain equal charges in series capacitors from charge conservation at an isolated intermediate electrode.
30. Why do parallel capacitors have equal voltage but generally unequal charges?
31. Derive $U_C=Q^2/(2C)$ by integrating incremental charging work.
32. Find the vacuum energy density in a parallel-plate capacitor using its field energy and volume.
33. Why should a plate's force be calculated using the *other* plate's field?
34. Compare the results of inserting a dielectric when a capacitor is isolated versus battery-connected.
35. Distinguish free and bound charge in the two versions of Gauss's law.
36. Explain corona discharge and why rounded electrodes reduce field concentration.

### Chapter 32: Electric Current in Conductors

37. Define current as a signed rate of charge transport and relate it to current-density flux.
38. Explain why electron drift opposes conventional current in a metal.
39. Derive $I=n|q|Av_d$ for one species of carriers.
40. Distinguish microscopic conductivity from a wire's geometrical resistance.
41. List three reasons a current–voltage relation might be non-ohmic.
42. Derive the terminal-voltage expression for a discharging cell with internal resistance.
43. Explain the power balance for a source driving two resistors in series.
44. Set up two Kirchhoff loop equations with an arbitrary assumed current direction and interpret a negative solution.
45. Derive resistance-equivalent relations for series and parallel networks.
46. Derive the Wheatstone bridge balance condition using equal midpoint potentials.
47. Explain why an ideal voltmeter has very large resistance and an ideal ammeter very small resistance.
48. Solve the $RC$ charging differential equation and interpret the time constant.

### Chapter 33: Thermal and Chemical Effects of Electric Current

49. Derive the Joule heating relation from the electrical power transferred to a resistor.
50. What experimental conditions must be controlled to verify $H\propto I^2$ independently?
51. Explain the thermocouple Seebeck effect and why a reference-junction temperature is required.
52. Distinguish Peltier junction heating from Joule resistive heating under current reversal.
53. What additional physical ingredient is needed for Thomson heating inside a homogeneous conductor?
54. Explain the energy-transport interpretation linking thermoelectric effects.
55. Distinguish electron conduction in a metal from ionic conduction in an electrolyte.
56. How are cathode and anode defined in terms of electrode reactions?
57. Starting from one entity requiring $z$ electrons, derive Faraday's deposition law.
58. Explain how a coulombmeter measures integrated charge from deposited mass.
59. Compare primary and secondary cells using charge/discharge reaction capability.
60. State the gross chemical changes in a lead–acid cell during discharge.

### Chapter 34: Magnetic Field

61. State the Lorentz force and give two velocity configurations producing zero magnetic force.
62. Explain why a magnetic field can change direction of motion but not speed for a free particle.
63. Derive cyclotron radius, angular frequency, and period from the centripetal-force relation.
64. Explain why a velocity component parallel to a uniform field produces helical motion.
65. Derive the helical pitch and describe how it changes if $v_\parallel$ doubles.
66. Describe a crossed-field velocity selector and derive its ideal pass-through speed.
67. From carrier forces, motivate $d\vec F=I\,d\vec l\times\vec B$.
68. Identify the conditions under which $F=ILB\sin\theta$ can be used without an integral.
69. Derive magnetic dipole moment for a rectangular current loop and state the normal-direction rule.
70. Why can the net force on a closed loop be zero while torque is nonzero?
71. Explain the stable and unstable orientations of a loop magnetic moment in uniform $\vec B$.
72. How are electric and magnetic fields related conceptually through frame changes?

### Chapter 35: Magnetic Field due to a Current

73. State Biot–Savart's law with the correct cross-product direction.
74. Why must contributions of curved current elements be integrated as vectors?
75. Derive the field of an infinitely long straight wire by a Biot–Savart integral.
76. State the magnetic field direction around a straight wire using the right-hand rule.
77. Explain attraction of parallel currents in the same direction from field and wire-force rules.
78. Derive the field at the center of a circular current loop.
79. Explain why transverse Biot–Savart contributions cancel along the symmetry axis of a loop.
80. Derive Ampère's law result for a long straight wire using a circular integration path.
81. Why is Ampère's law not automatically a shortcut for a finite bent wire?
82. Derive the long-solenoid interior field by a rectangular Amperian loop.
83. Explain why an ideal toroid has negligible exterior field and varying interior $B(r)$.
84. Compare the distance dependence of the wire's field with the far field of a compact current loop.

### Chapter 36: Permanent Magnets

85. Distinguish the classical pole model from a physical magnetic monopole.
86. Derive a magnetic dipole's far-field axial and equatorial amplitudes and compare their ratio.
87. Write the torque and potential-energy expressions for a magnetic bar in a uniform field.
88. Explain why magnetic scalar potential is restricted to suitable current-free regions.
89. Distinguish magnetic declination from inclination.
90. Resolve the terrestrial magnetic field into horizontal and vertical components.
91. Explain how a dip circle can overestimate true dip if its vertical plane is misaligned.
92. Define a neutral point and explain the required vector cancellation condition.
93. Derive the tangent galvanometer equation from two perpendicular fields.
94. Explain the purpose of a radial field in a moving-coil galvanometer.
95. Derive the galvanometer shunt formula by matching parallel voltages.
96. Explain why oscillation and deflection measurements together can determine both $M$ and $B_H$.

### Chapter 37: Magnetic Properties of Matter

97. Give the SI unit and definition of magnetization; contrast it with total dipole moment.
98. Explain the physical origins of dia-, para-, and ferromagnetic responses at an introductory level.
99. Derive $\vec B=\mu_0(\vec H+\vec M)$ and interpret the separate terms.
100. Define magnetic susceptibility and identify which response classes commonly have positive or negative values.
101. Derive $\mu_r=1+\chi_m$ in a linear isotropic medium.
102. Why is an externally applied $H$ not always identical to the local internal $H$ of a shaped specimen?
103. What assumptions support Curie's inverse-temperature law?
104. What happens to ordinary ferromagnetic order above its Curie temperature?
105. Explain domains, saturation, remanence, and coercivity on a qualitative hysteresis loop.
106. Why is the area of a hysteresis loop associated with dissipated energy per cycle?
107. Contrast magnetically soft and hard materials using intended applications.
108. Give two reasons a ferromagnetic core's behavior cannot always be represented by one constant permeability.

### Chapter 38: Electromagnetic Induction

109. Define oriented magnetic flux and explain three ways it can change with time.
110. State Faraday's law and give the sign convention used for induced emf.
111. Apply Lenz's law when an external flux **increases** into the page; then repeat for a **decreasing** flux.
112. Derive motional emf for a rod crossing uniform magnetic field lines.
113. Distinguish motional emf from the circulating electric field created by time-dependent $B$.
114. Explain magnetic braking in terms of induced currents and energy conservation.
115. Why do thin insulated laminations reduce eddy-current loss?
116. Derive inductance of a long solenoid and identify its geometrical dependencies.
117. Derive $I(t)$ for an initially unenergized series $RL$ circuit after voltage is applied.
118. Can ideal-inductor current jump instantaneously? Explain using $V=L\,dI/dt$.
119. Derive $U_L=LI^2/2$ and compare with $U_C=CV^2/2$.
120. Distinguish self-inductance from mutual inductance and explain why winding coupling is generally less than unity.

### Chapter 39: Alternating Current

121. Define peak, RMS, frequency, phase, and period for a sinusoidal waveform.
122. Derive the time-varying emf from uniform-rotation coil flux.
123. Show by integration that a sinusoid has zero mean but nonzero RMS current.
124. Explain current–voltage phase in a pure resistor, pure inductor, and pure capacitor.
125. Derive $X_L=\omega L$ and $X_C=1/(\omega C)$ from time-domain circuit relations.
126. Construct a phasor diagram for a series $RLC$ circuit and derive its impedance magnitude.
127. Distinguish a net inductive circuit from a net capacitive circuit using phase angle sign.
128. Derive ideal series-resonance frequency and describe how resistance affects the current peak.
129. Prove the average-power relation $P=VI\cos\phi$ for sinusoidal voltage and current.
130. Distinguish real power, apparent power, and power factor with an example.
131. Compare slip rings and a commutator in elementary AC-generator and DC-dynamo models.
132. Derive ideal transformer voltage and current ratios and explain why steady DC is unsuitable for an ordinary transformer.

### Chapter 40: Electromagnetic Waves

133. Explain the apparent paradox of Ampère's magnetostatic law applied to two spanning surfaces of a charging capacitor.
134. Derive the displacement-current term for a vacuum parallel-plate capacitor.
135. Show how the Ampère–Maxwell equation is consistent with charge continuity.
136. State all four Maxwell equations and identify the physical content of each.
137. Derive the vacuum wave equation for $\vec E$ from Maxwell's curl equations.
138. Derive the vacuum propagation speed $c=1/\sqrt{\mu_0\varepsilon_0}$.
139. State the mutual directions and phase relation of $\vec E$, $\vec B$, and propagation in a plane wave.
140. Prove that electric and magnetic contributions to energy density are equal for a vacuum plane wave.
141. Define the Poynting vector and derive average sinusoidal intensity from peak electric field.
142. Explain why perfect reflection transfers twice the normal momentum per incident unit energy compared with complete absorption.
143. Convert between wavelength and frequency and identify the broad electromagnetic spectral ordering.
144. Why do atmospheric windows depend strongly on radiation frequency and atmospheric composition?

---

## Source and scope

**Primary reference:** H. C. Verma, *Concepts of Physics*, Volume 2, Chapters **29–40** (textbook pp. **104–340**):

- Chapter 29: *Electric Field and Potential*, §§29.1–29.13.
- Chapter 30: *Gauss's Law*, §§30.1–30.6.
- Chapter 31: *Capacitors*, §§31.1–31.12.
- Chapter 32: *Electric Current in Conductors*, §§32.1–32.14.
- Chapter 33: *Thermal and Chemical Effects of Electric Current*, §§33.1–33.12.
- Chapter 34: *Magnetic Field*, §§34.1–34.6.
- Chapter 35: *Magnetic Field due to a Current*, §§35.1–35.8.
- Chapter 36: *Permanent Magnets*, §§36.1–36.15.
- Chapter 37: *Magnetic Properties of Matter*, §§37.1–37.9.
- Chapter 38: *Electromagnetic Induction*, §§38.1–38.9.
- Chapter 39: *Alternating Current*, §§39.1–39.12, with corrected numbering compared to typographical errors in the volume's table of contents.
- Chapter 40: *Electromagnetic Waves*, §§40.1–40.7.

The document follows all **123 numbered theory sections** across these 12 chapters and gives an original synthesis rather than verbatim reproduction. The **26 integrated examples** and **144 active-recall questions** are independently constructed. Some explanatory connections go beyond HCV's introductory development and are identified as additional models or refinements, notably the Drude relaxation-time picture, Kelvin thermoelectric relations, material constitutive caveats, impedance quality factor, complex-power language, and general energy/field formulations. For figures of experimental instruments, refer to the book's original diagrams alongside these notes.

**Study method:** Derive formulas from source configurations and boundary conditions, not merely from remembered shapes. Always distinguish a local field from an integrated flux, a charge distribution from its potential, a terminal voltage from emf, and instantaneous wave power from its cycle average. Re-solve the textbook's worked-out examples and numerical exercises separately, then use the unit's original problems and recall prompts for consolidation.
