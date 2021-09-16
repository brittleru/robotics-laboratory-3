# Robotics Laboratory 3
### Brief
This laboratory named use of programming languages to solve the direct problem of position in robot structures is taught by Sl. Dr. Ing. Laurentiu Adrian Cartal. The proposed constructive solution consists of a positioning mechanism with three degrees of freedom, which consists of three kinematic elements and three kinematic couplings. The three degrees of freedom of the positioning mechanism correspond to the movements of: Rotation at the base (Rz), vertical translation (Tz) and rotation of the articulated arm in horizontal plane (Rz).

### Kinematic sheme of the robot SCARA

The figure below shows the kinematic diagram of this robot:
- the arm 1 has a rotational movement ω1 with the vertical axis with respect to the support sp;
- arm 2 has a second rotational movement ω2 with respect to arm 1;
- the plate 3 has the rotational movement with respect to the arm 2;
- element 4 translates with vz from the plate 3;
- at the end of element 4 is fixed the gripping device DA which fixes the working object OL.
</br>

So, for the structure presented below, the inverse geometric problem for an imposed trajectory will be solved. Due to the fact that the movement in the direction of the oz axis is obtained by acting on a single degree of freedom, solving this problem is reduced to solving the problem of dyads in the theory of mechanisms.

![Kinematic sheme](https://github.com/brittleru/robotics-laboratory-3/blob/main/images/kinematic_scheme_of_structure.png?raw=true)


### Kinematic scheme in the xoy plane
![Kinematic sheme in xoy plan](https://github.com/brittleru/robotics-laboratory-3/blob/main/images/kinematic_scheme_in_xoy.png?raw=true)

From the figure above, knowing the position of the point M (x, y) in the xoy plane and the orientation angle φ, determine the angles q1, q2 and q3:
- q1 = f (x, y, z);
- q2 = f (x, y, z);
- q3 = f (x, y, z);
- q4 = f (x, y, z).
</br>

Having the equations we will determine the positions in the robot workspace of the points: - initially Ri (xi, yi, zi) and finally Rf (xf, yf, zf). In the next step, the trajectory will be discretized on a number of n segments.
</br></br>

Knowing the data of the SCARA robotic structure, the length of the arms: L1 = 200mm, L2 = 180m; vertical axis travel: 250mm; H1 = 0.228m; H2 = 0.016m; H3 = 0.028m; position in the local system a = 0.02m; c = 0.02; positions in the workspace: initial 𝑟𝑖 = (0.105, -0.220, 0.02)) and final 𝑟𝑓 = (0.325, 0.100, 0.150)), initial orientation φi = 0deg and final φf = 90deg, we will determine the following values


## Results
![results table](https://github.com/brittleru/robotics-laboratory-3/blob/main/images/results.png?raw=true)

## Conclusion
The trajectory described by the robot arm is a circular one, and for discretization, it was divided into 10 intermediate segments. Knowing the initial and final coordinates, we could calculate the coordinates of the intermediate points, according to the formula: rn = ri + n * Δr, where Δr = (ri + rf) / 10. The calculation of the position in the robot workspace can be done in two ways: either by transformation with matrices, or by analytical calculation.
</br></br>

You can check the results here: https://brittleru.github.io/robotics-laboratory-3/
