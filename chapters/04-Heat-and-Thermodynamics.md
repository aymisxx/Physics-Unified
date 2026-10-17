# Unit 04: Heat and Thermodynamics

**Heat and Temperature → Kinetic Theory of Gases → Calorimetry → Laws of Thermodynamics → Specific Heat Capacities of Gases → Heat Transfer**  
*Original revision notes following Chapters 23–28 of H. C. Verma, Concepts of Physics, Volume 2*

> **Purpose.** Build a unified picture of thermal physics: how temperature is operationally defined, why gas pressure emerges from molecular motion, how thermal energy is exchanged, which processes are permitted by the laws of thermodynamics, and how heat travels by conduction, convection, and radiation. The chapter sequence and section numbering follow HCV; the explanations, derivations, worked problems, and recall prompts are original rather than textbook transcriptions.
>
> **Notation.** Display equations use `$$ ... $$` for GitHub rendering. Absolute temperature is $T$ (K), Celsius temperature is $\theta$ (°C), heat transferred **into** a system is $Q$, work done **by** the system is $W$, internal energy is $U$, pressure is $p$, volume is $V$, number of moles is $n$, number of molecules is $N$, and Boltzmann's constant is $k_B$. Unless indicated, gases are treated as ideal and processes as quasistatic when a $p$–$V$ curve or $\int p\,dV$ is used. Symbols such as $k$, $K$, $\alpha$, and $\gamma$ are reused locally; always read their definitions.

## Roadmap

| Part | HCV chapter | Central ideas |
|---|---|---|
| **I** | **23. Heat and Temperature** | Thermal equilibrium, thermometric scales, gas thermometers, ideal-gas law, thermal expansion |
| **II** | **24. Kinetic Theory of Gases** | Molecular origin of pressure and temperature, speed distributions, vapour, humidity, phase diagrams |
| **III** | **25. Calorimetry** | Heat capacity, specific heat, latent heat, mixture problems, mechanical equivalent of heat |
| **IV** | **26. Laws of Thermodynamics** | First and second laws, $p$–$V$ work, heat engines, entropy, reversibility, Carnot efficiency |
| **V** | **27. Specific Heat Capacities of Gases** | $C_p$ versus $C_V$, Mayer's relation, isothermal and adiabatic processes, equipartition |
| **VI** | **28. Heat Transfer** | Fourier conduction, thermal resistance, convection, blackbody radiation, cooling, thermal detectors |

**Learning sequence**

```text
Macroscopic observations of hot/cold bodies
                    |
                    v
       Thermal equilibrium + temperature
                    |
                    v
      Molecular gas model and statistics
                    |
                    v
         Heat exchange / calorimetry
                    |
                    v
    First law: energy bookkeeping (Q, W, U)
                    |
                    v
    Second law: direction + limits of engines
                    |
                    v
  Heat capacities + isothermal/adiabatic paths
                    |
                    v
  Conduction / convection / thermal radiation
```

---

# Part I: Heat and Temperature

Temperature characterizes a body's thermal state and determines the *direction* of spontaneous heat transfer. Heat is **energy in transit** due to a temperature difference; it is not a substance stored inside a body. The microscopic storage mechanisms belong to the body's **internal energy**.

## 23.1 Hot and Cold Bodies

Rubbing hands, braking a bicycle, or compressing material can warm the object because mechanical work is transformed into internal energy. When a hotter body contacts a colder one through a thermally conducting boundary, energy generally flows from the hotter body to the colder one until thermal equilibrium is reached.

Distinguish three concepts:

- **Temperature** is a state variable that tells us which way heat would flow if two bodies were thermally connected.
- **Internal energy** is a property of the thermodynamic state, associated with microscopic kinetic and potential energy.
- **Heat $Q$** labels energy transferred *during a process* because of a temperature difference. After transfer, it is no longer a separately stored quantity called “heat.”

Mechanical energy is not destroyed when friction stops a body. It generally becomes microscopic internal energy of the body and its surroundings. Temperature need not increase when energy enters: during melting or boiling, the energy may change phase at nearly constant temperature.

## 23.2 Zeroth Law of Thermodynamics

Two systems are in **thermal equilibrium** if no net heat flows between them when placed in thermal contact. The zeroth law states:

> If system $A$ is in thermal equilibrium with $B$, and $A$ is in thermal equilibrium with $C$, then $B$ and $C$ are in thermal equilibrium with each other.

This transitive property makes a temperature scale possible. A thermometer is brought into equilibrium with an object; once equilibrium occurs, their temperatures are equal. Thermometers work because many physical properties vary predictably with thermal state.

**Caution:** Equal temperature does **not** require equal internal energy, equal masses, or equal heat capacities. A cup of water and a swimming pool can have the same temperature and radically different internal energies.

## 23.3 Defining Scale of Temperature: Mercury and Resistance Thermometers

A **thermometric property** is a reproducible measured quantity $X$ that changes with temperature, for example, the length of a mercury column or the electrical resistance of a metal wire. If two reproducible reference states correspond to $X_0$ and $X_{100}$, one can assign a linear empirical scale:

$$
\boxed{\theta_X=100\frac{X-X_0}{X_{100}-X_0}\;{}^\circ\mathrm C}.
$$

For a mercury-column thermometer, $X=l$; for a resistance thermometer, $X=R$. The formula *defines* a scale from two points and a linear interpolation; it does not prove that resistance or liquid expansion is exactly linear in a more fundamental temperature.

Historical ice-point and steam-point calibrations typically use phase transitions under specified pressure. The same two fixed points can make different thermometers agree at their endpoints but disagree between them because their thermometric properties are not identical functions of absolute temperature.

For a platinum resistance thermometer the relation takes the familiar empirical form

$$
\theta_R=100\frac{R_\theta-R_0}{R_{100}-R_0}.
$$

A working thermometer must also make reliable thermal contact without excessively changing the temperature of the object being measured.

## 23.4 Constant Volume Gas Thermometer

A gas bulb is connected to a manometer. A reservoir is adjusted so that the gas occupies the **same volume** for each measurement, while the manometer determines pressure. In an open mercury-manometer arrangement:

$$
\boxed{p=p_{\mathrm{atm}}+\rho_{\mathrm{Hg}}gh}
$$

when the column geometry gives the indicated positive pressure difference; reverse the sign if the gas pressure is below atmospheric pressure.

For a sufficiently dilute gas at constant $V$ and fixed molecule number, pressure changes almost in proportion to absolute temperature:

$$
\frac{p}{T}=\text{constant}\qquad(V,n\;\text{fixed}).
$$

With a measured pressure $p_{\mathrm{tr}}$ at the triple point of water, a gas-based temperature may be assigned as

$$
\boxed{T_{\mathrm{gas}}=273.16\,\mathrm K\;\frac{p}{p_{\mathrm{tr}}}}.
$$

This is the **historical reference-point construction** discussed by HCV, not the present SI definition of the kelvin. Practical errors include gas outside the heated bulb, expansion of the container, and departures from ideal-gas behavior.

## 23.5 Ideal Gas Temperature Scale

Different real gases at finite density give slightly different readings. As the gas becomes more dilute, these discrepancies diminish. The historical ideal-gas temperature scale is obtained through a zero-pressure extrapolation of constant-volume gas readings:

$$
\boxed{T=273.16\,\mathrm K\lim_{p_{\mathrm{tr}}\to0}\frac{p}{p_{\mathrm{tr}}}}.
$$

The limiting scale is independent of which sufficiently dilute gas is used and agrees with the thermodynamic absolute-temperature scale.

**SI clarification (context beyond the historical construction):** Since 2019 the kelvin is defined through a fixed numerical value of the Boltzmann constant. The triple point remains a useful physical reference, but its assigned historical role should not be confused with the current base-unit definition.

## 23.6 Celsius Temperature Scale

The Celsius and Kelvin scales have the same size increment but different zero points:

$$
\boxed{\theta\;(^\circ\mathrm C)=T\;(\mathrm K)-273.15},
\qquad
\boxed{T=\theta+273.15}.
$$

Temperature **differences** agree numerically: $\Delta T$ in kelvins equals $\Delta\theta$ in Celsius degrees. When dealing with gas laws or radiation $\propto T^4$, always use absolute Kelvin temperature.

At ordinary pressure, water freezes close to $0^\circ\mathrm C$ and boils close to $100^\circ\mathrm C$; boiling temperature depends on pressure. Temperatures below $0^\circ\mathrm C$ are perfectly possible, while negative kelvin values are not part of ordinary equilibrium thermometry.

## 23.7 Ideal Gas Equation

The equation of state of an ideal gas is

$$
\boxed{pV=nRT=Nk_BT},\qquad n=\frac{N}{N_A},\qquad R=N_Ak_B.
$$

Here $R\simeq8.314\,\mathrm{J\,mol^{-1}\,K^{-1}}$ and $k_B\simeq1.381\times10^{-23}\,\mathrm{J\,K^{-1}}$. The model works well for many gases at low density and at temperatures far from condensation.

For a fixed amount of ideal gas:

$$
p\propto\frac{T}{V},\qquad
pV=\text{constant}\;(T\;\text{fixed}),\qquad
\frac VT=\text{constant}\;(p\;\text{fixed}).
$$

An equation of state connects equilibrium variables. It does **not**, by itself, specify the heat or work exchanged along a process.

## 23.8 Callendar's Compensated Constant Pressure Thermometer

HCV describes a **constant-pressure gas thermometer** designed to compensate for the gas that remains outside the intended temperature bath. The apparatus uses matched gas-containing parts and an adjustable mercury volume. An appropriate volume adjustment restores equal gas pressures, while compensating parts remain at the reference temperature.

For a fixed amount of ideal gas at constant pressure, the underlying operating principle is

$$
\boxed{\frac VT=\text{constant}}.
$$

Unlike an uncompensated gas bulb with a long connecting tube, the matched arrangement reduces error introduced by gas at a different temperature from the measurement bulb. The experimental geometry and which volume is actually being adjusted matter: blindly treating the entire apparatus as a single uniform-temperature gas would defeat the compensation mechanism.

## 23.9 Adiabatic and Diathermic Walls

A **diathermic wall** allows thermal energy to pass relatively easily between neighboring systems. An **adiabatic wall** ideally prevents heat transfer through the boundary:

$$
\boxed{Q=0\quad\text{for an adiabatic process}}.
$$

Do not confuse *adiabatic* with *constant temperature*. An insulated gas can heat up when compressed or cool when expanded because work alters its internal energy. Real insulation approximates adiabatic behavior only over a suitable time interval.

## 23.10 Thermal Expansion

Most solids become larger when heated. For a small temperature change and approximately constant expansion coefficient, a rod of initial length $L_0$ obeys

$$
\boxed{L=L_0(1+\alpha\Delta T)},\qquad
\alpha=\frac{1}{L}\frac{dL}{dT}.
$$

