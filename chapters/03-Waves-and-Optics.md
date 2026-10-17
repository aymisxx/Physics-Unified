# Unit 03: Waves and Optics

**Wave Motion → Sound Waves → Light Waves → Geometrical Optics → Optical Instruments → Dispersion and Spectra → Speed of Light → Photometry**  
*Original revision notes following Chapters 15–22 of H. C. Verma, Concepts of Physics, Volume 1*

> **Purpose.** Develop the physics of disturbances that propagate, the superposition of waves, the wave and ray descriptions of light, image formation, optical instruments, dispersion, experimental measurements of light speed, and visual photometry. The sequence and section numbering match HCV for cross-referencing, but the explanations, derivations and examples here are independently written notes rather than textbook transcriptions.
>
> **Notation.** All display mathematics uses `$$ ... $$` for GitHub rendering. The wave speed is $v$, temporal frequency is $f$ or $\nu$, angular frequency $\omega$, wavelength $\lambda$, wave number $k$, and wave amplitude $A$. In optics, $n$ or $\mu$ denotes refractive index. When a symbol is reused in another chapter, its meaning is redefined. State sign conventions, approximation regimes, and whether a quantity represents particle motion or wave propagation.

## Roadmap

| Part | HCV chapter | Central ideas |
|---|---|---|
| **I** | **15. Wave Motion and Waves on a String** | Progressive waves, harmonic waves, energy transport, interference, reflection, standing waves, string resonance |
| **II** | **16. Sound Waves** | Longitudinal pressure disturbances, sound speed and intensity, air columns, beats, Doppler effect and acoustics |
| **III** | **17. Light Waves** | Electromagnetic character of light, Huygens' principle, interference, diffraction, resolving power and polarization |
| **IV** | **18. Geometrical Optics** | Reflection, refraction, mirrors, total internal reflection, prisms, lenses and aberrations |
| **V** | **19. Optical Instruments** | Human eye, microscopes, telescopes, magnifying power and resolution |
| **VI** | **20. Dispersion and Spectra** | Chromatic dispersion, prism combinations, spectra, spectrometers and rainbows |
| **VII** | **21. Speed of Light** | Historical measurement principles: Fizeau, Foucault and Michelson |
| **VIII** | **22. Photometry** | Radiant versus luminous flux, visual sensitivity, luminous intensity, illuminance and photometers |

**Learning sequence**

```text
Oscillation + elasticity + energy conservation
                    |
                    v
        Propagating disturbances (Ch. 15)
            /                     \
           v                       v
  Wave kinematics           Superposition / modes
           \                       /
            v                     v
        Longitudinal sound (Ch. 16)
                    |
                    v
          Electromagnetic light (Ch. 17)
            /                      \
           v                        v
   Interference / diffraction    Polarization
            \                      /
             v                    v
              Ray optics (Ch. 18)
                      |
                      v
             Instruments (Ch. 19)
                /               \
               v                 v
       Dispersion (Ch. 20)  Light speed (Ch. 21)
               \                 /
                v               v
                Photometry (Ch. 22)
```

---

# Part I: Wave Motion and Waves on a String

A vibrating body can pass a disturbance to neighboring material, which passes it onward. The disturbance carries energy; the medium generally undergoes local motion instead of travelling with the signal. Waves combine mechanics with the remarkable principle of **superposition**.

## 15.1 Wave Motion

In particle transport, matter itself travels from one place to another. In a mechanical wave, **energy and information move through locally responding matter**. A small segment of a stretched string moves transversely while the wave pattern moves longitudinally along the string. In sound, air molecules execute oscillatory motion even when a pressure pulse travels across a room.

A wave needs a physical mechanism coupling neighboring regions. Elastic forces couple string segments; compression and rarefaction couple fluid parcels. Mechanical waves need a medium; electromagnetic waves can propagate through vacuum.

Two independent velocities must not be confused:

- **Wave speed:** rate of progression of a selected phase or identifiable disturbance.
- **Particle velocity:** local velocity of an element of the medium, obtained by differentiating its displacement at fixed position.

## 15.2 Wave Pulse on a String

If a localized pulse has initial profile $g(x)$ and travels in the positive $x$-direction without distortion at constant speed $v$, its displacement field is

$$
\boxed{y(x,t)=g(x-vt)}.
$$

An equivalent description uses the history $f(t)$ of the disturbance at $x=0$:

$$
\boxed{y(x,t)=f\left(t-\frac{x}{v}\right)}.
$$

To see why, consider the point $x$ at time $t$. The state now arriving at $x$ left the origin an interval $x/v$ earlier. For left-moving disturbances,

$$
\boxed{y(x,t)=g(x+vt)}.
$$

The profile need not be sinusoidal. The traveling-wave condition is that the dependence on $x$ and $t$ occurs through a translating combination such as $x-vt$. For a sufficiently small, nondispersive pulse on an ideal string, shape and propagation speed remain constant.

### Wave equation as a differential equation

For a sufficiently smooth travelling profile $g(x-vt)$,

$$
\frac{\partial^2 y}{\partial t^2}=v^2 g''(x-vt),
\qquad
\frac{\partial^2 y}{\partial x^2}=g''(x-vt).
$$

Hence

$$
\boxed{\frac{\partial^2 y}{\partial t^2}=v^2\frac{\partial^2 y}{\partial x^2}}.
$$

This is the one-dimensional linear wave equation. It admits right- and left-moving profiles and their sums, subject to suitable boundary conditions.

## 15.3 Sine Wave Travelling on a String

A harmonic source produces a sinusoidal wave. A right-moving wave may be written

$$
\boxed{y(x,t)=A\sin(\omega t-kx+\phi_0)}.
$$

The argument of the sine is the **phase**. The definitions are

$$
\omega=2\pi f=\frac{2\pi}{T},
\qquad
k=\frac{2\pi}{\lambda},
\qquad
\boxed{v=\frac{\omega}{k}=f\lambda}.
$$

A surface of constant phase satisfies $\omega t-kx+\phi_0=C$. Differentiating gives $dx/dt=\omega/k$, confirming motion in the positive $x$-direction.

At fixed $x$, a particle oscillates according to SHM. Its transverse velocity and acceleration are

$$
\boxed{v_y=\frac{\partial y}{\partial t}=A\omega\cos(\omega t-kx+\phi_0)},
$$

$$
\boxed{a_y=\frac{\partial^2 y}{\partial t^2}=-\omega^2y}.
$$

Do not substitute $v_y$ for the wave speed $v$. At the maximum displacement of a string element, the element is momentarily at rest even though the wave continues propagating.

## 15.4 Velocity of a Wave on a String

Let an ideal string carry tension $F$ and have uniform mass per unit length $\mu$. For a short element $dx$, the net vertical force from the two tension components, at small slope, is

$$
F_y\simeq F\left[\left.\frac{\partial y}{\partial x}\right|_{x+dx}-\left.\frac{\partial y}{\partial x}\right|_x\right]
=F\frac{\partial^2y}{\partial x^2}dx.
$$

Its mass is $\mu\,dx$. Newton's second law gives

$$
\mu\,dx\frac{\partial^2y}{\partial t^2}=F\frac{\partial^2y}{\partial x^2}dx.
$$

Comparing with the wave equation,

$$
\boxed{v=\sqrt{\frac{F}{\mu}}}.
$$

**Conditions:** string is flexible, tension approximately uniform, deformation small, and transverse slopes small. Greater tension speeds the wave up; greater linear mass density slows it down. The local wave speed is independent of small amplitude.

## 15.5 Power Transmitted along the String by a Sine Wave

A string element receives power from the transverse component of the tension acting at its boundary. For a right-moving wave, the rate of energy transfer through position $x$ is

$$
P(x,t)=-F\frac{\partial y}{\partial x}\frac{\partial y}{\partial t}.
$$

For $y=A\sin(\omega t-kx)$,

$$
\frac{\partial y}{\partial x}=-Ak\cos(\omega t-kx),
\quad
\frac{\partial y}{\partial t}=A\omega\cos(\omega t-kx).
$$

Thus

$$
P(x,t)=FA^2k\omega\cos^2(\omega t-kx).
$$

The cycle-averaged power becomes

$$
\boxed{\langle P\rangle=\frac12\mu v\omega^2A^2}
$$

using $F=\mu v^2$ and $k=\omega/v$. The power grows as the **square of amplitude** and the **square of frequency** for fixed string parameters.

## 15.6 Interference and the Principle of Superposition

If the governing wave equation is linear, the displacement produced by multiple small waves is the algebraic sum:

$$
\boxed{y(x,t)=y_1(x,t)+y_2(x,t)+\cdots}.
$$

Superposition explains constructive interference (same-signed displacements reinforce), destructive interference (opposite displacements partly or fully cancel), and standing-wave patterns.

It does not say that waves permanently change each other when they overlap. Under ideal linear conditions, two pulses pass through their region of overlap and continue with their original forms.

## 15.7 Interference of Waves Going in Same Direction

For equal-frequency waves at the same location,

$$
y_1=A_1\sin\omega t,
\qquad
y_2=A_2\sin(\omega t+\delta),
$$

one can add corresponding sine and cosine components. The resultant amplitude $R$ is

$$
\boxed{R^2=A_1^2+A_2^2+2A_1A_2\cos\delta}.
$$

For equal amplitudes $A$,

$$
\boxed{R=2A\left|\cos\frac\delta2\right|}.
$$

Therefore $\delta=2m\pi$ gives maximum amplitude and $\delta=(2m+1)\pi$ gives cancellation. If coherent sources differ in path by $\Delta x$, their additional phase difference is

$$
\Delta\phi=\frac{2\pi}{\lambda}\Delta x.
$$

Any **initial phase difference** must also be included. Equal frequency and a stable phase relation are essential for a stable interference pattern.

## 15.8 Reflection and Transmission of Waves

At a junction of two strings, wave energy may be split into a reflected pulse and a transmitted pulse. Reflection arises because the two sides respond differently to displacement and tension.

For strings of common tension $F$ with wave speeds $v_1$ and $v_2$, continuity of displacement and transverse force at the junction gives the reflected displacement-amplitude ratio

$$
\boxed{\frac{A_r}{A_i}=\frac{v_2-v_1}{v_2+v_1}},
$$

and transmitted ratio

$$
\boxed{\frac{A_t}{A_i}=\frac{2v_2}{v_1+v_2}}.
$$

An incoming pulse travelling from a light string to a sufficiently heavy string reflects with inverted displacement; a pulse encountering a lighter string can reflect upright.

In the boundary limits, a **fixed end** reflects with phase reversal (displacement amplitude ratio $-1$), while an ideal **free end** reflects without phase reversal ($+1$). The energy-flux balance uses amplitude-squared factors weighted by each string's impedance, not bare squared amplitudes alone.

## 15.9 Standing Waves

When two harmonic waves of equal amplitude and frequency travel in opposite directions, their superposition forms a standing wave:

$$
y_1=A\sin(\omega t-kx),
\qquad
y_2=A\sin(\omega t+kx).
$$

Their sum is

$$
\boxed{y(x,t)=2A\sin(\omega t)\cos(kx)}.
$$

The oscillation amplitude depends on location:

$$
A_{\mathrm{local}}(x)=2A|\cos kx|.
$$

A **node** is always stationary; an **antinode** oscillates with maximum amplitude. Adjacent nodes are separated by $\lambda/2$, and a node and adjacent antinode by $\lambda/4$.

An ideal standing wave has no net average energy flow along the string even though individual parts store kinetic and elastic energy.

## 15.10 Standing Waves on a String Fixed at Both Ends (Qualitative Discussion)

Both endpoints must be displacement nodes. Only waves that fit an integer number of half-wavelengths into the length $L$ satisfy both boundary conditions:

$$
\boxed{L=n\frac{\lambda_n}{2}},\qquad n=1,2,3,\ldots
$$

With string wave speed $v=\sqrt{F/\mu}$,

$$
\boxed{f_n=\frac{nv}{2L}=\frac{n}{2L}\sqrt{\frac F\mu}}.
$$

The $n=1$ mode is the **fundamental**; $n=2,3,\ldots$ are higher harmonics. Plucking a string at different points changes how strongly different modes are excited, but not the allowed ideal frequencies.

## 15.11 Analytic Treatment of Vibration of a String Fixed at Both Ends

Select separated solutions of the string wave equation in the form

$$
y(x,t)=X(x)T(t).
$$

The boundary conditions $y(0,t)=y(L,t)=0$ demand spatial functions

$$
X_n(x)=\sin\left(\frac{n\pi x}{L}\right).
$$

The matching time variation has angular frequency

$$
\omega_n=\frac{n\pi v}{L}.
$$

Thus each normal mode may be expressed as

$$
\boxed{y_n(x,t)=B_n\sin\left(\frac{n\pi x}{L}\right)\cos(\omega_nt+\phi_n)}.
$$

A general small displacement can be expanded as a sum of these modes. This is the mathematical foundation for string timbre: the same fundamental pitch can occur with differing higher-mode amplitudes.

## 15.12 Vibration of a String Fixed at One End

If $x=0$ is fixed and $x=L$ is free to move transversely, one end is a node and the other an antinode. The free-end condition is approximately zero transverse slope:

