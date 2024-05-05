---
date: 2024-04-22
tags:
  - Academia/MechanicalEngineering/Semester2
title: Ordinary Differential Equations
---
# Finding Wronskian
Steps to find the Wronskian
1. Assume $y_1$ and $y_2$ to be the two functions given.
2. Substitute the $y_{1}$,$y'_{1}$,$y_{2}$ and $y'_{2}$ into the following matrix to find the Wronskian $$W_{(y_{1},y_{2})}=\begin{vmatrix} y_{1} & y_{2} \\ y_{1}' & y_{2}' \end{vmatrix}$$
3. If the determinant gives
	- Zero then it is a linearly dependant equation
	- Non-zero then it is a linearly independent equation
# Verifying if $y$ are solution of Ordinary Differential Equations(ODE)
Substitute $y$ into required equation and check whether if $\text{LHS}\neq \text{RHS}$
**TODO**
## Solving the Initial Value Problem(IVE)
Steps to solve IVE
- Find the General Solution if not given.
- Substitute it into the results given and solve the equations simultaneously.

# Solving for General Solution(GS)
There are two possible cases $R(x)$
- If $R(x)=0$ it is a homogeneous linear differential equation(LDE). In this case, the general solution(GS), $y$ is equal to $y_{c}$.
- If $R(x)\neq 0$ then it is a non homogeneous equation linear differential equation(LDE). In this case, the general solution(GS),$y$ is equal to $y=y_c+y_p$.
## Homogeneous Equations
Steps to find GS for homogeneous equations
- Convert it into $D_{x}y$ form. For example, $y'''$ can be written as $D^3y$.
- Take $y$ as common term
- Write the equation as a function of $D$ and y
- Auxiliary equation is of the form $f(m)=0$. Therefore write $F(D)$ in the form of $f(m)$, that is replace $D$ with $m$.
- Solve for m.
- General solution, y is written with respect to the following table 

| Values of m                     | Solution                                                                  |
| ------------------------------- | ------------------------------------------------------------------------- |
| $m_{1}$,$m_2$,$m_3$,...,$m_n$   | $y=C_{1}e^{m_{1}x}+C_{2}e^{m_{2}x}+C_{3}e^{m_{3}x}+\dots+C_{n}e^{m_{n}x}$ |
| $m_{1}=m_{2}=m_{3}=\dots=m_{n}$ | $y=(C_{1}+xC_{2}+x^2C_{3}+\dots+x^{n-1}C_{n})e^{mx}$                      |
| $\alpha\pm i\beta$              | $y=e^{\alpha x}[C_{1}\cos \beta x+c_{2}\sin \beta x]$                     |
## Non Homogeneous Equations
Steps to find the GS for non homogeneous equation
- Find $y_c$ by following the steps used in [Homogeneous Equations](Ordinary%20Differential%20Equations.md#Homogeneous%20Equations)
- Then find $y_p$ or particular integral
- Consider a trial solution for the equation, with the help of the following table

| Case | R(x)                                 | Trial Solution                                       |
| ---- | ------------------------------------ | ---------------------------------------------------- |
| 1    | $ke^{ax}$                            | $R(x)=Ae^{ax}$                                       |
| 2    | $k\sin ax$ or $k\cos ax$             | $R(x)=A\cos ax+B\sin ax$                             |
| 3    | $kx^m$                               | $R(x)=k_{0}+k_{1}x+K_{2}x^2+K_{3}x^3+\dots+K_{m}x^m$ |
| 4    | $ke^{ax}\cos bx$ or $ke^{ax}\sin bx$ | $R(x)=e^{ax}(A\cos bx+B\sin bx)$                     |
- Differentiate as required and substitute it into Ordinary Differential Equation(ODE)
- Solve for $A$,$B$ or the variables $k_{n}$.
	- Group in the form of polynomial when solving for $A$, $B$ and $k_{n}$
	- In cases 2,3 and 4, equate the coefficient of $x$ to 0, to solve for $A$,$B$ and $k_n$
- Substitute the values into the $A$,$B$ and $k_n$, to find $y_p$
- To find General solution, $y=y_{c}+y_{p}$ 
### Special Cases
- If multiple functions are present, perform the above steps for each of the functions and add them
- If the solution for $y_p$ is invalid, use modification rule. This is done by multiplying variable (like $x$) to the trial solution. This step is performed till the solution is valid
## Method of Variation of Parameters
When is this used?
This method is used when the $R(x)$ is not in [Non Homogeneous Equations](10-19%20Academia/10%20Mechanical%20Engineering/10.02%20Semester%202/Ordinary%20Differential%20Equations.md#Non%20Homogeneous%20Equations)
Steps performed
- Find the CF or $y_c$
- Equate it to $y_{c}=C_{1}y_{1}+C_{2}y_{2}$ to find $y_{1}$ and $y_{2}$
- Find the [Wronskian](10-19%20Academia/10%20Mechanical%20Engineering/10.02%20Semester%202/Ordinary%20Differential%20Equations.md#Finding%20Wronskian) of $y_1$ and $y_2$
- Find the $y_p$ using the following formula $$y_{p}=y_{1}\int \frac{y_{2}R(x)}{w}\, dx +y_{2}\int \frac{y_{1}R(x)}{w} \, dx  $$
- Find the general solution by $y_{c}+y_{p}$ 