For an isotropic solid, each perpendicular linear dimension expands by approximately the same fraction. Multiplying the dimensions and neglecting quadratic or higher powers of $\alpha\Delta T$ gives

$$
\boxed{\beta\simeq2\alpha},\qquad
\boxed{\gamma\simeq3\alpha},
$$

where $\beta$ and $\gamma$ are area and volume expansion coefficients. Correspondingly,

$$
A\simeq A_0(1+\beta\Delta T),\qquad
V\simeq V_0(1+\gamma\Delta T).
$$

A hole in a uniformly heated plate expands together with the material: imagine filling the hole with the same material and expanding the whole plate. An expansion coefficient may depend on temperature; over a wide range, use integration rather than a single constant $\alpha$. Fluids exhibit volume expansion; container expansion must be considered in liquid-thermometer and overflow measurements. Water's well-known density anomaly near $4^\circ\mathrm C$ shows that “all substances always expand on heating” is not universal.

---

# Part II: Kinetic Theory of Gases

Macroscopic gas properties emerge from many moving particles. The kinetic model bridges Newtonian mechanics and thermodynamics by replacing the impossible task of tracking every molecule with averages over molecular motion.

## 24.1 Introduction

A gas exerts pressure on walls and expands to fill available space. The microscopic explanation is incessant molecular motion, momentum exchange, and intermolecular interactions that are weak enough to neglect in the ideal-gas approximation. Macroscopic equilibrium does **not** mean microscopic particles are motionless.

## 24.2 Assumptions of Kinetic Theory of Gases

For the elementary ideal-gas model:

1. The gas contains an enormous number of identical molecules in random, isotropic motion.
2. Molecular dimensions are negligible relative to their mean separations.
3. Molecules move freely between collisions, with no appreciable long-range intermolecular force.
4. Collisions with walls and other molecules are elastic; collision durations are negligible compared with flight times.
5. The container is sufficiently large that bulk pressure is a stable time-averaged quantity.

These assumptions lead to the pressure relation derived next. They fail progressively at high density, near liquefaction, or in cases where molecular interactions are significant.

## 24.3 Calculation of the Pressure of an Ideal Gas

Take $N$ identical molecules of mass $m$ in a cube of side $L$ ($V=L^3$). A molecule has velocity component $v_x$ normal to a wall. In an elastic rebound, its momentum component changes by $-2mv_x$, delivering momentum $2mv_x$ to that wall.

The time between its successive collisions with that wall is $2L/|v_x|$. Consequently, its *average* force on the wall is

$$
\overline F_x=\frac{2m|v_x|}{2L/|v_x|}=\frac{mv_x^2}{L}.
$$

Sum over molecules and divide by the wall area $L^2$:

$$
p=\frac{m}{L^3}\sum_{i=1}^N v_{xi}^2=\frac{Nm}{V}\langle v_x^2\rangle.
$$

Random isotropic motion implies $\langle v_x^2\rangle=\langle v_y^2\rangle=\langle v_z^2\rangle=\langle v^2\rangle/3$. Therefore

$$
\boxed{p=\frac13\rho\langle v^2\rangle},\qquad
\boxed{pV=\frac13Nm\langle v^2\rangle}.
$$

This is **pressure from momentum transfer**, not pressure from molecules collectively moving outward with a preferred velocity. A gas in a uniformly moving train does not become hotter simply because its bulk speed relative to the ground is larger.

## 24.4 rms Speed

The root-mean-square speed is

$$
\boxed{v_{\mathrm{rms}}=\sqrt{\langle v^2\rangle}=\sqrt{\frac1N\sum_i v_i^2}},
\qquad
\boxed{p=\frac13\rho v_{\mathrm{rms}}^2}.
$$

The squared speeds appear because momentum transfer at a wall depends on $v_x^2$. The rms speed is generally *not* the ordinary arithmetic mean of the molecular speeds. Even at fixed temperature, different molecules have different velocities and directions.

## 24.5 Kinetic Interpretation of Temperature

Combine the kinetic pressure relation with the ideal-gas equation:

$$
\frac13 Nm v_{\mathrm{rms}}^2=Nk_BT
\quad\Longrightarrow\quad
\boxed{\frac12m v_{\mathrm{rms}}^2=\frac32k_BT}.
$$

Thus the mean **translational** kinetic energy per molecule is proportional to absolute temperature. It follows that

$$
\boxed{U_{\mathrm{trans}}=\frac32Nk_BT=\frac32nRT}
$$

for a gas with only the translational degrees of freedom in the energy model (notably a monatomic ideal gas). Diatomic and polyatomic molecules can also store energy in rotation and vibration; Chapter 27 returns to this distinction.

## 24.6 Deductions from Kinetic Theory

Using $N=nN_A$ and $R=N_Ak_B$ gives

$$
\boxed{v_{\mathrm{rms}}=\sqrt{\frac{3k_BT}{m}}=\sqrt{\frac{3RT}{M}}},
$$

where $M$ is **molar mass in kg/mol**, not the mass of the entire gas sample. At fixed $T$, lighter molecules move faster on average:

$$
\frac{v_{\mathrm{rms},1}}{v_{\mathrm{rms},2}}=\sqrt{\frac{M_2}{M_1}}.
$$

Pressure and molecular number density $n_N=N/V$ are related by $p=n_Nk_BT$. All ideal gases have the same mean translational kinetic energy **per molecule** at the same temperature, not the same rms speed.

## 24.7 Ideal Gas Equation

The microscopic result $pV=Nk_BT$ reproduces the macroscopic ideal-gas equation $pV=nRT$. Experimental gas laws become special cases: Boyle's law at fixed $T$, pressure proportional to $T$ at fixed $V$, and volume proportional to $T$ at fixed $p$.

The ideal-gas equation uses absolute pressure, absolute temperature, and the volume actually occupied by the gas. It cannot predict viscosity, diffusion, or phase changes without additional microscopic information.

## 24.8 Maxwell's Speed Distribution Law

A single rms speed does not describe all molecules. The Maxwell speed density gives the fraction of molecules whose speeds lie between $v$ and $v+dv$:

$$
\boxed{f(v)=4\pi\left(\frac{m}{2\pi k_BT}\right)^{3/2}v^2e^{-mv^2/(2k_BT)}},
\qquad dN=Nf(v)\,dv.
$$

The distribution is normalized by $\int_0^\infty f(v)\,dv=1$. Three characteristic speeds are

$$
\boxed{v_{\mathrm{mp}}=\sqrt{\frac{2k_BT}{m}}},\qquad
\boxed{\overline v=\sqrt{\frac{8k_BT}{\pi m}}},\qquad
\boxed{v_{\mathrm{rms}}=\sqrt{\frac{3k_BT}{m}}}.
$$

Their ordering is $v_{\mathrm{mp}}<\overline v<v_{\mathrm{rms}}$. Raising $T$ broadens the distribution, shifts it toward higher speeds, and lowers the height of its normalized peak. The high-speed tail matters for processes that require unusually energetic molecules.

## 24.9 Thermodynamic State

A thermodynamic **state** can be specified by independent state variables, such as $p$ and $V$ for a fixed amount of equilibrium ideal gas. The equation of state determines the remaining variable:

$$
\boxed{pV=nRT}.
$$

For a real gas the equation differs because molecular volume and interactions matter. A common model, written for $n$ moles using molar constants $a$ and $b$, is

$$
\boxed{\left(p+\frac{an^2}{V^2}\right)(V-nb)=nRT}\qquad\text{(van der Waals model).}
$$

The additive correction to $p$ approximates attractions; the reduced available volume approximates excluded molecular space. Neither is an exact description of every real gas. **State functions** such as $U,p,V,T$ differ conceptually from path-dependent transfers $Q$ and $W$.

## 24.10 Brownian Motion

Very small suspended particles exhibit irregular jitter in a fluid. The surrounding molecules collide with the particle from many directions; the momentary resultant impulse fluctuates randomly. The motion provides evidence for molecular agitation.

The jitter becomes more prominent for smaller suspended particles and is generally sensitive to fluid viscosity and temperature. Although the observed particle moves irregularly, the suspension can remain in macroscopic thermal equilibrium.

## 24.11 Vapour

A substance may exist as solid, liquid, or gas depending on pressure and temperature. A **vapour** is the gaseous phase of a substance at conditions where it can be condensed by changing pressure at the given temperature (below the critical temperature). The everyday usage of “vapour” and “gas” overlaps, but the phase-transition distinction becomes important near boiling and condensation.

## 24.12 Evaporation

Even below the boiling point, sufficiently energetic molecules near a liquid surface can escape into the gas phase. This surface phenomenon is **evaporation**. Escape preferentially removes higher-energy molecules, often cooling the remaining liquid when external heating does not replace the energy.

Evaporation rate tends to increase with higher temperature, larger exposed area, air movement, and lower ambient vapour pressure. It does not require bubbles forming throughout the liquid.

## 24.13 Saturated and Unsaturated Vapour: Vapour Pressure

In a closed container containing liquid and its vapour, evaporation and condensation can reach **dynamic equilibrium**: molecules continually cross the interface in both directions, but the net transfer vanishes. The corresponding pressure of the vapour is its **saturated vapour pressure** $p_{\mathrm{sat}}(T)$.

At fixed temperature, saturated vapour pressure is set by the substance and its temperature, provided some liquid remains. Unsaturated vapour has a partial pressure below $p_{\mathrm{sat}}(T)$ and can accept further evaporation. Vapour pressure generally rises steeply with temperature.

## 24.14 Boiling

A liquid boils when its saturated vapour pressure reaches the surrounding pressure so that vapour bubbles can persist and grow inside the liquid:

$$
\boxed{p_{\mathrm{sat}}(T_b)\simeq p_{\mathrm{external}}}
$$

for a liquid surface near atmospheric pressure, neglecting hydrostatic corrections, surface tension, and impurities. Lower external pressure lowers the boiling temperature; higher pressure raises it. Evaporation is a surface process, whereas boiling forms vapour throughout the liquid.

## 24.15 Dew Point

The **dew-point temperature** $T_d$ is the temperature to which a sample of moist air must be cooled, without changing its water-vapour content or total pressure appreciably, to reach saturation:

$$
\boxed{p_{\mathrm{water}}=p_{\mathrm{sat}}(T_d)}.
$$

Further cooling can produce condensation on surfaces or suspended particles. Dew point provides a physically informative measure of the amount of water vapour present; high relative humidity alone does not always mean a large absolute moisture content.

## 24.16 Humidity

Water vapour in air exerts its own **partial pressure**. Relative humidity compares that actual partial pressure with saturation pressure at the *same ambient temperature*:

$$
\boxed{\mathrm{RH}=100\%\times\frac{p_{\mathrm{water}}}{p_{\mathrm{sat}}(T_{\mathrm{air}})}}.
$$