$$
y(0,t)=0,\qquad \left.\frac{\partial y}{\partial x}\right|_{x=L}=0.
$$

For a spatial factor $\sin kx$, this means $\cos kL=0$ and hence

$$
\boxed{L=(2n-1)\frac{\lambda_n}{4}},
\qquad
\boxed{f_n=(2n-1)\frac{v}{4L}},\quad n=1,2,3,\ldots
$$

Only odd multiples of the lowest resonance appear for these ideal boundary conditions. Compare carefully with the fixed–fixed string, whose fundamental is $v/(2L)$.

## 15.13 Laws of Transverse Vibrations of a String: Sonometer

The fixed–fixed fundamental relation

$$
f_1=\frac{1}{2L}\sqrt{\frac F\mu}
$$

implies three laws:

| Quantity varied | Other quantities fixed | Frequency scaling |
|---|---|---|
| Length $L$ | $F,\mu$ | $f\propto L^{-1}$ |
| Tension $F$ | $L,\mu$ | $f\propto\sqrt F$ |
| Linear density $\mu$ | $L,F$ | $f\propto\mu^{-1/2}$ |

A **sonometer** uses a stretched wire over adjustable bridges. A hanging load sets tension, a known wire sets linear density, and resonance with a tuning fork reveals the natural frequency. A light paper rider on the wire can indicate an antinode by vigorous motion.

## 15.14 Transverse and Longitudinal Waves

A wave is **transverse** when the medium's local displacement is perpendicular to propagation, as for small disturbances on a stretched string. A wave is **longitudinal** when displacement is parallel to propagation, as for compressions in air.

Polarization is possible for transverse waves because they can oscillate along alternative perpendicular directions. A purely longitudinal scalar compression wave cannot be linearly polarized in that transverse-direction sense.

For longitudinal sound, distinguish displacement nodes and pressure nodes: because pressure change depends on displacement gradient, a displacement node is generally a pressure antinode.

## 15.15 Polarization of Waves

A wave whose disturbance selects one fixed transverse direction is **linearly polarized**. A string constrained to vertical motion produces a vertical transverse disturbance; a polarizing arrangement permits one vibration component and suppresses an orthogonal component.

If a linearly polarized wave meets an ideal analyzer whose allowed direction makes angle $\theta$ with the polarization, the transmitted displacement amplitude scales as $A\cos\theta$. For optical intensity this leads to Malus' law, discussed further in Chapter 17:

$$
\boxed{I=I_0\cos^2\theta}.
$$

**Part I takeaway:** Wave speed is governed by the medium; frequency by the source; the wavelength adjusts to $\lambda=v/f$. Reflection and boundary conditions determine resonances, whereas interference follows linear superposition.

---

# Part II: Sound Waves

Sound usually involves small, approximately longitudinal compressions and rarefactions in matter. The underlying physics connects fluid elasticity, wave propagation and oscillatory pressure fields.

## 16.1 The Nature and Propagation of Sound Waves

A vibrating source alternately compresses and dilutes the material in front of it. Local pressure differences exert forces on neighboring regions, advancing the disturbance. A sound wave in a gas therefore consists of correlated pressure, density and particle-velocity variations.

Under ordinary acoustic conditions, particles of air move only short distances around their equilibrium locations; their average motion is not the same as the propagation velocity. In vacuum, ordinary mechanical sound has no medium through which to travel.

## 16.2 Displacement Wave and Pressure Wave

Let $\xi(x,t)$ be the longitudinal displacement of a fluid particle from its equilibrium location. The local fractional change in volume is approximately $\partial\xi/\partial x$, so the pressure perturbation is

$$
\boxed{\Delta p=-B\frac{\partial\xi}{\partial x}},
$$

where $B$ is the relevant bulk modulus of the material. A negative displacement gradient corresponds to compression and positive pressure variation.

For a right-moving harmonic displacement wave,

$$
\xi(x,t)=\xi_m\cos(kx-\omega t),
$$

we obtain

$$
\Delta p=Bk\xi_m\sin(kx-\omega t).
$$

Thus the pressure and displacement oscillations are shifted by a quarter cycle in phase; the pressure amplitude is

$$
\boxed{p_m=Bk\xi_m=\rho v\omega\xi_m}.
$$

The factor $\rho v$ is the **characteristic acoustic impedance** per unit area for plane waves.

## 16.3 Speed of a Sound Wave in a Material Medium

A medium resists compression through an elastic modulus and resists acceleration through inertia. Newton's law and the linear pressure-displacement relation produce

$$
\rho\frac{\partial^2\xi}{\partial t^2}=B\frac{\partial^2\xi}{\partial x^2}.
$$

Consequently,

$$
\boxed{v=\sqrt{\frac B\rho}}.
$$

For a longitudinal wave in a thin elastic solid rod whose sides can deform, Young's modulus may replace the effective compressional stiffness, giving an approximation $v\simeq\sqrt{Y/\rho}$. The correct wave-speed formula depends on geometry and allowed deformation. Sound speeds in bulk solids involve appropriate elastic constants.

## 16.4 Speed of Sound in a Gas: Newton's Formula and Laplace's Correction

For an ideal gas, Newton's original treatment took the gas compression as approximately **isothermal**. The isothermal bulk modulus equals equilibrium pressure $p$, leading to

$$
v_{\mathrm{Newton}}=\sqrt{\frac p\rho}.
$$

But compression and rarefaction during an acoustic cycle usually occur too rapidly for appreciable heat exchange. The more suitable idealization is **adiabatic**. With $pV^\gamma=\text{constant}$,

$$
B_{\mathrm{adiabatic}}=-V\frac{dp}{dV}=\gamma p.
$$

Laplace's correction yields

$$
\boxed{v=\sqrt{\frac{\gamma p}{\rho}}=\sqrt{\frac{\gamma RT}{M}}},
$$

where $\gamma=C_p/C_v$, $M$ is molar mass, $T$ is absolute temperature and $R$ is the ideal-gas constant.

## 16.5 Effect of Pressure, Temperature and Humidity on the Speed of Sound in Air

The ideal-gas formula $v=\sqrt{\gamma RT/M}$ reveals three points:

- **Pressure at fixed temperature and composition:** speed is approximately independent of pressure because $p/\rho=RT/M$.
- **Temperature:** $v\propto\sqrt T$. Warmer air transmits sound faster under otherwise comparable conditions.
- **Humidity:** at comparable pressure and temperature, adding water vapor generally lowers the mean molar mass of air, tending to raise sound speed.

For ordinary dry air near room conditions, a practical approximation is

$$
v\simeq331\,\mathrm{m\,s^{-1}}+0.6\,\mathrm{m\,s^{-1}\,^{\circ}C^{-1}}\,\theta,
$$

where $\theta$ is Celsius temperature; this is a local linear approximation rather than a fundamental law.

## 16.6 Intensity of Sound Waves

Intensity is average power flow per unit area perpendicular to propagation. For a plane harmonic sound wave of displacement amplitude $\xi_m$,

$$
\boxed{I=\frac12\rho v\omega^2\xi_m^2}
$$

or, in terms of pressure amplitude,

$$
\boxed{I=\frac{p_m^2}{2\rho v}}.
$$

Sound intensity is proportional to the square of pressure amplitude. For a point source radiating uniformly in free space without absorption,

$$
\boxed{I(r)=\frac{P}{4\pi r^2}}.
$$

Real sound propagation may also involve reflection, absorption, directivity and interference.

## 16.7 Appearance of Sound to Human Ear

Three perceptual attributes are often distinguished: **pitch**, governed mainly by frequency; **loudness**, governed by intensity and human auditory response; and **quality or timbre**, governed by harmonic content and temporal structure.

A commonly used physical sound-intensity level is

$$
\boxed{\beta=10\log_{10}\left(\frac I{I_0}\right)\ \mathrm{dB}},
$$

with reference $I_0=10^{-12}\,\mathrm{W\,m^{-2}}$ in standard introductory acoustics. The decibel scale is logarithmic: multiplying intensity by $10$ adds $10\,\mathrm{dB}$, while doubling intensity adds about $3\,\mathrm{dB}$. Sound-intensity level is not a complete psychophysical measure of perceived loudness.

## 16.8 Interference of Sound Waves

At a listener, two coherent sound waves of the same frequency and a stable phase relation interfere. The total pressure amplitude obeys the same resultant-amplitude relation as other waves:

$$
p_{\mathrm{res}}^2=p_1^2+p_2^2+2p_1p_2\cos\delta.
$$

For in-phase sources, path difference $m\lambda$ favors constructive interference, whereas $(m+1/2)\lambda$ favors destructive interference. The observed pattern depends on the total phase difference, including any source phase offset.

Two independent sound sources without a stable relative phase generally produce averaged intensity addition rather than stable spatial interference fringes.

## 16.9 Standing Longitudinal Waves and Vibrations of Air Columns

Reflection of sound waves creates standing patterns inside tubes. The relevant end conditions are approximately:

| End | Displacement | Pressure variation |
|---|---|---|
| Open end | Antinode | Node |
| Rigid closed end | Node | Antinode |

For an open–open pipe of effective acoustic length $L$, both ends behave as displacement antinodes. The allowed frequencies are

$$
\boxed{f_n=\frac{nv}{2L}},\qquad n=1,2,3,\ldots
$$

For a closed–open pipe, the conditions are a displacement node at the closed end and an antinode at the open end:

$$
\boxed{f_n=(2n-1)\frac{v}{4L}},\qquad n=1,2,3,\ldots
$$

The open-end antinode is slightly outside the physical pipe; an **end correction** must be included in accurate measurements. For a simple unflanged opening, a rough correction is $e\simeq0.6r$ per open end, where $r$ is tube radius.

## 16.10 Determination of Speed of Sound in Air

A resonance-tube experiment uses an adjustable air column and a tuning fork of known frequency $f$. Resonance occurs when an allowed standing-wave mode fits the effective length.

For a tube closed at the water surface and open at the other end, successive resonant lengths differ by approximately half a wavelength:

$$
L_2-L_1=\frac\lambda2.
$$

Therefore,

$$
\boxed{v=2f(L_2-L_1)}.
$$

Using the **difference** between two resonance lengths largely eliminates the unknown end correction, as long as conditions remain unchanged.

## 16.11 Beats

Superimpose two waves of nearby frequencies $f_1$ and $f_2$:

$$
\sin(2\pi f_1t)+\sin(2\pi f_2t)
=2\cos\big(\pi(f_1-f_2)t\big)\sin\big(\pi(f_1+f_2)t\big).
$$

The fast factor oscillates at the mean frequency, while the slow envelope modulates amplitude. The count of loudness maxima per second is

$$
\boxed{f_{\mathrm{beat}}=|f_1-f_2|}.
$$

The beat phenomenon is especially useful for tuning instruments or comparing unknown and standard tuning-fork frequencies.

## 16.12 Diffraction

Sound spreads into regions not predicted by straight-line rays when it passes through an aperture or around an edge. The effect becomes noticeable when the aperture or obstacle has dimensions comparable to the wavelength.

Low-frequency sound has longer wavelengths in the same medium, so it tends to bend around everyday obstacles more readily than high-frequency sound. Diffraction and reflection together help explain why voices can be heard around corners, even where the speaker is not visible.

## 16.13 Doppler Effect

The Doppler effect is an apparent frequency change caused by relative motion of source, observer and the transmitting medium.

For sound in a still medium, choose **positive $v_o$ toward the source** and **positive $v_s$ toward the observer**. In the collinear case,

