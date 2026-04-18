# 3 Degree of Freedom (3-DoF)

with 3-dof, we can input one more thing, that is slope. Slope that i'm talking about is slope of El3 towards horizontal axis.

So, Know values are $r_1,r_2,r_3,x,y,\text{and }\phi$

![3-Dof](/Degree-Of-Freedoms/3-DOF/3-dof%20Media/slope%20explained.PNG)

As you can see from Picture above, $\phi$ is the input that we talking about, and $\beta$ is El3's slope towards horizontal axis. $\phi$ and $\beta$ actually has equal value.


>[!NOTE]
>Angle increase while counter-clockwise, and decrease when clockwise. Thats why $\beta$ is positive while $\phi$ is negative. because $\beta$ is actually rotating $66°$ clockwise

Now to find the angles in Nodes ($\theta_3,\theta_2,\theta_1$), we will use $\phi$ first to find El2 positions.

The formula is :
- x-axis:

$$
El2_x = El3_x-r_3\cdot\cos(\phi)
$$

- y-axis:

$$
El2_y = El3_y-r_3\cdot\sin(\phi)
$$

Now we get the EL2 positions, we can calculate the rest of it like we calculate 2-dof:

- finding $\theta_2$ :

$$
\theta_2 = \cos^{-1} \left(\frac{x^2 + y^2 - r_1^2 - r_2^2}{2r_1r_2}\right)\cdot(-1)
$$

>[!NOTE]
>(-1) is just to make the robot elbow up [(See the bottom of 2-dof-Kinematics.md)](../2-DOF/2-dof-Kinematics.md)

- finding $k_1$ and $k_2$ values:

$$
k_1 = r_1+r2\cdot\cos(\theta_2) 
$$

$$
k_2 = r_2\cdot\sin(\theta_2)
$$

- Finding $\theta_1$

$$
\theta_1 = \tan^{-1}(\frac{y}{x})-\tan^{-1}(\frac{k_2}{k_1})
$$

Now we got all of them, except $\theta_3$.. to Find it, we need to get back to Forward kinematics first:

We know that the coordinate of the tip of robot (end effector) is equal to their $r$ that multiplied by $\cos(\theta)$ or ( $\sin(\theta)$ for y coordinate) and the angle was accumulated as we closer to the end effector. 

Using the same logic, we know the slope ($\phi$) was equal to all the angles ($\theta_1+\theta_2+\theta_3$). which means, to find $\theta_3$, we just need to subtract both sides with $\theta_1$ and $\theta_2$

$$
\theta_1+\theta_2+\theta_3 {\color{#27AE60} -\theta_1-\theta_2} = \phi {\color{#27AE60} -\theta_1-\theta_2}
$$

$$
\downarrow
$$

$$
\theta_3 = \phi{\color{#27AE60} -\theta_1-\theta_2}
$$


