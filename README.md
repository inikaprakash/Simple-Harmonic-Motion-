# Complex Numbers in Simple and Quantum Harmonic Motion

An introduction to the role of **complex numbers in simple harmonic motion (SHM)** and **quantum harmonic motion**, with emphasis on complex exponentials, Euler's formula, phasors, damping, wavefunctions, quantised energy levels, and operator formalism.

## Overview

Harmonic oscillators provide a useful connection between classical and quantum physics. In classical mechanics, a mass–spring system, pendulum (for small oscillations), or other harmonic oscillator can be described by real-valued position, velocity, and acceleration. Complex numbers provide a compact mathematical representation of the same sinusoidal dynamics.

In quantum mechanics, complex numbers are fundamental rather than merely convenient. A quantum harmonic oscillator is described by a complex-valued wavefunction, and its measurable predictions are obtained from quantities such as the probability density `|ψ(x,t)|²`.

This project compares these two descriptions and explains why complex mathematics is so effective for oscillatory systems.

## Simple Harmonic Motion

For an ideal harmonic oscillator, the displacement can be written as

$$
x(t)=a\cos(\omega t)+b\sin(\omega t),
$$

where:

- `a` and `b` are determined by the initial conditions,
- `ω` is the angular frequency,
- `t` is time.

Using Euler's formula,

$$
e^{i\theta}=\cos\theta+i\sin\theta,
$$

sinusoidal motion can be represented compactly using a complex exponential. For example,

$$
z(t)=Ae^{i(\omega t+\phi)},
$$

where `A` is the amplitude and `φ` is the phase. The physical displacement is obtained from the appropriate real component, for example

$$
x(t)=\operatorname{Re}\left[Ae^{i(\omega t+\phi)}\right]
=A\cos(\omega t+\phi).
$$

The complex representation is therefore a mathematical convenience: the observable classical position remains real-valued.

## Why Complex Numbers Are Useful in SHM

Complex numbers allow the sine and cosine components of oscillatory motion to be treated as a single exponential function. This simplifies differentiation, integration, phase calculations, and the analysis of driven or coupled oscillators.

For a harmonic oscillator,

$$
\frac{d^2x}{dt^2}+\omega^2x=0,
$$

an exponential trial solution `x(t) = e^{rt}` gives the characteristic equation

$$
r^2+\omega^2=0,
$$

with roots

$$
r=\pm i\omega.
$$

The complex roots lead directly to sinusoidal solutions through Euler's formula.

## Phasors

A **phasor** represents an oscillation as a rotating vector in the complex plane.

- The magnitude represents the amplitude.
- The angle represents the phase.
- The real component can represent the cosine component.
- The imaginary component can represent the sine component.

The phasor approach is particularly useful when comparing oscillations with different phases or solving linear systems involving sinusoidal forcing.

## Damped Harmonic Motion

Damped harmonic motion occurs when an oscillator loses mechanical energy, causing its amplitude to decrease with time. A common model is

$$
\frac{d^2x}{dt^2}+2\gamma\frac{dx}{dt}+\omega_0^2x=0,
$$

where `γ` is a damping parameter and `ω₀` is the undamped natural angular frequency.

The characteristic equation is

$$
r^2+2\gamma r+\omega_0^2=0.
$$

Depending on the discriminant, the system can be underdamped, critically damped, or overdamped. In the underdamped regime, complex-conjugate roots produce oscillatory solutions with an exponentially decaying envelope. Complex analysis therefore provides a natural way to describe both oscillation and decay.

## Classical vs Quantum Harmonic Motion

| Feature | Classical SHM | Quantum Harmonic Oscillator |
|---|---|---|
| State description | Position and momentum | Quantum state / wavefunction |
| Mathematical framework | Newtonian mechanics | Quantum mechanics |
| Energy | Continuous in the ideal classical model | Discrete energy eigenvalues |
| Position | A definite classical variable | Measurement outcome described probabilistically |
| Wavefunction | Not required | Fundamental state description |
| Complex numbers | Convenient representation | Fundamental to the quantum formalism |
| Dynamics | Equation of motion | Schrödinger equation |
| Operators | Not required in the same role | Position and momentum operators are central |

