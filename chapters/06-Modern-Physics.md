# Unit 06: Modern Physics

**Electric Current through Gases → Photoelectric Effect and Matter Waves → Atomic Physics → X-rays → Semiconductors → Nuclear Physics → Special Relativity**  
*Original revision notes following Chapters 41–47 of H. C. Verma, Concepts of Physics, Volume 2*

> **Purpose.** Connect the experimental discoveries that revealed the electron and atomic structure to quantum descriptions of light and matter, radiation, solid-state electronics, nuclear energy, and relativistic mechanics. Numbered theory sections follow HCV; explanations, derivations, applications, examples, and questions are independently written. Consult the book's figures for apparatus layouts, spectra, circuit diagrams, and energy-level sketches.
>
> **Scope and source fidelity.** This is a theory-focused revision companion, not a reproduction of the textbook or a collection of its exercise solutions. Historical devices (vacuum valves, classical gas-discharge tubes) are included because HCV teaches them. Clearly marked **Extension** passages provide modern clarification or a short bridge to engineering; do not confuse them with material required by the book.
>
> **Notation.** SI units unless otherwise stated. $e=1.602176634\times10^{-19}\,\mathrm C$ is the *positive magnitude* of the electron charge, so the electron has charge $-e$; $h$ is Planck's constant, $\hbar=h/(2\pi)$, $c$ the vacuum speed of light, $\varepsilon_0$ vacuum permittivity, $k_B$ Boltzmann's constant, and $N_A$ Avogadro's constant. Use $m_e$ for electron mass, $m_0$ for rest mass, $\nu$ for frequency, $\lambda$ for wavelength, $\phi$ for work function, $\gamma$ for the Lorentz factor, and $T_{1/2}$ for half-life. Context distinguishes $V$ as voltage from $V$ as volume. Every displayed equation is delimited by `$$ ... $$` (GitHub display math).

## Roadmap

| Part | HCV chapter | Central questions |
|---|---|---|
| **I** | **41. Electric Current through Gases** | How do gases conduct? How were cathode rays, the electron, and thermionic devices understood? |
| **II** | **42. Photoelectric Effect and Wave–Particle Duality** | Why does light arrive in energy quanta? Why does matter have a wavelength? |
| **III** | **43. Bohr's Model and Physics of the Atom** | Why are atomic spectra discrete? What replaces classical electron orbits? |
| **IV** | **44. X-rays** | How are X-rays produced, characterized, and diffracted? |
| **V** | **45. Semiconductors and Semiconductor Devices** | How do energy bands, junctions, transistors, and logic gates work? |
| **VI** | **46. The Nucleus** | What binds nuclei, governs decay, and supplies fission/fusion energy? |
| **VII** | **47. The Special Theory of Relativity** | How can inertial observers agree on physics yet disagree on space and time? |

**Conceptual dependency map**

```text
Gases and charge transport
          |
          v
Cathode rays -> electron -> charge-to-mass measurements
          |
          +-----------------------------+
          |                             |
          v                             v
Thermionic emission              Light as photons
and vacuum devices                      |
                                        v
                            Photoelectric thresholds
                                        |
                                        v
                              de Broglie matter waves
                                        |
                                        v
                         Atomic spectra and energy states
                                        |
                         +--------------+----------------+
                         v                               v
                  X-ray production                 Energy bands
                  and diffraction                  and electronics
                         |
                         v
             Nuclear structure and decay
                         |
                         v
                  Fission and fusion

Maxwell's electromagnetic waves + relativity principle
                         |
                         v
              Special relativity -> E^2=p^2c^2+m_0^2c^4
                         |
                         +----> photon momentum, mass-energy,
                                atomic/nuclear applications
```

---

# Part I: Electric Current through Gases

The metal-wire model of conduction assumes mobile electrons already exist in large numbers. A neutral gas behaves differently: charge carriers must usually be created by ionization, collisions, radiation, or electron emission from a heated surface. Historically, controlling these phenomena led to the discovery of the electron and to vacuum electronic devices.

## 41.1 Discharge through Gases at Low Pressure

A gas normally has a small density of free carriers because most molecules are neutral and electrons and positive ions recombine. An electric field accelerates any carriers present. Energetic particles may ionize neutral molecules, generating further electrons and ions; in a suitable field, an **ionization avalanche** sustains conduction.

In a discharge tube, the negative electrode is the **cathode** and the positive electrode the **anode**. A high potential difference across a dilute gas produces luminous structures whose appearance changes as pressure decreases: a positive column, cathode or negative glow, Faraday dark space, Crookes dark space, and, under suitable conditions, striations. These are regions of different excitation, ionization, and electric-field structure, *not* a series of different substances.

**Sparking potential** is the minimum electrode potential difference needed for a spark under the specified conditions. HCV introduces **Paschen's law** in the form

$$
\boxed{V_{\mathrm{spark}}=f(pd),}
$$

where $p$ is gas pressure and $d$ is electrode separation for a given gas/electrode arrangement. This says the breakdown voltage depends on the pressure–distance product under the conditions of the law; it **does not** claim that voltage is simply proportional to $pd$. Collision frequency, ionization, and electrode secondary emission determine the shape of the Paschen curve.

**Physical picture:** energetic positive ions striking the cathode can release secondary electrons. The field accelerates these electrons, which excite and ionize gas molecules. Excited species emit light on returning to lower energy states. Extremely low pressure ultimately reduces ordinary collision-driven glow because too few gas molecules remain.

**Figure companion:** HCV's discharge-tube illustrations in §41.1 distinguish the positive column, two dark spaces, negative glow, and striations. Label where charge-carrier production is strongest before memorizing names.

## 41.2 Cathode Rays

When the residual gas pressure becomes very small, streams from the cathode travel approximately in straight lines, produce fluorescence on suitable surfaces, cast shadows, and carry energy and momentum. These streams are **cathode rays**, now understood as beams of electrons.

The evidence for a negatively charged particle beam includes:

- Deflection toward the positive plate in a transverse electric field.
- Magnetic deflection consistent with the Lorentz force on negative charges.
- Production of heating and mechanical effects when the beam strikes matter.
- Similar charge-to-mass behavior across different cathode materials and gases.

The trajectory is governed by

$$
\boxed{\vec F=q\left(\vec E+\vec v\times\vec B\right),\qquad q=-e.}
$$

For an electron accelerated from rest through a potential drop $V_a$, provided the speed is nonrelativistic,

$$
\boxed{\frac12m_ev^2=eV_a,\qquad v=\sqrt{\frac{2eV_a}{m_e}}.}
$$

This beam model explains why a small electron mass permits strong magnetic deflection. If $v$ becomes a substantial fraction of $c$, use relativistic kinetic energy instead.

## 41.3 Canal Rays or Positive Rays

A perforated cathode in a discharge tube permits positively charged ions moving toward it to pass through holes and continue behind it. These **canal rays** or **positive rays** travel oppositely to the cathode-ray electrons. They are not universally streams of protons: their masses and charge states depend on which gas and ions are present.

For an ion of mass $M$, charge $Q>0$, and kinetic energy gained across potential $V_a$,

$$
\frac12Mv^2\simeq QV_a,
$$

within the nonrelativistic approximation. Ions generally accelerate more slowly than electrons under the same potential because $M\gg m_e$. Deflection experiments separate particles according to mass-to-charge ratio. The qualitative contrast is essential: **cathode rays are the same fundamental electron in many discharge conditions, whereas positive rays reveal properties of the gas ions**.

## 41.4 Discovery and Properties of Electron

Experiments identified a negative particle smaller than an atom and established its charge-to-mass ratio. Two measurements play complementary roles:

**Thomson-type $e/m$ determination.** In crossed electric and magnetic fields adjusted so that a beam passes undeflected, opposite transverse forces balance:

$$
eE=evB\quad\Longrightarrow\quad \boxed{v=\frac EB},
$$

assuming the beam velocity is perpendicular to both fields and the selected directions give opposing forces. If the same beam subsequently moves in a *magnetic-only* region on a circle of radius $r$,

$$
\frac{m_ev^2}{r}=evB
\quad\Longrightarrow\quad
\boxed{\frac e{m_e}=\frac v{Br}=\frac E{B^2r}}.
$$

Be careful: $e/m_e$ is the **magnitude**; the electron's signed $q/m$ is negative.

**Measurement of elementary charge.** Millikan's oil-drop method balances electrical, gravitational, and buoyant forces on tiny charged droplets. After accounting for effective weight and drag, measured charges are consistent with integer multiples of a smallest value:

$$
\boxed{|q|=ne,\qquad n=1,2,3,\ldots}
$$

Knowing $e$ and $e/m_e$ determines

$$
\boxed{m_e=\frac{e}{e/m_e}\simeq9.109\times10^{-31}\ \mathrm{kg}.}
$$

**Key properties:** electrons carry negative electric charge, possess inertia and spin, and participate in electrical conduction, atomic structure, and electromagnetic interactions. Classical $e/m$ measurements describe translational dynamics; electron spin requires quantum theory.

## 41.5 Thermionic Emission

A metal contains mobile electrons, but an electron must overcome a surface-energy barrier before escaping. Heating increases the population with sufficient energy to leave the surface. This is **thermionic emission**, the operating principle of heated cathodes in vacuum valves.

The minimum surface escape energy is the **work function**, usually specified in electronvolts:

$$
\boxed{1\ \mathrm{eV}=1.602176634\times10^{-19}\ \mathrm J.}
$$

HCV emphasizes the heated-cathode picture and electronic applications. **Extension (standard emission model):** for some idealized thermionic emitters, Richardson–Dushman emission is approximately

$$
J=A_RT^2\exp\!\left(-\frac{\phi}{k_BT}\right),
$$

where $J$ is emitted-current density, $A_R$ an effective material-dependent constant, and $T$ the absolute temperature. This is a useful extension, not a general law for all surfaces and operating conditions.

Thermionic emission must be distinguished from **photoelectric emission**: heat supplies electron energy in the former, individual photons supply it in the latter.

## 41.6 Diode Valve

A vacuum diode contains a heated cathode and a collecting anode. With the anode positive relative to the cathode, emitted electrons accelerate toward it, yielding conventional current in the opposite direction of electron motion. With a strongly negative anode, electrons are repelled and idealized current is nearly zero. The device therefore rectifies alternating potentials.

Current is limited by the rate of emission or, in some operating regimes, by a **space charge** of emitted electrons surrounding the cathode. A useful qualitative current–voltage curve has a rise followed by emission-limited saturation as collection becomes efficient.

**Extension (space-charge-limited ideal planar diode):** the Child–Langmuir result for zero initial emission velocity, vacuum gap $d$, and an ideal one-dimensional geometry is

$$
J=\frac49\varepsilon_0\sqrt{\frac{2e}{m_e}}\frac{V^{3/2}}{d^2}.
$$

The $V^{3/2}$ law should not be applied to every vacuum-diode operating region. A semiconductor $p$–$n$ diode (Chapter 45) rectifies by a different microscopic mechanism.

## 41.7 Triode Valve

In a **triode**, a wire grid is placed between cathode and anode. A small grid-voltage change controls a larger change in anode current: the grid modifies the electron stream without ideally drawing much grid current. The three electrodes are cathode, control grid, and anode or plate.

The concept of amplification is a controlled energy-transfer process, not creation of energy. A power supply provides the energy appearing in an amplified output signal. If a small grid input changes the plate current by $\Delta I_p$,

$$
\Delta V_{\mathrm{out}}\approx-R_L\Delta I_p
$$

for a conventional resistive plate load $R_L$ and fixed supply, assuming small-signal linearization. The minus sign indicates an inverting plate-voltage response to increased current.

Useful characteristics include the **transconductance** $g_m$, plate resistance $r_p$, and amplification factor $\mu$ (notations may differ between contexts):

$$
g_m=\left(\frac{\partial I_p}{\partial V_g}\right)_{V_p},\qquad
r_p=\left(\frac{\partial V_p}{\partial I_p}\right)_{V_g},\qquad
\mu=g_mr_p.
$$

These quantities describe local slopes near an operating point rather than a universally linear triode.

## 41.8 Triode as an Amplifier

An amplifier uses a **bias** to set a working operating point and an input signal to make small excursions around it. A grid-voltage variation changes plate current; through the load resistance, that produces a larger output-voltage swing. Signal reproduction requires the operating interval to remain approximately linear and avoid cutoff or saturation-related distortion.

If $i_p(t)=I_{p0}+\delta i_p(t)$, a plate resistor gives

$$
V_p(t)=V_{\mathrm{supply}}-R_Li_p(t),
$$

so the AC component is $\delta V_p=-R_L\delta i_p$. Using the first-order relation $\delta i_p\approx g_m\delta V_g$ for sufficiently small excursions at an approximately fixed plate potential,

$$
\boxed{A_v\approx-g_mR_L}
$$

is a **simplified upper-level estimate**; a more realistic small-signal gain includes plate resistance and load effects, typically reducing the magnitude. HCV's central lesson is that a weak control signal can regulate stronger energy flow supplied by an external source. In modern electronics, the analogous control role is often implemented with transistors.

---

# Part II: Photoelectric Effect and Wave–Particle Duality

Classical wave optics explains interference and diffraction, but the energy exchanged between light and matter is not always continuous. Photon and matter-wave concepts connect radiation, atoms, and the quantum description of motion.

## 42.1 Photon Theory of Light

Light of frequency $\nu$ arrives or exchanges energy in **photons**, each carrying

$$
\boxed{E_\gamma=h\nu=\frac{hc}{\lambda},\qquad
p_\gamma=\frac{E_\gamma}{c}=\frac h\lambda.}
$$

Here $\lambda$ is the wavelength *in vacuum* if $c$ is used; use $v_{\mathrm{phase}}$ carefully in a material. Photons have zero rest mass, propagate at $c$ in vacuum, and carry energy and momentum. Increasing light frequency increases **energy per photon**, while increasing the number of photons arriving each second increases energy flux at fixed frequency.

For $N$ monochromatic photons,

$$
E_{\mathrm{total}}=Nh\nu.
$$

A helpful conversion for photons in vacuum is

$$
\boxed{E_\gamma(\mathrm{eV})\simeq\frac{1240}{\lambda(\mathrm{nm})}}.
$$

The photon model does not abolish wave properties: diffraction and interference still occur. The classical wave description predicts many field patterns, while photons describe quantum energy exchange and detection statistics.

## 42.2 Photoelectric Effect