If moist air cools without losing water vapour, $p_{\mathrm{sat}}$ falls and RH rises until condensation becomes possible. RH is not the percentage of the air's mass made of water, and $100\%$ RH does not mean that air consists entirely of water vapour.

## 24.17 Determination of Relative Humidity

A **dew-point hygrometer** cools a polished surface and detects the temperature at which condensation first forms. At that temperature, the actual water-vapour partial pressure equals saturation pressure:

$$
p_{\mathrm{water}}=p_{\mathrm{sat}}(T_d),\qquad
\mathrm{RH}=100\%\frac{p_{\mathrm{sat}}(T_d)}{p_{\mathrm{sat}}(T_{\mathrm{air}})}.
$$

A wet-and-dry-bulb hygrometer instead uses evaporative cooling of the wetted bulb. Its interpretation requires a calibration or psychrometric relation that depends on heat and mass transfer; it is **not** generally correct to substitute a simple ratio of wet- to dry-bulb temperatures into the RH equation.

## 24.18 Phase Diagrams: Triple Point

A pressure–temperature ($p$–$T$) diagram displays regions where solid, liquid, or vapour is stable and curves where two phases coexist. The **triple point** is the intersection at which all three phases can coexist in equilibrium. The end of the liquid–vapour coexistence curve is the **critical point**; above the critical temperature, increasing pressure alone does not create a distinct liquid phase.

The solid–liquid boundary can slope differently for different substances. For water, the negative local slope reflects ice's lower density relative to liquid water near melting.

The triple point of water is close to $273.16\,\mathrm K$ and $611\,\mathrm{Pa}$. HCV uses it in its historical gas-thermometry discussion. A phase diagram is an *equilibrium map*, not the trajectory that every heating or cooling experiment must follow.

## 24.19 Dew and Fog

**Dew** forms when moisture condenses on a surface cooled below the local dew point. **Fog** is a suspension of minute liquid droplets near the ground formed when humid air becomes saturated and droplets nucleate on available particles.

Both phenomena are condensation, but the location and growth mechanism differ. Cooling air to saturation, adding moisture, or mixing air masses can create suitable conditions; wind and available condensation nuclei influence the outcome.

---
# Part III: Calorimetry

Calorimetry applies conservation of energy to thermal interactions. The central calculation is not “use $mc\Delta T$ on everything,” but **identify each physical stage**, calculate the energy transferred in that stage, and enforce an energy balance.

## 25.1 Heat as a Form of Energy

The historical expression “heat is a form of energy” conveys the equivalence of thermal and mechanical processes: friction and thermal contact can have the same effect on internal energy. More precisely, **heat is energy transferred by a temperature difference**. Its SI unit is the joule (J).

If a system receives energy as heat, it may warm, melt, evaporate, expand against the surroundings, or perform a combination of these. The final temperature alone does not specify the amount of heat supplied unless the process and other energy transfers are known.

## 25.2 Units of Heat

Common units include the **joule** and the traditional **calorie**. The approximate energy conversion used in introductory calorimetry is

$$
\boxed{1\,\mathrm{cal}\simeq4.186\,\mathrm J},\qquad
\boxed{1\,\mathrm{kcal}\simeq4186\,\mathrm J}.
$$

A calorie was historically tied to the energy required to raise the temperature of a specified mass of water through a specified interval; definitions vary slightly with the chosen interval. In SI calculations use joules consistently. A food-label “Calorie” often means a kilocalorie, not a small calorie.

## 25.3 Principle of Calorimetry

An isolated collection of bodies conserves total energy. If their only interactions are internal heat transfers and no phase changes or work complicate the analysis, the heat lost by warmer bodies equals the heat gained by colder ones:

$$
\boxed{\sum_i Q_i=0},
$$

where $Q_i$ is positive when body $i$ absorbs energy by heating. For constant specific heat capacity $c_i$,

$$
\boxed{\sum_i m_i c_i(T_f-T_i)=0}.
$$

Use this only after checking that all bodies actually reach one final temperature and that there is no heat leakage, unmodeled container heat capacity, mechanical work, or phase transition. The calorimeter and stirrer may absorb a measurable fraction of the energy.

## 25.4 Specific Heat Capacity and Molar Heat Capacity

For a body warmed through a modest temperature interval with approximately constant heat capacity,

$$
\boxed{Q=mc\Delta T},\qquad
\boxed{C_{\mathrm{body}}=mc}.
$$

The **specific heat capacity** $c$ has units $\mathrm{J\,kg^{-1}\,K^{-1}}$, while the **heat capacity** of the whole body has units $\mathrm{J\,K^{-1}}$.

For $n$ moles, molar heat capacity $C$ is defined by

$$
\boxed{Q=nC\Delta T},\qquad
[C]=\mathrm{J\,mol^{-1}\,K^{-1}}.
$$

When $c$ changes appreciably with temperature, replace $mc\Delta T$ by

$$
\boxed{Q=m\int_{T_i}^{T_f}c(T)\,dT}
$$

for a specified process under which the heat capacity is defined. The **water equivalent** of a calorimeter is the mass of water with the same heat capacity:

$$
\boxed{m_{\mathrm{eq}}=\frac{C_{\mathrm{cal}}}{c_{\mathrm{water}}}}.
$$

For gases the heat capacity depends strongly on constraints such as constant volume versus constant pressure; see Chapter 27.

## 25.5 Determination of Specific Heat Capacity in Laboratory

In HCV's **Regnault apparatus**, a solid specimen is brought to a known higher temperature in a steam-heated chamber and transferred promptly into water contained in a calorimeter. The equilibrium temperature is measured after mixing.

For specimen mass $m_s$, initially at $T_s$, water mass $m_w$, initial water/calorimeter temperature $T_w$, final temperature $T_f$, and calorimeter heat capacity $C_{\mathrm{cal}}$:

$$
m_sc_s(T_s-T_f)=\big(m_wc_w+C_{\mathrm{cal}}\big)(T_f-T_w).
$$

Solving for the unknown specimen specific heat gives

$$
\boxed{c_s=\frac{(m_wc_w+C_{\mathrm{cal}})(T_f-T_w)}{m_s(T_s-T_f)}}.
$$

A known solid can similarly calibrate an unknown liquid's specific heat. Important experimental errors are heat loss during transfer, poor mixing, uncertainty in specimen temperature, and an ignored heat capacity of the calorimeter or stirrer.

## 25.6 Specific Latent Heat of Fusion and Vaporization

Energy can change **phase** without a corresponding temperature rise. At an equilibrium phase transition near fixed pressure,

$$
\boxed{Q=mL},
$$

where $L_f$ is the specific latent heat of **fusion** (solid to liquid) and $L_v$ of **vaporization** (liquid to vapour). Units are $\mathrm{J\,kg^{-1}}$.

Melting and vaporizing usually absorb energy; freezing and condensing release it. The reverse transitions have equal magnitude of latent heat at the same state conditions. A phase-change problem often contains both sensible-heating terms $mc\Delta T$ and latent terms $mL$.

For example, to take a mass of ice from a subzero temperature to liquid water above the melting point, the energy is the sum

$$
Q=mc_{\mathrm{ice}}(0-T_i)+mL_f+mc_{\mathrm{water}}(T_f-0),
$$

with consistent Celsius temperature *differences*. At nonstandard pressure, both transition temperatures and latent heats may differ from tabulated values.

## 25.7 Measurement of Specific Latent Heat of Fusion of Ice

Place a known mass $m_i$ of ice at $0^\circ\mathrm C$ into warmer water in a calorimeter. Suppose initial water temperature is $T_w>0$, final temperature $T_f>0$, and both masses are known. The ice absorbs energy to melt and then warm from $0^\circ\mathrm C$ to $T_f$:

$$
(m_wc_w+C_{\mathrm{cal}})(T_w-T_f)=m_iL_f+m_ic_wT_f.
$$

Therefore

$$
\boxed{L_f=\frac{(m_wc_w+C_{\mathrm{cal}})(T_w-T_f)-m_ic_wT_f}{m_i}}.
$$

The ice should be drained of excess surface water and brought close to its melting temperature before introduction. Ice colder than $0^\circ\mathrm C$ requires an additional warming term; a final mixture still containing ice requires different accounting.

## 25.8 Measurement of Specific Latent Heat of Vaporization of Water

Pass steam near its boiling temperature into a cooler calorimeter. If $m_s$ of steam condenses and the final temperature is $T_f$ below the boiling temperature $T_b$, the steam delivers energy by **condensation and subsequent cooling of condensed water**:

$$
\underbrace{m_sL_v}_{\text{condensation}}+
\underbrace{m_sc_w(T_b-T_f)}_{\text{condensed water cooling}}
=\underbrace{(m_wc_w+C_{\mathrm{cal}})(T_f-T_w)}_{\text{original water + calorimeter}}.
$$

Rearranging,

$$
\boxed{L_v=\frac{(m_wc_w+C_{\mathrm{cal}})(T_f-T_w)}{m_s}-c_w(T_b-T_f)}.
$$

Measure $m_s$ from the mass increase of the calorimeter and contents. Account for any steam that escaped or condensed before entering the water; these are major experimental error sources.

## 25.9 Mechanical Equivalent of Heat

Experiments measuring temperature rise from mechanical work established a numerical conversion between the older heat unit calorie and mechanical energy in joules. If mechanical work $W$ has the same heating effect as $H$ calories, traditionally

$$
\boxed{W=J_{\mathrm{mech}}H},\qquad
\boxed{J_{\mathrm{mech}}\simeq4.186\,\mathrm{J/cal}}.
$$