## Quantised Energy Levels

The classical harmonic oscillator can have a continuous range of total energies. For a mass–spring oscillator,

$$
E=\frac{p^2}{2m}+\frac{1}{2}m\omega^2x^2.
$$

In quantum mechanics, solving the Schrödinger equation for the harmonic-oscillator potential gives discrete energy eigenvalues:

$$
E_n=\hbar\omega\left(n+\frac{1}{2}\right),
\qquad n=0,1,2,\ldots
$$

The lowest energy is therefore

$$
E_0=\frac{1}{2}\hbar\omega.
$$

This non-zero **ground-state energy** is consistent with the uncertainty principle. A quantum harmonic oscillator cannot simultaneously have exactly zero position uncertainty and zero momentum uncertainty.

> **Important clarification:** quantisation is not because a particle must have a whole-number multiple of an energy unit. Rather, the allowed energy eigenvalues arise from the boundary and normalisation conditions imposed by the quantum-mechanical Schrödinger equation.

## Quantum Wavefunction

In quantum mechanics, the state of a particle is described by a wavefunction `ψ(x,t)`, which is generally complex-valued.

The probability density for position is

$$
\rho(x,t)=|\psi(x,t)|^2=\psi^*(x,t)\psi(x,t).
$$

Thus, the complex phase of the wavefunction contains physical information even though the probability density depends on its magnitude squared.

For the quantum harmonic oscillator, the stationary-state wavefunctions have the general form

$$
\psi_n(x)=N_n H_n(\xi)e^{-\xi^2/2},
$$

where `Hₙ` is a Hermite polynomial, `Nₙ` is a normalisation factor, and `ξ` is a dimensionless position coordinate. Time evolution introduces a phase factor:

$$
\psi_n(x,t)=\psi_n(x)e^{-iE_nt/\hbar}.
$$

The complex exponential is therefore fundamental to quantum time evolution.

## Operator Formalism

Classical mechanics describes an oscillator using equations of motion such as Newton's second law. Quantum mechanics instead represents observables using operators acting on states.

For example, in the position representation,

$$
\hat{x}=x,
$$

and the momentum operator is

$$
\hat{p}=-i\hbar\frac{\partial}{\partial x}.
$$

The time-dependent Schrödinger equation is

$$
i\hbar\frac{\partial\psi}{\partial t}=\hat{H}\psi,
$$

where `Ĥ` is the Hamiltonian operator. For the one-dimensional harmonic oscillator,

$$
\hat{H}=\frac{\hat{p}^2}{2m}+\frac{1}{2}m\omega^2\hat{x}^2.
$$

Complex numbers therefore enter the foundations of quantum dynamics through the wavefunction, momentum operator, and Schrödinger equation.

## Role of Complex Numbers: Classical vs Quantum

The distinction is important:

### In classical SHM

Complex numbers are primarily a **computational representation**. A real physical oscillation can be encoded using a complex exponential, and the physical quantity is recovered by taking its real part (or by using an equivalent complex-amplitude convention).

### In quantum harmonic motion

Complex numbers are **intrinsic to the formalism**. Quantum states are represented in a complex Hilbert space, and relative phase affects interference and the outcomes of measurements. The wavefunction itself is not simply a classical oscillation written with complex notation.

## Mathematical Connection

The same mathematical structure appears in both systems:

```text
Euler's formula
      ↓
Complex exponentials
      ↓
Oscillatory phase evolution
      ↓
 ┌───────────────┬──────────────────┐
 │ Classical SHM │ Quantum oscillator│
 │               │                  │
 │ x(t)          │ ψ(x,t)           │
 │ real observable│ complex state   │
 │ phasors        │ quantum phase    │
 └───────────────┴──────────────────┘
```