When light shines on an appropriate metal, electrons can escape if the energy of an absorbed photon exceeds the material's surface barrier. The minimum energy to remove an electron is the **work function** $\phi$. Conservation of energy gives Einstein's equation

$$
\boxed{K_{\max}=h\nu-\phi=\frac{hc}{\lambda}-\phi.}
$$

Some emitted electrons lose energy before escape, so not every photoelectron has $K_{\max}$. The threshold frequency and wavelength are

$$
\boxed{\nu_0=\frac\phi h,\qquad\lambda_0=\frac{hc}{\phi}.}
$$

A vacuum photocell uses an illuminated emitting cathode and collecting anode. As positive collector potential increases, photocurrent approaches **saturation** when nearly all emitted electrons are collected. A sufficiently negative collector opposes the emitted electrons; the stopping-potential magnitude $V_s$ satisfies

$$
\boxed{eV_s=K_{\max}=h\nu-\phi.}
$$

Thus a graph of stopping potential against light frequency has slope $h/e$ and frequency-axis intercept $\nu_0$:

$$
V_s=\frac he\nu-\frac\phi e.
$$

**The crucial observations** are (i) a threshold frequency, (ii) maximum electron kinetic energy controlled by frequency rather than intensity, (iii) stronger intensity increasing saturation current when emission is allowed and other conditions fixed, and (iv) emission without a classical energy-accumulation delay under ordinary photoelectric conditions.

**Diagnostic:** light of frequency *below* $\nu_0$ does not eject electrons in the ideal one-photon process merely because the beam is made extremely intense. At very high intensities, multiphoton processes can occur, but those belong to an extended regime beyond the basic HCV model.

## 42.3 Matter Waves

De Broglie extended the wave–particle connection to material particles. A moving particle of momentum magnitude $p$ is associated with wavelength

$$
\boxed{\lambda_{\mathrm{dB}}=\frac hp.}
$$

For a nonrelativistic particle $p=mv$ and $K=p^2/(2m)$, so

$$
\boxed{\lambda_{\mathrm{dB}}=\frac h{mv}=\frac h{\sqrt{2mK}}.}
$$

For an electron accelerated from rest through voltage $V$ in a nonrelativistic setting,

$$
\boxed{\lambda_{\mathrm{dB}}=\frac h{\sqrt{2m_eeV}}.}
$$

Its convenient numerical form is $\lambda_{\mathrm{dB}}\simeq1.227\,\mathrm{nm}/\sqrt{V/(1\,\mathrm V)}$ for nonrelativistic electrons. Electron diffraction by crystals experimentally supports the wave picture. Quantum mechanics treats matter waves as **probability amplitudes**, not as ordinary elastic ripples in a material medium.

A classical everyday object also has $\lambda=h/p$, but the wavelength is extraordinarily small at ordinary momentum, which is why its interference behavior is not noticed in daily life. When kinetic energies are relativistic, use $p=\gamma m_0v$ rather than $m_0v$.

---
# Part III: Bohr's Model and Physics of the Atom

The line spectrum of hydrogen is evidence that atoms can exchange only certain energies. Rutherford's nuclear atom explains scattering, but classical mechanics and electrodynamics alone fail to explain atomic stability. Bohr quantization predicts hydrogen energies; quantum mechanics explains what the allowed states actually mean.

## 43.1 Early Atomic Models

In Thomson's early picture, a positively charged distribution contained negatively charged electrons, maintaining overall atomic neutrality. Rutherford's **alpha-particle scattering** experiments contradicted this diffuse-charge model: although most alpha particles traversed thin metal foil with small deflections, a tiny fraction scattered through large angles. A concentrated positive nucleus, containing most of an atom's mass, accounts for the strong deflections.

The key geometry is that nuclei are extremely small compared with whole atoms. The nuclear picture does *not*, by itself, explain the stability of electrons around the nucleus. Classical charged particles undergoing centripetal acceleration should radiate according to classical electromagnetic theory.

For a particle undergoing Coulomb-dominated circular motion around a heavy nucleus,

$$
\frac{m_ev^2}{r}=\frac{Ze^2}{4\pi\varepsilon_0r^2},
$$

where $Z$ is nuclear charge number. The equation balances forces but does not establish that the orbit is stable or permitted in an atom.

**Figure companion:** HCV compares Thomson-type charge distribution with a central nucleus and introduces the scattering geometry. Track how rare large-angle scattering leads to a compact nuclear charge rather than merely memorizing model names.

## 43.2 Hydrogen Spectra

A dilute hydrogen discharge emits light only at certain discrete frequencies. These form spectral **series** grouped by the lower energy level reached. An empirical description is the Rydberg formula

$$
\boxed{\frac1\lambda=R_H\left(\frac1{n_f^2}-\frac1{n_i^2}\right),\quad n_i>n_f,}
$$

where $R_H$ is the hydrogen Rydberg constant and $n_i,n_f$ are positive integers. For hydrogen, $R_H\approx1.097\times10^7\,\mathrm{m^{-1}}$ (the more accurate value for real hydrogen incorporates reduced mass).

| Series | Lower level $n_f$ | Typical region |
|---|---:|---|
| Lyman | 1 | Ultraviolet |
| Balmer | 2 | Visible and near ultraviolet |
| Paschen | 3 | Infrared |
| Brackett | 4 | Infrared |
| Pfund | 5 | Infrared |

A spectral line corresponds to a transition, not an electron literally tracing a glowing path. Its photon energy is the positive level difference:

$$
\boxed{h\nu=E_{n_i}-E_{n_f}.}
$$

For upward absorption, the same magnitude of energy must be supplied by an appropriate interaction; spontaneous emission is the downward case.

## 43.3 Difficulties with Rutherford's Model

The Rutherford atom has two important successes: a compact, positively charged nucleus and predominantly empty atomic volume. It also has two fatal classical shortcomings:

1. An orbiting electron is accelerated, so classical electromagnetic theory predicts continuous radiation, energy loss, shrinking radius, and eventual collapse.
2. A particle steadily spiraling inward would radiate over a continuously changing range of frequencies, not the sharply separated hydrogen spectral lines.

The electrostatic energy of a classical electron in circular Coulomb motion is

$$
U(r)=-\frac{Ze^2}{4\pi\varepsilon_0r},\qquad
K(r)=\frac{Ze^2}{8\pi\varepsilon_0r},
$$

and therefore

$$
E(r)=K+U=-\frac{Ze^2}{8\pi\varepsilon_0r}.
$$

This mechanical expression alone permits a continuum of radii and energies. Bohr's innovation was an additional quantization postulate.

## 43.4 Bohr's Model

Bohr postulated special **stationary states** in which the electron does not radiate despite the classical acceleration picture. For a circular orbit in a hydrogen-like atom, quantization is introduced as

$$
\boxed{m_evr=n\hbar=\frac{nh}{2\pi},\qquad n=1,2,3,\ldots}
$$

with Coulomb force providing centripetal acceleration:

$$
\frac{m_ev^2}{r}=\frac{Ze^2}{4\pi\varepsilon_0r^2}.
$$

Use $v=n\hbar/(m_er)$ in the force equation:

$$
\frac{n^2\hbar^2}{m_er^3}=\frac{Ze^2}{4\pi\varepsilon_0r^2}
\quad\Longrightarrow\quad
\boxed{r_n=\frac{4\pi\varepsilon_0\hbar^2}{m_eZe^2}n^2.}
$$

Define the Bohr radius for the idealized infinitely heavy proton:

$$
\boxed{a_0=\frac{4\pi\varepsilon_0\hbar^2}{m_ee^2}\simeq0.0529\ \mathrm{nm};\qquad r_n=\frac{n^2a_0}{Z}.}
$$

From the force equation, $K=Ze^2/(8\pi\varepsilon_0r_n)$ and $U=-2K$. Hence

$$
E_n=-\frac{Ze^2}{8\pi\varepsilon_0r_n}
=-\frac{m_eZ^2e^4}{8\varepsilon_0^2h^2n^2}.
$$

In convenient hydrogen-like units,

$$
\boxed{E_n\simeq-\frac{13.6Z^2}{n^2}\ \mathrm{eV}.}
$$

For hydrogen $Z=1$, its ground-state energy is approximately $-13.6\,\mathrm{eV}$ relative to a separated electron and proton at rest. The **ionization energy from state $n$** is the positive energy required to reach the free-electron threshold:

$$
\boxed{E_{\mathrm{ion}}(n)=-E_n=\frac{13.6Z^2}{n^2}\ \mathrm{eV}.}
$$

The frequency of a downward transition is

$$
h\nu=13.6Z^2\,\mathrm{eV}\left(\frac1{n_f^2}-\frac1{n_i^2}\right),
$$

recovering the Rydberg form. **Assumptions:** single-electron atom or ion, fixed/very heavy nucleus, Coulomb interaction, no fine structure or external fields, and nonrelativistic motion. A reduced electron–nucleus mass improves accuracy.

**Physical meaning:** $n$ labels allowed energies; it is not a statement that an electron is a miniature planet running on a visibly fixed orbit. That image is a transitional model.

## 43.5 Limitations of Bohr's Model

Bohr's simple model reproduces the leading gross spectrum of hydrogen and hydrogen-like ions, but it does not successfully provide a comprehensive atomic theory. Limitations include:

- Inadequate description of multi-electron spectra and interactions between electrons.
- Failure to fully account for line intensities and selection rules.
- Fine spectral splitting and detailed magnetic-field/electric-field spectral behavior without added theory.
- Arbitrary coexistence of classical orbits with a postulate that stationary electrons do not radiate.
- No systematic probability description of where the electron would be detected.

A successful numerical energy formula is not evidence that all microscopic assumptions behind its derivation are literally correct. Quantum mechanics replaces the orbit picture with wavefunctions and physical observables.

## 43.6 The Wave Function of an Electron

Quantum mechanics describes an electron through a complex-valued wavefunction $\psi(\vec r,t)$. For a normalized one-particle state, the **Born probability rule** gives

$$
\boxed{dP=|\psi(\vec r,t)|^2\,d^3r,\qquad
\int_{\mathbb R^3}|\psi(\vec r,t)|^2\,d^3r=1.}
$$

The wavefunction itself is a probability **amplitude**, not probability density. A density has dimensions of inverse volume for an ordinary three-dimensional spatial wavefunction. Detection is localized, even though the state's possible outcomes are distributed.

The **time-dependent Schrödinger equation** for a single nonrelativistic electron in a scalar potential $U(\vec r,t)$ is

$$
\boxed{i\hbar\frac{\partial\psi}{\partial t}
=\left[-\frac{\hbar^2}{2m_e}\nabla^2+U(\vec r,t)\right]\psi.}
$$

For stationary potentials, separate variables:

$$
\psi(\vec r,t)=\psi_E(\vec r)e^{-iEt/\hbar},
$$

leading to the time-independent eigenvalue equation

$$
\boxed{\left[-\frac{\hbar^2}{2m_e}\nabla^2+U(\vec r)\right]\psi_E=E\psi_E.}
$$

An eigenstate's spatial probability density is time independent because the overall phase disappears in $|\psi|^2$; this differs profoundly from an electron running around a classical circle.

## 43.7 Quantum Mechanics of the Hydrogen Atom

For hydrogen-like ions with a heavy nucleus of charge $+Ze$, use the Coulomb potential energy

$$
U(r)=-\frac{Ze^2}{4\pi\varepsilon_0r}.
$$

Then the stationary Schrödinger equation is

$$
\boxed{-\frac{\hbar^2}{2m_e}\nabla^2\psi
-\frac{Ze^2}{4\pi\varepsilon_0r}\psi=E\psi.}
$$

Allowed bound-state solutions are characterized by quantum numbers:

$$
n=1,2,\ldots;\qquad \ell=0,1,\ldots,n-1;\qquad m_\ell=-\ell,\ldots,+\ell.
$$

In the ideal Coulomb problem, energies depend on $n$ alone and agree with the leading Bohr formula:

$$
E_n\simeq-\frac{13.6Z^2}{n^2}\ \mathrm{eV}.
$$

For the hydrogen $1s$ orbital with the infinitely heavy nucleus approximation,

$$
\boxed{\psi_{100}(r)=\frac1{\sqrt{\pi a_0^3}}e^{-r/a_0}.}
$$

Its **radial probability distribution** is not just $|\psi|^2$: the volume of a spherical shell grows as $4\pi r^2dr$. Therefore

$$
\boxed{P(r)\,dr=4\pi r^2|\psi_{100}(r)|^2\,dr
=\frac{4r^2}{a_0^3}e^{-2r/a_0}\,dr.}
$$

Differentiate $r^2e^{-2r/a_0}$ and set the derivative to zero: the most probable *radial distance* is $r=a_0$. That numerical agreement with the Bohr ground-state radius does **not** restore a definite circular orbit. In the Coulomb model the $n=2$ shell has the same gross energy for distinct permitted $\ell,m_\ell$ values; external perturbations and finer physics can break degeneracies.

**Figure companion:** HCV's radial-probability plots compare quantum states; the plotted radial distribution already includes shell volume. Do not mistake the peak of $|\psi(r)|^2$ for the peak of radial probability.

## 43.8 Nomenclature in Atomic Physics

Atomic electron configurations use a hierarchy of labels:

- **Principal quantum number $n$:** principal shell and gross hydrogen-like energy.
- **Orbital angular-momentum number $\ell$:** subshell; $\ell=0,1,2,3$ correspond to $s,p,d,f$.
- **Magnetic quantum number $m_\ell$:** $2\ell+1$ possible spatial orientations for each $\ell$.
- **Spin projection $m_s=\pm\tfrac12$:** two electron spin states (not a classical spinning ball).

For a fixed $n$, the number of distinct spatial orbital states is

$$
\sum_{\ell=0}^{n-1}(2\ell+1)=n^2,
$$

and including the two spin choices gives

$$
\boxed{N_{\mathrm{states}}=2n^2.}
$$

Pauli's exclusion principle prohibits two identical electrons in an atom from occupying the same complete set of quantum numbers. This provides the counting basis for shell capacities: $K$ ($n=1$) holds 2 electrons, $L$ ($n=2$) holds 8, $M$ ($n=3$) holds 18 under the ideal quantum-state counting. Actual filling order across shells and subshells also depends on electron interactions and energies.

The magnitude of orbital angular momentum in a state with quantum number $\ell$ is

$$
|\vec L|=\sqrt{\ell(\ell+1)}\,\hbar,
$$

