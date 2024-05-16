---
date: 2024-04-25
tags:
  - Academia/MechanicalEngineering/Semester2
title: Basics of Electrical Engineering Module 1
---
# DC Circuits
Power equations $$P=VI=I^2R=\frac{V^2}{R}$$
where
- $P$ is power
- $V$ is voltage
- $I$ is current
- $R$ is resistance
### Voltage Division Rule
This rule is used to determine the voltage between resistors in series combination.
The formulae used to calculate is $$V_{out}=\frac{R_{x}}{R_{\text{equivalent}}}V$$
where 
- $V_{out}$ is the voltage from specific resistor
- $R_{x}$ is the resistor from which the $V_{out}$ is taken from
- $R_{\text{equivalent}}$ is the total resistance in the circuit
- $V$ is the voltage in the circuit (Can be calculated with Ohm's law)
### Current Division Rule
This rule is used to determine the current between resistors in parallel combination.
The formulae used to calculate is $$I_{\text{out}}=\frac{I\times(\text{Combination other resistors other than x})}{R_{x}+(\text{Combination other resistors other than x})}$$
where
- $I_{\text{out}}$ is the current from specific resistor
- $I$ is the current in the circuit (Calculated from Ohm's law)
- $(\text{Combination other resistors other than x})$ is the combination of other resistors (in parallel)
- $R_\text{x}$ is the resistor from which the $I_\text{out}$ is taken from
# Analysis of DC Circuits
# Terminology
## Node
A junction where two or more elements connect is called a node.

There are two types of nodes
- **Simple Node**
  Two elements are connected and current division rule takes place
- **Principle Node**
  More than 2 elements are connected and current division rule takes place

Therefore in **nodal analysis** we only consider **principle node** only.
### Reference Node
One node is assigned $V=0$ is considered as reference node. All other nodes are measured relatively to reference node. Most commonly used methods are
- Negative terminal of the power source
- Node connected to most number of branches
## Mesh
A loop does not contain any inner loop
## Voltage Drop
Voltage drop occurs when there is a voltage drop on transferring charge between two points. Voltage drop is represented with $V$.

Representation
- $+\text{ve}$ during rise in potential
- $-\text{ve}$ during fall in potential

Dealing with elements
- **Battery or electric cell**
	- From positive to negative terminal, fall in potential
	- From negative to positive terminal, rise in potential
# Kirchoff's Laws
## Kirchoff's First Law (Current Law) (Junction Rule)
The algebraic sum of all currents entering and leaving node is equal to zero. This is based on **Law of Conservation of Charge**.
## Kirchoff's Second Law (Voltage Law) (Loop Rule)
The algebraic sum of all voltages around in a close loop is equal to zero. This is based on the **Law of Conservation of Energy**.
# Analysis of Circuits
## Mesh Analysis
Here [Kirchoff's Second Law (Voltage Law) (Loop Rule)](10-19%20Academia/10%20Mechanical%20Engineering/10.02%20Semester%202/BEE%20Module%201.md#Kirchoff's%20Second%20Law%20(Voltage%20Law)%20(Loop%20Rule)) is used for analysis.

Application
- Applicable to planar networks only (Non-crossed branches)
- Number of equations required to solve electrical network = number of meshes = $\text{number of branches}- (\text{number of nodes} - 1)$

Steps in analysis
- Identify the meshes
- Assume the flow of current in clockwise or anticlockwise, preferably in clockwise direction (Ignore the position and orientation of voltage or power supply)
- Develop KVL for each loop
- Use [Voltage Drop](10-19%20Academia/10%20Mechanical%20Engineering/10.02%20Semester%202/BEE%20Module%201.md#Voltage%20Drop) for voltages
- The voltage through resistor is considered negative.
- For resistors that are common between more than 1 meshes, consider the flow of current and subtract or add them accordingly. For example, if resistor $R_1$ is common between current flow $I_1$ and $I_2$ flowing clockwise and anticlockwise respectively, the voltage from $R_1$ can be written as $R_1(I_{1}-I_{2})$
- Solve the system of equations
## Node Analysis
Here [Kirchoff's First Law (Current Law) (Junction Rule)](10-19%20Academia/10%20Mechanical%20Engineering/10.02%20Semester%202/BEE%20Module%201.md#Kirchoff's%20First%20Law%20(Current%20Law)%20(Junction%20Rule)) is used for analysis.

Here we only consider nodes having more than two branches or principle node.

Application
- Applicable to planar and non planar networks
- Equations required to solve nodal analysis = $\text{number of nodes}-1$

>[!tip] 
>When two nodes are beside each other, take a common node between them and ignore the previous two

Steps in analysis
- Identify the principle nodes
- Consider a node as reference node and assign $V=0$
- Develop KCL for each loop  by adding the currents flowing from the node
- Format for obtaining current $\frac{\sum{\text{voltage}}}{\sum{\text{resistance}}}$
- If any current is provided at a path, just consider the current and nothing else (like resistors)

To find voltage through a resistor take the term of the selected resistor and substitute the values of calculated voltages as required.
# Magnetic Circuits
Magnetic Field
- Space or region, poles experience force
- Strongest at poles, weakest at centre
- N-S outside and S-N inside the magnet
- Closed loops and they do not intersect

Magnetic Flux
- amount of magnetic field by magnetic source
- Unit is **Wb**
- $1 \text{Wb}=10^8 \text{lines}$
- Magnetic Flux Density is flux per unit area $$B=\frac{\phi}{A}Wbm^{-2}\text{or Tesla}$$
Magnetomotive Force
- Force which tends to drive flux through magnetic flux (AT)
- $$\text{mmf = Number of turns in coil × Current}$$
- Magnetic Intensity/ Field Strength ($\frac{mmf}{\text{length}}$) $$H=\frac{NI}{l}$$

Permeability
- Ability to force magnetic flux through medium
- $$\mu=\frac{B}{H}$$
  Where
  - $B$ is magnetic flux density
  - $H$ is Magnetic field strength

Reluctance
- Opposition to flow of flux by magnetic circuit
- $$S=\frac{1}{\mu A}$$
  Where
  - $\mu$ is permeability
  - $A$ is area of cross section
- $$S=\frac{NI}{\phi}$$
# Electromagnetic Induction
Faraday's law of Electromagnetic Induction
- Whenever a conductor is placed in a varying magnetic field, an electromotive force is induced. If the conductor circuit is closed, a current is induced, which is called induced current.

Lenz's Law
- In electromagnetism, statement that an induced electric current flows in a direction such that the current opposes the change that induced it.
- $$e=-\frac{d\lambda}{dt}=-N \frac{d\phi}{dt}$$
## Dynamically Induced emf
- emf induced due to relative motion between conductor and field
- $$e=Blv\sin \theta$$
	- If no angle is given$$e=Blv$$
## Statically Induced emf
- emf induced without relative motion between conductor and field
- AC current is used
- Principle of transformer
- Unit is Henry
### Self Induced Emf
- Emf induced due to change in flux produced by its own winding
- $$L=\frac{N\phi}{I}$$
- Reluctance $$e=-L \frac{dT}{dt}$$
### Mutually Induced Emf
- Emf induced due to change in flux produced in nearby coil
- $$M=\frac{N_{2}\phi_{2}}{I_{1}}$$
- Reluctance $$e=-M \frac{dI_{1}}{dt}$$
- Coefficient of coupling
  degree of coupling between two magnetically linked coils or ratio of mutual inductance actually present between the coils to the maximum possible value.
  $$M=k\sqrt{ L_{1}L_{2}}$$ Where
  - If $k=0$ magnetically isolated and if $k=1$ tightly coupled
  - $L_1$ and $L_2$ are the inductance of two coils