$$
\boxed{f'=f\frac{v+v_o}{v-v_s}}.
$$

Here $v$ is sound speed relative to the medium. A source approaching a stationary observer compresses wavelengths ahead of it; an observer approaching the source encounters wavefronts more frequently. If either object recedes, reverse the corresponding velocity sign.

**Why source and observer motion differ for sound:** source motion changes the wavelength in the medium, whereas observer motion changes the rate of encountering a wavelength already present in that medium. With wind, first specify velocities relative to the moving air.

## 16.14 Sonic Booms

When a source moves at speed $u$ faster than the sound speed $v$ in the medium, new compressions originate outside earlier expanding wavefronts. Their envelope forms a **Mach cone**:

$$
\boxed{\sin\mu=\frac vu=\frac1{M_a}},
$$

where $\mu$ is the cone half-angle and $M_a=u/v$ the Mach number. Passing shock fronts produce abrupt pressure changes experienced as a sonic boom. A boom is not one isolated sound generated only at the moment of crossing Mach 1; the moving supersonic body continuously produces a shock structure.

## 16.15 Musical Scale

Music organizes frequencies into perceived pitch intervals. A frequency ratio of $2:1$ is an **octave**. In equal temperament, one octave is divided into 12 equal logarithmic intervals, giving

$$
\boxed{f_n=f_0\,2^{n/12}}
$$

for an increase of $n$ semitones. Actual instruments produce fundamentals and overtones, so tuning, consonance and timbre also depend on spectral content and harmonic relations. The mathematics of musical notes is therefore closely connected to standing-wave frequencies.

## 16.16 Acoustics of Buildings

The acoustic experience inside a room involves **direct sound**, many reflections, absorption, and reverberation. Hard reflecting surfaces can prolong sound and reduce speech clarity; absorbing material reduces repeated reflections.

A common approximate room-acoustics parameter is reverberation time $T_{60}$, the duration for sound-energy level to decrease by $60\,\mathrm{dB}$ after the source stops. Under a diffuse-field approximation, Sabine's relation is

$$
\boxed{T_{60}\simeq0.161\frac V{A_{\mathrm{eq}}}},
$$

with $V$ in cubic meters and equivalent absorption area $A_{\mathrm{eq}}$ in square meters. This engineering relation assumes a suitable room and approximately diffuse sound field; it is not a universal law for every room. Good auditorium design balances sufficient sound reinforcement against echoes and excessive reverberation.

**Part II takeaway:** Sound links elastic compression to wave motion. Its speed follows a stiffness-to-inertia ratio; reflection produces air-column resonance; relative motion changes observed frequency; and geometry and absorption shape room acoustics.

---
# Part III: Light Waves

Light is an electromagnetic wave, and visible light is one part of a much wider electromagnetic spectrum. The characteristic features of wave motion, notably interference and diffraction, cannot be explained by geometric rays alone.

## 17.1 Waves or Particles

The particle viewpoint explains localized transfer of energy and momentum, while the wave viewpoint explains interference, diffraction and polarization. Historically, ray-like propagation encouraged a corpuscular picture, whereas Young's and Fresnel's work strongly supported a wave picture.

In modern physics, light consists of photons with energy $E=hf$ and momentum $p=h/\lambda$. **Wave–particle duality** does not mean choosing two incompatible classical models simultaneously; it means neither the picture of tiny billiard balls nor that of a continuous classical wave captures every observation. This chapter emphasizes the wave phenomena, with quantum features reserved for later study.

## 17.2 The Nature of Light Waves

Classical light is a coupled disturbance in electric and magnetic fields. For a plane wave travelling along the positive $x$-axis, one possible linear polarization is

$$
\vec E(x,t)=E_0\sin(kx-\omega t)\,\hat y,
\qquad
\vec B(x,t)=B_0\sin(kx-\omega t)\,\hat z.
$$

The fields and propagation direction are mutually perpendicular, with magnitudes related in vacuum by

$$
\boxed{E_0=cB_0},
\qquad
\boxed{c\simeq3.00\times10^8\,\mathrm{m\,s^{-1}}}.
$$

Unlike transverse waves on strings, the electromagnetic field does not need a mechanical material to oscillate. Energy flux is represented by the Poynting vector, which points along the propagation direction for a plane wave.

For a nonmagnetic transparent medium with refractive index $n$,

$$
\boxed{v=\frac cn}.
$$

The frequency remains fixed when light crosses a stationary interface, but speed and wavelength change:

$$
\lambda_{\mathrm{medium}}=\frac{\lambda_0}{n}.
$$

## 17.3 Huygens' Principle

Every point of an advancing wavefront can be regarded as a source of secondary wavelets; the envelope of the later wavelets constructs the next wavefront. This geometrical construction predicts reflection and refraction.

### Reflection from a plane surface

The reflected wavefront is constructed from points on the surface reached at different times. Equal propagation speed in the incident and reflected medium gives

$$
\boxed{i=r},
$$

with both angles measured from the normal.

### Refraction across a boundary

Let light enter medium 2 from medium 1. Because the secondary wavelets advance at speeds $v_1$ and $v_2$ on the two sides, the geometry gives

$$
\frac{\sin i}{\sin r}=\frac{v_1}{v_2}=\frac{n_2}{n_1}.
$$

Thus

$$
\boxed{n_1\sin i=n_2\sin r}.
$$

This is Snell's law. Huygens' elementary construction describes directions; explaining intensity patterns requires interference and more detailed wave theory.

## 17.4 Young's Double Hole Experiment

A first aperture illuminated by a source provides a shared wavefront. Two smaller holes in that wavefront then act as coherent secondary sources. At a distant point $P$, light travels different distances from the two holes and arrives with a phase difference

$$
\boxed{\Delta\phi=\frac{2\pi}{\lambda}\Delta r+\Delta\phi_0},
$$

where $\Delta r=r_2-r_1$ and $\Delta\phi_0$ is the initial source-phase difference.

For coherent equal-intensity beams,

$$
\boxed{I=4I_0\cos^2\left(\frac{\Delta\phi}{2}\right)}.
$$

The maximum and minimum conditions for equal initial phase are

$$
\boxed{\Delta r=m\lambda\quad\text{(bright)}},
$$

$$
\boxed{\Delta r=\left(m+\frac12\right)\lambda\quad\text{(dark)}}.
$$

This is a spatial redistribution of energy through interference, not creation or destruction of optical energy.

## 17.5 Young's Double Slit Experiment

Two narrow slits separated by $d$ are illuminated coherently. A screen is placed at distance $D$, with $D\gg d$ and observation near the center. For a point at transverse coordinate $y$,

$$
\Delta r=d\sin\theta\simeq\frac{dy}{D}.
$$

The centers of bright fringes satisfy

$$
y_m\simeq\frac{m\lambda D}{d},
$$

and dark fringes lie halfway between consecutive bright fringes. The **fringe width** is

$$
\boxed{\beta=\frac{\lambda D}{d}}.
$$

Increasing wavelength or screen distance increases spacing; increasing slit separation decreases it. The textbook formula assumes narrow slits, coherent illumination, small observation angles and a screen far compared with slit separation.

For unequal slit intensities $I_1$ and $I_2$,

$$
\boxed{I=I_1+I_2+2\sqrt{I_1I_2}\cos\Delta\phi}.
$$

Visibility is maximized by comparable beam amplitudes.

## 17.6 Optical Path

Phase accumulation depends on travel through a medium, not merely physical distance. Optical path length is defined by

$$
\boxed{\mathrm{OPL}=\int n(s)\,ds}.
$$

In a homogeneous medium, $\mathrm{OPL}=n\ell$. In terms of vacuum wavelength $\lambda_0$, the phase difference arising from optical path difference $\Delta(\mathrm{OPL})$ is

$$
\boxed{\Delta\phi=\frac{2\pi}{\lambda_0}\Delta(\mathrm{OPL})}.
$$

This makes it possible to combine geometric distances and refractive indices within a single interference calculation. Any phase shift associated with reflection must be added separately.

## 17.7 Interference from Thin Films

Light reflected from the front and rear surfaces of a transparent film follows two paths that can recombine. Let film thickness be $t$, refractive index $n$, and internal refraction angle $r$. The propagation contribution to optical path difference is

$$
\boxed{\Delta(\mathrm{OPL})=2nt\cos r}.
$$

Reflection at a boundary leading into a **higher refractive index** introduces a phase change of $\pi$ for the reflected electric field, while reflection toward a lower-index medium does not.

When exactly one of the two interfering reflected beams experiences a $\pi$ reversal, constructive reflected interference requires

$$
\boxed{2nt\cos r=\left(m+\frac12\right)\lambda_0},
$$

and destructive reflected interference requires

$$
\boxed{2nt\cos r=m\lambda_0}.
$$

If both or neither reflected beams acquire such reversal, these roles interchange. Soap-film colors and thin-film optical coatings depend on this combination of geometry, wavelength and interface phase.

## 17.8 Fresnel's Biprism

A biprism consists of two weak prisms arranged base-to-base. A single narrow slit viewed through its two halves appears as two **virtual coherent sources**, because both originate from the same incident light. The overlapping emerging beams create fringes much as in Young's experiment.

If the separation between the virtual sources is $d$ and the distance to the observation plane is $D$, then in the usual paraxial geometry

$$
\boxed{\beta=\frac{\lambda D}{d}}.
$$

The virtue of the biprism is that two mutually coherent optical sources can be created from one slit rather than requiring independent light sources to maintain stable phase.

## 17.9 Coherent and Incoherent Sources

Sources are **coherent** when their relative phase remains sufficiently stable over the observation time for a persistent interference pattern. Equal frequency is necessary for strictly stationary fringes, but not sufficient without phase stability.

An ordinary thermal lamp contains many emitters whose phases fluctuate rapidly. Splitting one wavefront or one beam into two paths preserves the required correlation much better than combining light from unrelated lamps.

The distinction between **temporal coherence** (phase correlation over time) and **spatial coherence** (correlation across source locations) explains why spectral narrowing and a small source aperture improve fringe visibility.

## 17.10 Diffraction of Light

Diffraction is the spreading and interference of wave components when an aperture, edge or obstacle limits the wavefront. Geometrical optics predicts sharp ray boundaries; diffraction replaces them with intensity patterns.

Two useful limiting descriptions are:

- **Fraunhofer diffraction:** source and observation effectively far away, or lenses transform the geometry into the far-field pattern.
- **Fresnel diffraction:** finite propagation distance and curved wavefront contributions must be retained.

The size of the opening relative to $\lambda$ controls the angular scale of the spreading. Diffraction becomes fundamental when optical structures are small enough that the ray approximation fails.

## 17.11 Fraunhofer Diffraction by a Single Slit

Take a slit of width $a$ uniformly illuminated by monochromatic light of wavelength $\lambda$. Each infinitesimal portion of the slit contributes an oscillating field. Summing those contributions at observation angle $\theta$ gives

$$
\boxed{I(\theta)=I(0)\left(\frac{\sin\alpha}{\alpha}\right)^2},
\qquad
\alpha=\frac{\pi a\sin\theta}{\lambda}.
$$

Intensity minima occur when

$$
\boxed{a\sin\theta=m\lambda},\qquad m=\pm1,\pm2,\ldots
$$

The central bright maximum is wider than the neighboring secondary maxima: its angular width between first zeros is approximately $2\lambda/a$ for small angles. Narrowing the slit broadens the diffraction envelope.

**Important distinction:** In double-slit interference, slit separation largely sets fine fringe spacing. In single-slit diffraction, slit **width** sets the broad envelope.

## 17.12 Fraunhofer Diffraction by a Circular Aperture

A circular opening gives a central bright **Airy disc** and fainter concentric rings. For an unobstructed circular aperture of diameter $D$, the angular radius to the first dark ring is approximately

$$
\boxed{\theta_1\simeq1.22\frac{\lambda}{D}}.
$$

A finite aperture can therefore never focus a perfectly collimated monochromatic point source to a mathematical point in the focal plane. A larger aperture concentrates the diffraction image into a smaller angular region.

This relation is for the first minimum of the ideal circular-aperture pattern. Aberrations, atmospheric turbulence and detector sampling may broaden observed spots further.

## 17.13 Fresnel Diffraction at a Straight Edge

A sharp opaque edge blocks one portion of a wavefront. In geometrical optics the shadow boundary is perfectly sharp, but wavelets from the exposed part interfere across the boundary. A sequence of light and dark regions may occur near the edge, with some light entering the nominal shadow.

Here the observation distance is not so large that all contributing wavefronts can be treated as parallel. Hence the diffraction analysis must retain propagation phase changes associated with varying distance, as in Fresnel's approach.

## 17.14 Limit of Resolution

Two nearby objects are **resolved** if their diffraction images remain distinguishable. Under the Rayleigh criterion for two equally bright point sources observed through an ideal circular aperture,

$$
\boxed{\theta_{\min}\simeq1.22\frac{\lambda}{D}}.
$$

The numerical factor corresponds to the maximum of one Airy pattern approximately overlapping the first minimum of the other. Reducing wavelength or enlarging aperture improves diffraction-limited angular resolution.

**Resolution is not the same as magnification.** Enlarging a blurred pattern cannot recover detail absent from the optical image.

## 17.15 Scattering of Light

Scattering redirects incident radiation when light interacts with molecules, particles or spatial variations in refractive index. For particles much smaller than the wavelength and under appropriate assumptions, **Rayleigh scattering** has strong wavelength dependence:

$$
\boxed{I_{\mathrm{scattered}}\propto\frac1{\lambda^4}}
$$

for otherwise fixed conditions. Shorter wavelengths scatter more strongly, helping explain the blue daytime sky and the reddening of the direct Sun at low elevation. For particles comparable to or larger than the wavelength, other scattering regimes apply and the simple fourth-power law is inadequate.

Scattering differs from absorption: absorption transfers optical energy into other forms, while scattering primarily redistributes propagation directions.

## 17.16 Polarization of Light

A linearly polarized plane wave has its electric field oscillating along a fixed transverse direction. Unpolarized light has no single persistent transverse direction. Two mutually perpendicular electric-field components with an appropriate phase offset can produce **elliptical** or **circular** polarization.

For an ideal polarizer and incident linearly polarized intensity $I_0$,

$$
\boxed{I=I_0\cos^2\theta}\quad\text{(Malus' law)}.
$$

For incident unpolarized light, an ideal first polarizer transmits half the averaged intensity. Reflection can also preferentially polarize light. At **Brewster's angle**, the reflected and refracted rays are perpendicular and

$$
\boxed{\tan\theta_B=\frac{n_2}{n_1}}
$$

for an interface from medium 1 to medium 2. Polarization is decisive evidence that the classical optical field has transverse character.

**Part III takeaway:** Interference probes phase differences, diffraction probes the finite size of apertures, and polarization probes field direction. Ray optics emerges when wavelength is much smaller than relevant geometric features.

---

# Part IV: Geometrical Optics

Geometrical optics represents light transport by rays. It is highly useful for lenses, mirrors and instruments when characteristic dimensions greatly exceed the optical wavelength and diffraction is not the dominant effect.

> **Coordinate convention for this part.** Use HCV's Cartesian sign convention: origin at the mirror pole, spherical-surface vertex or thin-lens optical center; positive $x$ usually points along the incident light. Signed quantities $u,v,R,f$ are **coordinates**, not automatically positive distances. For the common layout of incident light travelling left to right, an object on the left has $u<0$.

## 18.1 Reflection at Smooth Surfaces

At a sufficiently smooth reflecting interface, incident and reflected rays lie in the plane containing the surface normal, and

$$
\boxed{i=r}.
$$

Reflection from a plane mirror produces a virtual image behind the mirror at the same perpendicular distance as the object is in front. The image is erect and the same size under the usual paraxial interpretation.

A plane mirror is a geometrical idealization. Real surfaces may absorb, scatter or transmit light in addition to reflecting it.

## 18.2 Spherical Mirrors

A spherical mirror is a portion of a sphere with a reflecting surface. Its **pole** is where the principal axis meets the reflecting surface; the **center of curvature** is the center of the sphere; the **radius of curvature** is $R$; and the **principal focus** is where initially parallel paraxial rays meet (or appear to originate).

- **Concave mirror:** converges initially parallel rays; for the common left-incident configuration, its center and paraxial focus lie left of the pole, so $R<0$ and $f<0$.
- **Convex mirror:** diverges parallel rays; its virtual focus lies behind the mirror, giving $R>0$ and $f>0$.

Only paraxial rays are assumed to meet at a common focus for an ideal spherical mirror.

## 18.3 Relation between $u$, $v$ and $R$ for Spherical Mirrors

Consider a near-axis incident ray from a point object on the principal axis. Using the law of reflection and small-angle approximations, the geometry gives

$$
\frac2R=\frac1u+\frac1v.
$$

Therefore the **mirror formula** and focal relation are

$$
\boxed{\frac1u+\frac1v=\frac1f},
\qquad
\boxed{f=\frac R2}.
$$

The formula applies to concave and convex mirrors when all coordinates are used consistently. A real object in front of a mirror has $u<0$ for left-to-right incident light; a real reflected image in front has $v<0$; a virtual image behind has $v>0$.

## 18.4 Extended Objects and Magnification

For an object whose height $h_o$ is small compared with other geometric dimensions, paraxial ray triangles give image height $h_i$ and transverse magnification

$$
\boxed{m=\frac{h_i}{h_o}=-\frac vu}.
$$

A negative value indicates an inverted image, while a positive value indicates an erect image relative to the chosen transverse axis. The magnitude $|m|$ measures the size ratio.

An image can be **real** or **virtual** independently of whether it is larger or smaller than the object. Real images are formed by actual converging rays; virtual images are located by backward ray extensions.

## 18.5 Refraction at Plane Surfaces

When a ray passes across a plane interface between refractive indices $n_1$ and $n_2$, the directions are related by Snell's law:

$$
\boxed{n_1\sin i=n_2\sin r}.
$$

At normal incidence the ray travels without angular deviation, but its wave speed and wavelength may still change.

### Apparent depth

Viewed near normal incidence from medium 2, an object at real depth $d$ in medium 1 appears at depth $d'$ satisfying, in the paraxial approximation,

$$
\boxed{\frac{d'}{d}\simeq\frac{n_2}{n_1}}.
$$

For viewing from air into water, $n_2\simeq1<n_1$, so the object looks shallower. This relation uses small viewing angles; oblique viewing requires full ray geometry.

## 18.6 Critical Angle

For light initially in medium 1 with $n_1>n_2$, increasing incidence angle eventually brings the refracted angle to $90^\circ$. The critical angle $\theta_c$ obeys

$$
\boxed{\sin\theta_c=\frac{n_2}{n_1}}.
$$

At greater angles, an ideal smooth interface supports **total internal reflection**. This phenomenon requires incidence from higher to lower refractive index. It is not possible for the reverse direction under ordinary isotropic transparent-medium conditions.

## 18.7 Optical Fibre

An optical fiber guides light through repeated total internal reflection or, more generally, through the wave-guiding behavior of a higher-index core surrounded by lower-index cladding.

A simple step-index fiber has

$$
n_{\mathrm{core}}>n_{\mathrm{clad}}.
$$

For a fiber with external refractive index $n_0$, a common ray-optics acceptance relation is

$$
\boxed{n_0\sin\theta_{\max}=\sqrt{n_{\mathrm{core}}^2-n_{\mathrm{clad}}^2}},
$$

within its idealized meridional-ray model. Actual signal quality also depends on mode propagation, dispersion, absorption, bending losses and fiber geometry.

## 18.8 Prism

A triangular prism refracts light at two nonparallel faces. Let $A$ be the prism angle, $i$ incidence angle at its first face, $e$ emergence angle at its second face, and $r_1,r_2$ the internal angles to the surface normals. Geometry yields

$$
\boxed{r_1+r_2=A},
\qquad
\boxed{\delta=i+e-A},
$$

where $\delta$ is the net deviation. At **minimum deviation**, the path is symmetric: $i=e$ and $r_1=r_2=A/2$. For refractive index $n$ relative to surrounding air,

$$
\boxed{n=\frac{\sin[(A+\delta_{\min})/2]}{\sin(A/2)}}.
$$

For a thin prism at small angles,

$$
\boxed{\delta\simeq(n-1)A}.
$$

This approximation is especially useful in elementary dispersion calculations.

## 18.9 Refraction at Spherical Surfaces

A paraxial ray crossing a spherical boundary separates two media of refractive indices $n_1$ and $n_2$. Using Snell's law in its small-angle form and a consistent Cartesian axis,

$$
\boxed{\frac{n_2}{v}-\frac{n_1}{u}=\frac{n_2-n_1}{R}}.
$$

For rays incident left-to-right, a center of curvature on the right gives $R>0$. The formula can describe a real or virtual image depending on the signed image coordinate $v$.

This is the central building block of the thin-lens formula: a thin lens is approximately two successive spherical refractions.

## 18.10 Extended Objects: Lateral Magnification

For a small off-axis object close to the principal axis, geometry at the refracting surface gives

$$
\boxed{m=\frac{h_i}{h_o}=\frac{n_1v}{n_2u}}.
$$

The refractive indices matter because angles and ray directions change at the interface. The sign describes inversion or erectness. Do not use the mirror magnification formula $-v/u$ for a single refracting spherical surface.

## 18.11 Refraction through Thin Lenses

A thin lens consists of two refracting surfaces sufficiently close that their axial separation is negligible compared with object and image distances. A ray through its optical center is approximately undeviated in the same surrounding medium. Other rays are bent toward or away from the axis.

An ideal **converging lens** has positive focal length for left-to-right incident light; an ideal **diverging lens** has negative focal length. The same glass shape can change its converging/diverging character in a surrounding material with a different refractive index.

The lens model assumes paraxial rays, uniform transparent media and negligible lens thickness.

## 18.12 Lens Maker's Formula and Lens Formula

Apply the spherical-refraction equation first to the front surface of index $n_1\to n_2$ and then to the rear surface $n_2\to n_1$. In the thin-lens approximation, the intermediate-image terms cancel when the two equations are added:

$$
\frac1v-\frac1u=\left(\frac{n_2}{n_1}-1\right)\left(\frac1{R_1}-\frac1{R_2}\right).
$$

For lens refractive index $n_{\ell}$ and surrounding medium $n_m$,

$$
\boxed{\frac1f=\left(\frac{n_{\ell}}{n_m}-1\right)\left(\frac1{R_1}-\frac1{R_2}\right)}
$$

is the **thin-lens maker's formula**. The imaging formula is

$$
\boxed{\frac1v-\frac1u=\frac1f}.
$$

For a usual biconvex converging lens with light from left to right, $R_1>0$, $R_2<0$, and $f>0$ if $n_\ell>n_m$.

## 18.13 Extended Objects: Lateral Magnification

A paraxial ray through the optical center continues essentially undeviated. Similar triangles then yield

$$
\boxed{m=\frac{h_i}{h_o}=\frac vu}.
$$

A positive $m$ indicates erect image; a negative $m$ indicates inverted image. For a real object left of a converging lens, $u<0$; a real image right of it has $v>0$, so $m<0$ as expected.

The lens and mirror image formulas have different signs, so their magnification formulas must not be interchanged mechanically.

## 18.14 Power of a Lens

Lens power measures convergence or divergence in inverse meters:

$$
\boxed{P=\frac1{f\,(\mathrm m)}}.
$$

Its unit is the **dioptre (D)**. Positive power indicates convergence and negative power indicates divergence in the standard optical convention. A $+2\,\mathrm D$ thin lens in air has a focal length of $+0.50\,\mathrm m$.

## 18.15 Thin Lenses in Contact

For two thin lenses in contact, treat the image made by the first as the object for the second. Adding the individual lens equations gives

$$
\boxed{\frac1{f_{\mathrm{eq}}}=\frac1{f_1}+\frac1{f_2}}.
$$

Equivalently,

$$
\boxed{P_{\mathrm{eq}}=P_1+P_2}.
$$

The focal length can be positive, negative or effectively infinite depending on the combination. This simple sum assumes the lenses are in contact and immersed in the same surrounding medium.

## 18.16 Two Thin Lenses Separated by a Distance

When lenses are separated by axial distance $d$, applying the thin-lens equation consecutively is the safest way to locate an image. A paraxial effective-power expression in a common surrounding medium is

$$
\boxed{P_{\mathrm{eq}}=P_1+P_2-dP_1P_2},
$$

where $d$ is in meters and the powers in inverse meters. Thus

$$
\boxed{f_{\mathrm{eq}}=\frac{f_1f_2}{f_1+f_2-d}}.
$$

**Critical qualification:** this effective focal length is measured relative to the equivalent system's **principal planes**, not generally from either physical lens. The separated pair is not equivalent to a single lens sitting arbitrarily at one of the originals. For actual finite-object image positions, propagate the first image through the second lens and account for $d$ explicitly.

## 18.17 Defects of Images

Perfect paraxial lenses and mirrors are idealizations. Real instruments may show:

| Aberration | Cause or observable effect | Common mitigation |
|---|---|---|
| Spherical | Marginal and paraxial rays focus differently | Stops, aspheric surfaces, optimized lenses |
| Chromatic | Refractive index varies with wavelength | Achromatic lens combinations |
| Coma | Off-axis point appears asymmetrically distorted | Optical design and aperture control |
| Astigmatism | Different focus in orthogonal planes for off-axis objects | Corrective lens design |
| Field curvature | Best focus lies on curved surface | Field flatteners |
| Distortion | Magnification varies across the field | Geometric design and calibration |

A smaller aperture often reduces geometrical aberrations, but closing it excessively makes diffraction blur worse. Optical engineering therefore balances geometric and wave limits.

**Part IV takeaway:** Use ray geometry to find images, but keep signed coordinates straight. A mirror obeys $1/u+1/v=1/f$, while a thin lens obeys $1/v-1/u=1/f$. Every imaging law has paraxial and medium assumptions.

---
# Part V: Optical Instruments

An optical instrument rearranges light rays to form a usable image or increase the angular size of a viewed object. **Magnification, clarity and resolution** are distinct performance measures.

## 19.1 The Eye

The eye is a biological optical instrument whose cornea and lens converge incoming light onto the retina. The retina carries light-sensitive receptor cells, and the brain interprets the resulting signals.

The eye varies the curvature, and therefore the optical power, of its lens through **accommodation**. An ordinary relaxed eye focuses distant objects; a more curved lens helps focus nearby objects.

The **far point** is the most distant point sharply visible without optical correction. The **near point** is the closest point sharply visible under maximum comfortable accommodation. For elementary instrument formulas, the conventional least distance of distinct vision for a normal eye is

$$
\boxed{D\simeq25\,\mathrm{cm}}.
$$

This is a practical reference distance for the standard formulas, not a universal biological constant for every person.

## 19.2 The Apparent Size

Objects appear larger or smaller largely according to the angle they subtend at the eye. For a small object of height $h$ perpendicular to the line of sight at distance $r$,

$$
\boxed{\theta\simeq\frac hr}\qquad\text{(radians; small angles)}.
$$

An instrument's **angular magnification** is the ratio of the angle subtended by the final viewed image to the reference angle subtended by the object when viewed directly under a specified condition:

$$
\boxed{M=\frac{\theta_{\mathrm{instrument}}}{\theta_{\mathrm{reference}}}}.
$$

The reference viewing distance must be stated. Angular magnification differs from transverse magnification $h_i/h_o$.

## 19.3 Simple Microscope

A simple microscope is a short-focal-length converging lens producing an enlarged virtual image when the object lies inside its focal length.

With the eye close to the lens and the final virtual image at the near point $D$, the approximate angular magnification is

$$
\boxed{M_D=1+\frac Df}.
$$

If the instrument is adjusted so the final image lies at infinity, the eye views with minimal accommodation and

$$
\boxed{M_\infty=\frac Df}.
$$

A shorter focal length gives greater angular magnification, subject to practical limitations such as aberration and usable working distance.

## 19.4 Compound Microscope

A compound microscope combines an **objective** of very short focal length with an **eyepiece** acting as a magnifier. The objective first forms a magnified real intermediate image; the eyepiece then presents a larger-angle virtual image to the eye.

To first approximation, total angular magnification is the product of objective transverse magnification and eyepiece angular magnification:

$$
\boxed{M=m_oM_e}.
$$

If the objective produces intermediate-image distance $v_o$ for object distance $u_o$, then $m_o=v_o/u_o$ with signs interpreted appropriately. In a common large-tube-length approximation, $|m_o|\simeq L/f_o$, where $L$ is the effective optical tube length.

Consequently,

$$
\boxed{|M_\infty|\simeq\frac L{f_o}\frac D{f_e}},
$$

for final image at infinity, and

$$
\boxed{|M_D|\simeq\frac L{f_o}\left(1+\frac D{f_e}\right)},
$$

for final image at near point. The effective tube length and optical layout matter; these are standard approximations, not exact for every microscope.

## 19.5 Telescopes

A telescope increases the apparent angular size of distant objects. Its objective collects light and forms an intermediate image; the eyepiece enables the observer to view that image.

### Astronomical telescope in normal adjustment

For a converging objective of focal length $f_o>0$ and converging eyepiece $f_e>0$, the distance between the lenses is approximately $f_o+f_e$ when the final image is at infinity. The angular magnification is

$$
\boxed{M=-\frac{f_o}{f_e}}.
$$

The minus sign denotes inversion. Its magnitude is

$$
\boxed{|M|=\frac{f_o}{f_e}}.
$$

### Galilean telescope

A converging objective with a diverging eyepiece ($f_e<0$) provides an erect virtual image. In normal adjustment,

$$
\boxed{M=-\frac{f_o}{f_e}>0},
\qquad
L\simeq f_o+f_e.
$$

The Galilean layout can be compact but has a restricted field of view. Telescope aperture, not magnification alone, controls light gathering and diffraction-limited resolving capability.

## 19.6 Resolving Power of a Microscope and a Telescope

**Resolving power** describes separation of fine detail, not just enlargement. The diffraction-limited telescope criterion for circular objective diameter $D_o$ is

$$
\boxed{\theta_{\min}\simeq1.22\frac\lambda{D_o}}.
$$

Thus angular resolving power can be described by $1/\theta_{\min}$: larger aperture or shorter wavelength resolves closer angular details.

For a microscope, numerical aperture is

$$
\boxed{\mathrm{NA}=n\sin\alpha},
$$

with surrounding medium refractive index $n$ and objective half-acceptance angle $\alpha$. A conventional Abbe-type estimate of minimum resolvable feature spacing is

$$
\boxed{d_{\min}\simeq\frac\lambda{2\mathrm{NA}}}.
$$

Increasing numerical aperture, including through immersion liquid, improves resolution in the approximation. The exact coefficient varies with illumination and resolution criterion.

## 19.7 Defects of Vision

Optical correction works by changing the combined power of eye and external lens.

| Condition | Optical difficulty | Typical correction |
|---|---|---|
| **Myopia** (short-sightedness) | Distant images focus in front of retina for the uncorrected eye | Diverging lens, negative power |
| **Hypermetropia** (long-sightedness) | Near focusing may place the image behind the retina | Converging lens, positive power |
| **Presbyopia** | Accommodation range decreases with age | Near-vision aid or multifocal correction |
| **Astigmatism** | Focusing differs with orientation | Cylindrical or toric correction |

For a myopic eye with far point magnitude $F$ measured from the correcting lens, the lens should create a virtual image at its far point when the object is at infinity:

$$
\boxed{f\simeq-F}.
$$

For hypermetropia, if a near object at distance $D$ must appear at the eye's actual near point $N>D$, a correcting lens placed near the eye obeys

$$
\frac1f=\frac1{-N}-\frac1{-D}=\frac1D-\frac1N.
$$

These expressions ignore spectacle vertex distance and individual ocular details. Actual prescriptions are made through clinical refraction.

**Part V takeaway:** Distinguish lateral from angular magnification, and never equate larger apparent size with better resolution. Optical instruments are limited by lens geometry, diffraction, and the physiology of the eye.

---

# Part VI: Dispersion and Spectra

Refractive index generally varies with frequency and wavelength. A prism is therefore more than a ray deflector: it can separate components of white light according to their wavelengths.

## 20.1 Dispersion

**Dispersion** is the variation of propagation behavior, especially refractive index, with wavelength or frequency. In an ordinary transparent dispersive material over much of the visible spectrum,

$$
n_{\mathrm{violet}}>n_{\mathrm{red}}.
$$

Consequently, for a thin prism,

$$
\delta_v\simeq(n_v-1)A,
\qquad
\delta_r\simeq(n_r-1)A,
$$

so its angular spread between violet and red is

$$
\boxed{\Delta\delta\simeq(n_v-n_r)A}.
$$

Dispersion is not the same phenomenon as diffraction. Diffraction comes from interference of portions of a limited wavefront, whereas prism dispersion comes from wavelength-dependent material response.

## 20.2 Dispersive Power

For a thin prism, **dispersive power** compares the angular dispersion with the average angular deviation. Using refractive indices at representative violet, yellow and red wavelengths,

$$
\boxed{\omega=\frac{n_v-n_r}{n_y-1}}.
$$

The material's dispersive power is approximately independent of the thin-prism angle $A$ under this definition. A high-dispersion material separates colors more strongly for a given mean deflection.

The selected standard wavelengths matter when making precise material comparisons.

## 20.3 Dispersion without Average Deviation and Average Deviation without Dispersion

Consider two thin prisms with signed refracting angles $A_1,A_2$. Let $n_{1y},n_{2y}$ be their yellow-light refractive indices, and $\omega_1,\omega_2$ their dispersive powers.

The mean deviation of the combination is

$$
\boxed{\delta_y=(n_{1y}-1)A_1+(n_{2y}-1)A_2}.
$$

Its color separation is

$$
\boxed{\Delta\delta=\omega_1(n_{1y}-1)A_1+\omega_2(n_{2y}-1)A_2}.
$$

### Direct-vision (zero mean deviation) combination

Set $\delta_y=0$ while retaining $\Delta\delta\ne0$. The prism angles must satisfy

$$
\boxed{(n_{1y}-1)A_1=-(n_{2y}-1)A_2}.
$$

Different dispersive powers ensure that the red–violet spread need not vanish along with the mean deviation.

### Achromatic combination

Set $\Delta\delta=0$ while permitting a nonzero overall mean deviation:

$$
\boxed{\omega_1(n_{1y}-1)A_1=-\omega_2(n_{2y}-1)A_2}.
$$

This is the basic idea of achromatization: different materials have different relationships between average refractive power and chromatic spread.

## 20.4 Spectrum

When white or polychromatic light is separated into wavelength components, the resulting distribution forms a **spectrum**. A spectrometer may map different wavelengths to different angles; the observed intensity distribution depends on the source and any intervening material.

The visible spectrum has an approximate range from $400$ to $700\,\mathrm{nm}$, with boundary values depending on detection conditions and the observer. A continuous visible spectrum can be produced by a hot dense emitter; gases and other sources often produce characteristic spectral features.

## 20.5 Kinds of Spectra

Important spectral categories include:

| Spectrum type | Physical mechanism | Typical observation |
|---|---|---|
| **Continuous emission** | Broad range of wavelengths from a suitable emitter | Unbroken range of colors |
| **Line emission** | Discrete transitions in isolated atoms or ions | Bright isolated lines |
| **Band emission** | Groups of molecular transitions | Clusters or bands |
| **Absorption** | Selective attenuation of a broad background by intervening material | Dark lines or bands superposed on a continuum |

The relation between emission and absorption features makes spectroscopy useful for identifying chemical species and studying temperature and environmental conditions. Intensity and line width require more physics than wavelength matching alone.

## 20.6 Ultraviolet and Infrared Spectrum

Electromagnetic radiation extends beyond visible wavelengths:

- **Ultraviolet (UV):** shorter wavelengths, and thus higher photon energies, than visible violet light.
- **Infrared (IR):** longer wavelengths, and thus lower photon energies, than visible red light.

The classical relation $c=f\lambda_0$ applies in vacuum, and the photon-energy relation from modern physics is

$$
\boxed{E=hf=\frac{hc}{\lambda_0}}.
$$

These bands are useful for identifying material properties and studying thermal radiation, atmospheric absorption and imaging. UV and IR are not different classes of electromagnetic wave; the labels denote spectral ranges.

## 20.7 Spectrometer

A basic prism spectrometer combines a **collimator**, a **prism table**, and a viewing telescope with angular measurement. The collimator makes light from a narrow slit approximately parallel, the prism deviates different wavelengths by different angles, and the telescope identifies the emergent directions.

A common procedure for refractive-index measurement is:

1. Measure prism angle $A$ by reflection geometry.
2. Locate the position of minimum deviation for a known spectral line and record $\delta_{\min}$.
3. Compute the refractive index using

$$
\boxed{n=\frac{\sin[(A+\delta_{\min})/2]}{\sin(A/2)}}.
$$

Careful focusing, slit adjustment and repeated angle readings help reduce instrumental error.

## 20.8 Rainbow

A rainbow results from sunlight interacting with water droplets through **refraction, internal reflection and wavelength-dependent deviation**. Because different colors follow slightly different paths, they emerge with different preferred viewing angles relative to the antisolar direction.

A primary rainbow involves one internal reflection and commonly has red outside and violet inside. A secondary rainbow involves two internal reflections and has reversed color order, usually with lower intensity.

The bow is an angular pattern related to the Sun–observer axis; it is not a fixed colored arc sitting at a particular location in the sky. Different observers receive light from different droplets.

**Part VI takeaway:** Dispersion connects wavelength-dependent refraction to spectral analysis. Prism combinations can suppress mean deviation or chromatic spread, but those are distinct design constraints.

---

# Part VII: Speed of Light

The speed of light can be measured experimentally by converting an extremely short transit time into an observable timing or angular change. HCV presents several historical optical methods based on controlled interruptions or rotating mirrors.

## 21.1 Historical Introduction

Early philosophical debate included whether light propagated instantaneously. Astronomical timing, particularly changes in the apparent timing of Jupiter's moon eclipses across the Earth's orbit, provided evidence of finite light travel time.

Terrestrial measurements became practical through rapidly moving mechanical optical components. The speed of light in vacuum is now defined exactly in SI units as

$$
\boxed{c=299\,792\,458\,\mathrm{m\,s^{-1}}}.
$$

Historically, the goal was to **measure** $c$; in the modern SI, $c$ fixes the meter relative to the second. Measurement experiments remain excellent illustrations of propagation and timing physics.

## 21.2 Fizeau Method

A light beam passes through a gap in a rotating toothed wheel, travels to a distant mirror at distance $D$, and returns toward the wheel. At a suitable rotation speed, the returning beam is intercepted by the next tooth rather than passing through its original gap.

If the wheel has $N$ teeth alternating with $N$ gaps and rotates at $f_w$ revolutions per second, the time to advance from a gap to the next tooth is

$$
\Delta t=\frac1{2Nf_w}.
$$

At the **first extinction**, the light round-trip time is $2D/c=\Delta t$. Hence

$$
\boxed{c=4NDf_w}.
$$

This expression is for the first extinction and the stated counting convention. Higher extinction conditions require the appropriate tooth/gap timing multiple. The method needs a long path because light transit time is very small.

## 21.3 Foucault Method

Foucault used a rotating mirror to turn short optical transit time into an angular change. A light beam reflects from a rapidly rotating plane mirror, travels to a second mirror, and returns to the rotating mirror.

During the round trip, the first mirror rotates through

$$
\Delta\theta=\Omega\Delta t,
$$

where $\Omega$ is its angular speed. Because the direction of a reflected ray changes by twice the change in mirror angle, the returning image experiences a small deflection approximately

$$
\boxed{\Delta\alpha\simeq2\Omega\Delta t}.
$$

The optical arrangement converts this angle into a measurable lateral image displacement. The exact conversion depends on mirror spacing and imaging geometry. Compared with Fizeau's large outdoor baseline, Foucault's layout can work in a smaller laboratory apparatus.

## 21.4 Michelson Method

Michelson refined rotating-mirror time-of-flight measurements by improving optical alignment, path length and timing sensitivity. In a polygonal-mirror arrangement, a beam returns after a known total distance $D$ and enters the telescope when the polygon rotates by one face spacing during the transit.

For a mirror with $N$ equal faces at rotation frequency $f_w$,

$$
\Delta t=\frac1{Nf_w}.
$$

If $D$ denotes the **total optical distance travelled between successive interactions with the rotating polygon**, then

$$
\boxed{c=DNf_w}.
$$

If one instead denotes the one-way length by $L$, then $D=2L$ and $c=2LNf_w$. These relations depend on the specified image-restoration condition and optical path definition; they are not interchangeable without checking geometry.

**Part VII takeaway:** The old experiments all exploit $\text{distance}=c\times\text{time}$. Mechanical modulation or mirror rotation makes a minuscule optical transit interval observable.

---

# Part VIII: Photometry

Radiometry describes electromagnetic energy transport. Photometry weights visible radiation according to the human eye's average response. Equal optical powers at different wavelengths need not appear equally bright.

## 22.1 Total Radiant Flux

**Radiant flux** is radiant energy transferred per unit time:

$$
\boxed{\Phi_e=\frac{dE}{dt}}.
$$

Its SI unit is the **watt**. Total radiant flux includes radiation across all relevant wavelengths, whether visible, ultraviolet, infrared or other bands.

For a distribution over wavelength,

$$
\Phi_e=\int\frac{d\Phi_e}{d\lambda}\,d\lambda.
$$

Radiant power is an energy-rate quantity, not a measure of visual brightness.

## 22.2 Luminosity of Radiant Flux

The average eye's sensitivity is wavelength-dependent. Under photopic (daylight-adapted) conditions, it is greatest near green-yellow light around $555\,\mathrm{nm}$ and falls toward the ends of the visible spectrum.

Let $V(\lambda)$ be the **relative luminous sensitivity**, normalized so its peak is 1. The same radiant power may correspond to different luminous outputs because different wavelengths receive different values of $V(\lambda)$.

This sensitivity curve is a property of human vision under the adopted observation conditions, not an additional physical energy carried by the light.

## 22.3 Luminous Flux: Relative Luminosity

The photometrically weighted counterpart of radiant flux is **luminous flux**, written $\Phi_v$, measured in **lumens (lm)**. A modern photometric conversion uses the luminous-efficacy constant $K_m=683\,\mathrm{lm\,W^{-1}}$ for the maximum photopic response:

$$
\boxed{\Phi_v=683\int V(\lambda)\frac{d\Phi_e}{d\lambda}\,d\lambda}.
$$

For monochromatic light,

$$
\boxed{\Phi_v=683\,V(\lambda)\Phi_e}.
$$

**Textbook convention note:** Some numerical examples in the supplied HCV edition use $685\,\mathrm{lm\,W^{-1}}$ at $555\,\mathrm{nm}$. The equations here use the modern standardized $683\,\mathrm{lm\,W^{-1}}$; when checking an HCV numerical answer, retain the coefficient used in that particular example.

## 22.4 Luminous Efficiency

**Luminous efficacy of radiation** compares visible-light output to the radiant power producing it:

$$
\boxed{K=\frac{\Phi_v}{\Phi_e}}\qquad(\mathrm{lm\,W^{-1}}).
$$

For a source driven by electrical input power $P_{\mathrm{in}}$, **overall luminous efficacy** instead uses

$$
\boxed{K_{\mathrm{overall}}=\frac{\Phi_v}{P_{\mathrm{in}}}}.
$$

The denominators are different. A source can be efficient at converting electricity into radiation but inefficient at producing radiation where human vision is most sensitive, or vice versa. The quantity in lm/W is often called *luminous efficacy*, not dimensionless thermodynamic efficiency.

## 22.5 Luminous Intensity or Illuminating Power

**Luminous intensity** in a specified direction is the luminous flux emitted per unit solid angle:

$$
\boxed{I_v=\frac{d\Phi_v}{d\Omega}}.
$$

The unit is the **candela (cd)**, equal to lumen per steradian. An isotropic point source with total luminous flux $\Phi_v$ has

$$
\boxed{I_v=\frac{\Phi_v}{4\pi}}.
$$

This differs from illuminance at a surface. An ideal point source's intensity does not fall with distance, but the flux intercepted by a fixed area does.

## 22.6 Illuminance

**Illuminance** measures incident luminous flux per unit area on a receiving surface:

$$
\boxed{E_v=\frac{d\Phi_v}{dA}}.
$$

Its SI unit is the **lux**, $1\,\mathrm{lx}=1\,\mathrm{lm\,m^{-2}}$. The orientation of the illuminated area matters because it determines the solid angle that area subtends as seen from the light source.

## 22.7 Inverse Square Law

A point source emitting luminous intensity $I_v$ toward a small area $dA$ at distance $r$ sends flux into the solid angle

$$
d\Omega=\frac{dA\cos\theta}{r^2},
$$

where $\theta$ is the angle between the surface normal and the ray direction. Therefore

$$
d\Phi_v=I_vd\Omega.
$$

Dividing by the area gives

$$
\boxed{E_v=\frac{I_v\cos\theta}{r^2}}.
$$

At normal incidence,

$$
\boxed{E_v=\frac{I_v}{r^2}}.
$$

This inverse-square result assumes a sufficiently point-like source in a nonabsorbing medium, without significant reflections or obstructions.

## 22.8 Lambert's Cosine Law

For an ideal diffusely emitting plane surface, luminous intensity observed in a direction making angle $\theta$ with the surface normal follows approximately

$$
\boxed{I_v(\theta)=I_v(0)\cos\theta}.
$$

This is **Lambert's cosine law** for a Lambertian emitter. The cosine appears because the projected emitting area becomes smaller at oblique viewing directions.

Do not confuse this **source-emission cosine** with the **receiver-orientation cosine** in illuminance. Both can occur in the same optical calculation, and then each must be accounted for at its respective surface.

## 22.9 Photometers

A classical visual photometer compares light sources by adjusting distances until two equally oriented target regions appear equally illuminated. With sources treated as point-like, facing the targets normally,

$$
E_1=\frac{I_1}{r_1^2},\qquad E_2=\frac{I_2}{r_2^2}.
$$

At equal illuminance, $E_1=E_2$, so

$$
\boxed{\frac{I_1}{I_2}=\frac{r_1^2}{r_2^2}}.
$$

A grease-spot or Bunsen-type photometer uses the appearance of a translucent patch to detect approximately equal illumination from two sides. Accurate comparison also requires attention to source spectra, viewing geometry and observer response.

**Part VIII takeaway:** Watts describe radiant power, lumens describe visually weighted power, candelas describe luminous flux per solid angle, and lux describes incident luminous flux per area. They answer different measurement questions.

---
# Consolidated Formula Sheet

Use this as a rapid revision index. For an unfamiliar problem, first identify whether its assumptions match the formula.

## Wave Motion and Waves on a String (Chapter 15)

| Quantity or relation | Formula | Conditions / interpretation |
|---|---|---|
| Right-moving profile | $y=g(x-vt)$ | Rigidly translating waveform |
| Left-moving profile | $y=g(x+vt)$ | Rigidly translating waveform |
| Harmonic wave | $y=A\sin(\omega t-kx+\phi_0)$ | Right-moving sinusoid |
| Wave relationships | $\omega=2\pi f$, $k=2\pi/\lambda$, $v=f\lambda=\omega/k$ | Periodic travelling wave |
| String speed | $v=\sqrt{F/\mu}$ | Uniform ideal string, small slopes |
| Particle velocity | $v_y=\partial y/\partial t$ | Not the propagation velocity |
| Mean transmitted power | $\langle P\rangle=\tfrac12\mu v\omega^2A^2$ | Sinusoidal travelling wave |
| Two-wave amplitude | $R^2=A_1^2+A_2^2+2A_1A_2\cos\delta$ | Same frequency and polarization |
| Fixed–fixed string | $f_n=nv/(2L)$ | Both displacement nodes |
| Fixed–free string | $f_n=(2n-1)v/(4L)$ | One node, one antinode |
| Standing-wave form | $y=2A\sin\omega t\cos kx$ | Equal counterpropagating waves |
| Node spacing | $\lambda/2$ | Adjacent nodes |

## Sound Waves (Chapter 16)

| Quantity or relation | Formula | Conditions / interpretation |
|---|---|---|
| Compressional pressure | $\Delta p=-B\,\partial\xi/\partial x$ | Small longitudinal displacement |
| Sound speed | $v=\sqrt{B/\rho}$ | Effective bulk modulus $B$ |
| Ideal-gas sound speed | $v=\sqrt{\gamma p/\rho}=\sqrt{\gamma RT/M}$ | Adiabatic ideal-gas approximation |
| Pressure amplitude | $p_m=\rho v\omega\xi_m$ | Plane sinusoidal sound |
| Intensity | $I=\tfrac12\rho v\omega^2\xi_m^2=p_m^2/(2\rho v)$ | Plane harmonic sound |
| Isotropic sound spreading | $I=P/(4\pi r^2)$ | No absorption, point source |
| Sound intensity level | $\beta=10\log_{10}(I/I_0)$ dB | Specify reference $I_0$ |
| Open–open tube | $f_n=nv/(2L)$ | Effective tube length |
| Closed–open tube | $f_n=(2n-1)v/(4L)$ | Effective tube length |
| Resonance tube | $v=2f(L_2-L_1)$ | Adjacent resonances |
| Beats | $f_b=|f_1-f_2|$ | Nearby frequencies |
| Doppler sound | $f'=f(v+v_o)/(v-v_s)$ | $v_o$ toward source, $v_s$ toward observer |
| Mach angle | $\sin\mu=1/M_a$ | Supersonic source |

## Light Waves (Chapter 17)

| Quantity or relation | Formula | Conditions / interpretation |
|---|---|---|
| Vacuum relation | $c=f\lambda_0$ | EM waves in vacuum |
| Medium speed | $v=c/n$ | Phase speed in ordinary transparent medium |
| Snell's law | $n_1\sin i=n_2\sin r$ | Refraction at an interface |
| Optical path length | $\mathrm{OPL}=\int n(s)\,ds$ | Phase accumulated along path |
| Path phase | $\Delta\phi=2\pi\Delta(\mathrm{OPL})/\lambda_0$ | Add interface phase changes |
| Two-beam intensity | $I=I_1+I_2+2\sqrt{I_1I_2}\cos\delta$ | Coherent common polarization |
| Double-slit fringe width | $\beta=\lambda D/d$ | Far-field, small angles |
| Film propagation OPD | $2nt\cos r$ | Film thickness $t$ |
| Single-slit zeros | $a\sin\theta=m\lambda$ | Fraunhofer diffraction, $m\ne0$ |
| Single-slit intensity | $I=I_0(\sin\alpha/\alpha)^2$ | $\alpha=\pi a\sin\theta/\lambda$ |
| Circular-aperture angle | $\theta\simeq1.22\lambda/D$ | First Airy minimum |
| Malus' law | $I=I_0\cos^2\theta$ | Linear polarization and ideal analyzer |
| Brewster angle | $\tan\theta_B=n_2/n_1$ | Ordinary dielectric interface |

## Geometrical Optics (Chapter 18)

| Quantity or relation | Formula | Conditions / interpretation |
|---|---|---|
| Mirror formula | $1/u+1/v=1/f$ | Cartesian signed distances |
| Mirror focal length | $f=R/2$ | Paraxial spherical mirror |
| Mirror magnification | $m=-v/u$ | Transverse magnification |
| Apparent depth | $d'/d\simeq n_2/n_1$ | Near-normal plane refraction |
| Critical angle | $\sin\theta_c=n_2/n_1$ | $n_1>n_2$ |
| Prism minimum deviation | $n=\sin[(A+\delta_m)/2]/\sin(A/2)$ | Prism in air |
| Thin prism deviation | $\delta\simeq(n-1)A$ | Small-angle prism |
| Spherical refraction | $n_2/v-n_1/u=(n_2-n_1)/R$ | Paraxial single interface |
| Spherical-interface mag. | $m=n_1v/(n_2u)$ | Signed distances |
| Thin-lens formula | $1/v-1/u=1/f$ | Thin paraxial lens |
| Lens maker | $1/f=(n_\ell/n_m-1)(1/R_1-1/R_2)$ | Thin lens, common outer medium |
| Lens magnification | $m=v/u$ | Signed distances |
| Lens power | $P=1/f\ (f\text{ in meters})$ | Dioptres |
| Lenses in contact | $P=P_1+P_2$ | Negligible separation |
| Separated lenses | $P=P_1+P_2-dP_1P_2$ | Equivalent system power |

## Instruments, Dispersion, Light Speed and Photometry (Chapters 19–22)

| Quantity or relation | Formula | Conditions / interpretation |
|---|---|---|
| Simple magnifier, infinity | $M=D/f$ | Eye near lens |
| Simple magnifier, near point | $M=1+D/f$ | Standard viewing convention |
| Compound microscope, infinity | $|M|\simeq(L/f_o)(D/f_e)$ | Effective tube-length approximation |
| Astronomical telescope | $M=-f_o/f_e$ | Normal adjustment |
| Telescope Rayleigh limit | $\theta_{\min}\simeq1.22\lambda/D_o$ | Ideal circular pupil |
| Microscope feature limit | $d_{\min}\simeq\lambda/(2n\sin\alpha)$ | Abbe-style estimate |
| Thin prism angular spread | $\Delta\delta\simeq(n_v-n_r)A$ | Normal visible dispersion |
| Dispersive power | $\omega=(n_v-n_r)/(n_y-1)$ | Selected spectral lines |
| Fizeau first extinction | $c=4NDf_w$ | $N$ teeth, one-way mirror distance $D$ |
| Michelson polygon | $c=DNf_w$ | $D$ total transit path, $N$ faces |
| Radiant flux | $\Phi_e=dE/dt$ | W |
| Luminous flux | $\Phi_v=683\int V(\lambda)d\Phi_e$ | lm; wavelength-integral shorthand |
| Luminous intensity | $I_v=d\Phi_v/d\Omega$ | cd = lm/sr |
| Illuminance | $E_v=d\Phi_v/dA$ | lux = lm/m$^2$ |
| Point-source illuminance | $E_v=I_v\cos\theta/r^2$ | Negligible absorption |
| Lambertian emission | $I_v(\theta)=I_v(0)\cos\theta$ | Diffuse planar source |
| Photometer ratio | $I_1/I_2=r_1^2/r_2^2$ | Equal illuminance at equal orientations |

---

# Integrated Worked Examples

Each problem is independently constructed for revision and does not reproduce HCV's worked examples. Wherever a calculation depends on a model, the model is stated.

## Example A: Wave speed, wavelength and standing-string resonance

**Problem.** A taut string has tension $F=49\,\mathrm N$, linear density $\mu=0.010\,\mathrm{kg\,m^{-1}}$, and length $L=0.70\,\mathrm m$ between fixed supports. Find its wave speed, its fundamental frequency and the wavelength of its third harmonic.

The transverse wave speed is

$$
v=\sqrt{\frac{49}{0.010}}=70\,\mathrm{m\,s^{-1}}.
$$

With fixed nodes at both ends,

$$
f_1=\frac v{2L}=\frac{70}{1.40}=50\,\mathrm{Hz}.
$$

For the third harmonic, $L=3\lambda_3/2$, so

$$
\lambda_3=\frac{2L}{3}=\frac{1.40}{3}\simeq0.467\,\mathrm m.
$$

**Answer:** $\boxed{v=70\,\mathrm{m\,s^{-1}},\ f_1=50\,\mathrm{Hz},\ \lambda_3\simeq0.467\,\mathrm m}$. The third-harmonic frequency is $150\,\mathrm{Hz}$.

## Example B: Power carried by a harmonic string wave

**Problem.** A string has $\mu=0.020\,\mathrm{kg\,m^{-1}}$ and wave speed $v=40\,\mathrm{m\,s^{-1}}$. A small right-moving wave has amplitude $A=2.0\,\mathrm{mm}$ and frequency $f=25\,\mathrm{Hz}$. Find its average power flow.

First,

$$
\omega=2\pi f=50\pi\,\mathrm{rad\,s^{-1}}.
$$

Therefore

$$
\langle P\rangle=\frac12(0.020)(40)(50\pi)^2(0.002)^2
\simeq3.95\times10^{-2}\,\mathrm W.
$$

**Answer:** $\boxed{\langle P\rangle\simeq0.0395\,\mathrm W}$. If amplitude doubles at unchanged frequency and string properties, average power quadruples.

## Example C: Two-source wave interference

**Problem.** Two coherent transverse waves have equal amplitude $A$ and phase separation $120^\circ$ at a point. What is their resultant displacement amplitude?

Use

$$
R^2=2A^2+2A^2\cos120^\circ.
$$

Because $\cos120^\circ=-1/2$,

$$
R^2=A^2,
\qquad
\boxed{R=A}.
$$

Interference changes the local amplitude, but this single-point result does not by itself determine energy flow over the complete spatial interference pattern.

## Example D: Air-column resonance and end correction

**Problem.** An open–closed air column resonates at $200\,\mathrm{Hz}$. Take the speed of sound as $340\,\mathrm{m\,s^{-1}}$. Estimate the effective length at the fundamental.

For a closed–open tube,

$$
f_1=\frac v{4L_{\mathrm{eff}}}.
$$

Hence

$$
L_{\mathrm{eff}}=\frac{340}{4(200)}=0.425\,\mathrm m.
$$

**Answer:** $\boxed{L_{\mathrm{eff}}=42.5\,\mathrm{cm}}$. The physical tube may be slightly shorter because the open-end displacement antinode lies just outside the opening.

## Example E: Doppler shift of a moving source

**Problem.** A source emits $400\,\mathrm{Hz}$ while moving at $20\,\mathrm{m\,s^{-1}}$ toward a stationary listener. Take sound speed $340\,\mathrm{m\,s^{-1}}$. Find the observed frequency.

With observer at rest, $v_o=0$; source approaching, $v_s=+20\,\mathrm{m\,s^{-1}}$:

$$
f'=f\frac v{v-v_s}=400\frac{340}{340-20}.
$$

Therefore

$$
\boxed{f'=425\,\mathrm{Hz}}.
$$

A source approaching the listener makes the listener detect a **higher** pitch. Recession reverses the sign of $v_s$.

## Example F: Young's double-slit fringe width

**Problem.** Two slits are separated by $d=0.30\,\mathrm{mm}$ and illuminate a screen $D=2.0\,\mathrm m$ away with wavelength $\lambda=600\,\mathrm{nm}$. Estimate fringe spacing.

With SI conversions,

$$
\beta=\frac{\lambda D}{d}
=\frac{(600\times10^{-9})(2.0)}{0.30\times10^{-3}}
=4.0\times10^{-3}\,\mathrm m.
$$

**Answer:** $\boxed{\beta=4.0\,\mathrm{mm}}$.

## Example G: Quarter-wave thin-film coating

**Problem.** A transparent film of refractive index $n=1.50$ has air on both sides. Find the smallest nonzero thickness that maximizes reflection at normal incidence for vacuum wavelength $550\,\mathrm{nm}$, assuming the two reflected rays dominate.

The air-to-film front reflection acquires a $\pi$ phase shift, while the film-to-air reflection does not. Therefore constructive reflection for the smallest positive thickness requires

$$
2nt=\frac{\lambda_0}{2}.
$$

Thus

$$
t=\frac{\lambda_0}{4n}=\frac{550}{4(1.50)}\,\mathrm{nm}.
$$

**Answer:** $\boxed{t\simeq91.7\,\mathrm{nm}}$. An anti-reflection coating generally has a different surrounding-index ordering and uses the appropriate reflection phases and amplitude balance; a quarter-wave thickness alone does not automatically imply anti-reflection.

## Example H: Single-slit diffraction angle

**Problem.** A slit has width $a=0.10\,\mathrm{mm}$ and is illuminated by $\lambda=500\,\mathrm{nm}$ light. Find the angle of the first dark minimum.

Use $a\sin\theta=\lambda$:

$$
\sin\theta=\frac{500\times10^{-9}}{0.10\times10^{-3}}=0.005.
$$

For a small angle, $\theta\simeq\sin\theta$, giving

$$
\boxed{\theta\simeq5.0\times10^{-3}\,\mathrm{rad}\simeq0.286^\circ}.
$$

Reducing slit width increases the diffraction angular spread.

## Example I: Concave-mirror image

**Problem.** A concave mirror has focal length $f=-20\,\mathrm{cm}$. An object is at $u=-60\,\mathrm{cm}$ in HCV's Cartesian convention. Find image location and magnification.

Apply $1/u+1/v=1/f$:

$$
\frac1v=\frac1f-\frac1u=-\frac1{20}+\frac1{60}=-\frac1{30}.
$$

Hence $v=-30\,\mathrm{cm}$. Its magnification is

$$
m=-\frac vu=-\frac{-30}{-60}=-0.50.
$$

**Answer:** $\boxed{v=-30\,\mathrm{cm},\ m=-0.50}$. The image is real, inverted and half as tall as the object.

## Example J: Converging-lens image

**Problem.** A thin converging lens has $f=+10\,\mathrm{cm}$. A real object sits at $u=-15\,\mathrm{cm}$. Find image distance and signed magnification.

From $1/v-1/u=1/f$,

$$
\frac1v=\frac1f+\frac1u=\frac1{10}-\frac1{15}=\frac1{30}.
$$

Thus $v=+30\,\mathrm{cm}$ and

$$
m=\frac vu=\frac{30}{-15}=-2.
$$

**Answer:** $\boxed{v=+30\,\mathrm{cm},\ m=-2}$. The real image is twice as large and inverted.

## Example K: Two thin lenses in contact

**Problem.** A converging lens of focal length $+20\,\mathrm{cm}$ touches a diverging lens of focal length $-40\,\mathrm{cm}$. Find combined power and focal length.

Convert focal lengths to meters:

$$
P_1=\frac1{0.20}=+5.0\,\mathrm D,
\qquad
P_2=\frac1{-0.40}=-2.5\,\mathrm D.
$$

Therefore

$$
P=P_1+P_2=+2.5\,\mathrm D,
\qquad
f=\frac1P=0.40\,\mathrm m.
$$

**Answer:** $\boxed{P=+2.5\,\mathrm D,\ f=+40\,\mathrm{cm}}$.

## Example L: Telescope magnification and diffraction limit

**Problem.** An astronomical telescope in normal adjustment uses $f_o=1.0\,\mathrm m$, $f_e=25\,\mathrm{mm}$ and objective diameter $D_o=80\,\mathrm{mm}$. For $\lambda=550\,\mathrm{nm}$, find the magnification magnitude and Rayleigh angular limit.

Magnification magnitude:

$$
|M|=\frac{1.0}{0.025}=40.
$$

Angular resolution:

$$
\theta_{\min}=1.22\frac{550\times10^{-9}}{0.080}
\simeq8.39\times10^{-6}\,\mathrm{rad}.
$$

**Answer:** $\boxed{|M|=40,\ \theta_{\min}\simeq8.39\,\mu\mathrm{rad}}$. Increasing eyepiece magnification alone does not improve this objective-aperture diffraction limit.

## Example M: Prism deviation and dispersion

**Problem.** A thin prism has angle $A=4^\circ$, with $n_r=1.500$ and $n_v=1.520$. Estimate red deviation, violet deviation and angular color separation.

Use $\delta\simeq(n-1)A$:

$$
\delta_r\simeq(1.500-1)(4^\circ)=2.00^\circ,
$$

$$
\delta_v\simeq(1.520-1)(4^\circ)=2.08^\circ.
$$

So

$$
\boxed{\Delta\delta\simeq0.08^\circ}.
$$

This uses the thin-prism small-angle approximation; for a larger prism the full refraction geometry is required.

## Example N: Fizeau wheel speed

**Problem.** A Fizeau-style wheel has $N=720$ teeth and a one-way reflecting mirror distance $D=8.63\,\mathrm{km}$. Estimate the first-extinction wheel frequency using $c\simeq3.00\times10^8\,\mathrm{m\,s^{-1}}$.

At the first extinction,

$$
f_w=\frac c{4ND}.
$$

Substitution gives

$$
f_w=\frac{3.00\times10^8}{4(720)(8630)}\simeq12.1\,\mathrm{rev\,s^{-1}}.
$$

**Answer:** $\boxed{f_w\simeq12.1\,\mathrm{Hz}}$. The rate is mechanically manageable although the light round trip is extremely short.

## Example O: Illuminance on an inclined surface

**Problem.** A point source has luminous intensity $I_v=100\,\mathrm{cd}$ toward a patch at $r=2.0\,\mathrm m$. The patch normal makes $60^\circ$ with the incoming ray. Find illuminance.

$$
E_v=\frac{I_v\cos\theta}{r^2}=
\frac{100\cos60^\circ}{2.0^2}.
$$

Thus

$$
\boxed{E_v=12.5\,\mathrm{lx}}.
$$

If the patch turns to face the source normally at the same distance, illuminance doubles to $25\,\mathrm{lx}$.

## Example P: Visual weighting of monochromatic light

**Problem.** A monochromatic source emits $2.0\,\mathrm W$ of visible radiant flux at a wavelength where $V(\lambda)=0.80$. Find luminous flux using the modern photometric coefficient.

$$
\Phi_v=683(0.80)(2.0)=1092.8\,\mathrm{lm}.
$$

**Answer:** $\boxed{\Phi_v\simeq1.09\times10^3\,\mathrm{lm}}$. A source of equal radiant power at peak sensitivity would produce more lumens.

---
# Common Misconceptions and Diagnostic Questions

| Misconception | Correct principle |
|---|---|
| "A wave carries the medium bodily across space." | A mechanical wave generally propagates through local oscillations of the medium. |
| "A particle on a vibrating string moves at the wave speed." | Local transverse particle velocity and longitudinal wave speed are different quantities. |
| "A wave must be sinusoidal." | Any sufficiently smooth translated profile can be a travelling wave in an ideal nondispersive medium. |
| "Higher amplitude automatically makes a string wave faster." | In the small-amplitude ideal-string approximation, $v=\sqrt{F/\mu}$ does not depend on amplitude. |
| "The frequency changes when a wave enters a different medium." | At a stationary boundary, driving frequency remains the same; phase speed and wavelength can change. |
| "Constructive interference violates energy conservation." | Interference redistributes energy; the integrated energy balance remains valid. |
| "Standing waves carry as much average power forward as travelling waves." | An ideal standing wave is the sum of equal opposite power flows, yielding zero net time-average transfer. |
| "Every standing-wave system has all integer harmonics." | Allowed harmonics depend on the boundary conditions. |
| "A free end and a fixed end produce identical reflected pulse phase." | Ideal fixed ends invert transverse displacement; ideal free ends do not. |
| "Pressure and displacement nodes coincide in a sound tube." | In longitudinal acoustic standing waves they are typically complementary. |
| "Newton's isothermal formula accurately describes ordinary sound in air." | Sound compression is usually better approximated as adiabatic, giving Laplace's $\gamma$ factor. |
| "Sound speed rises with ordinary gas pressure at constant temperature." | In an ideal gas with fixed composition, the pressure cancels against density. |
| "The sound source and listener velocities are interchangeable in the Doppler formula." | They play distinct roles because sound propagates relative to its medium. |
| "A sonic boom happens only when the aircraft first exceeds sound speed." | A sustained supersonic source generates shock structures continuously. |
| "Interference proves light always behaves like a classical wave." | Interference is one aspect of light; other observations require a quantum description. |
| "Two independent bulbs of the same color will form stable Young fringes." | Stable mutual phase is necessary for persistent fringes. |
| "A thicker film must always have greater reflected brightness." | Interference depends periodically on optical path and reflection phase. |
| "A ray reflecting from any surface undergoes a $\pi$ phase reversal." | Relative index ordering determines the conventional reflection phase rule. |
| "Narrowing a single slit narrows its central diffraction maximum." | Narrowing a slit broadens the angular diffraction envelope. |
| "An ideal lens makes a point image of an infinitely distant point source." | Diffraction produces a finite Airy spot for a finite aperture. |
| "Magnifying a diffraction-limited image improves optical resolution." | It only enlarges existing detail and blur. |
| "Only transverse elastic waves can be polarized." | Electromagnetic light is also transverse and can have several polarization states. |
| "The magnification formula is identical for lenses and mirrors." | With HCV Cartesian coordinates, $m=v/u$ for lenses and $m=-v/u$ for mirrors. |
| "All object and image distances are positive by definition." | Image equations require explicitly signed Cartesian coordinates. |
| "A convex lens always converges light in any surrounding medium." | Converging power depends on the refractive-index contrast and surface geometry. |
| "Total internal reflection can occur when going from air into glass." | For ordinary transparent media it requires light moving from higher to lower refractive index. |
| "A pair of separated thin lenses can be placed at one lens location and treated as the contact equivalent." | System principal planes generally shift; use sequential imaging or the full system matrix. |
| "Lens power and focal length have the same sign for every sign convention." | The relation $P=1/f$ is meaningful only with the stated focal sign convention. |
| "A telescope with higher magnification always resolves finer stars." | Aperture and wavelength govern the ideal diffraction limit. |
| "Increasing a microscope's tube length automatically improves resolution." | It increases magnification in simple models, but not the numerical-aperture diffraction limit. |
| "Dispersion and diffraction are the same thing." | Dispersion arises from wavelength-dependent propagation in a medium; diffraction from wavefront restriction and interference. |
| "A combination giving zero mean deviation must give zero color dispersion." | Two-prism combinations can have zero mean deviation but nonzero wavelength spread. |
| "Rainbows are stationary colored objects at a definite distance." | Their direction is determined by sunlight, droplets and observer geometry. |
| "The old Fizeau speed-of-light formula works without knowing whether path length is one-way or round-trip." | Optical path and wheel counting conventions determine numerical factors. |
| "One watt of any visible wavelength corresponds to the same number of lumens." | Luminous flux is weighted by the eye's wavelength sensitivity. |
| "Candela, lumen and lux are interchangeable names for brightness." | They respectively measure flux per solid angle, total visually weighted flux and flux per area. |
| "A source's luminous intensity falls as $1/r^2$." | For a point source, intensity per solid angle is distance-independent; received illuminance falls as $1/r^2$. |
| "Lambert's law and inverse-square illumination are the same cosine law." | One cosine describes directional emission; the other the receiving surface's projected area. |

---

# Active-Recall Checkpoints

Do not start by looking at the equation sheet. First write the physical assumptions, choose coordinates, and explain why the selected relationship follows.

### Chapter 15: Wave Motion and Waves on a String

1. What is transported by a mechanical wave and what generally remains localized?
2. Explain the physical meanings of $y(x,t)=g(x-vt)$ and $y(x,t)=g(x+vt)$.
3. Derive the one-dimensional wave equation from a translating smooth profile.
4. Distinguish $\partial y/\partial t$ from $\omega/k$ for a sinusoidal string wave.
5. Derive $v=f\lambda$ from constant phase.
6. Use a short string element to obtain $v=\sqrt{F/\mu}$.
7. Derive the instantaneous and time-average power transmitted by a harmonic string wave.
8. Explain why the resultant of two equal-amplitude coherent waves can range from zero to twice the individual amplitude.
9. Derive reflection and transmission displacement coefficients at a junction of ideal strings under common tension.
10. Explain pulse reflection at fixed and free ends using boundary constraints.
11. Construct a standing wave from counterpropagating waves and identify nodes and antinodes.
12. Derive all allowed frequencies for a string fixed at both ends.
13. Derive the spatial factor $\sin(n\pi x/L)$ from the boundary conditions.
14. Derive the odd-harmonic sequence for a fixed–free string.
15. Explain the three sonometer laws and specify which variables are held fixed.
16. Distinguish transverse from longitudinal mechanical waves and relate polarization to direction of displacement.

### Chapter 16: Sound Waves

17. Explain compressions and rarefactions in terms of pressure, density and local displacement.
18. Derive $\Delta p=-B\partial\xi/\partial x$ for small one-dimensional displacement.
19. Why are pressure and displacement waves phase-shifted by a quarter cycle in a travelling sound wave?
20. Derive acoustic wave speed from a material's bulk modulus and density.
21. Why is sound propagation in air usually treated as adiabatic rather than isothermal?
22. Starting from $pV^\gamma=\text{constant}$, derive Laplace's corrected speed of sound.
23. Predict changes in sound speed when temperature rises or humidity increases.
24. Derive the relationship between sound pressure amplitude and displacement amplitude.
25. Derive plane-wave intensity in terms of $p_m$, $\rho$ and sound speed.
26. Explain the difference between intensity, intensity level, pitch, loudness and timbre.
27. Why do sound tubes exhibit complementary pressure and displacement boundary conditions?
28. Derive the resonance series of an open–open air column.
29. Derive the resonance series of a closed–open air column and explain end correction.
30. Show why adjacent resonances of a closed–open resonance tube differ in effective length by $\lambda/2$.
31. Obtain the beat frequency from the sum of two nearby frequencies.
32. Explain diffraction of sound around a large obstacle.
33. Derive the moving-source and moving-observer Doppler formula from the medium frame.
34. Define Mach number and derive the supersonic Mach-cone angle.
35. Why do room acoustics depend on reflection and reverberation as well as source power?

### Chapter 17: Light Waves

36. Which observations motivate the wave description and which motivate the quantum description of light?
37. State the relative directions of electric field, magnetic field and propagation for a plane EM wave.
38. Use Huygens' construction to obtain Snell's law.
39. Explain how Young's double-hole experiment creates mutual coherence.
40. Derive the two-source interference intensity relation for unequal source intensities.
41. Obtain the bright- and dark-fringe path-difference conditions.
42. Derive the double-slit fringe-width expression and identify all small-angle assumptions.
43. Define optical path length and convert an OPL difference into phase difference.
44. Explain the reflection phase inversion rule for a thin film.
45. Derive reflected-light bright and dark conditions for a film with exactly one reflection phase reversal.
46. Explain how Fresnel's biprism forms coherent virtual sources.
47. Distinguish temporal coherence from spatial coherence.
48. Explain the distinction between Fraunhofer and Fresnel diffraction.
49. Derive the first single-slit diffraction minimum using contributions from paired parts of the slit.
50. Why is the central single-slit maximum twice the angular width between zeros of a typical neighboring region?
51. Explain why a finite circular aperture forms an Airy pattern rather than a point image.
52. Derive the qualitative dependence of angular resolution on aperture size and wavelength.
53. Explain how a straight edge creates oscillations near a geometrical shadow boundary.
54. Under what conditions does Rayleigh's fourth-power scattering law apply?
55. Describe linear, circular and elliptical polarization using transverse electric-field components.
56. Derive Malus' law from electric-field projection and intensity proportionality.

### Chapter 18: Geometrical Optics

57. State HCV's Cartesian sign convention and its effect on object and image coordinates.
58. Explain where paraxial approximation enters spherical-mirror ray construction.
59. Derive the spherical-mirror formula using small reflection angles.
60. Show why the paraxial focal length of a spherical mirror is $R/2$.
61. Derive mirror lateral magnification and interpret its sign.
62. Explain apparent depth at a plane refracting interface using Snell's law.
63. Derive the critical-angle relation and identify which direction supports total internal reflection.
64. Describe the physical requirements for light guidance inside an optical fiber.
65. Derive $r_1+r_2=A$ and $\delta=i+e-A$ for a prism.
66. Why is the path through a prism symmetric at minimum deviation?
67. Derive the refractive-index formula for a prism using minimum deviation.
68. Starting with paraxial Snell's law, obtain the imaging relation for a spherical refracting interface.
69. Why does magnification at a single refracting surface contain a refractive-index ratio?
70. Derive the thin-lens maker's equation by combining two spherical refractions.
71. Explain why thin lenses obey $1/v-1/u=1/f$ under this convention.
72. Compare the image position and orientation produced by converging and diverging lenses.
73. Define lens power and explain why a negative lens has negative power.
74. Derive the combined power of thin lenses in contact.
75. Explain why separated lenses generally require shifted principal planes.
76. Distinguish spherical aberration, chromatic aberration, coma and distortion.

### Chapter 19: Optical Instruments

77. Explain the roles of cornea, eye lens, retina and accommodation.
78. Distinguish near point from far point and describe the conventional reference distance $D$.
79. Explain why apparent size depends on angle rather than only physical object height.
80. Derive simple microscope angular magnification for a final image at infinity.
81. Derive simple microscope angular magnification for a final image at the near point.
82. Explain how a compound microscope combines objective and eyepiece magnifications.
83. Distinguish astronomical and Galilean telescope configurations and image orientations.
84. Derive the astronomical telescope's normal-adjustment magnification.
85. Explain the role of objective diameter in telescope resolution.
86. Define numerical aperture and explain why immersion oil can improve microscope resolution.
87. Explain optical corrections for myopia, hypermetropia and astigmatism.

### Chapter 20: Dispersion and Spectra

88. What material property causes color-dependent refraction through a prism?
89. Derive angular dispersion of a thin prism between two selected wavelengths.
90. Define prism dispersive power and explain why its thin-prism value is largely independent of prism angle.
91. Construct a two-prism combination with zero mean deviation but nonzero dispersion.
92. Construct an achromatic prism combination with nonzero mean deviation.
93. Distinguish continuous emission, line emission and absorption spectra.
94. Explain how a prism spectrometer measures refractive index using minimum deviation.
95. Explain primary and secondary rainbow color ordering from the number of internal reflections.

### Chapter 21: Speed of Light

96. Why can astronomical timing reveal a finite speed of light?
97. Derive the first-extinction condition in Fizeau's toothed-wheel method.
98. Explain how Foucault's rotating mirror turns transit time into angular image displacement.
99. State the meaning of optical path $D$ and mirror-face count $N$ in Michelson's polygon method.
100. Why is the modern SI numerical value of vacuum light speed exact rather than experimentally uncertain?

### Chapter 22: Photometry

101. Distinguish radiant flux from luminous flux.
102. Explain why equal radiant powers at two visible wavelengths may produce different luminous fluxes.
103. Interpret the photopic eye-sensitivity function $V(\lambda)$.
104. Distinguish luminous efficacy of radiation from overall electrical luminous efficacy.
105. Define luminous intensity and explain its unit candela.
106. Derive the inverse-square illuminance equation including the receiving-surface cosine factor.
107. Differentiate source intensity, incident illuminance and perceived brightness.
108. Explain Lambert's cosine law for an ideal diffuse plane emitter.
109. Derive the photometer distance-squared intensity ratio from equal illuminance.
110. Why must HCV's numerical coefficient for luminous flux be checked before comparing textbook solutions?

---

## Source and scope

**Primary reference:** H. C. Verma, *Concepts of Physics*, Volume 1, Chapters **15–22** (textbook pp. **303–455**):

- Chapter 15: *Wave Motion and Waves on a String*, §§15.1–15.15.
- Chapter 16: *Sound Waves*, §§16.1–16.16.
- Chapter 17: *Light Waves*, §§17.1–17.16.
- Chapter 18: *Geometrical Optics*, §§18.1–18.17.
- Chapter 19: *Optical Instruments*, §§19.1–19.7.
- Chapter 20: *Dispersion and Spectra*, §§20.1–20.8.
- Chapter 21: *Speed of Light*, §§21.1–21.4.
- Chapter 22: *Photometry*, §§22.1–22.9.

These notes follow the textbook's sequence and core theory but are a **self-contained, original synthesis**. The integrated examples and active-recall prompts are original. Modern terminology, contextual clarifications and a few explicitly identified approximation/engineering extensions (such as Sabine reverberation time, optical-fiber numerical aperture, principal-plane interpretation and current photometric normalization) are provided to make the notes more useful for contemporary revision. They should not be mistaken for verbatim HCV passages or for claims that every extension appears in the chapter under that heading.

**Study method:** Read the corresponding HCV theory first or alongside each section. Derive the boxed equations from assumptions. Attempt the textbook's worked examples and exercises independently, then use this unit's examples, formula sheet, misconception table and active-recall questions to test whether the concepts transfer to new problems.