and one component is quantized as $L_z=m_\ell\hbar$. These are quantum angular-momentum rules rather than a classical rigid-body rotation model.

## 43.9 Laser

**LASER** stands for *Light Amplification by Stimulated Emission of Radiation*. The three key photon–atom processes are:

1. **Absorption:** a photon supplies energy $\Delta E=E_2-E_1$ to promote an atom.
2. **Spontaneous emission:** an excited atom decays and emits a photon without an incident triggering photon.
3. **Stimulated emission:** a resonant incoming photon causes emission into the same optical mode, supporting coherent amplification.

Gain requires **population inversion** between relevant levels, meaning the upper-level occupation exceeds the lower-level occupation in the sense required for net stimulated emission. A pumping mechanism provides energy to create inversion, often aided by a metastable state. An optical resonator can provide feedback and select modes; an output coupler extracts part of the light.

$$
\boxed{h\nu=E_2-E_1,\qquad \lambda=\frac{hc}{E_2-E_1}.}
$$

Laser light can have high directionality, high spectral purity, and high coherence, but a real laser is not perfectly monochromatic or perfectly collimated. Optical intensity becomes extremely large when energy is concentrated into a small beam cross-section; total energy still comes from the pumping system.

**Engineering connection:** lasers are important in optical metrology, LiDAR, interferometry, material processing, and coherent communications. These applications follow from stimulated emission and beam properties; they are not the same as an introductory derivation of laser gain.

---

# Part IV: X-rays

X-rays are electromagnetic radiation with wavelengths of approximately atomic length scales. That makes crystals natural diffraction structures and allows high-energy photon interactions with inner-shell electrons and nuclei.

## 44.1 Production of X-rays

A typical X-ray tube accelerates electrons from a cathode toward a high-$Z$ target or anode. The incident electrons decelerate sharply in the target and can also create inner-shell vacancies. Both processes produce X-rays, though via different mechanisms.

If an electron gains kinetic energy $eV_a$ by acceleration through voltage $V_a$, then the maximum energy a single X-ray photon can carry is bounded by

$$
\boxed{E_{\gamma,\max}=eV_a.}
$$

Most incoming-electron energy commonly becomes heat rather than outgoing X-ray photons, requiring thermal management of the target. Increasing tube voltage raises electron impact energy; increasing filament current chiefly changes the number of emitted electrons available for acceleration.

**Figure companion:** HCV's X-ray tube sketches show the electron-emitting filament, focusing geometry, acceleration field, target, and radiation exit path. Separate the electron beam from the emitted X-ray beam.

## 44.2 Continuous and Characteristic X-rays

**Continuous spectrum (bremsstrahlung):** electrons decelerate in the Coulomb fields of target atoms. Different energy losses produce photons over a continuous range. The largest possible photon energy corresponds to nearly all an incoming electron's acquired energy appearing in a single photon. Thus

$$
\frac{hc}{\lambda_{\min}}=eV_a
\quad\Longrightarrow\quad
\boxed{\lambda_{\min}=\frac{hc}{eV_a}.}
$$

This is the **Duane–Hunt relation**, valid for the elementary tube model where acceleration energy sets the limit. A quick useful form is

$$
\boxed{\lambda_{\min}(\mathrm{nm})\simeq\frac{1.240}{V_a(\mathrm{kV})}.}
$$

**Characteristic spectrum:** an incoming electron ejects an inner-shell electron from a target atom. When an outer electron fills the vacancy, a photon is emitted whose energy matches the target's inner-shell binding-energy difference. These lines depend strongly on target atomic number and configuration.

The labels $K_\alpha$, $K_\beta$, etc. name transitions *ending* in a $K$-shell vacancy: approximately $L\rightarrow K$ for $K_\alpha$ and $M\rightarrow K$ for $K_\beta$. Characteristic lines appear only when incident electrons can create the relevant vacancy. The continuous cutoff depends chiefly on tube voltage; characteristic energies depend on target atomic structure.

## 44.3 Soft and Hard X-rays

**Hard** X-rays have relatively high photon energies and short wavelengths; **soft** X-rays have lower energies and longer wavelengths. These are relative categories, not two separate types of waves:

$$
\boxed{E_\gamma=h\nu=\frac{hc}{\lambda}.}
$$

Raising acceleration voltage moves the continuous-spectrum short-wavelength cutoff toward smaller $\lambda$ and can make higher-energy lines accessible. Raising filament emission at fixed accelerating voltage usually raises intensity but does not alter the cutoff wavelength in the basic tube model.

Different materials attenuate X-rays differently, depending on photon energy, density, composition, and interaction processes. 'Harder' often correlates with greater penetration in a given application, but attenuation is not determined by photon energy alone for all materials and energies.

## 44.4 Moseley's Law

Moseley's studies established a connection between characteristic X-ray frequency and **atomic number** $Z$, supporting the modern ordering of elements by nuclear charge. An empirical expression for related characteristic lines within a sequence is

$$
\boxed{\sqrt\nu=a(Z-b),}
$$

where $a,b$ depend on the selected line series and screening approximation. The square root follows because inner-shell energy scales approximately as effective nuclear charge squared:

$$
E_n\approx-13.6\,\mathrm{eV}\frac{(Z-\sigma)^2}{n^2}.
$$

For a simplified $K_\alpha$ transition $n=2\rightarrow1$,

$$
h\nu\approx13.6\,\mathrm{eV}\,(Z-\sigma)^2\left(1-\frac14\right),
$$

so $\nu\propto(Z-\sigma)^2$ and $\sqrt\nu\propto Z-\sigma$. A constant screening parameter is an approximation, not a universally exact description of all X-ray lines.

The physical lesson is historical as well as mathematical: X-ray frequency provides evidence about nuclear charge more directly than chemical mass ordering.

## 44.5 Bragg's Law

An X-ray beam scattered by successive, equally spaced lattice planes interferes constructively at certain angles. For plane spacing $d$ and grazing or Bragg angle $\theta$ measured **relative to the planes** (not their normal), the extra path length between waves from adjacent planes is

$$
\Delta\ell=2d\sin\theta.
$$

Constructive interference requires an integer number of wavelengths:

$$
\boxed{2d\sin\theta=n\lambda,\qquad n=1,2,\ldots.}
$$

A common error is using $\cos\theta$ because the angle was measured from the normal. Draw the geometry first and identify what 'incident angle' means in a given diagram. Bragg diffraction probes crystal spacings because $\lambda$ is comparable to atomic dimensions.

**Interpretation:** Bragg's law identifies maxima from a chosen set of equally spaced planes. Actual diffraction intensities also depend on lattice symmetry, atomic scattering factors, crystal orientation, and finite crystal size. It is not an assertion that X-rays reflect from atoms like a mirror without wave interference.

## 44.6 Properties and Uses of X-rays

X-rays are electromagnetic waves, not fast electrons or charged nuclear projectiles. In vacuum they travel at $c$, carry energy and momentum, exhibit diffraction and interference, produce ionization and fluorescence in suitable matter, and are not themselves deflected by static electric or magnetic fields. They can expose detectors and damage biological tissues because their photon energies can ionize atoms and molecules.

**Uses emphasized by their properties:** radiography through differential attenuation, non-destructive inspection, diffraction-based structure determination, material and elemental analysis, and selected medical treatments. The same interactions that make X-rays useful also make shielding and dose control important.

A simple idealized attenuation law for a narrow monoenergetic beam through uniform matter is

$$
\boxed{I(x)=I_0e^{-\mu x},}
$$

with attenuation coefficient $\mu$. **Extension:** real imaging usually involves polychromatic beams and scattered radiation, so a single constant $\mu$ is an approximation.

---
# Part V: Semiconductors and Semiconductor Devices

A quantum view of electrons in solids explains why copper conducts, glass insulates, and silicon can be engineered to switch or amplify current. The core idea is **available energy states**, combined with the motion of electrons and holes in a crystal.

## 45.1 Introduction

For many materials at moderate fields, current density obeys a local relation

$$
\boxed{\vec J=\sigma\vec E,\qquad\rho=\frac1\sigma,}
$$

where $\sigma$ is electrical conductivity and $\rho$ resistivity. Metals have many accessible charge-carrier states and usually high conductivity. An insulating crystal has a large energy gap that suppresses thermal carrier production under ordinary conditions. A semiconductor lies between these behaviors and is especially useful because its carrier population is controllable through temperature, impurities, light, and junction formation.

**Why temperature trends differ:** in a typical metal, increasing temperature enhances scattering and may increase resistivity. In an intrinsic semiconductor over ordinary ranges, increasing temperature creates many more carriers, often increasing its conductivity despite mobility changes. This is a competition between **carrier number** and **carrier mobility**.

## 45.2 Energy Bands in Solids

Isolated atoms have discrete bound-electron energies. When enormous numbers of atoms form a crystal, overlapping interactions split formerly identical atomic states into many closely spaced states, producing **bands**. An occupied electron state can only respond to a small applied energy by changing state if an unoccupied state is accessible.

The **valence band** contains high-lying occupied bonding states, the **conduction band** contains states supporting mobile conduction, and the **band gap** $E_g$ is an energy interval with no allowed crystal electron states:

$$
\boxed{E_g=E_{\mathrm{CB,edge}}-E_{\mathrm{VB,edge}}.}
$$

Materials are usefully classified as follows:

| Material behavior | Band picture | Response at ordinary temperature |
|---|---|---|
| Metal | Partly filled band or overlapping occupied/empty bands | Many accessible states, high conductivity |
| Semiconductor | Modest band gap | Some carriers thermally excited; doping changes density greatly |
| Insulator | Relatively large band gap | Very few free carriers under ordinary conditions |

A useful thermal-energy scale is

$$
\boxed{k_BT\simeq0.0259\ \mathrm{eV}\quad\text{at }T=300\ \mathrm K.}
$$

Do not confuse $k_BT$ with the band gap itself; carrier generation involves statistical populations rather than a statement that all carriers possess exactly $k_BT$.

## 45.3 The Semiconductor

In silicon and germanium, neighboring atoms form covalent bonds. At sufficiently low temperature in an ideal pure crystal, the valence band is filled and the conduction band nearly empty. Thermal excitation can promote electrons across the gap, leaving vacant valence-band states called **holes**. An electron–hole pair consists of one conduction electron and one hole.

A hole behaves as a mobile carrier of effective positive charge $+e$, although it is not a physical free proton. When a valence electron from a neighboring bond fills a vacancy, the vacancy effectively moves in the opposite direction. In an intrinsic semiconductor,

$$
\boxed{n=p=n_i,}
$$

where $n$ and $p$ are electron and hole number densities and $n_i$ is intrinsic density. Generation and recombination continually change individual carriers while equilibrium establishes the mean populations.

**Conceptual distinction:** the crystal may remain electrically neutral even while both kinds of mobile carriers exist. Neutrality is about *total net charge*, not the absence of charges capable of moving.

## 45.4 p-type and n-type Semiconductors

**Doping** deliberately adds small amounts of suitable impurity atoms to a semiconductor.

- A pentavalent donor replacing a tetravalent host atom (for example, phosphorus in silicon) supplies an easily excited electron, producing **n-type** material. Electrons are majority carriers.
- A trivalent acceptor (for example, boron in silicon) can accept an electron from a bond, leaving a mobile hole, producing **p-type** material. Holes are majority carriers.

A donor that loses an electron becomes a *fixed positive dopant ion*; an acceptor that captures an electron becomes a *fixed negative dopant ion*. The mobile carriers are not the same thing as the immobile ionized impurities.

Under simple full-ionization and nondegenerate equilibrium approximations,

$$
n\simeq N_D\quad\text{(n-type)},\qquad
p\simeq N_A\quad\text{(p-type)},
$$

when compensating dopants are negligible. **Extension (equilibrium mass action):**

$$
\boxed{np=n_i^2,}
$$

for a nondegenerate semiconductor in thermal equilibrium, so increasing majority density generally reduces minority density. Heavy doping, strong fields, or nonequilibrium carrier injection can invalidate simplistic forms.

## 45.5 Density of Charge Carriers and Conductivity

In an applied electric field, electrons and holes have opposite drift directions but their **conventional-current contributions add**. In a low-field drift approximation,

$$
\vec v_{d,e}=-\mu_e\vec E,\qquad\vec v_{d,h}=+\mu_h\vec E,
$$

where mobilities $\mu_e,\mu_h$ are positive coefficients. The electron current density is $(-e)n\vec v_{d,e}$; the hole current density is $(+e)p\vec v_{d,h}$. Therefore

$$
\boxed{\vec J=e(n\mu_e+p\mu_h)\vec E,}
$$

and

$$
\boxed{\sigma=e(n\mu_e+p\mu_h).}
$$

Units check: $[e]=\mathrm C$, $[n]=\mathrm{m^{-3}}$, $[\mu]=\mathrm{m^2/(V\,s)}$, giving $[\sigma]=\mathrm{S/m}$. Doping changes $n$ and $p$; impurity scattering can also modify mobility, so conductivity is not determined by dopant concentration alone.

In an intrinsic semiconductor $n=p=n_i$:

$$
\sigma_i=en_i(\mu_e+\mu_h).
$$

## 45.6 p–n Junction

When p-type and n-type regions form one junction, majority carriers initially **diffuse** across the interface: electrons from n to p, holes from p to n. They recombine, leaving behind fixed donor and acceptor ions. The space-charge region develops an electric field that opposes further majority-carrier diffusion.

This relatively carrier-depleted region is the **depletion layer**. Equilibrium occurs when net electron and hole currents vanish because drift and diffusion effects balance. A **built-in potential** develops, but a voltmeter connected to equilibrium semiconductor contacts does not simply read that potential as an accessible external battery voltage; contact potentials also matter.

Qualitatively:

```text
 p-type bulk       depletion region        n-type bulk
 holes +          fixed - | fixed +       electrons -
    diffusion  ------>        <------  diffusion
                opposing internal electric field
```

Applying **forward bias** (p side positive relative to n side) reduces the effective junction barrier and substantially increases carrier injection. **Reverse bias** increases the barrier, widening the depletion region and permitting only a small reverse current until breakdown effects become important.

## 45.7 p–n Junction Diode

A semiconductor diode's nonlinear current–voltage curve permits substantial forward current but little reverse current over a suitable operating range. In the standard ideal diode approximation,

$$
\boxed{I=I_s\left(e^{eV_D/(\eta k_BT)}-1\right),}
$$