This connection makes the harmonic oscillator a useful example for understanding how complex analysis enters physics at both classical and quantum levels.

## Appendix: Computational Work

The project is accompanied by Google Colab notebooks:

- [Colab notebook 1](https://colab.research.google.com/drive/1QZZFOXxHaJi_gHz6hVD7Ww9PD4dXxdgj?usp=drive_link)
- [Colab notebook 2](https://colab.research.google.com/drive/1cOrq28CjmeQZ0wMf8bTvYNTGCvfCr3U8?usp=drive_link)

These notebooks can be used to explore the mathematical and computational aspects of harmonic motion interactively.

## Learning Objectives

This project aims to demonstrate:

- How Euler's formula connects complex exponentials with sinusoidal motion.
- Why complex roots naturally arise when solving the SHM differential equation.
- How phasors encode amplitude and phase.
- How complex roots describe oscillation in damped systems.
- Why the quantum harmonic oscillator has discrete energy levels.
- How wavefunctions encode quantum states using complex numbers.
- Why `|ψ|²` is interpreted as a probability density.
- How position and momentum operators enter quantum mechanics.
- The conceptual difference between using complex numbers as a classical mathematical tool and treating them as part of the quantum formalism.

## References and Further Reading

The following sources informed the project and provide further background on harmonic motion, complex numbers, quantum mechanics, wavefunctions, phasors, and operator methods.

1. **Adrian.** *Solutions of the 1D Schrödinger Equation.* University of Cambridge.  
   https://www.qi.damtp.cam.ac.uk/files/Adrian/notespart2.completed.2019.pdf

2. **Anchordoqui, L. (2019).** *Quantum Mechanics.*  
   https://www.lehman.edu/faculty/anchordoqui/400_4.pdf

3. **Basic Electronics Tutorials.** *Phasor Diagram and Phasor Algebra used in AC Circuits.*  
   https://www.electronics-tutorials.ws/accircuits/phasors.html

4. **Basic Electronics Tutorials.** *Complex Numbers and Phasors in Polar and Rectangular Form.*  
   https://www.electronics-tutorials.ws/accircuits/complex-numbers.html

5. **Bowers, P. L. (2020).** *The Harmonic Oscillator: Classical versus Quantum.* Cambridge University Press.  
   https://assets.cambridge.org/97811084/29764/excerpt/9781108429764_excerpt.pdf

6. **University of California, Irvine.** *Chapter 7: The Schrödinger Equation in One Dimension.*  
   https://ps.uci.edu/~cyu/p51A/LectureNotes/Chapter7/Chapter7.pdf

7. **Lehman College.** *Chapter 23: Simple Harmonic Motion.*  
   https://www.lehman.edu/faculty/anchordoqui/chapter23.pdf

8. **University of Illinois.** *Complex Numbers and Phasor Technique.*  
   https://ws.engr.illinois.edu/sitemanager/getfile.asp?id=184

9. **University of Illinois.** *Complex Numbers in Quantum Mechanics.*  
   https://courses.physics.illinois.edu/phys580/fa2013/susy_v2.pdf

10. **Lumen Learning.** *The Heisenberg Uncertainty Principle.*  
    https://courses.lumenlearning.com/suny-physics/chapter/29-7-probability-the-heisenberg-uncertainty-principle/

11. **Lumen Learning.** *The Wave Nature of Matter Causes Quantization.*  
    https://courses.lumenlearning.com/suny-physics/chapter/30-6-the-wave-nature-of-matter-causes-quantization/

12. **Earl, R. (2004).** *Complex Numbers.* Mathematical Institute, University of Oxford.

13. **Essler, F. (2020).** *Lecture Notes for Quantum Mechanics.* University of Oxford.  
    https://www-thphys.physics.ox.ac.uk/people/FabianEssler/QM/QM2019_1.pdf

14. **MIT Mathematics. (2019).** *Formalism of Quantum Mechanics.*  
    https://math.mit.edu/~dav/quantum.pdf

15. **Fowler, M.** *Lectures on Oscillations and Waves.* University of Virginia.  
    https://galileo.phys.virginia.edu/classes/152.mf1i.spring02/Osc_Waves_Lectures.pdf

16. **University of Virginia.** *Simple Harmonic Oscillator.*  
    https://galileo.phys.virginia.edu/classes/751.mf1i.fall02/SimpleHarmOsc.htm

17. **Hautmann, F. (2011).** *Complex Numbers and Ordinary Differential Equations.* University of Oxford.  
    https://www-thphys.physics.ox.ac.uk/people/FrancescoHautmann/Cp4/comp_ode_notes_11.pdf

18. **Georgia State University HyperPhysics.** *Quantum Harmonic Oscillator.*  
    http://hyperphysics.phy-astr.gsu.edu/hbase/quantum/hosc2.html

19. **IOP Spark.** *Simple Harmonic Motion (SHM).*  
    https://spark.iop.org/collections/simple-harmonic-motion-shm

20. **Morin, D.** *Chapter 1: Oscillations.* Harvard University.  
    https://scholar.harvard.edu/files/david-morin/files/waves_oscillations.pdf

21. **Noor-ul-ain, F., Ahmad, M., Khan, M. R. & Aslam, M. (2023).** *Schrödinger Wave Equation for Simple Harmonic Oscillator.* IntechOpen.  
    https://www.intechopen.com/chapters/87998

22. **Bucknell University.** *Phasors & Phasor Diagrams.*  
    https://www.eg.bucknell.edu/~koutslts/Ph212E/Infn/phasor_handout_part1.pdf

23. **Reed College. (2010).** *Schrödinger's Equation — Physics 342.*  
    https://www.reed.edu/physics/courses/P342.S10/Physics342/page1/files/Lecture.5.pdf

24. **Physics LibreTexts / OpenStax. (2016).** *Wave Functions.*  
    https://phys.libretexts.org/Bookshelves/University_Physics/University_Physics_(OpenStax)/University_Physics_III_-_Optics_and_Modern_Physics_(OpenStax)/07%3A_Quantum_Mechanics/7.02%3A_Wavefunctions

25. **Physics LibreTexts. (2021).** *Interpretation of the Wave Function ψ(x).*  
    https://phys.libretexts.org/Bookshelves/Quantum_Mechanics/Advanced_Quantum_Mechanics_(Kok)/13%3A_The_Schrodinger_Equation/13.7%3A_Interpretation_of_the_Wave_Function_(x)

26. **Weber State University.** *Wavefunctions.*  
    https://physics.weber.edu/schroeder/quantum/Wavefunctions.pdf

27. **Prof. Niel.** *Harmonic Oscillators and Complex Numbers.* University of Colorado.  
    https://physicscourses.colorado.edu/phys2210/phys2210_fa20/lecture/lec3x-harmonic-oscillators-complex/

28. **Science by Degrees.** *Circular Motion and Phasors.*  
    https://sciencebydegrees.com/topics/13-phasors/

29. **Tong, D.** *Quantum Mechanics.* University of Cambridge.  
    https://www.damtp.cam.ac.uk/user/tong/quantum.html

30. **Tong, D.** *The Formalism of Quantum Mechanics.* University of Cambridge.  
    https://www.damtp.cam.ac.uk/user/tong/qm/qm3.pdf

31. **Vvedensky, D. D. (1982).** *Operator Methods in Quantum Mechanics.*  
    https://doi.org/10.1088/0031-9112/33/4/037

## Notes on the Sources

Some of the original source material was supplied as a bibliography with numbered citations. The references above have been consolidated into a readable list rather than preserving the original in-text numbering. The local Word/temporary image paths from the source material were not included because they are not portable GitHub assets.

## Author

**Inika Prakash**  
GitHub: [@inikaprakash](https://github.com/inikaprakash)

## License

No specific open-source licence is currently included in this repository. Unless a licence is added, the contents should be treated as **all rights reserved** by the repository owner.