Here $J_{\mathrm{mech}}$ is the historical **mechanical equivalent of heat**, not the joule symbol used as a unit. HCV describes a frictional cone experiment (Searle's cone method): an applied torque does work over many revolutions and warms a vessel plus its water.

For applied torque $\tau=M_wgr$ and $N_{\mathrm{rev}}$ turns,

$$
W=\tau(2\pi N_{\mathrm{rev}})=2\pi N_{\mathrm{rev}}M_wgr.
$$

Comparing this work in joules with the vessel-plus-water heating in calories measures $J_{\mathrm{mech}}$. The lesson is physical equivalence of energy transfers, not that heat is a mechanical force.

---

# Part IV: Laws of Thermodynamics

Kinetic theory explains gas properties microscopically. Thermodynamics instead makes powerful predictions about **energy, work, heat, and process direction** without needing detailed molecular trajectories.

## 26.1 The First Law of Thermodynamics

For a closed system, neglecting macroscopic kinetic and potential energy changes, energy conservation reads

$$
\boxed{\Delta U=Q-W}\qquad\Longleftrightarrow\qquad\boxed{Q=\Delta U+W}.
$$

Our sign convention is **$Q>0$ into the system** and **$W>0$ done by the system** on its surroundings. Other texts sometimes use work *on* the system; convert signs before comparing formulas.

For an infinitesimal process,

$$
\boxed{dU=\delta Q-\delta W}.
$$

$U$ is a **state function**, so its net change depends only on endpoints. Heat and work depend on the process and are not state functions, hence the distinguishable notation $\delta Q$ and $\delta W$. In a cycle, $\Delta U_{\mathrm{cycle}}=0$ and therefore $Q_{\mathrm{net}}=W_{\mathrm{net}}$.

## 26.2 Work Done by a Gas

A gas in a cylinder pushes on a movable piston. When the piston moves quasistatically through $dx$, its work contribution is force times displacement:

$$
\delta W=(pA)\,dx=p\,dV.
$$

Thus, **boundary work** along a quasistatic path is

$$
\boxed{W=\int_{V_i}^{V_f}p\,dV}.
$$

The signed area under a $p$–$V$ curve is the work done by the gas: expansion gives positive work and compression negative work. Common cases:

$$
\boxed{W_{\mathrm{isochoric}}=0}\qquad(V=\text{constant}),
$$

$$
\boxed{W_{\mathrm{isobaric}}=p(V_f-V_i)}\qquad(p=\text{constant}),
$$

$$
\boxed{W_{\mathrm{isothermal,ideal}}=nRT\ln\!\left(\frac{V_f}{V_i}\right)}.
$$

The isothermal formula assumes an ideal gas and a reversible/quasistatic isothermal path. A genuine fast irreversible expansion cannot generally be assigned this same $p$–$V$ area from the gas's equilibrium equation of state.

## 26.3 Heat Engines

A cyclic heat engine receives heat $Q_H$ from a hot reservoir at temperature $T_H$, does net work $W_{\mathrm{out}}$, and rejects $Q_C$ to a cold reservoir at $T_C$.

$$
\boxed{W_{\mathrm{out}}=Q_H-Q_C},\qquad
\boxed{\eta=\frac{W_{\mathrm{out}}}{Q_H}=1-\frac{Q_C}{Q_H}}.
$$

Here $Q_H$ and $Q_C$ denote **positive magnitudes** of heat absorbed and rejected. The engine returns to its original state after one cycle, so its own internal energy has zero net change.

A refrigerator runs the useful transfer in the opposite direction by consuming external work. Its cooling coefficient of performance is $\mathrm{COP}_R=Q_C/W_{\mathrm{in}}$, which is *not* an efficiency bounded by one.

## 26.4 The Second Law of Thermodynamics

The first law forbids energy creation but allows many processes that never occur spontaneously. The **second law** imposes directionality. Two equivalent classical formulations are:

- **Kelvin–Planck statement:** A cyclic engine cannot take heat from a single thermal reservoir and convert that heat entirely into work with no other effect.
- **Clausius statement:** A process cannot have as its sole result transferring heat from a colder body to a hotter body.

Work can be completely degraded to thermal energy by friction, but a cyclic engine cannot generally convert all thermal energy from a single reservoir into work. Transferring heat from cold to hot is possible in a refrigerator only with suitable compensating work and other effects.

The second law does **not** claim that all organized systems must locally become more disordered. It constrains the total entropy change of an appropriately defined isolated system.

## 26.5 Reversible and Irreversible Processes

A **reversible** process is an ideal limiting process that can be reversed while leaving both system *and surroundings* unchanged. It proceeds via equilibrium states with vanishing gradients and negligible dissipative effects.

Real processes involving friction, sudden expansion, mixing, finite-temperature-difference heat transfer, or unrestrained gas expansion are **irreversible**. Going sufficiently slowly is necessary for many reversibility approximations, but slow motion alone does not eliminate friction or other dissipation.

For a reversible path, one can consistently use the system's instantaneous equilibrium pressure in $\delta W=p\,dV$ and temperature in $\delta Q_{\mathrm{rev}}=T\,dS$.

## 26.6 Entropy

Entropy $S$ is a thermodynamic state function whose change on a reversible path obeys

$$
\boxed{dS=\frac{\delta Q_{\mathrm{rev}}}{T}},\qquad
\boxed{\Delta S=\int_i^f\frac{\delta Q_{\mathrm{rev}}}{T}}.
$$

For a thermal reservoir at uniform temperature $T$, a reversible exchange of heat magnitude $Q$ corresponds to $\Delta S=\pm Q/T$, with the sign determined by whether the reservoir receives or loses heat.

The decisive inequality for an isolated system is

$$
\boxed{\Delta S_{\mathrm{isolated}}\ge0},
$$

with equality for a reversible process and a strictly positive increase for an irreversible process. Entropy of a **subsystem** may fall if its surroundings gain enough entropy. For reversible heat transfer between infinitesimally different temperatures, total entropy production tends to zero; for finite-temperature-difference transfer, it is positive.

## 26.7 Carnot Engine

A Carnot engine is an ideal reversible cycle operating between two thermal reservoirs at $T_H$ and $T_C$. It consists of two reversible **isothermal** legs and two reversible **adiabatic** legs. Over a reversible cycle, the engine's entropy returns to its original value. The heat transfers satisfy

$$
\frac{Q_H}{T_H}=\frac{Q_C}{T_C}.
$$

Combining this with the efficiency definition:

$$
\boxed{\eta_{\mathrm{Carnot}}=1-\frac{T_C}{T_H}},\qquad
\boxed{\eta_{\mathrm{real}}\le\eta_{\mathrm{Carnot}}}.
$$

Both temperatures must be in kelvins. The Carnot efficiency is an **upper bound** for cyclic engines operating between those reservoirs, independent of the engine's working substance. A theoretical $100\%$ efficiency would require $T_C=0$ K, which is not attainable for a practical finite system; finite temperature differences and friction further lower real performance.

---

# Part V: Specific Heat Capacities of Gases

A gas can absorb thermal energy while expanding and doing work. That is why the amount of heat needed for the **same temperature rise** can differ sharply between fixed-volume and fixed-pressure processes.

## 27.1 Two Kinds of Specific Heat Capacities of Gases

Define the **molar** heat capacities of a gas for two specific constraints:

$$
\boxed{C_V=\frac1n\left(\frac{\delta Q}{dT}\right)_V},\qquad
\boxed{C_p=\frac1n\left(\frac{\delta Q}{dT}\right)_p}.
$$

At constant volume, boundary work $p\,dV$ vanishes and supplied heat changes internal energy. At constant pressure, heating usually causes expansion; some energy goes into boundary work.

For an ideal gas, internal energy depends only on temperature, so

$$
\boxed{dU=nC_V\,dT}.
$$

These heat capacities have units $\mathrm{J\,mol^{-1}\,K^{-1}}$. Their ratio is denoted by $\gamma=C_p/C_V$. For ordinary ideal gases with positive heat capacities, $C_p>C_V$.

## 27.2 Relation between $C_p$ and $C_V$ for an Ideal Gas

From the first law, for quasistatic constant-pressure heating,

$$
\delta Q_p=dU+p\,dV=nC_VdT+p\,dV.
$$

The ideal-gas equation at fixed $p$ gives $p\,dV=nR\,dT$. Therefore

$$
nC_pdT=nC_VdT+nRdT
\quad\Longrightarrow\quad
\boxed{C_p-C_V=R}.
$$

This is **Mayer's relation** and applies to an ideal gas with molar heat capacities defined as above. With $\gamma=C_p/C_V$,

$$
\boxed{C_V=\frac{R}{\gamma-1}},\qquad
\boxed{C_p=\frac{\gamma R}{\gamma-1}}.
$$

For a real gas, $C_p-C_V$ is generally not equal to $R$.

## 27.3 Determination of $C_p$ of a Gas

HCV describes a **flow-calorimeter method**: gas at approximately constant pressure passes through a heated coil, transfers thermal energy to a calorimeter, and is collected or metered to determine how many moles underwent the temperature change.

An energy balance links the thermal energy released by $n$ moles of gas to the temperature rise of water and calorimeter:

$$
\boxed{nC_p\Delta T_{\mathrm{gas}}\simeq C_{\mathrm{receiver}}\Delta T_{\mathrm{receiver}}}.
$$

The apparatus measures $C_p$ rather than $C_V$ because the flowing gas is allowed to expand and its pressure is maintained approximately constant. Accurate laboratory analysis requires a measured flow rate, careful upstream/downstream temperatures, and accounting for heat lost to the room.

## 27.4 Determination of $C_V$ of a Gas

HCV's **Joly differential steam calorimeter** employs matched hollow vessels, one containing gas and the other acting as a comparison. Both are heated in steam, and condensation on the vessels reveals the additional energy needed to warm the gas.

The comparison removes most of the energy required to warm the copper vessels themselves. For a fixed-volume gas sample,

$$
\boxed{Q_{\mathrm{gas}}=nC_V\Delta T}.
$$

The small *difference* in condensate masses, multiplied by the latent heat of steam condensation, supplies the energy estimate. Care is needed with equal surface conditions, pressure, incomplete condensation, and ensuring that the vessel volumes remain sufficiently fixed.

## 27.5 Isothermal and Adiabatic Processes

**Isothermal:** $T$ is held constant. For an ideal gas, $\Delta U=0$, so the first law yields $Q=W$. Reversible expansion then gives

$$
\boxed{W=Q=nRT\ln(V_f/V_i)}.
$$

**Adiabatic:** no heat crosses the boundary, so $Q=0$ and $\Delta U=-W$. During adiabatic expansion, an ideal gas cools; during compression, it warms. A process can be adiabatic even if highly irreversible.

The notation “heat capacity of an isothermal process is infinite” and “of an adiabatic process is zero,” used in introductory discussions, is shorthand for $\delta Q/dT$ along those special paths. For isothermal heating, $dT=0$ while $\delta Q$ may be nonzero; for adiabatic motion $\delta Q=0$ while $dT$ may be nonzero. These are **not** the intrinsic material heat capacities $C_p$ and $C_V$.

## 27.6 Relations between $p$, $V$, $T$ in a Reversible Adiabatic Process

For a *reversible/quasistatic* adiabatic process in an ideal gas with approximately constant $C_V$ and $C_p$,

$$
0=dU+p\,dV=nC_V\,dT+p\,dV.
$$

Differentiate $pV=nRT$:

$$
p\,dV+V\,dp=nR\,dT.
$$

Eliminate $dT$ and use $C_p=C_V+R$:

$$
C_p p\,dV+C_VV\,dp=0
\quad\Longrightarrow\quad
\frac{dp}{p}+\gamma\frac{dV}{V}=0.
$$

Integrating with constant $\gamma$ gives **Poisson's relations**:

$$
\boxed{pV^\gamma=\text{constant}},
$$

$$
\boxed{TV^{\gamma-1}=\text{constant}},
$$

$$
\boxed{T^\gamma p^{1-\gamma}=\text{constant}}.
$$

Equivalently,

$$
\boxed{\frac{T_f}{T_i}=\left(\frac{V_i}{V_f}\right)^{\gamma-1}
=\left(\frac{p_f}{p_i}\right)^{(\gamma-1)/\gamma}}.
$$

**Do not** apply $pV^\gamma=\text{constant}$ to an arbitrary irreversible adiabatic process such as free expansion into vacuum. Adiabatic means $Q=0$; the Poisson relations also need reversible equilibrium-state evolution and a suitable ideal-gas model.

## 27.7 Work Done in an Adiabatic Process

For a reversible ideal-gas adiabat $pV^\gamma=K$, where $K$ is constant,

$$
W=\int_{V_i}^{V_f}KV^{-\gamma}\,dV
=\frac{p_iV_i-p_fV_f}{\gamma-1}.
$$

Thus

$$
\boxed{W_{\mathrm{adiabatic,rev}}=\frac{p_iV_i-p_fV_f}{\gamma-1}=nC_V(T_i-T_f)}.
$$

An adiabatically expanding gas does positive work while cooling. The same net result $W=-\Delta U$ holds for any adiabatic process of the specified closed system with no other energy changes, but the **pressure–volume integral using $pV^\gamma$** requires reversibility.

## 27.8 Equipartition of Energy

Classical equipartition assigns an average energy of $\tfrac12k_BT$ to every independent quadratic term in a molecule's energy. Three translational terms give $\tfrac32k_BT$ per molecule. Rotational and vibrational motions can contribute additional terms when thermally active.

For an ideal-gas molecule with $f$ active quadratic energy terms, in the classical approximation,

$$
\boxed{\langle E\rangle=\frac f2 k_BT},\qquad
\boxed{U=\frac f2 nRT}.
$$

Consequently, if $f$ is temperature-independent,

$$
\boxed{C_V=\frac f2 R},\qquad
\boxed{C_p=\left(\frac f2+1\right)R},\qquad
\boxed{\gamma=\frac{f+2}{f}}.
$$

| Molecular model | Active quadratic terms $f$ | $C_V$ | $C_p$ | $\gamma$ |
|---|---:|---:|---:|---:|
| Monatomic, translation | 3 | $3R/2$ | $5R/2$ | $5/3$ |
| Rigid diatomic, translation + rotation | 5 | $5R/2$ | $7R/2$ | $7/5$ |
| Diatomic with one classical vibrational mode also active | 7 | $7R/2$ | $9R/2$ | $9/7$ |

A vibrational normal mode contributes two quadratic terms, one kinetic and one potential. **Physical limitation:** At ordinary temperatures, many molecular vibrational modes are quantum-mechanically frozen out, so their classical $k_BT$-scale equipartition prediction does not apply. The relevant $f$, heat capacities, and $\gamma$ can change with temperature.

---
# Part VI: Heat Transfer

Heat can travel between regions by three fundamentally different mechanisms: **conduction** transfers energy across a material without bulk transport of matter; **convection** involves bulk fluid motion; **radiation** uses electromagnetic energy and requires no material medium.

## 28.1 Thermal Conduction

Fourier's law relates conduction to the temperature gradient. For one-dimensional flow through a material of thermal conductivity $K$ and cross-section $A$:

$$
\boxed{\dot Q=-KA\frac{dT}{dx}}.
$$

The minus sign indicates energy flow **down** a temperature gradient. For a uniform rod of length $L$ with steady linear temperature profile between end temperatures $T_H$ and $T_C$:

$$
\boxed{\dot Q=\frac{KA(T_H-T_C)}{L}}.
$$

The SI unit of $K$ is $\mathrm{W\,m^{-1}\,K^{-1}}$. A larger conductivity means more energy transferred each second under the same geometry and temperature difference. Metals tend to conduct well; insulating materials much less so. The **thermal resistance** is

$$
\boxed{R_{\mathrm{th}}=\frac{L}{KA}},\qquad
\boxed{\dot Q=\frac{T_H-T_C}{R_{\mathrm{th}}}}.
$$

Its unit is $\mathrm{K/W}$. This assumes steady, one-dimensional conduction and negligible edge losses; real contact interfaces can contribute additional resistance.

## 28.2 Series and Parallel Connection of Rods

Thermal-resistance networks parallel electrical-resistance networks, but the analogue of electric current is **heat-transfer rate** $\dot Q$, and the analogue of voltage difference is **temperature difference** $\Delta T$.

For **series** segments in steady state, the same $\dot Q$ passes through each segment:

$$
\boxed{R_{\mathrm{eq,series}}=\sum_i R_i},\qquad
\boxed{\dot Q=\frac{T_H-T_C}{\sum_i R_i}}.
$$

At a junction, temperatures divide according to the relative resistances. For two sections,

$$
T_H-T_j=\dot Q R_1,\qquad T_j-T_C=\dot Q R_2.
$$

For **parallel** rods sharing the same hot and cold end temperatures, their heat currents add:

$$
\boxed{\frac1{R_{\mathrm{eq,parallel}}}=\sum_i\frac1{R_i}},\qquad
\boxed{\dot Q_{\mathrm{total}}=\sum_i\dot Q_i}.
$$

These results hold for idealized steady conduction. Heat leaks, contact resistance, and temperature-dependent $K$ can invalidate a naïve lumped network.

## 28.3 Measurement of Thermal Conductivity of a Solid

HCV describes **Searle's apparatus**, particularly suitable for a good heat-conducting rod. Steam warms one end of the insulated rod and flowing water removes energy near the other end. Thermometers establish the temperature difference $T_1-T_2$ between two points separated by distance $L$ in the rod. The cooling water gains temperature from $T_{\mathrm{in}}$ to $T_{\mathrm{out}}$.

If mass $m$ of water flows in time $t$, steady-energy balance gives

$$
\frac{KA(T_1-T_2)}{L}=\frac{mc_w(T_{\mathrm{out}}-T_{\mathrm{in}})}{t}.
$$

Therefore

$$
\boxed{K=\frac{mc_wL(T_{\mathrm{out}}-T_{\mathrm{in}})}{At(T_1-T_2)}}.
$$

The rod needs lateral insulation and a genuine steady state: thermometer readings should stop changing before measurements are taken. The area and distance must correspond to the same uniform section carrying the modeled heat current.

## 28.4 Convection

Convection transfers thermal energy through **moving fluid**. In **natural convection**, density changes in gravity drive circulation: warmer, less dense fluid often rises and cooler fluid descends. In **forced convection**, a fan, pump, wind, or other external influence moves the fluid.

Examples include heating circulating water, cooling electronic components with a fan, and heat transport in blood. For practical heat-transfer calculations beyond HCV's introductory description, engineers often use an effective convection coefficient $h$:

$$
\dot Q_{\mathrm{conv}}\approx hA(T_s-T_\infty).
$$

This is a **common engineering correlation form**, not a universal fundamental law; $h$ depends on geometry, flow regime, fluid properties, and boundary conditions. Convection and conduction usually coexist at a solid–fluid interface.

## 28.5 Radiation

Every body with nonzero temperature emits electromagnetic radiation associated with its thermal state. Radiation can cross a vacuum, so the Sun heats Earth without a material conduction or convection path through space.

Incoming radiant energy can be **absorbed**, **reflected**, or **transmitted**. For an opaque surface, energy fractions obey

$$
\boxed{a+r=1},
$$

where $a$ is absorptivity and $r$ is reflectivity for the specified incident spectrum and conditions. At thermal equilibrium an object emits as much energy as it absorbs overall; a warmer object in cooler surroundings typically experiences net radiative loss.

## 28.6 Prevost Theory of Exchange

Prevost's key idea is that **all bodies continually radiate**, whether the surroundings are warmer or colder. A hot body cools because it emits more radiation than it absorbs, **not** because cold surroundings somehow switch off its emission. A cooler body in a warmer room still emits radiation while absorbing more than it emits.

Thus net radiative transfer is the *difference between outgoing and incoming radiant-energy rates*. This sets the stage for Stefan–Boltzmann exchange calculations.

## 28.7 Blackbody Radiation

A **blackbody** absorbs all incident radiation, independent of the incident wavelength and direction in the ideal model. In thermal equilibrium it is also the strongest thermal emitter permitted at its temperature. Its emission spectrum depends only on temperature.

A small hole in a cavity whose internal walls are maintained at uniform temperature is a close approximation: rays entering the hole undergo many reflections before escaping, increasing the likelihood of absorption. Real dark paint is not necessarily a perfect blackbody at all wavelengths, especially in infrared.

Blackbody radiation is a cornerstone of the historical transition from classical to quantum physics.

## 28.8 Kirchhoff's Law

In thermal equilibrium, **spectral, directional emissivity** equals the corresponding **spectral, directional absorptivity** under matching wavelength, direction, and polarization conditions. Informally:

$$
\boxed{\varepsilon_\lambda(T)=a_\lambda(T)}
\quad\text{(matched equilibrium conditions).}
$$

A good absorber at a particular wavelength is also a good emitter at that wavelength. HCV introduces emissive and absorptive powers and develops the relation between ordinary thermal absorptivity and emissivity. At an ideal blackbody, both equal one.

The law is **not** an assertion that every dark-looking object emits identically in the infrared, or that emission and absorption are equal when the object and surroundings have different temperatures.

## 28.9 Nature of Thermal Radiation

Thermal electromagnetic radiation spans many wavelengths. As temperature rises, total emission increases and the spectrum shifts toward shorter wavelengths. The peak wavelength of an ideal blackbody approximately obeys **Wien's displacement law**:

$$
\boxed{\lambda_{\mathrm{max}}T=b},\qquad
b\simeq2.898\times10^{-3}\,\mathrm{m\,K}.
$$

The classical account of the blackbody spectrum fails at short wavelengths. Planck's quantum hypothesis introduces discrete energy exchange associated with frequency:

$$
\boxed{E=h\nu}\qquad\text{(single quantum)}.
$$

This anticipates HCV's later modern-physics chapters. A glowing object does not emit only at $\lambda_{\mathrm{max}}$; it radiates over a broad spectrum.

## 28.10 Stefan–Boltzmann Law

The total radiant power emitted by a perfect blackbody of area $A$ at absolute temperature $T$ is

$$
\boxed{P_{\mathrm{emit}}=\sigma AT^4},\qquad
\sigma\simeq5.670\times10^{-8}\,\mathrm{W\,m^{-2}\,K^{-4}}.
$$

For a grey body with effective emissivity $\varepsilon$ treated as approximately constant over the thermal band,

$$
\boxed{P_{\mathrm{emit}}=\varepsilon\sigma AT^4},\qquad 0\le\varepsilon\le1.
$$

If the body is surrounded by a large uniform enclosure at temperature $T_s$, the idealized **net loss** is

$$
\boxed{P_{\mathrm{net}}=\varepsilon\sigma A(T^4-T_s^4)}.
$$

All temperatures must be in **kelvins**. This exchange formula assumes the usual grey-surface, uniform-enclosure simplifications. When $T=T_s$, emission does not stop; outgoing and incoming rates balance.

## 28.11 Newton's Law of Cooling

When a body differs only modestly in temperature from its surroundings, its net heat-loss rate may be approximately proportional to the temperature excess:

$$
\boxed{\frac{dT}{dt}=-k(T-T_s)},\qquad k>0.
$$

One motivation comes from linearizing the radiation term:

$$
T^4-T_s^4\approx4T_s^3(T-T_s)
\quad\text{for }|T-T_s|\ll T_s.
$$

Convection may add another approximately linear contribution. For a lumped body with constant heat capacity $mc$, the proportionality $k$ incorporates area, cooling coefficients, and heat capacity. Separating variables gives

$$
\int\frac{d(T-T_s)}{T-T_s}=-k\int dt,
$$

hence

$$
\boxed{T(t)=T_s+(T_0-T_s)e^{-kt}}.
$$

The time constant is $\tau=1/k$. HCV also uses finite-interval, average-temperature approximations for practical cooling questions. For large temperature differences, strong spatial temperature gradients, or changing surrounding conditions, a single exponential need not be accurate.

## 28.12 Detection and Measurement of Radiation

HCV describes two experimental approaches:

**Bolometer.** An absorbing element warms under incident radiation, changing its electrical resistance. A bridge circuit converts the resistance imbalance into a detectable electrical signal. Thermal isolation increases sensitivity; calibration connects output to incident radiation.

**Thermopile.** Dissimilar-metal thermocouples generate a thermoelectric emf when their junctions are at different temperatures (Seebeck effect). Many junctions connected in series produce a larger signal. Blackened hot junctions absorb incoming radiation, while reference junctions are shielded.

These devices detect radiation **indirectly** through the heating it causes. They differ from photon-counting detectors, whose microscopic operating principles are developed in later physics.

---

# Consolidated Formula Sheet

The formulas here are a **revision index**. Read the assumptions in the corresponding theory sections before using them.

## Temperature and Expansion (Chapter 23)

| Quantity or relation | Formula / reminder |
|---|---|
| Empirical linear thermometric scale | $\theta_X=100(X-X_0)/(X_{100}-X_0)$ |
| Celsius–Kelvin | $T=\theta+273.15$ |
| Ideal-gas equation | $pV=nRT=Nk_BT$ |
| Constant-volume gas thermometer | $p\propto T$ for fixed $n,V$ in dilute limit |
| Linear expansion | $\Delta L=\alpha L_0\Delta T$ |
| Area and volume expansion (isotropic) | $\beta\simeq2\alpha,\;\gamma\simeq3\alpha$ |
| Finite-temperature-range expansion | $dL/L=\alpha(T)\,dT$ |

## Kinetic Theory and Vapour (Chapter 24)

| Quantity or relation | Formula / reminder |
|---|---|
| Molecular pressure | $p=\rho\langle v^2\rangle/3$ |
| RMS speed | $v_{\mathrm{rms}}=\sqrt{3RT/M}$ |
| Mean translational KE / molecule | $\langle K\rangle=3k_BT/2$ |
| Most probable speed | $v_{\mathrm{mp}}=\sqrt{2k_BT/m}$ |
| Mean speed | $\overline v=\sqrt{8k_BT/(\pi m)}$ |
| Maxwell distribution | $f(v)=4\pi[m/(2\pi k_BT)]^{3/2}v^2e^{-mv^2/(2k_BT)}$ |
| Saturated boiling condition | $p_{\mathrm{sat}}(T_b)\simeq p_{\mathrm{ext}}$ |
| Relative humidity | $\mathrm{RH}=100\%\,p_{\mathrm{water}}/p_{\mathrm{sat}}(T)$ |
| Dew-point relation | $p_{\mathrm{water}}=p_{\mathrm{sat}}(T_d)$ |

## Calorimetry (Chapter 25)

| Quantity or relation | Formula / reminder |
|---|---|
| Sensible heating | $Q=mc\Delta T=nC\Delta T$ |
| Phase change | $Q=mL$ |
| Water equivalent | $m_{\mathrm{eq}}=C_{\mathrm{cal}}/c_w$ |
| Ideal isolated mixture | $\sum_iQ_i=0$ |
| Conversion | $1\,\mathrm{cal}\simeq4.186\,\mathrm J$ |

## Thermodynamic Laws (Chapter 26)

| Quantity or relation | Formula / reminder |
|---|---|
| First law (work done by system) | $\Delta U=Q-W$ |
| Quasistatic boundary work | $W=\int p\,dV$ |
| Reversible isothermal ideal-gas work | $W=nRT\ln(V_f/V_i)$ |
| Engine work and efficiency | $W=Q_H-Q_C,\;\eta=1-Q_C/Q_H$ |
| Reversible entropy change | $\Delta S=\int\delta Q_{\mathrm{rev}}/T$ |
| Isolated-system entropy inequality | $\Delta S_{\mathrm{isolated}}\ge0$ |
| Carnot maximum efficiency | $\eta_C=1-T_C/T_H$ |

## Gas Heat Capacities and Adiabats (Chapter 27)

| Quantity or relation | Formula / reminder |
|---|---|
| Mayer relation | $C_p-C_V=R$ (ideal gas, molar capacities) |
| Ratio of heat capacities | $\gamma=C_p/C_V$ |
| Internal-energy change | $\Delta U=nC_V\Delta T$ (constant $C_V$ ideal gas) |
| Reversible adiabat | $pV^\gamma=\mathrm{constant}$ |
| Alternative adiabat relations | $TV^{\gamma-1}=\mathrm{constant}$, $T^\gamma p^{1-\gamma}=\mathrm{constant}$ |
| Reversible adiabatic work | $W=(p_iV_i-p_fV_f)/(\gamma-1)$ |
| Equipartition | $\langle E\rangle=fk_BT/2$ |

## Conduction and Radiation (Chapter 28)

| Quantity or relation | Formula / reminder |
|---|---|
| Fourier conduction | $\dot Q=-KA\,dT/dx$ |
| Steady rod conduction | $\dot Q=KA(T_H-T_C)/L$ |
| Thermal resistance | $R_{\mathrm{th}}=L/(KA)$ |
| Series/parallel resistance | $R_s=\sum R_i,\;1/R_p=\sum1/R_i$ |
| Blackbody radiant power | $P=\sigma AT^4$ |
| Net greybody radiant exchange | $P_{\mathrm{net}}=\varepsilon\sigma A(T^4-T_s^4)$ |
| Wien displacement law | $\lambda_{\mathrm{max}}T\simeq2.898\times10^{-3}\,\mathrm{m\,K}$ |
| Newton cooling approximation | $T(t)=T_s+(T_0-T_s)e^{-kt}$ |

---
# Integrated Worked Examples

All numerical problems below are **independently constructed** to revise HCV concepts; they are not copied from the textbook. Every solution begins by identifying the physical model and its assumptions.

## Example A: Calibrating an Empirical Gas Thermometer

At fixed gas volume, an instrument reads $80\,\mathrm{kPa}$ at $0^\circ\mathrm C$ and $110\,\mathrm{kPa}$ at $100^\circ\mathrm C$. Find the temperature corresponding to $87.5\,\mathrm{kPa}$ **on its linear, two-point scale**.

**Model:** An empirical pressure scale linearly interpolated between two reference points.

$$
\theta=100\frac{p-p_0}{p_{100}-p_0}
=100\frac{87.5-80}{110-80}
=\boxed{25^\circ\mathrm C}.
$$

This calculation defines the thermometer's empirical reading. It does not require claiming that the gas is ideal over all pressures or that the constructed two-point scale is perfectly thermodynamic.

## Example B: Expansion of a Heated Metal Rod

A $1.50\,\mathrm m$ metal rod has $\alpha=12\times10^{-6}\,\mathrm{K^{-1}}$. Its temperature rises by $50\,\mathrm K$. Estimate its extension.

**Model:** Small linear expansion with approximately constant coefficient.

$$
\Delta L=\alpha L_0\Delta T
=(12\times10^{-6})(1.50)(50)\,\mathrm m
=\boxed{9.0\times10^{-4}\,\mathrm m=0.90\,\mathrm{mm}}.
$$

The small relative change $\alpha\Delta T=6\times10^{-4}$ justifies the first-order expression.

## Example C: Molecular Speed of Nitrogen

Find the rms molecular speed of nitrogen at $300\,\mathrm K$. Use molar mass $M=0.028\,\mathrm{kg/mol}$.

**Model:** Ideal gas in equilibrium.

$$
v_{\mathrm{rms}}=\sqrt{\frac{3RT}{M}}
=\sqrt{\frac{3(8.314)(300)}{0.028}}
\approx\boxed{517\,\mathrm{m/s}}.
$$

This molecular speed is not the speed at which a nitrogen sample as a whole flows through a pipe.

## Example D: Most Probable, Mean, and RMS Speeds

For oxygen at $300\,\mathrm K$ with $M=0.032\,\mathrm{kg/mol}$, compare its three characteristic Maxwell speeds.

$$
v_{\mathrm{mp}}=\sqrt{\frac{2RT}{M}}\approx\boxed{395\,\mathrm{m/s}},
$$

$$
\overline v=\sqrt{\frac{8RT}{\pi M}}\approx\boxed{446\,\mathrm{m/s}},
$$

$$
v_{\mathrm{rms}}=\sqrt{\frac{3RT}{M}}\approx\boxed{484\,\mathrm{m/s}}.
$$

The inequalities $v_{\mathrm{mp}}<\overline v<v_{\mathrm{rms}}$ provide a quick consistency check.

## Example E: Humidity from Dew Point

Air at $20^\circ\mathrm C$ has dew point $10^\circ\mathrm C$. Suppose tabulated saturation vapour pressures are $1.23\,\mathrm{kPa}$ at $10^\circ\mathrm C$ and $2.34\,\mathrm{kPa}$ at $20^\circ\mathrm C$. Find RH.

**Model:** Water-vapour partial pressure equals saturation pressure at dew point.

$$
\mathrm{RH}=100\%\frac{p_{\mathrm{sat}}(10^\circ\mathrm C)}{p_{\mathrm{sat}}(20^\circ\mathrm C)}
=100\%\frac{1.23}{2.34}
\approx\boxed{52.6\%}.
$$

Do not use $10/20=50\%$: those temperatures are not vapour pressures, and Celsius temperature ratios have no relevance here.

## Example F: Mixing Two Water Samples

Mix $0.20\,\mathrm{kg}$ of water at $80^\circ\mathrm C$ with $0.30\,\mathrm{kg}$ at $20^\circ\mathrm C$. Find the final temperature.

**Model:** Same specific heat for both samples, isolated container of negligible heat capacity, no phase change.

$$
0.20c_w(80-T_f)=0.30c_w(T_f-20).
$$

Cancel $c_w$ and solve:

$$
16-0.20T_f=0.30T_f-6
\quad\Longrightarrow\quad
\boxed{T_f=44^\circ\mathrm C}.
$$

The result lies between the starting temperatures, as energy conservation requires in this situation.

## Example G: Ice Added to Warm Water

Add $0.020\,\mathrm{kg}$ of ice at $0^\circ\mathrm C$ to $0.200\,\mathrm{kg}$ of water at $60^\circ\mathrm C$. Assume no calorimeter loss. Take $L_f=3.34\times10^5\,\mathrm{J/kg}$ and $c_w=4186\,\mathrm{J/(kg\,K)}$.

**First test:** Warm water can release $0.200(4186)(60)\approx50.2\,\mathrm{kJ}$ while cooling to $0^\circ\mathrm C$. Melting all the ice needs only $0.020(3.34\times10^5)=6.68\,\mathrm{kJ}$, so all ice melts and $T_f>0$.

**Energy balance:**

$$
0.200c_w(60-T_f)=0.020L_f+0.020c_wT_f.
$$

Thus

$$
T_f=\frac{0.200(4186)(60)-0.020(3.34\times10^5)}{0.220(4186)}
\approx\boxed{47.3^\circ\mathrm C}.
$$

The preliminary phase check prevents using a physically inconsistent final-state formula.

## Example H: Condensing Steam into Water

A mass $0.005\,\mathrm{kg}$ of saturated steam at $100^\circ\mathrm C$ condenses into $0.500\,\mathrm{kg}$ of water initially at $20^\circ\mathrm C$. Neglect losses and container capacity. Take $L_v=2.26\times10^6\,\mathrm{J/kg}$.

$$
0.005L_v+0.005c_w(100-T_f)=0.500c_w(T_f-20).
$$

The left side includes **condensation plus cooling of the condensate**. Rearranging,

$$
T_f=\frac{0.005L_v+0.005c_w(100)+0.500c_w(20)}{0.505c_w}
\approx\boxed{26.1^\circ\mathrm C}.
$$

Even a small steam mass transfers substantial energy because $L_v$ is large.

## Example I: First-Law Energy Ledger

A closed gas sample absorbs $750\,\mathrm J$ of heat and performs $200\,\mathrm J$ of work on its surroundings. Find $\Delta U$.

$$
\Delta U=Q-W=750-200=\boxed{550\,\mathrm J}.
$$

If the gas instead had $200\,\mathrm J$ of work done *on* it, the same convention would give $W=-200\,\mathrm J$ and $\Delta U=950\,\mathrm J$. Keep the sign convention visible.

## Example J: Reversible Isothermal Expansion

One mole of ideal gas expands reversibly at $300\,\mathrm K$ to twice its initial volume. Find the work done by the gas and heat absorbed.

$$
W=nRT\ln2=(1)(8.314)(300)(0.6931)
\approx\boxed{1.73\times10^3\,\mathrm J}.
$$

For an ideal gas at constant $T$, $\Delta U=0$. Thus $Q=W\approx1.73\,\mathrm{kJ}$, positive into the gas. The gas absorbs heat to replace the energy it transfers as work.

## Example K: Engine Efficiency versus Carnot Limit

An engine receives $2000\,\mathrm J$ from a $600\,\mathrm K$ reservoir, rejects $1200\,\mathrm J$ to a $300\,\mathrm K$ reservoir, and completes a cycle.

$$
W=2000-1200=\boxed{800\,\mathrm J},\qquad
\eta=\frac{800}{2000}=\boxed{40\%}.
$$

The ideal maximum between these reservoirs is

$$
\eta_C=1-\frac{300}{600}=\boxed{50\%}.
$$

The specified engine is compatible with the Carnot bound since $40\%<50\%$.

## Example L: Entropy Generated by Heat Flow

A $400\,\mathrm K$ thermal reservoir sends $600\,\mathrm J$ as heat to a $300\,\mathrm K$ reservoir. Treat the two reservoir temperatures as constant.

$$
\Delta S_H=-\frac{600}{400}=-1.50\,\mathrm{J/K},
$$

$$
\Delta S_C=+\frac{600}{300}=+2.00\,\mathrm{J/K}.
$$

Hence

$$
\boxed{\Delta S_{\mathrm{total}}=+0.50\,\mathrm{J/K}>0}.
$$

The net entropy increase quantifies irreversibility of spontaneous heat transfer across a finite temperature difference.

## Example M: Gas Heat Capacities from $\gamma$

An ideal gas has $\gamma=1.40$. Determine its molar $C_V$ and $C_p$.

$$
C_V=\frac{R}{\gamma-1}=\frac{8.314}{0.40}
\approx\boxed{20.8\,\mathrm{J/(mol\,K)}},
$$

$$
C_p=\frac{\gamma R}{\gamma-1}\approx\boxed{29.1\,\mathrm{J/(mol\,K)}}.
$$

Check: $C_p-C_V\approx8.3\,\mathrm{J/(mol\,K)}=R$.

## Example N: Reversible Adiabatic Compression

One mole of ideal gas with $\gamma=1.40$ is compressed reversibly and adiabatically from $T_i=300\,\mathrm K$ to **half** its initial volume. Determine final temperature and work **done by** the gas.

$$
T_f=T_i\left(\frac{V_i}{V_f}\right)^{\gamma-1}
=300(2)^{0.40}\approx\boxed{396\,\mathrm K}.
$$

Using $C_V\simeq20.8\,\mathrm{J/(mol\,K)}$,

$$
W=nC_V(T_i-T_f)
\approx(1)(20.8)(300-396)
\approx\boxed{-2.00\,\mathrm{kJ}}.
$$

Negative work by the gas means positive work **on** it. No heat is supplied; its internal energy rises because of compression work.

## Example O: Two Conducting Rods in Series

Two rods have equal cross-sectional area $A=0.005\,\mathrm{m^2}$. Rod 1 has $L_1=0.10\,\mathrm m$, $K_1=200\,\mathrm{W/(m\,K)}$. Rod 2 has $L_2=0.20\,\mathrm m$, $K_2=100\,\mathrm{W/(m\,K)}$. The ends are at $100^\circ\mathrm C$ and $20^\circ\mathrm C$.

$$
R_1=\frac{0.10}{200(0.005)}=0.10\,\mathrm{K/W},
\quad
R_2=\frac{0.20}{100(0.005)}=0.40\,\mathrm{K/W}.
$$

$$
\dot Q=\frac{100-20}{0.10+0.40}=\boxed{160\,\mathrm W}.
$$

The junction temperature is

$$
T_j=100-(160)(0.10)=\boxed{84^\circ\mathrm C}.
$$

The larger temperature drop occurs in the rod with greater thermal resistance.

## Example P: Radiation Loss to a Cooler Room

A grey object has $A=0.020\,\mathrm{m^2}$, $\varepsilon=0.80$, and temperature $400\,\mathrm K$ in a large enclosure at $300\,\mathrm K$. Compute its net radiation loss.

$$
P_{\mathrm{net}}=\varepsilon\sigma A(T^4-T_s^4)
$$

$$
=(0.80)(5.670\times10^{-8})(0.020)(400^4-300^4)
\approx\boxed{15.9\,\mathrm W}.
$$

Using $400^4$ alone would calculate **emission**, not the **net** heat exchange with a radiating room.

## Example Q: Exponential Cooling

A liquid initially at $70^\circ\mathrm C$ is surrounded by air at $20^\circ\mathrm C$. Under a lumped Newton-cooling model with $k=0.030\,\mathrm{min^{-1}}$, find its temperature after 20 minutes.

$$
T(20)=20+(70-20)e^{-0.030(20)}
=20+50e^{-0.6}
\approx\boxed{47.4^\circ\mathrm C}.
$$

The temperature excess has fallen to approximately $54.9\%$ of its initial value. This is a single-time-constant approximation, not a guarantee for every real cooling experiment.

## Example R: Conductivity from Water-Flow Calorimetry

In a Searle-type setup, cooling water flows at $0.010\,\mathrm{kg/s}$ and warms by $5\,\mathrm K$. In the rod, two thermometers $0.20\,\mathrm m$ apart differ by $40\,\mathrm K$; its cross-sectional area is $0.005\,\mathrm{m^2}$. Assume negligible leakage.

$$
\dot Q=\dot m c_w\Delta T_w
=(0.010)(4186)(5)=209.3\,\mathrm W.
$$

$$
K=\frac{\dot QL}{A\Delta T_{\mathrm{rod}}}
=\frac{209.3(0.20)}{0.005(40)}
\approx\boxed{209\,\mathrm{W/(m\,K)}}.
$$

Steady-state energy balance links water calorimetry to Fourier conduction. The calculated value is the inferred rod conductivity, not the water conductivity.

---

# Common Misconceptions and Diagnostic Questions

| Misconception | Correct interpretation |
|---|---|
| “Heat is the thermal energy stored in a body.” | Heat denotes **energy transfer** due to a temperature difference; internal energy is a state property. |
| “Same temperature means same internal energy.” | Different masses, materials, or phases can have very different internal energies at the same temperature. |
| “An adiabatic process is always isothermal.” | Adiabatic means $Q=0$; temperature can change because of work. |
| “All thermometers agree once calibrated at two temperatures.” | They agree at calibration points, but thermometric properties can give different intermediate readings. |
| “All liquids always expand when warmed.” | Water exhibits anomalous behavior near $4^\circ\mathrm C$; expansion coefficients need not keep one sign. |
| “Every gas molecule travels at the rms speed.” | Maxwell's distribution contains a broad range of molecular speeds. |
| “A moving gas bottle is hotter because it has larger kinetic energy in the laboratory frame.” | Temperature is related to random molecular motion relative to the macroscopic fluid motion. |
| “Relative humidity is the fraction of air that is water.” | It is a ratio of **vapour partial pressure** to saturation vapour pressure at ambient temperature. |
| “Water boils only at $100^\circ\mathrm C$.” | Boiling temperature depends on external pressure. |
| “$mc\Delta T$ describes melting.” | At constant-temperature phase change use $mL$ and check for any accompanying warming/cooling stages. |
| “Work and heat are state functions.” | They depend on the path; internal energy and entropy are state functions. |
| “A cyclic engine has nonzero $\Delta U$ because it produces work.” | After a complete cycle the engine returns to its initial state, giving $\Delta U=0$. |
| “An engine between two reservoirs can always reach Carnot efficiency.” | Carnot efficiency is a reversible ideal upper bound; real dissipation lowers performance. |
| “A reversible adiabatic equation applies to all insulated expansions.” | Relations such as $pV^\gamma=\mathrm{constant}$ require a reversible ideal-gas path and suitable heat-capacity assumptions. |
| “Entropy must rise in every individual object.” | Entropy of a subsystem can decrease while the total entropy of an isolated assembly increases. |
| “$C_p=C_V$ because temperature changes by the same amount.” | Constant-pressure heating supplies energy for expansion work; for an ideal gas $C_p-C_V=R$. |
| “Heat flows faster through the material with greatest thermal resistance.” | For fixed $\Delta T$, $\dot Q=\Delta T/R_{\mathrm{th}}$ is smaller for greater resistance. |
| “A body at room temperature does not radiate.” | All ordinary bodies emit thermal radiation; equilibrium means **net** radiant exchange is zero. |
| “Use Celsius temperature in Stefan's $T^4$ law.” | The fourth power requires **absolute Kelvin temperature**. |
| “Newton's cooling law is exact regardless of temperature difference.” | Its simple linear/exponential form is an approximation tied to particular heat-transfer conditions. |

**Diagnostic strategy before any numerical question:** Identify the system boundary, initial and final states, heat/work sign convention, constraints ($p$, $V$, or $T$ constant; reversible or not), phase changes, material parameters, and whether the model is transient or steady.

---
# Active-Recall Checkpoints

Try these **without looking at the formula sheet**. For a derivation, state its assumptions first. For a qualitative question, explain the physical mechanism instead of naming a law alone.

### Chapter 23: Heat and Temperature

1. Distinguish heat, temperature, and internal energy by specifying which are state properties and which represent transfer.
2. Explain how friction can increase a body's temperature without heat transfer from a hotter body.
3. State the zeroth law and explain why it permits a thermometer to compare thermal states.
4. Why does thermal equilibrium not imply equal internal energy?
5. Construct an empirical linear temperature scale using two fixed-point readings of a thermometric property.
6. Why can mercury and platinum-resistance thermometers disagree between calibration points?
7. Describe the constant-volume gas thermometer and show how the manometer determines gas pressure.
8. Why does extrapolating gas pressure toward zero make different gas thermometers agree more closely?
9. State the distinction between the historical triple-point construction and the present SI definition of the kelvin.
10. Explain why $\Delta T=10\,\mathrm K$ corresponds to a Celsius *difference* of $10^\circ\mathrm C$, while $10^\circ\mathrm C\ne10\,\mathrm K$ as absolute temperatures.
11. Explain the purpose of Callendar's compensated gas thermometer.
12. Contrast an adiabatic boundary with a diathermic boundary and provide one practical approximation of each.
13. Derive $\beta\simeq2\alpha$ and $\gamma\simeq3\alpha$ for isotropic small thermal expansion.
14. Explain why a hole in a freely heated metal plate expands rather than contracts.
15. Describe how expansion of a containing vessel affects a measured liquid-volume increase.

### Chapter 24: Kinetic Theory of Gases

16. List the ideal-gas molecular assumptions and identify two conditions where they begin to fail.
17. Derive the momentum delivered to a stationary wall by one elastic molecular collision.
18. Derive the pressure relation $p=\rho\langle v^2\rangle/3$ using collision frequency and isotropy.
19. Distinguish molecular speed, rms speed, random velocity, and the bulk flow velocity of a gas sample.
20. Use kinetic theory and $pV=Nk_BT$ to derive $\langle K_{\mathrm{trans}}\rangle=3k_BT/2$.
21. Why can helium and oxygen at the same temperature have different rms molecular speeds?
22. Distinguish most-probable speed, mean speed, and rms speed, and rank them.
23. Explain qualitatively why the Maxwell speed distribution broadens with increasing temperature.
24. Identify which features of real molecular behavior motivate corrections to the ideal-gas equation.
25. Explain Brownian motion in terms of unequal momentary molecular impulses.
26. Distinguish a vapour below critical temperature from a supercritical fluid.
27. Explain why evaporation can cool a liquid even when the liquid is initially below its boiling point.
28. Describe dynamic evaporation–condensation equilibrium above a liquid in a closed vessel.
29. Why is saturated vapour pressure principally temperature-dependent, provided liquid is still present?
30. Distinguish evaporation from boiling based on where vapour forms.
31. Explain why liquid water boils at a lower temperature on a high mountain.
32. Define dew point and relate it to actual water-vapour partial pressure.
33. Derive relative humidity from the ratio of actual to saturated vapour pressure.
34. Why is relative humidity not simply the mass fraction of water in air?
35. Explain how a dew-point hygrometer infers relative humidity.
36. Identify solid–liquid, liquid–vapour, and solid–vapour coexistence curves on a $p$–$T$ diagram.
37. Define triple point and critical point, and explain their conceptual difference.
38. Distinguish dew from fog and describe conditions that produce each.

### Chapter 25: Calorimetry

39. Explain why heat is measured in joules even though calorimetry historically used calories.
40. State the calorimetry energy-balance principle and identify the system that must be regarded as isolated.
41. Why does the calorimeter's own heat capacity matter in a mixture experiment?
42. Distinguish specific heat capacity, molar heat capacity, and the heat capacity of a finite body.
43. Derive the water-equivalent mass of a vessel from its heat capacity.
44. State how $Q=mc\Delta T$ generalizes when the specific heat capacity changes with temperature.
45. Develop the energy equation used in Regnault's solid-specific-heat experiment.
46. Distinguish latent heat of fusion from latent heat of vaporization.
47. Construct the complete stage-by-stage energy ledger for heating ice below $0^\circ\mathrm C$ until it becomes steam.
48. Why must ice at a negative temperature be warmed before melting in a calorimetry problem?
49. In a steam-condensation calorimeter, why must cooling of the condensed water be included?
50. Explain how a friction-based experiment can measure the mechanical equivalent of heat.
51. When can a proposed calorimetry final temperature be rejected before detailed algebra?

### Chapter 26: Laws of Thermodynamics

52. State the first law using the convention “work done **by** the system is positive.”
53. Explain why $Q$ and $W$ are path dependent but $U$ is a state function.
54. Derive $\delta W=p\,dV$ for a quasistatic piston displacement.
55. Derive the reversible isothermal work expression for an ideal gas.
56. Sketch two $p$–$V$ paths between the same endpoints and explain how their work can differ.
57. Why does a cyclic heat engine have zero net change in internal energy?
58. Derive engine efficiency from the heat received and rejected per cycle.
59. State the Kelvin–Planck and Clausius formulations of the second law.
60. Explain why transferring heat from cold to hot in a refrigerator does not violate the second law.
61. Distinguish a reversible process from an irreversible process using both system and surroundings.
62. Explain entropy as a state function defined through reversible heat exchange.
63. Calculate total entropy change when heat transfers between two reservoirs at different temperatures.
64. Describe the four stages of a Carnot cycle and derive its efficiency relation.
65. Explain why Carnot efficiency is independent of the working gas.
66. Can the entropy of an object decrease? Under what condition is this compatible with the second law?

### Chapter 27: Specific Heat Capacities of Gases

67. Define $C_V$ and $C_p$ and explain which experimental constraint each refers to.
68. Derive Mayer's relation $C_p-C_V=R$ for an ideal gas.
69. Derive expressions for $C_V$ and $C_p$ in terms of $R$ and $\gamma$.
70. Why is heat capacity at constant pressure generally larger than that at constant volume for an ideal gas?
71. Explain the working principle of a gas-flow calorimeter measuring $C_p$.
72. Explain how a differential condensation method can measure $C_V$.
73. Show that reversible isothermal ideal-gas expansion satisfies $Q=W$.
74. Explain why an adiabatic expansion may cool a gas even though $Q=0$.
75. Derive $pV^\gamma=\mathrm{constant}$ from the first law and the ideal-gas equation.
76. Derive $TV^{\gamma-1}=\mathrm{constant}$ and $T^\gamma p^{1-\gamma}=\mathrm{constant}$.
77. Why do the reversible adiabatic relations not generally apply to free expansion into vacuum?
78. Derive $W=(p_iV_i-p_fV_f)/(\gamma-1)$ and interpret its sign for compression.
79. Explain the quadratic-degree-of-freedom statement of equipartition.
80. Find the ideal values of $C_V$, $C_p$, and $\gamma$ for monatomic and rigid diatomic gases.
81. Why does each active vibrational mode contribute both kinetic and potential terms?
82. Explain why quantum effects can invalidate the classical equipartition result for molecular vibration.

### Chapter 28: Heat Transfer

83. Distinguish conduction, convection, and radiation by their physical transport mechanisms.
84. Derive the steady-rod conduction formula from Fourier's law.
85. Explain the units and physical meaning of thermal conductivity $K$.
86. Derive thermal resistance and show the analogy with Ohm's law.
87. Construct thermal-resistance networks for two rods in series and two rods in parallel.
88. In a two-layer rod, show how the interfacial temperature depends on the resistance ratio.
89. Derive the conductivity formula used in Searle's apparatus from energy conservation.
90. Distinguish natural from forced convection, giving two examples of each.
91. Explain how water's anomalous expansion helps lakes freeze from the top downward.
92. Why can radiative energy reach a distant object through vacuum?
93. Explain Prevost's exchange principle and distinguish emitted from **net** radiation.
94. Describe why a cavity with a small aperture approximates a blackbody.
95. State Kirchhoff's relation between spectral emissivity and absorptivity at equilibrium.
96. Explain the physical meaning of Wien's displacement relation.
97. Why did the blackbody spectrum motivate Planck's energy-quantum hypothesis?
98. Use Stefan–Boltzmann law to determine how blackbody radiant power changes when absolute temperature doubles.
99. Derive the net greybody radiation-loss formula for a body inside a uniform-temperature enclosure.
100. Linearize $T^4-T_s^4$ for $T$ near $T_s$ and connect it to Newton's cooling law.
101. Solve Newton's cooling equation for a constant ambient temperature and interpret the time constant.
102. Explain how a bolometer converts incident radiation to an electrical reading.
103. Explain how a thermopile uses temperature differences and the Seebeck effect to measure radiation.

---

## Source and scope

**Primary reference:** H. C. Verma, *Concepts of Physics*, Volume 2, Chapters **23–28** (textbook pp. **1–103**):

- Chapter 23: *Heat and Temperature*, §§23.1–23.10.
- Chapter 24: *Kinetic Theory of Gases*, §§24.1–24.19.
- Chapter 25: *Calorimetry*, §§25.1–25.9.
- Chapter 26: *Laws of Thermodynamics*, §§26.1–26.7.
- Chapter 27: *Specific Heat Capacities of Gases*, §§27.1–27.8.
- Chapter 28: *Heat Transfer*, §§28.1–28.12.

The notes follow the textbook's **65 numbered theory sections**, central derivations, and experimental themes. They are an **original synthesis**, not a verbatim reproduction. The 18 integrated examples and 103 active-recall questions are independently constructed. Where a clarification or model extends beyond the HCV treatment, it is marked in context, including the modern SI kelvin definition, greybody assumptions, convection-coefficient model, and quantum limitations of classical equipartition.

**Study method:** Read the HCV text in parallel, reproduce each major derivation from its assumptions, work the textbook's examples and exercises independently, and then use this unit's examples, formula tables, misconception checks, and active-recall questions for consolidation. For calorimetry and thermodynamics problems, always begin with a **system boundary and an energy ledger** rather than hunting for a formula.