where $I_s$ is a reverse-saturation scale, $\eta$ an ideality factor, and $V_D$ the forward anode-to-cathode voltage. **Extension:** this exponential model is useful for quantitative electronics, but HCV primarily motivates the behavior through junction bias and characteristic curves. $\eta$ and $I_s$ depend on device physics, temperature, and operating region.

The simple **constant-drop approximation** (often around $0.7\,\mathrm V$ for an ordinary silicon diode at certain currents and temperatures) is a circuit shortcut, *not* a universal turn-on threshold. Real forward voltage varies continuously with current and temperature.

At sufficiently strong reverse bias, breakdown may occur through field- or avalanche-related processes. A device intentionally designed to operate in reverse breakdown can regulate voltage, but ordinary diode ratings must be respected.

## 45.8 p–n Junction as a Rectifier

A half-wave rectifier conducts principally during one half of an AC cycle. With a sinusoidal input $v_s(t)=V_m\sin(\omega t)$ and an ideal diode plus resistive load,

$$
v_{\mathrm{out}}(t)=\begin{cases}V_m\sin(\omega t),&0<\omega t<\pi,\\0,&\pi<\omega t<2\pi,\end{cases}
$$

repeated periodically. The average output over a cycle is

$$
\boxed{\overline V=\frac1{2\pi}\int_0^\pi V_m\sin\theta\,d\theta=\frac{V_m}{\pi}.}
$$

A **full-wave rectifier** converts both input half-cycles into the same load-voltage polarity, using a center-tapped arrangement or a bridge of diodes. For an ideal full-wave rectified sine,

$$
\boxed{\overline V=\frac1{2\pi}\int_0^{2\pi}V_m|\sin\theta|\,d\theta=\frac{2V_m}{\pi}.}
$$

Real rectifiers include forward drops and finite losses. A filter capacitor can smooth the pulsating output but introduces ripple and charging-current effects. Compare the physical direction of diode current in each conducting branch, not only the shape of the output sketch.

## 45.9 Junction Transistors

A **bipolar junction transistor** (BJT) has emitter, base, and collector regions, arranged as $npn$ or $pnp$. In the common active region, its emitter–base junction is forward biased while its collector–base junction is reverse biased. The thin base allows many injected carriers to reach the collector rather than recombine there.

Conventional terminal currents satisfy charge conservation:

$$
\boxed{I_E=I_C+I_B.}
$$

Define current-gain parameters

$$
\boxed{\alpha=\frac{I_C}{I_E},\qquad
\beta=\frac{I_C}{I_B}=\frac{\alpha}{1-\alpha},\qquad
\alpha=\frac{\beta}{\beta+1},}
$$

for appropriately defined DC or local incremental operating conditions. In normal active operation $\alpha$ is close to unity and $\beta$ may be much larger than unity. These ratios are approximations and are not constant over every voltage and current.

**Modes:** cutoff (small conduction), forward active (amplifying), and saturation (both junctions effectively forward biased, appropriate for an ON switch in simple digital designs). A transistor is not merely two separate back-to-back diodes; the shared thin base and carrier transport are essential.

**Amplifier viewpoint:** a small input change controls a larger collector-current change, and a load converts that current modulation into output voltage. As with the vacuum triode, energy comes from the power supply. A common-emitter stage often produces inverted voltage gain.

## 45.10 Logic Gates

A binary logical variable takes values $0$ or $1$; physical circuit voltages represent those values in specified ranges. Boolean operations provide the mathematical foundation of digital electronics.

| $A$ | $B$ | $A\land B$ (AND) | $A\lor B$ (OR) | $A\oplus B$ (XOR) | $\overline{A\land B}$ (NAND) |
|---:|---:|---:|---:|---:|---:|
| 0 | 0 | 0 | 0 | 0 | 1 |
| 0 | 1 | 0 | 1 | 1 | 1 |
| 1 | 0 | 0 | 1 | 1 | 1 |
| 1 | 1 | 1 | 1 | 0 | 0 |

A **NOT** gate maps $0\rightarrow1$ and $1\rightarrow0$; NOR is NOT(OR). In Boolean algebra, AND is often written $AB$, OR as $A+B$, and NOT as $\overline A$. The symbol $+$ in this context is *logical OR*, not ordinary integer addition: $1+1=1$ in Boolean OR.

Example: simplify

$$
Y=A+(AB).
$$

Using absorption,

$$
\boxed{A+AB=A.}
$$

Electronic gates are physical circuits implementing these abstract truth tables; supply rails, fan-out, propagation delay, and noise margins determine whether the implementation reliably respects the intended logic. **Extension:** NAND and NOR are each functionally complete, so either can be used to construct arbitrary combinational Boolean operations.

**Figure companion:** HCV presents switch–lamp analogies and diode/transistor gate circuits. Draw the circuit current paths for each truth-table row to connect Boolean abstraction with device physics.

---
# Part VI: The Nucleus

Atomic chemistry primarily depends on electrons; nuclear transformations concern protons, neutrons, and the forces holding them together. The main bookkeeping quantities are nucleon number, electric charge, total energy, and momentum.

## 46.1 Properties of a Nucleus

A nucleus contains $Z$ protons and $N$ neutrons. The **mass number** is $A=Z+N$, and nuclide notation is

$$
\boxed{{}^{A}_{Z}X,\qquad N=A-Z.}
$$

**Isotopes** share $Z$ but differ in $N$; **isobars** share $A$; **isotones** share $N$. The nuclear radius approximately scales as

$$
\boxed{R=r_0A^{1/3},\qquad r_0\approx1.1\text{–}1.2\ \mathrm{fm},\quad1\ \mathrm{fm}=10^{-15}\ \mathrm m.}
$$

Because volume scales as $R^3\propto A$ while nuclear mass is approximately proportional to $A$, the mean nuclear density is roughly independent of mass number. This approximation summarizes a family of nuclei rather than claiming an identical sharp-edge radius and density for every isotope.

**Mass and energy:** $1$ unified atomic mass unit ($\mathrm u$) is one twelfth of the mass of a neutral $^{12}\mathrm C$ atom, and

$$
\boxed{1\ \mathrm u\,c^2\simeq931.5\ \mathrm{MeV}.}
$$

Nuclear spin arises from coupled nucleon orbital and intrinsic-spin angular momenta. Stable nuclei occupy a limited region of a plot of neutron number $N$ versus proton number $Z$; heavier stable nuclei generally need more neutrons relative to protons because Coulomb repulsion between protons grows with $Z$.

## 46.2 Nuclear Forces

Protons repel electrostatically, yet many nuclei remain bound. At separations of a few femtometres or less, an attractive **residual strong interaction** among nucleons supplies binding; its short range and saturation properties are crucial. At extremely small separations, an effective repulsive core is often used in nuclear models to describe short-range behavior.

A qualitative comparison:

| Interaction | Relevance inside a nucleus |
|---|---|
| Residual strong nuclear force | Provides most nucleon binding over short separations |
| Electromagnetic force | Repels proton pairs and influences stability |
| Weak interaction | Responsible for beta transformations |
| Gravitation | Negligible for ordinary nuclear binding |

Nuclear forces depend on internal quantum properties such as spin and isospin. The familiar statement 'nuclear force is strongest' must always be qualified by the short distance scale and the interaction being compared.

## 46.3 Binding Energy

The mass of a bound nucleus is **less** than the combined mass of the same free protons and neutrons. The difference is the **mass defect**. Using nuclear masses,

$$
\boxed{\Delta m=Zm_p+Nm_n-m_{\mathrm{nucleus}},\qquad B=\Delta m\,c^2.}
$$

Using **neutral atomic masses** instead, electron masses can be handled consistently by

$$
\boxed{B\simeq\big[Zm({}^1\mathrm H)+Nm_n-m_{\mathrm{atom}}({}^A_ZX)\big]c^2,}
$$

neglecting small electron-binding corrections. Do **not** mix bare nuclear masses and neutral-atom masses indiscriminately.

The average binding energy per nucleon is $B/A$. It increases sharply for light nuclei, reaches a broad high region around iron/nickel, and declines slowly for very heavy nuclei. This qualitative curve explains why **fusion of suitably light nuclei** and **fission of certain heavy nuclei** can both release energy: products can be more tightly bound per nucleon than reactants.

For any reaction, the energy available from a decrease in total rest mass is the **$Q$-value**:

$$
\boxed{Q=(m_{\mathrm{initial}}-m_{\mathrm{final}})c^2.}
$$

A positive $Q$ is exothermic; negative $Q$ requires an energy input and/or suitable initial kinetic energy. Energy and momentum conservation jointly determine the kinetic-energy partition among products.

## 46.4 Radioactive Decay

Unstable nuclides can transform spontaneously, emitting particles or photons. Important modes are:

**Alpha decay:** a parent nucleus emits $^4_2\mathrm{He}$, decreasing $A$ by four and $Z$ by two:

$$
\boxed{{}^{A}_{Z}X\rightarrow{}^{A-4}_{Z-2}Y+{}^4_2\mathrm{He}.}
$$

**Beta-minus decay:** a neutron transforms into a proton, electron, and electron antineutrino:

$$
\boxed{n\rightarrow p+e^-+\bar\nu_e,}
$$

so the parent nucleus keeps the same $A$ but increases $Z$ by one.

**Beta-plus decay:** a proton transforms into a neutron, positron, and electron neutrino, when energetically permitted:

$$
\boxed{p\rightarrow n+e^++\nu_e}\quad\text{(inside an energetically allowed nucleus).}
$$

An isolated free proton does not spontaneously undergo this reaction because the final rest masses exceed the initial mass. **Electron capture** is another proton-to-neutron conversion channel inside appropriate atoms, $p+e^-\rightarrow n+\nu_e$.

**Gamma decay:** an excited nucleus releases a high-energy photon with unchanged $A$ and $Z$:

$$
{}^{A}_{Z}X^*\rightarrow{}^{A}_{Z}X+\gamma.
$$

The emissions' energy distributions differ: alpha emission from a given transition is typically discrete (recoil included), whereas the beta spectrum is continuous because energy is shared with a neutrino and the recoiling daughter. Charge, lepton number, nucleon number, energy, and momentum guide the bookkeeping.

## 46.5 Law of Radioactive Decay

Assume each nucleus has a constant probability $\lambda\,dt$ of decaying during a sufficiently short time interval $dt$, independent of its age. If $N(t)$ undecayed nuclei remain,

$$
\frac{dN}{dt}=-\lambda N.
$$

Separate and integrate:

$$
\int_{N_0}^{N(t)}\frac{dN}{N}=-\lambda\int_0^t dt'
\quad\Longrightarrow\quad
\boxed{N(t)=N_0e^{-\lambda t}.}
$$

The **activity** is the expected number of decays per second:

$$
\boxed{\mathcal A(t)=-\frac{dN}{dt}=\lambda N(t)=\mathcal A_0e^{-\lambda t}.}
$$

Half-life satisfies $N(T_{1/2})=N_0/2$, yielding

$$
\boxed{T_{1/2}=\frac{\ln2}{\lambda}\simeq\frac{0.693}{\lambda}.}
$$

The **mean lifetime** is $\tau=1/\lambda$. The SI activity unit is **becquerel** ($1\,\mathrm{Bq}=1$ decay per second); the historical curie satisfies

$$
1\ \mathrm{Ci}=3.7\times10^{10}\ \mathrm{Bq}.
$$

After $n$ half-lives, $N=N_0/2^n$. The exponential law describes expected behavior of large populations; the decay time of a particular nucleus remains probabilistic.

## 46.6 Properties and Uses of Nuclear Radiation

| Radiation | Identity | Charge | Typical penetration and shielding trend |
|---|---|---:|---|
| Alpha ($\alpha$) | $^4_2\mathrm{He}$ nucleus | $+2e$ | Strongly ionizing, typically stopped by thin material |
| Beta-minus ($\beta^-$) | Electron | $-e$ | Greater range than alpha in many common situations; low-$Z$ shielding can reduce bremsstrahlung concerns |
| Beta-plus ($\beta^+$) | Positron | $+e$ | Annihilation can generate gamma photons |
| Gamma ($\gamma$) | High-energy photon | $0$ | Penetrating; attenuation depends strongly on energy and shielding material |

Alpha, beta, and gamma emissions are **ionizing radiation**, able to remove electrons from atoms. They can be detected by ionization chambers, scintillators, semiconductor detectors, and photographic or related historical methods. Applications include tracer techniques, material inspection, sterilization, medical imaging, and selected cancer treatments.

A radioactive source's **activity** is not by itself a direct measure of absorbed biological dose. Radiation energy, type, geometry, exposure duration, and shielding all matter. Absorbed dose is measured in gray ($\mathrm{Gy}=\mathrm{J/kg}$), while equivalent and effective doses use sieverts ($\mathrm{Sv}$) with radiation/tissue weighting. These are useful safety distinctions beyond elementary activity calculations.

## 46.7 Energy from the Nucleus

Binding-energy differences mean a nuclear rearrangement can release large energy compared with ordinary chemical bond changes. The governing relation is

$$
\boxed{E_{\mathrm{released}}=Q=(m_i-m_f)c^2.}
$$

Mass–energy is conserved even when total rest mass decreases: missing rest mass reappears as kinetic energy, photon energy, or other product energies. A practical reaction must also be accessible at a useful rate, controllable, and engineered to transfer its energy where desired.

In a fission process, energetic fragments deposit energy as heat in surrounding matter. In a fusion plasma, product charged particles may transfer kinetic energy to the plasma and its boundary structures. The mere existence of a positive $Q$ does not guarantee a technologically usable power source.

## 46.8 Nuclear Fission

In **fission**, a sufficiently heavy nucleus divides into two main fragments, often with neutrons and gamma photons emitted. Both spontaneous and neutron-induced fission occur depending on the nuclide and conditions. For a representative neutron-induced fissile-uranium process,

$$
{}^{235}_{92}\mathrm U+{}^1_0n
\rightarrow{}^{236}_{92}\mathrm U^*
\rightarrow\text{fission fragments}+\text{neutrons}+\text{energy}.
$$

A typical fission of $^{235}\mathrm U$ yields of order $200\,\mathrm{MeV}$ total energy. There are many possible fragment pairs; no single mass split characterizes every event. Some emitted neutrons may trigger further fissions, creating a **chain reaction**.

Define a basic neutron multiplication factor $k_{\mathrm{eff}}$, the ratio of neutron population in successive idealized generations:

$$
\boxed{k_{\mathrm{eff}}<1:\ \text{subcritical};\qquad
k_{\mathrm{eff}}=1:\ \text{critical};\qquad
k_{\mathrm{eff}}>1:\ \text{supercritical}.}
$$

'Critical' means a self-sustaining chain reaction, not necessarily dangerous runaway power. Multiplication depends on absorption, leakage, fission probability, neutron energy, and system configuration.

## 46.9 Uranium Fission Reactor

HCV introduces the reactor as a controlled, sustained sequence of nuclear fissions. Its major functional blocks are:

| Component | Physical function |
|---|---|
| Fuel | Contains fissile nuclides, typically including $^{235}\mathrm U$ |
| Moderator (in many thermal reactors) | Slows fast neutrons through scattering so selected fission reactions become more probable |
| Control absorbers | Remove neutrons and change reactivity |
| Coolant/heat-transfer circuit | Carries deposited fission energy to a conversion system or heat sink |
| Structural containment and shielding | Maintains geometry and controls exposure and releases |

Prompt neutrons are emitted essentially with the fission event; **delayed neutrons** are emitted after decay of some fission products. Their small fractional contribution enormously improves practical controllability by lengthening relevant response times. A reactor is engineered so heat generation, heat removal, reactivity feedback, and shielding satisfy operating constraints.

**Study boundary:** the conceptual treatment concerns energy production and reactor physics. It is not a design procedure for fissile-material handling or reactor construction.

## 46.10 Nuclear Fusion

Fusion combines sufficiently light nuclei into more tightly bound products. A celebrated example is

$$
\boxed{{}^2_1\mathrm H+{}^3_1\mathrm H
\rightarrow{}^4_2\mathrm{He}+{}^1_0n+17.6\ \mathrm{MeV}.}
$$

Both nuclei are positively charged, so they repel over long distances. Fusion needs a sufficiently high encounter energy or quantum tunneling probability to overcome the **Coulomb barrier** and let the short-range nuclear interaction act.

The Coulomb potential-energy scale for two nuclei separated by $r$ is

$$
U_C(r)=\frac{Z_1Z_2e^2}{4\pi\varepsilon_0r}.
$$

A hot plasma contains a distribution of particle velocities, not one speed set exactly by temperature. Quantum tunneling lets some encounters produce fusion even when classical kinetic energy is below the nominal barrier. Stellar fusion proceeds through reaction networks and densities over long times, not by all protons colliding with enough classical energy to climb one fixed barrier.

## 46.11 Fusion in Laboratory

Laboratory fusion systems seek to create and maintain a hot, dense plasma long enough for significant fusion reactions to occur. Common conceptual approaches are:

- **Magnetic confinement:** fields guide charged plasma particles, as in tokamak- or stellarator-type configurations.
- **Inertial confinement:** fuel is rapidly compressed and heated so reactions occur before substantial expansion.

A simplified performance framework uses density $n$, characteristic confinement time $\tau_E$, and temperature $T$. These enter the **Lawson-type criteria** for whether a given fuel cycle and plasma regime can achieve a desired fusion energy balance. There is no single universal threshold applicable to all configurations without specifying physics and losses.

Key competing channels are fusion heating, conductive and radiative losses, particle escape, plasma instabilities, and structural limits. A plasma creating some fusion events is not equivalent to a power plant exporting net electrical energy. The HCV chapter motivates the fundamental nuclear reaction; confinement engineering is a useful broader context.

---
# Part VII: The Special Theory of Relativity

Classical mechanics assumes that all observers share a universal time and that velocities simply add. Maxwell's electromagnetic-wave equations suggest a fixed vacuum light speed. Special relativity reconciles inertial-frame equivalence with this speed by replacing absolute space and time with observer-dependent measurements linked by Lorentz transformations.

## 47.1 The Principle of Relativity

An **inertial frame** is one in which freely moving bodies follow straight lines at constant velocity. The relativity principle says the basic laws of physics have the same form in every inertial frame. No self-contained experiment can distinguish uniform inertial motion from inertial rest merely by labeling one frame 'really at rest'.

Galilean mechanics relates coordinates in two frames moving at constant relative speed $v$ along $x$ by $x'=x-vt$ and $t'=t$. These imply ordinary velocity addition $u'_x=u_x-v$, but that rule is incompatible with a frame-independent light speed $c$.

Einstein's special-relativity postulates are:

1. **The laws of physics are the same in every inertial frame.**
2. **The speed of light in vacuum has the same value $c$ in every inertial frame**, regardless of the motions of source and observer.

The postulates concern local measurements using clocks and length standards in each frame. They do not claim two observers always assign the same time or distance to separated events.

## 47.2 Are Maxwell's Laws Independent of Frame?

Maxwell's equations in vacuum predict propagating electromagnetic disturbances at

$$
\boxed{c=\frac1{\sqrt{\mu_0\varepsilon_0}}\simeq2.998\times10^8\ \mathrm{m/s}.}
$$

If all inertial observers can use Maxwell's laws in their usual form, the predicted vacuum light speed is the same for them. This directly conflicts with the naive Galilean prediction that the speed relative to an observer chasing the beam should be $c-v$.

The resolution changes how coordinates and clock readings between moving frames are related. In the usual standard configuration of frame $S'$ moving at velocity $v$ along $+x$ relative to $S$,

$$
\boxed{x'=\gamma(x-vt),\qquad
t'=\gamma\left(t-\frac{vx}{c^2}\right),}
$$

$$
\boxed{y'=y,\quad z'=z,\qquad
\gamma=\frac1{\sqrt{1-v^2/c^2}}.}
$$

These **Lorentz transformations** are a concise mathematical formulation extending the book's thought experiments. Notice that $t'$ depends on *both* $t$ and $x$: simultaneity is not generally shared across frames.

For $|v|\ll c$, the transformations approach the Galilean relations to leading order.

## 47.3 Kinematical Consequences

### A. Length perpendicular to motion

For a rod oriented perpendicular to the relative velocity, its transverse length is unchanged between the two standard inertial frames:

$$
\boxed{L_\perp=L_{0,\perp}.}
$$

There is no universal contraction of all dimensions. Length contraction depends on the direction in which the length is measured.

### B. Time dilation

A clock at rest in its own frame measures the **proper time** $\Delta\tau$ between two events at the same place in that clock's frame. A frame in which the clock moves at constant speed $v$ assigns a larger coordinate interval:

$$
\boxed{\Delta t=\gamma\Delta\tau.}
$$

**Light-clock derivation:** take two mirrors separated by transverse distance $L_0$. In the clock frame, a light pulse covers $2L_0$ in one round-trip:

$$
\Delta\tau=\frac{2L_0}{c}.
$$

In a frame where the clock moves horizontally, each half of the light path is diagonal. By Pythagoras,

$$
\left(\frac{c\Delta t}{2}\right)^2
=L_0^2+\left(\frac{v\Delta t}{2}\right)^2.
$$

Substitute $L_0=c\Delta\tau/2$ and solve:

$$
(c^2-v^2)\Delta t^2=c^2\Delta\tau^2
\quad\Longrightarrow\quad
\boxed{\Delta t=\frac{\Delta\tau}{\sqrt{1-v^2/c^2}}}. 
$$

Every ideal physical clock follows the same rule, not just clocks that use light pulses.

### C. Length contraction parallel to motion

**Proper length** $L_0$ is the length of an object measured in its rest frame. Observers for whom the object moves *parallel to its length* obtain

$$
\boxed{L_\parallel=\frac{L_0}{\gamma}=L_0\sqrt{1-v^2/c^2}.}
$$

The two endpoint positions used to measure the moving length must be recorded **simultaneously in the measuring frame**. Confusing measurements made at different times is a common source of erroneous arguments.

### D. Relativity of simultaneity

Two spatially separated events may be simultaneous in $S$ ($\Delta t=0$) but not in $S'$:

$$
\boxed{\Delta t'=\gamma\left(\Delta t-\frac{v\Delta x}{c^2}\right).}
$$

For $\Delta t=0$ and $\Delta x\ne0$, generally $\Delta t'\ne0$. **Simultaneity** is frame dependent. However, the causal ordering of two events that can influence one another (timelike or lightlike separation) cannot reverse between physical inertial frames.

### E. Synchronizing clocks

Synchronizing distant clocks is operational: in a frame, send light pulses, compare travel times, and adopt a consistent convention for the assumed two-way-invariant light speed. Clocks judged synchronized in one inertial frame may not be synchronized in a moving one. This is a consequence of Lorentz transformations, not a defect of clocks.

**Extension (invariant spacetime interval):** for two events,

$$
\boxed{c^2\Delta\tau^2=c^2\Delta t^2-\Delta x^2-\Delta y^2-\Delta z^2}
$$

when the separation is timelike and $\Delta\tau$ denotes their invariant proper-time separation. All inertial frames agree on the interval even though coordinate time and space separations differ.

## 47.4 Dynamics at Large Velocity

At high speed, simply substituting $p=m_0v$ into Newtonian dynamics no longer gives a relativistically consistent description. Define momentum with the Lorentz factor:

$$
\boxed{\vec p=\gamma m_0\vec v,\qquad
\vec F=\frac{d\vec p}{dt}.}
$$

At $v\ll c$, $\gamma\approx1$, recovering $\vec p\approx m_0\vec v$. At relativistic speed, force and acceleration do not remain related by a single universal scalar $m_0$ in arbitrary directions. It is safer to use momentum directly.

**Terminology note:** HCV introduces **moving or relativistic mass** $m=\gamma m_0$. Modern presentations generally use the frame-invariant mass $m_0$ (often simply $m$) and let energy and momentum carry the frame dependence. Both descriptions can produce the same introductory formulas if notations are handled consistently; these notes prefer **invariant rest mass** to avoid confusing mass with velocity-dependent energy.

For a constant force $F$ applied along one axis to a particle initially at rest,

$$
p(t)=Ft=\frac{m_0v}{\sqrt{1-v^2/c^2}}.
$$

Solving for $v$ gives

$$
\boxed{v(t)=\frac{Ftc}{\sqrt{m_0^2c^2+F^2t^2}}.}
$$

As $t\rightarrow\infty$, this approaches $c$ from below but does not exceed it for a massive particle.

## 47.5 Energy and Momentum

The rest energy of a particle is

$$
\boxed{E_0=m_0c^2.}
$$

Its total energy in a frame where it moves at speed $v$ is $E=\gamma m_0c^2$; its kinetic energy is

$$
\boxed{K=(\gamma-1)m_0c^2.}
$$

Taylor-expanding at low speed,

$$
\gamma=\left(1-\frac{v^2}{c^2}\right)^{-1/2}
\approx1+\frac{v^2}{2c^2}+\frac{3v^4}{8c^4}+\cdots,
$$

so

$$
K\approx\frac12m_0v^2+\frac{3m_0v^4}{8c^2}+\cdots.
$$

The complete relation between total energy, momentum, and rest mass is

$$
\boxed{E^2=p^2c^2+m_0^2c^4.}
$$

To verify, substitute $E=\gamma m_0c^2$ and $p=\gamma m_0v$:

$$
E^2-p^2c^2
=\gamma^2m_0^2c^2(c^2-v^2)=m_0^2c^4.
$$

For a photon $m_0=0$, giving $E=pc$ and $p=h/\lambda$. **Mass–energy equivalence** does not say that energy has to be deposited as matter to be conserved; all forms of energy and momentum enter the relativistic conservation laws.

## 47.6 The Ultimate Speed

Massive particles can approach but cannot reach $c$ under finite-energy acceleration in special relativity. Because $\gamma\rightarrow\infty$ as $v\rightarrow c$ for fixed nonzero $m_0$,

$$
\lim_{v\to c^-}K=(\gamma-1)m_0c^2\rightarrow\infty.
$$

Light in vacuum travels at $c$; that speed is the invariant causal propagation limit of relativistic spacetime. The one-dimensional velocity-addition law follows from Lorentz transformations:

$$
\boxed{u'_x=\frac{u_x-v}{1-u_xv/c^2}.}
$$

If $u_x=c$, then $u'_x=c$; for ordinary massive bodies, subluminal input velocities remain subluminal under a physical frame transformation.

HCV briefly discusses speculative **tachyons** in historical context. There is no confirmed experimental observation of tachyonic particles capable of carrying information into an observer's past. The causal speed limit is established physics; speculative superluminal particles are not an observed alternative to it.

## 47.7 Twin Paradox

Consider two initially co-located twins. One remains approximately in a single inertial frame while the other travels outward at high speed and returns. For symmetric constant-speed outward and inward legs of Earth-frame duration $T$ each, neglecting turnaround duration,

$$
\Delta t_{\mathrm{Earth}}=2T,\qquad
\boxed{\Delta\tau_{\mathrm{traveler}}=\frac{2T}{\gamma}.}
$$

At $v=0.8c$, $\gamma=5/3$ and $1/\gamma=0.6$: if Earth measures $20$ years for the two legs, the traveler ages $12$ years in the idealized model. This matches the type of numerical example used by HCV.

**Why symmetry does not force equal aging:** the traveler changes inertial frames at turnaround, whereas the stay-at-home twin remains in one chosen inertial frame in the idealization. The two worldlines between reunion events accumulate different proper times. Acceleration is important in explaining why the traveler's frame cannot remain the same throughout, but a large instantaneous acceleration is not required as a separate 'aging force'.

A compact spacetime expression is

$$
\boxed{\Delta\tau=\int\sqrt{1-\frac{v(t)^2}{c^2}}\,dt,}
$$

for a trajectory expressed using one inertial frame's coordinates. The actual ages at reunion are local physical measurements, not mere optical illusions. Muon-lifetime measurements and precision-clock experiments provide related empirical support for time dilation.

---
# Integrated Worked Examples

These are **original** problems constructed for revision; they are not copied from HCV's exercise sets. Follow the physical model, substitute units explicitly, then test whether the answer is plausible.

### Example 1: Electron charge-to-mass ratio in crossed fields (Chapter 41)

**Problem.** A beam passes undeflected through perpendicular fields of strengths $E=3.0\times10^4\,\mathrm{V/m}$ and $B=2.0\times10^{-3}\,\mathrm T$. With the electric field off and the same magnetic field applied, the circular radius is $r=4.0\,\mathrm{cm}$. Determine the selected speed and measured $e/m_e$.

**Solution.** Zero transverse force requires $eE=evB$:

$$
v=\frac EB=\frac{3.0\times10^4}{2.0\times10^{-3}}
=1.5\times10^7\ \mathrm{m/s}.
$$

Magnetic circular motion gives $e/m_e=v/(Br)$:

$$
\frac e{m_e}=
\frac{1.5\times10^7}{(2.0\times10^{-3})(0.040)}
=\boxed{1.875\times10^{11}\ \mathrm{C/kg}}.
$$

The result is reasonably close to the electron's accepted magnitude $1.759\times10^{11}\,\mathrm{C/kg}$, consistent with approximate experimental inputs.

### Example 2: Electron acceleration and its nonrelativistic domain (Chapter 41)

**Problem.** Electrons accelerate from rest through $200\,\mathrm V$. Estimate their speed and decide whether $v\ll c$.

**Solution.** Take $eV=\tfrac12m_ev^2$:

$$
v=\sqrt{\frac{2(1.602\times10^{-19})(200)}{9.109\times10^{-31}}}
\simeq\boxed{8.39\times10^6\ \mathrm{m/s}}.
$$

Then $v/c\simeq0.028$, so a nonrelativistic estimate is appropriate. At accelerating voltages approaching the electron's rest-energy scale ($m_ec^2/e\simeq511\,\mathrm{kV}$), a relativistic treatment is essential.

### Example 3: Photon count in monochromatic radiation (Chapter 42)

**Problem.** A source outputs $1.0\,\mathrm{mW}$ of $500\,\mathrm{nm}$ light. Estimate photons emitted per second.

**Solution.** Each photon has $E=hc/\lambda$:

$$
E_\gamma=\frac{(6.626\times10^{-34})(2.998\times10^8)}{500\times10^{-9}}
\simeq3.97\times10^{-19}\ \mathrm J.
$$

Therefore

$$
\dot N=\frac P{E_\gamma}=\frac{1.0\times10^{-3}}{3.97\times10^{-19}}
\simeq\boxed{2.52\times10^{15}\ \mathrm{s^{-1}}}.
$$

Doubling optical power at the same wavelength doubles the photon arrival rate, not the energy per photon.

### Example 4: Photoelectric threshold and stopping voltage (Chapter 42)

**Problem.** A metal has work function $2.2\,\mathrm{eV}$. Light of wavelength $400\,\mathrm{nm}$ strikes it. Find $K_{\max}$ and stopping potential magnitude.

**Solution.** Using $hc=1240\,\mathrm{eV\,nm}$,

$$
E_\gamma=\frac{1240}{400}\ \mathrm{eV}=3.10\,\mathrm{eV},
$$

$$
K_{\max}=3.10-2.20=\boxed{0.90\ \mathrm{eV}}.
$$

Since $eV_s=K_{\max}$, the stopping-voltage magnitude is $\boxed{V_s=0.90\ \mathrm V}$. At fixed wavelength, increasing intensity raises the current ceiling but not this ideal stopping voltage.

### Example 5: De Broglie wavelength of an accelerated electron (Chapter 42)

**Problem.** Find the wavelength of an electron accelerated from rest through $150\,\mathrm V$.

**Solution.** Apply the low-energy electron relation:

$$
\lambda=\frac{1.227\ \mathrm{nm}}{\sqrt{150}}
\simeq\boxed{0.100\ \mathrm{nm}}.
$$

This is comparable to atomic lattice spacing, which is why electron diffraction is experimentally accessible. The formula presupposes an electron accelerated nonrelativistically and negligible energy loss.

### Example 6: Hydrogen transition wavelength (Chapter 43)

**Problem.** Determine the photon wavelength emitted in hydrogen during $n=3\rightarrow n=2$.

**Solution.** The positive energy released is

$$
\Delta E=13.6\left(\frac1{2^2}-\frac1{3^2}\right)\mathrm{eV}
=13.6\left(\frac5{36}\right)\mathrm{eV}
\simeq1.889\,\mathrm{eV}.
$$

Thus

$$
\lambda=\frac{1240\ \mathrm{eV\,nm}}{1.889\ \mathrm{eV}}
\simeq\boxed{656\ \mathrm{nm}}.
$$

This line is in the Balmer series; the emitted photon's energy is the *difference* between levels, not the magnitude of either level individually.

### Example 7: Hydrogen-like ion binding scale (Chapter 43)

**Problem.** In the elementary fixed-nucleus Bohr model, estimate ground-state energy and radius for a hydrogen-like ion with $Z=2$.

**Solution.** Put $n=1$ and $Z=2$ into the hydrogen-like formulas:

$$
E_1=-\frac{13.6(2)^2}{1^2}=\boxed{-54.4\ \mathrm{eV}},
$$

$$
r_1=\frac{a_0}{2}=\frac{0.0529}{2}\,\mathrm{nm}
=\boxed{0.0265\ \mathrm{nm}}.
$$

Increasing $Z$ deepens the Coulomb energy and contracts the length scale for a one-electron ion. A neutral helium atom has two electrons and cannot be modeled with these same single-electron formulas.

### Example 8: Radial probability versus spatial density (Chapter 43)

**Problem.** The hydrogen ground-state wavefunction is $\psi_{100}=e^{-r/a_0}/\sqrt{\pi a_0^3}$. Determine the most probable *radial distance*.

**Solution.** The radial shell probability is proportional to $r^2e^{-2r/a_0}$. Differentiate:

$$
\frac d{dr}\left(r^2e^{-2r/a_0}\right)
=e^{-2r/a_0}\left(2r-\frac{2r^2}{a_0}\right).
$$

Stationary points occur at $r=0$ and $r=a_0$. Because radial probability vanishes at $r=0$, rises to a peak, and decays for large $r$, the nonzero peak is

$$
\boxed{r_{\mathrm{most\ probable}}=a_0.}
$$

The *pointwise density* $|\psi|^2$ is largest at the origin, but the *probability in a thin spherical shell* is not.

### Example 9: Laser transition energy (Chapter 43)

**Problem.** A laser's dominant output wavelength is $632.8\,\mathrm{nm}$. Estimate the energy gap in eV.

**Solution.** Use $\Delta E=hc/\lambda$:

$$
\Delta E\simeq\frac{1240}{632.8}\,\mathrm{eV}
\simeq\boxed{1.96\ \mathrm{eV}}.
$$

This is the optical transition energy per photon, not a statement that the laser's total stored energy is only a few electronvolts.

### Example 10: Minimum wavelength of tube X-rays (Chapter 44)

**Problem.** Electrons reach an X-ray target with acceleration voltage $50\,\mathrm{kV}$. Find $\lambda_{\min}$.

**Solution.** In electronvolt units, maximum photon energy is $50{,}000\,\mathrm{eV}$. Thus

$$
\lambda_{\min}=\frac{1240\ \mathrm{eV\,nm}}{50{,}000\ \mathrm{eV}}
=\boxed{0.0248\ \mathrm{nm}}.
$$

Raising filament current without changing voltage can intensify the spectrum but does not change this ideal cutoff.

### Example 11: Bragg spacing from diffraction angle (Chapter 44)

**Problem.** First-order X-ray diffraction is observed at a grazing angle of $30^\circ$ using $0.154\,\mathrm{nm}$ radiation. Calculate the plane spacing.

**Solution.** Bragg's law gives

$$
d=\frac{n\lambda}{2\sin\theta}
=\frac{(1)(0.154\,\mathrm{nm})}{2\sin30^\circ}
=\boxed{0.154\ \mathrm{nm}}.
$$

If the given angle were measured from the normal instead, first convert it to the Bragg grazing angle.

### Example 12: Relative characteristic X-ray frequencies (Chapter 44)

**Problem.** Assume a particular characteristic series follows $\sqrt\nu=a(Z-1)$. Estimate the frequency ratio for elements with $Z=30$ and $Z=20$.

**Solution.** Square the relation and take the ratio:

$$
\frac{\nu_{30}}{\nu_{20}}
=\left(\frac{30-1}{20-1}\right)^2
=\frac{841}{361}
\simeq\boxed{2.33}.
$$

The result depends on using the same spectral series and effective-screening approximation for both elements.

### Example 13: Conductivity with two carrier species (Chapter 45)

**Problem.** In a sample, $n=10^{21}\,\mathrm{m^{-3}}$, $p=10^{15}\,\mathrm{m^{-3}}$, $\mu_e=0.14\,\mathrm{m^2/(V\,s)}$, and $\mu_h=0.05\,\mathrm{m^2/(V\,s)}$. Estimate conductivity.

**Solution.** Use

$$
\sigma=e(n\mu_e+p\mu_h).
$$

Substitution yields

$$
\sigma=(1.602\times10^{-19})\left[(10^{21})(0.14)+(10^{15})(0.05)\right]
\simeq\boxed{22.4\ \mathrm{S/m}}.
$$

The hole contribution is tiny for the specified populations; it would be incorrect to omit it merely because holes are not physical protons.

### Example 14: Equilibrium minority carrier density (Chapter 45)

**Problem.** A nondegenerate, equilibrium n-type semiconductor has $n_i=10^{16}\,\mathrm{m^{-3}}$ and $n=10^{21}\,\mathrm{m^{-3}}$. Find $p$.

**Solution.** Under the equilibrium mass-action relation,

$$
p=\frac{n_i^2}{n}
=\frac{(10^{16})^2}{10^{21}}
=\boxed{10^{11}\ \mathrm{m^{-3}}}.
$$

This result must not be carried over unchanged into strong optical illumination or injected-current conditions where the system is not in thermal equilibrium.

### Example 15: Ideal rectifier averages (Chapter 45)

**Problem.** An ideal diode rectifier is fed with a $12\,\mathrm V$ peak sinusoid. Find the mean output for ideal half-wave and full-wave rectification.

**Solution.** The cycle averages are

$$
\overline V_{\mathrm{half}}=\frac{V_m}{\pi}
=\boxed{3.82\ \mathrm V},
$$

$$
\overline V_{\mathrm{full}}=\frac{2V_m}{\pi}
=\boxed{7.64\ \mathrm V}.
$$

These are averages of **pulsating, unfiltered** waveforms, not DC outputs of a smoothed practical supply with a filter capacitor.

### Example 16: Transistor current bookkeeping (Chapter 45)

**Problem.** A BJT has collector current $I_C=3.0\,\mathrm{mA}$ and current gain $\beta=100$ in its operating region. Find base and emitter currents.

**Solution.** Apply $I_C=\beta I_B$:

$$
I_B=\frac{I_C}{\beta}=\frac{3.0\,\mathrm{mA}}{100}
=\boxed{30\ \mathrm{\mu A}}.
$$

KCL at the device gives

$$
I_E=I_C+I_B=\boxed{3.03\ \mathrm{mA}}.
$$

The collector current is controlled through the transistor's carrier transport; the collector supply supplies the output energy.

### Example 17: Nuclear radius scaling (Chapter 46)

**Problem.** Using $r_0=1.2\,\mathrm{fm}$, estimate the nuclear radius for $A=56$.

**Solution.** The empirical scaling gives

$$
R=1.2(56)^{1/3}\,\mathrm{fm}
\simeq\boxed{4.59\ \mathrm{fm}}.
$$

If $A$ increased by a factor of $8$, the approximate radius would double because $(8A)^{1/3}=2A^{1/3}$.

### Example 18: Binding energy from mass defect (Chapter 46)

**Problem.** A nucleus has mass defect $\Delta m=0.0300\,\mathrm u$ relative to separated constituent nucleons. Find its binding energy.

**Solution.** Convert mass defect to energy:

$$
B=\Delta mc^2=(0.0300)(931.5\,\mathrm{MeV})
=\boxed{27.9\ \mathrm{MeV}}.
$$

If the nucleus has $A=4$, its average binding energy is $B/A\simeq6.99\,\mathrm{MeV/nucleon}$. The binding energy is not the same quantity as the nucleus's total rest energy.

### Example 19: Activity after several half-lives (Chapter 46)

**Problem.** A sample initially has activity $800\,\mathrm{Bq}$. What activity remains after three half-lives?

**Solution.** The activity falls with the same exponential factor as the surviving population:

$$
\mathcal A=\mathcal A_0\left(\frac12\right)^3
=\frac{800}{8}
=\boxed{100\ \mathrm{Bq}}.
$$

The initial number of radioactive nuclei is not required because the half-life determines the ratio directly.

### Example 20: Alpha-decay bookkeeping (Chapter 46)

**Problem.** An unspecified nuclide $^{210}_{84}X$ alpha decays. Find daughter mass and atomic numbers.

**Solution.** An emitted alpha particle contains two protons and two neutrons:

$$
{}^{210}_{84}X\rightarrow{}^{206}_{82}Y+{}^4_2\mathrm{He}.
$$

Thus $\boxed{A_d=206,\ Z_d=82}$. Check both conservation statements: $210=206+4$ and $84=82+2$.

### Example 21: Energy per mole of idealized fission events (Chapter 46)

**Problem.** Suppose each of one mole of nuclei undergoes a fission process releasing $200\,\mathrm{MeV}$ per event. Estimate total released energy.

**Solution.** Convert the energy of one event:

$$
Q=200\times10^6(1.602\times10^{-19})\ \mathrm J
=3.204\times10^{-11}\ \mathrm J.
$$

For $N_A=6.022\times10^{23}$ events,

$$
E_{\mathrm{total}}=N_AQ
\simeq\boxed{1.93\times10^{13}\ \mathrm J}.
$$

This ideal total is not a prediction of usable electrical output; conversion efficiency, losses, and the exact reaction mix must be considered separately.

### Example 22: Time dilation at $0.8c$ (Chapter 47)

**Problem.** A clock moves at $v=0.8c$ relative to a laboratory, and the lab observes a $10\,\mathrm s$ time interval between two ticks located at the same place in the clock's rest frame. Find the elapsed time read by the moving clock.

**Solution.** Compute

$$
\gamma=\frac1{\sqrt{1-0.8^2}}=\frac53.
$$

Since $\Delta t=\gamma\Delta\tau$,

$$
\Delta\tau=\frac{10}{5/3}=\boxed{6.0\ \mathrm s}.
$$

The answer is a comparison of different frame measurements for a defined pair of events; the traveler does not experience its own clock as defective.

### Example 23: Length contraction at $0.8c$ (Chapter 47)

**Problem.** A spacecraft has proper length $L_0=100\,\mathrm m$ and moves parallel to its length at $0.8c$. Find length measured by a stationary observer.

**Solution.** Using $\gamma=5/3$,

$$
L=\frac{L_0}{\gamma}
=\frac{100}{5/3}
=\boxed{60\ \mathrm m}.
$$

A dimension measured perpendicular to motion would remain unchanged in the standard configuration.

### Example 24: Relativistic kinetic energy (Chapter 47)

**Problem.** A particle with rest energy $m_0c^2=2.0\,\mathrm{MeV}$ moves at $0.8c$. Determine total and kinetic energies.

**Solution.** With $\gamma=5/3$,

$$
E=\gamma m_0c^2=\frac53(2.0)=\boxed{3.33\ \mathrm{MeV}},
$$

$$
K=(\gamma-1)m_0c^2
=\left(\frac53-1\right)(2.0)
=\boxed{1.33\ \mathrm{MeV}}.
$$

The Newtonian formula $\tfrac12m_0v^2$ would give $0.64\,\mathrm{MeV}$ and substantially underestimates the relativistic value.

### Example 25: Relativistic velocity addition (Chapter 47)

**Problem.** A light pulse moves at $u_x=c$ in frame $S$. Another observer's frame $S'$ moves at $v=0.6c$ along the same axis. Find $u'_x$.

**Solution.** Apply relativistic addition:

$$
u'_x=\frac{c-0.6c}{1-(c)(0.6c)/c^2}
=\frac{0.4c}{0.4}
=\boxed{c}.
$$

Direct Galilean subtraction would have given $0.4c$, violating the invariance postulate.

### Example 26: Twin journey and proper time (Chapter 47)

**Problem.** A traveler journeys outward for $10$ Earth-frame years at $0.8c$ and returns over another $10$ Earth-frame years at the same speed. Assume negligibly brief turnaround. How much does each twin age?

**Solution.** The Earth-frame twin experiences $\Delta t=20\,\mathrm{yr}$. Each travel leg has factor $1/\gamma=0.6$:

$$
\Delta\tau_{\mathrm{traveler}}
=(10)(0.6)+(10)(0.6)
=\boxed{12\ \mathrm{yr}}.
$$

Hence the reunited travelers differ in accumulated time by $\boxed{8\ \mathrm{yr}}$. The essential physics is the difference between their worldlines, not an arbitrary preference for one observer's point of view.

---
# Consolidated Formula Sheet

This is a lookup sheet for **revision after derivation**, not a substitute for deciding which physical model applies.

## A. Electron beams, light, and matter waves (Chapters 41–42)

| Quantity/model | Relationship | Applicability |
|---|---|---|
| Electron force | $\vec F=-e(\vec E+\vec v\times\vec B)$ | Classical electron beam with electromagnetic fields |
| Energy from accelerating voltage | $K=eV$ | Electron accelerated from rest through $V$, neglecting losses |
| Nonrelativistic electron speed | $v=\sqrt{2eV/m_e}$ | $eV\ll m_ec^2$ |
| Crossed-field velocity selection | $v=E/B$ | Perpendicular fields with opposing transverse forces |
| Circular-beam charge/mass ratio | $e/m_e=v/(Br)$ | Beam perpendicular to uniform $\vec B$ |
| Photon energy | $E_\gamma=h\nu=hc/\lambda$ | Wavelength in vacuum when using $c$ |
| Photon momentum | $p_\gamma=E_\gamma/c=h/\lambda$ | Photon in vacuum |
| Photoelectric maximum energy | $K_{\max}=h\nu-\phi$ | Basic one-photon process, above threshold |
| Threshold frequency | $\nu_0=\phi/h$ | Given emitting surface |
| Threshold wavelength | $\lambda_0=hc/\phi$ | Above this wavelength, no ideal one-photon emission |
| Stopping potential | $eV_s=K_{\max}$ | $V_s$ is magnitude of retarding potential |
| Matter wavelength | $\lambda=h/p$ | Momentum may be relativistic |
| Nonrelativistic matter wavelength | $\lambda=h/\sqrt{2mK}$ | $K\ll mc^2$ |
| Voltage-to-wavelength for electrons | $\lambda=1.227\,\mathrm{nm}/\sqrt{V/(1\,\mathrm V)}$ | Nonrelativistic electron from rest |

## B. Atomic physics (Chapter 43)

| Quantity/model | Relationship | Applicability |
|---|---|---|
| Bohr angular momentum | $m_evr=n\hbar$ | One-electron ideal Bohr model |
| Bohr radius scale | $a_0\simeq0.0529\,\mathrm{nm}$ | Hydrogen with effectively fixed nucleus |
| Hydrogen-like orbit radius | $r_n=a_0n^2/Z$ | Elementary Bohr model |
| Hydrogen-like energy | $E_n\simeq-13.6Z^2/n^2\,\mathrm{eV}$ | Gross Coulomb energies, single electron |
| Photon in atomic transition | $h\nu=E_i-E_f$ | Downward emission, $E_i>E_f$ |
| Rydberg wavelength law | $1/\lambda=R_H(1/n_f^2-1/n_i^2)$ | Hydrogen emission series |
| Schrödinger stationary equation | $[-\hbar^2\nabla^2/(2m_e)+U]\psi=E\psi$ | Nonrelativistic one-electron model |
| Spatial Born rule | $dP=|\psi|^2d^3r$ | Normalized state |
| Radial probability for spherically symmetric state | $P(r)dr=4\pi r^2|\psi(r)|^2dr$ | Spherical spatial probability density |
| Quantum numbers | $n\ge1,\ 0\le\ell\le n-1,\ -\ell\le m_\ell\le\ell$ | Hydrogen-like orbitals |
| Shell-state counting (with spin) | $2n^2$ | Available independent-electron quantum states in a shell |
| Laser transition | $\Delta E=h\nu$ | Optical transition supporting emission |

## C. X-rays (Chapter 44)

| Quantity/model | Relationship | Applicability |
|---|---|---|
| Maximum tube photon energy | $E_{\gamma,\max}=eV_a$ | Elementary acceleration model |
| Continuous X-ray cutoff | $\lambda_{\min}=hc/(eV_a)$ | Duane–Hunt relation |
| Bragg maxima | $2d\sin\theta=n\lambda$ | $\theta$ measured to crystal planes |
| Moseley relation | $\sqrt\nu=a(Z-b)$ | Given characteristic X-ray series, screening approximation |
| Ideal beam attenuation | $I=I_0e^{-\mu x}$ | Narrow monoenergetic beam, uniform material |

## D. Semiconductor devices (Chapter 45)

| Quantity/model | Relationship | Applicability |
|---|---|---|
| Drift conductivity | $\sigma=e(n\mu_e+p\mu_h)$ | Low-field electron/hole drift |
| Intrinsic carrier equality | $n=p=n_i$ | Pure semiconductor at equilibrium |
| Mass-action relation | $np=n_i^2$ | Nondegenerate thermal equilibrium |
| Ideal diode current | $I=I_s[\exp(eV_D/(\eta k_BT))-1]$ | Approximate junction model |
| Half-wave mean rectification | $\overline V=V_m/\pi$ | Ideal diode, unfiltered sinusoidal input |
| Full-wave mean rectification | $\overline V=2V_m/\pi$ | Ideal full-wave rectified sine |
| Transistor terminal currents | $I_E=I_C+I_B$ | BJT conventional currents |
| Common-emitter gain relation | $\beta=I_C/I_B$ | At specified operating region |
| Common-base gain relation | $\alpha=I_C/I_E$ | At specified operating region |
| Relation of BJT gains | $\beta=\alpha/(1-\alpha)$ | Compatible definitions |

## E. Nuclear physics (Chapter 46)

| Quantity/model | Relationship | Applicability |
|---|---|---|
| Nuclear composition | $A=Z+N$ | Mass/proton/neutron numbering |
| Radius scaling | $R\approx r_0A^{1/3}$ | Empirical nuclear radius scale |
| Mass defect | $\Delta m=Zm_p+Nm_n-m_{\mathrm{nucleus}}$ | Consistent **nuclear** masses |
| Binding energy | $B=\Delta mc^2$ | Bound versus separated nucleons |
| Reaction energy | $Q=(m_i-m_f)c^2$ | Consistent reactant/product masses |
| Radioactive population | $N=N_0e^{-\lambda t}$ | Constant decay probability per unit time |
| Activity | $\mathcal A=\lambda N$ | Expected decays per second |
| Half-life | $T_{1/2}=\ln2/\lambda$ | Exponential radioactive decay |
| Mean lifetime | $\tau=1/\lambda$ | Exponential waiting-time distribution |
| After $n$ half-lives | $N/N_0=2^{-n}$ | Exponential radioactive decay |
| Mass unit conversion | $1\,\mathrm u\,c^2\simeq931.5\,\mathrm{MeV}$ | Atomic/nuclear mass–energy conversion |

## F. Special relativity (Chapter 47)

| Quantity/model | Relationship | Applicability |
|---|---|---|
| Lorentz factor | $\gamma=(1-v^2/c^2)^{-1/2}$ | Relative inertial-frame speed $|v|<c$ |
| Time dilation | $\Delta t=\gamma\Delta\tau$ | Events at one location in clock's rest frame |
| Parallel length contraction | $L=L_0/\gamma$ | Object moving along measured direction |
| Standard Lorentz transform | $x'=\gamma(x-vt)$; $t'=\gamma(t-vx/c^2)$ | Collinear standard frames |
| Relativistic momentum | $\vec p=\gamma m_0\vec v$ | Massive particle |
| Total energy | $E=\gamma m_0c^2$ | Massive particle |
| Rest energy | $E_0=m_0c^2$ | Invariant rest mass |
| Kinetic energy | $K=(\gamma-1)m_0c^2$ | Massive particle |
| Energy–momentum identity | $E^2=p^2c^2+m_0^2c^4$ | Free particle |
| Photon limit | $E=pc$ | Zero-rest-mass photon in vacuum |
| Longitudinal velocity addition | $u'_x=(u_x-v)/(1-u_xv/c^2)$ | Collinear velocities |
| Proper time on a trajectory | $d\tau=dt\sqrt{1-v^2/c^2}$ | Timelike worldline in chosen inertial frame |

## G. Constants and unit conversions

| Quantity | Common revision value |
|---|---|
| Planck constant $h$ | $6.62607015\times10^{-34}\ \mathrm{J\,s}$ (exact SI value) |
| Reduced Planck constant $\hbar$ | $h/(2\pi)$ |
| Vacuum light speed $c$ | $299\,792\,458\ \mathrm{m/s}$ (exact SI value) |
| Elementary charge magnitude $e$ | $1.602176634\times10^{-19}\ \mathrm C$ (exact SI value) |
| Electron rest mass $m_e$ | $9.109\times10^{-31}\ \mathrm{kg}$ (approx.) |
| Electron rest energy $m_ec^2$ | $511\ \mathrm{keV}$ (approx.) |
| Boltzmann constant $k_B$ | $1.380649\times10^{-23}\ \mathrm{J/K}$ (exact SI value) |
| $1\,\mathrm{eV}$ | $1.602176634\times10^{-19}\ \mathrm J$ |
| $1\,\mathrm{MeV}$ | $10^6\,\mathrm{eV}$ |
| $1\,\mathrm{fm}$ | $10^{-15}\,\mathrm m$ |
| $1\,\mathrm{nm}$ | $10^{-9}\,\mathrm m$ |
| $1\,\mathrm u\,c^2$ | $931.5\,\mathrm{MeV}$ (approx.) |
| $hc$ | $1240\,\mathrm{eV\,nm}$ (approx.) |
| $1\,\mathrm{Bq}$ | $1$ radioactive disintegration per second |

---

# Common Misconceptions and Diagnostic Checks

### Chapter 41: Electric Current through Gases

1. **"A gas has no charge carriers."** Usually it has few; ionization and recombination control the actual population.
2. **"Canal rays are protons in every discharge tube."** Positive ions reflect the composition and charge states of the gas.
3. **"Cathode rays are light waves."** The cathode-ray beam consists of electrons, even though collisions produce visible glow and fluorescence.
4. **"Thomson directly weighed one electron."** The classical beam experiment determines charge-to-mass magnitude; charge determination is a distinct measurement.
5. **"A vacuum diode and semiconductor diode have the same microscopic mechanism."** The first depends on emitted electrons crossing a vacuum; the second on carrier motion through a junction.
6. **"A triode creates electrical power."** It modulates energy taken from a power source; bias and operating region matter.

### Chapter 42: Photoelectric Effect and Wave–Particle Duality

7. **"More intense light always produces faster photoelectrons."** At fixed above-threshold frequency, intensity chiefly changes photoelectron number/current, not $K_{\max}$.
8. **"Red light of arbitrary intensity can eject electrons from any metal."** The basic one-photon effect requires $h\nu\ge\phi$.
9. **"Stopping potential is the surface's work function expressed in volts."** It represents maximum emitted kinetic energy divided by $e$ and depends on photon frequency.
10. **"Photon momentum requires a nonzero rest mass."** Massless photons have $p=E/c$.
11. **"An electron literally oscillates on a stretched medium because it has a wavelength."** De Broglie wavelength characterizes quantum phase and momentum, not a classical material ripple.
12. **"$\lambda=h/(mv)$ is exact at all particle speeds."** The universal form is $\lambda=h/p$; relativistic momentum differs from $mv$.

### Chapter 43: Atomic Physics

13. **"Rutherford's nuclear model fully explains atomic stability."** Classical orbiting electrons would radiate, contradicting stable atoms.
14. **"Bohr's allowed orbit is a visible planetary trajectory proven by spectroscopy."** Bohr is an effective historical model; quantum mechanics uses stationary wavefunctions.
15. **"The Rydberg integer is the photon number."** The integers label principal energy levels of the atom.
16. **"The more negative an atomic energy, the easier the ionization."** Relative to zero at separation, a more negative bound energy requires greater energy to remove the electron.
17. **"$|\psi(r)|^2$ alone is the radial probability density."** A spherical-shell radial distribution requires the geometrical factor $4\pi r^2$ for a spherically symmetric state.
18. **"A laser is bright only because every photon has high energy."** High power and tight beam area can occur with ordinary visible photon energies; pumping sustains the population inversion.

### Chapter 44: X-rays

19. **"X-rays are fast-moving electrons."** They are electromagnetic photons, commonly created by electron impacts.
20. **"Tube voltage changes only X-ray intensity."** It also changes the continuous-spectrum short-wavelength cutoff.
21. **"The filament current sets the maximum X-ray photon energy."** Filament current mainly controls electron supply; acceleration voltage sets the elementary energy limit.
22. **"Characteristic X-ray lines have the same energies for all targets."** Their energies depend on the target's electron binding structure and atomic number.
23. **"Bragg's angle is always the angle to the plane normal."** In the common $2d\sin\theta=n\lambda$ geometry, $\theta$ is measured to the reflecting plane.
24. **"Stronger X-rays automatically mean better and safer imaging."** Energy, attenuation, contrast, and ionizing dose introduce competing trade-offs.

### Chapter 45: Semiconductors

25. **"A hole is a free positively charged nucleus traveling through silicon."** It is an effective positive mobile vacancy in occupied electronic states.
26. **"An n-type semiconductor must have net negative electric charge."** Bulk material can remain neutral while electrons are majority carriers.
27. **"Band gap is the same as the total energy of any conduction electron."** It is a separation between energy-band edges.
28. **"The depletion region contains literally no electric charge."** It contains relatively few mobile carriers but includes fixed ionized dopants and an internal field.
29. **"An ordinary silicon diode conducts nothing below exactly $0.700\,\mathrm V$."** Real I–V characteristics are continuous, strongly current- and temperature-dependent.
30. **"The collector current is exactly $\beta$ times base current for every operating condition."** BJT gain is dependent on bias, device, temperature, and region.
31. **"Boolean $A+B$ always means ordinary arithmetic addition."** In a logic table it represents OR; $1\lor1=1$.
32. **"A transistor is simply two independent p–n diodes."** The thin base and coupled carrier transport create transistor action.

### Chapter 46: The Nucleus

33. **"Atomic mass number $A$ equals nuclear mass in kilograms or atomic mass units exactly."** $A$ is an integer count of nucleons; actual mass reflects binding and particle masses.
34. **"Radioactivity means a nucleus has an exact scheduled decay time."** Exponential decay is a probability law, not a deterministic clock for each nucleus.
35. **"Binding energy is stored positive potential energy in the same sense as separated charges."** Binding energy is the positive energy required to unbind the system; the bound state has lower total energy.
36. **"Alpha, beta, and gamma emissions all change both $A$ and $Z$."** Their effects on nuclide composition are different.
37. **"A radioactive source with twice the activity must deliver twice the dose in every situation."** Dose depends on radiation type, energy, exposure geometry, and absorption.
38. **"Critical reactor means an explosive runaway state."** Criticality describes a self-sustaining neutron chain reaction; thermal and reactivity control are separate questions.
39. **"Fusion generates energy without any confinement or collision limitations."** Coulomb repulsion, tunneling, plasma losses, and reaction rates determine practical feasibility.

### Chapter 47: Special Relativity

40. **"Relativity says everything is subjective and no quantities are invariant."** Proper time, rest mass, and the spacetime interval are invariant under suitable transformations.
41. **"A moving clock looks slower only because its light takes longer to reach me."** Time dilation compares corrected operational measurements of event times, independent of optical propagation delay.
42. **"Every dimension of a moving object contracts."** Only components parallel to relative motion contract in the standard setup.
43. **"Simultaneous in one inertial frame means simultaneous in all."** Spacelike-separated event simultaneity is frame dependent.
44. **"Mass must grow with speed as a fundamental change in the particle's invariant mass."** Invariant rest mass remains fixed; the older 'relativistic mass' convention folds $\gamma$ into a mass-like symbol.
45. **"If I chase a light pulse at half the speed of light, I measure the pulse at half $c$."** The correct relativistic velocity law preserves $c$.
46. **"The traveling twin ages less solely because acceleration directly slows biological chemistry."** The aging difference is the accumulated proper-time difference along different worldlines.

---
# Active-Recall Questions

Attempt these **without consulting the formulas**. For derivations, state the assumptions and define each measured frame or coordinate before writing the equations.

### Chapter 41: Electric Current through Gases

1. Explain why a neutral gas ordinarily carries far less current than a metal at the same field strength.
2. Describe how collisions and cathode secondary emission sustain a discharge.
3. What is the experimental meaning of sparking potential, and which variables enter Paschen's law?
4. Distinguish the positive column, cathode glow, Crookes dark space, and Faraday dark space.
5. List three observations proving cathode rays behave as negatively charged particles.
6. Why does a cathode-ray beam bend more strongly than a heavy positive-ion beam under comparable conditions?
7. How does a perforated cathode help demonstrate canal rays?
8. Why are canal rays not always made of protons?
9. Derive the velocity-selector relation $v=E/B$ and specify necessary orientations.
10. Derive $e/m_e=v/(Br)$ from magnetic circular motion.
11. Explain why separate determinations of electron charge and charge-to-mass ratio are needed for electron mass.
12. Distinguish thermionic emission from the photoelectric effect.
13. How does the anode potential change conduction in a heated-cathode diode valve?
14. Explain how a triode amplifies a small grid signal without generating electrical energy from nothing.

### Chapter 42: Photoelectric Effect and Wave–Particle Duality

15. State the energy and momentum relations for a photon and define their units.
16. Explain why fixed-frequency optical intensity is related to photon flux rather than photon energy.
17. Define work function, threshold wavelength, and threshold frequency.
18. Derive Einstein's photoelectric equation using an energy balance at the emitting surface.
19. Why do some photoelectrons emerge with less than the maximum kinetic energy?
20. Explain saturation photocurrent in an illuminated vacuum photocell.
21. Derive the stopping-potential relation and predict the slope of $V_s$ versus frequency.
22. Why does making a below-threshold beam brighter fail in the elementary one-photon model?
23. State de Broglie's wavelength relation and explain why it applies to electrons and macroscopic objects.
24. Derive the nonrelativistic electron de Broglie wavelength after acceleration through potential $V$.
25. Why is electron diffraction by crystals evidence of matter-wave behavior?
26. At large particle speed, which momentum relation should replace $p=mv$ in the de Broglie formula?

### Chapter 43: Bohr's Model and Physics of the Atom

27. Compare Thomson's diffuse-charge atom with Rutherford's nuclear atom.
28. Why did large-angle alpha scattering imply a concentrated nuclear charge?
29. Explain two failures of a purely classical Rutherford-style orbiting-electron model.
30. Write the Rydberg formula and identify initial and final principal quantum numbers.
31. Distinguish the Lyman, Balmer, and Paschen series by their final levels.
32. State Bohr's postulates and identify which postulate has no classical justification.
33. Starting from Coulomb attraction and angular-momentum quantization, derive $r_n\propto n^2/Z$.
34. Derive $E_n\propto-Z^2/n^2$ for a single-electron hydrogen-like atom.
35. Explain the negative sign of bound-electron energy and the positive ionization energy.
36. Why does Bohr's elementary spectrum succeed for hydrogen while failing as a complete quantum theory?
37. Distinguish a complex probability amplitude from a nonnegative probability density.
38. State the normalization condition for a one-electron spatial wavefunction.
39. Write the time-independent Schrödinger equation for an electron in a Coulomb field.
40. Give the allowed ranges of $n$, $\ell$, and $m_\ell$.
41. Why does the number of orbital states for fixed $n$ sum to $n^2$?
42. Explain how electron spin changes the shell-state count to $2n^2$.
43. Distinguish pointwise $|\psi|^2$ from radial shell probability in the $1s$ hydrogen state.
44. Derive the location of the maximum of the hydrogen $1s$ radial probability distribution.
45. Explain absorption, spontaneous emission, and stimulated emission using two atomic energy levels.
46. Why are population inversion, pumping, and feedback important in laser operation?

### Chapter 44: X-rays

47. Describe the roles of cathode, accelerating voltage, and target in a conventional X-ray tube.
48. What is bremsstrahlung, and why does it produce a continuous spectrum?
49. Derive the Duane–Hunt minimum-wavelength relation.
50. Distinguish continuous X-ray radiation from characteristic X-ray lines.
51. How does a K-shell vacancy lead to $K_\alpha$ emission?
52. Why do characteristic line frequencies depend strongly on target atomic number?
53. Explain why increasing tube voltage affects hardness and the spectral cutoff.
54. Explain why increasing filament current chiefly affects radiation intensity in the elementary tube model.
55. State Moseley's law and derive its scaling from an effective nuclear charge.
56. Explain the historical role of Moseley's experiments in establishing atomic number as the periodic-table ordering variable.
57. Derive Bragg's condition from path difference between crystal planes and define the diffraction angle.
58. State two important uses and two hazards or limitations associated with X-ray interactions with matter.

### Chapter 45: Semiconductors and Semiconductor Devices

59. Describe how discrete atomic electron levels broaden into energy bands when atoms form a solid.
60. Explain how available unoccupied states distinguish a metal from an ordinary insulator.
61. Define the valence band, conduction band, and band gap.
62. Why can increasing temperature raise intrinsic semiconductor conductivity while raising metallic resistivity?
63. Describe electron–hole pair generation without claiming a hole is a proton.
64. Distinguish intrinsic, n-type, and p-type material in terms of majority carriers.
65. What charge is left behind by an ionized donor or acceptor atom?
66. Derive $\sigma=e(n\mu_e+p\mu_h)$, including drift directions and charge signs.
67. When is the relation $np=n_i^2$ appropriate?
68. Explain formation of the depletion region and built-in field at a p–n junction.
69. Contrast forward and reverse bias with reference to the junction barrier.
70. Why does a simple diode I–V curve not have an exact universal $0.7\,\mathrm V$ threshold?
71. Sketch a half-wave rectified sine and derive its average value.
72. Sketch a full-wave rectified sine and derive its average value.
73. Explain why a smoothing capacitor changes the behavior of a rectifier output.
74. Define emitter, base, and collector in an $npn$ transistor and describe normal active biasing.
75. Derive $I_E=I_C+I_B$ and the relation between $\alpha$ and $\beta$.
76. Construct truth tables for AND, OR, NOT, and NAND; explain the meaning of logical voltage levels.

### Chapter 46: The Nucleus

77. Explain nuclide notation, and distinguish isotopes, isotones, and isobars.
78. Derive the roughly constant-density conclusion from $R\propto A^{1/3}$.
79. Describe why the ratio $N/Z$ generally increases along the stable-nuclide region for larger $Z$.
80. Compare the roles of residual strong, electromagnetic, and weak interactions within nuclear physics.
81. Define mass defect, binding energy, and binding energy per nucleon.
82. Derive a binding-energy expression using nuclear masses, and explain the danger of mixing atomic and nuclear masses.
83. Explain qualitatively why the binding-energy-per-nucleon curve allows both fission and fusion energy release.
84. Define nuclear-reaction $Q$-value and explain the meaning of positive and negative signs.
85. Write balanced general equations for alpha, beta-minus, beta-plus, and gamma decay.
86. Why does a beta-decay electron have a continuous energy spectrum?
87. Derive the exponential decay equation starting from $dN/dt=-\lambda N$.
88. Derive $T_{1/2}=\ln2/\lambda$ and compare half-life with mean lifetime.
89. Define activity and distinguish becquerel from absorbed-dose units.
90. Explain why two identical unstable nuclei need not decay at the same instant.
91. Compare penetration, ionization, and shielding trends for alpha, beta, and gamma radiation.
92. Explain neutron-induced fission of $^{235}\mathrm U$ and why fragment masses vary.
93. Distinguish subcritical, critical, and supercritical multiplication using $k_{\mathrm{eff}}$.
94. Why are delayed neutrons significant for the controllability of many fission reactors?
95. Describe the roles of fuel, moderator, neutron absorbers, coolant, and shielding in a basic reactor model.
96. Explain the Coulomb barrier, quantum tunneling, and the confinement challenge for fusion.

### Chapter 47: The Special Theory of Relativity

97. State the two postulates of special relativity and explain their tension with Galilean velocity addition.
98. Derive $c=1/\sqrt{\mu_0\varepsilon_0}$ from the vacuum electromagnetic-wave equations.
99. Write the standard Lorentz transformations for collinear relative inertial motion.
100. Show how the Lorentz transformations approach the Galilean case at $v\ll c$.
101. Derive time dilation from a moving transverse light clock.
102. Define proper time and identify which clock measures it.
103. State length contraction and explain why endpoint measurements must be simultaneous in the measuring frame.
104. Does a rod contract transverse to its motion? State the idealized result and geometry.
105. Use the Lorentz time transformation to show that simultaneity of spatially separated events can change between frames.
106. State relativistic momentum and explain why $\vec F=d\vec p/dt$ is safer than blindly setting $F=m_0a$.
107. Derive relativistic kinetic energy and recover $K\simeq m_0v^2/2$ at low velocity.
108. Verify the invariant relation $E^2=p^2c^2+m_0^2c^4$.
109. Obtain the photon relation $E=pc$ from the zero-rest-mass energy–momentum formula.
110. Derive longitudinal relativistic velocity addition and verify invariance when one speed is $c$.
111. Explain why a massive particle cannot be accelerated to $c$ with finite energy.
112. Explain the twin paradox using proper time accumulated along different worldlines rather than a claim that all frames have absolute time.

---

## Source and scope

**Primary reference:** H. C. Verma, *Concepts of Physics*, **Volume 2**, Chapters **41–47** (textbook pages **341–460**, including examples and exercise sections):

- **41. Electric Current through Gases:** §§41.1–41.8.
- **42. Photoelectric Effect and Wave–Particle Duality:** §§42.1–42.3.
- **43. Bohr's Model and Physics of the Atom:** §§43.1–43.9.
- **44. X-rays:** §§44.1–44.6.
- **45. Semiconductors and Semiconductor Devices:** §§45.1–45.10.
- **46. The Nucleus:** §§46.1–46.11.
- **47. The Special Theory of Relativity:** §§47.1–47.7.

These notes include the **54 numbered theory sections** across the seven chapters and preserve the textbook's conceptual progression. The narrative, **26 worked examples**, misconception checks, and **112 active-recall questions** are independently constructed. Historical treatments are preserved in context; explicitly identified extensions include thermionic and diode emission models, the semiconductor mass-action law and diode equation, selected experimental refinements, the invariant-spacetime interval, and contemporary terminology for rest mass.

**Suggested study method:** First reconstruct the physical experiment or model; next identify the conserved quantities and idealizing assumptions; then derive the equation; finally solve a textbook example and attempt the recall questions without looking. The most important bridges across this unit are photon $E=pc$, atomic state quantization, band-based conduction, nuclear mass defect, and the relativistic energy–momentum identity.

**Volume II conclusion:** Together with Unit 04 (Chapters 23–28) and Unit 05 (Chapters 29–40), this finishes the sequence through **Chapter 47**, the concluding chapter of *Concepts of Physics*.
