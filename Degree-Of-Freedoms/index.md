## Forward Kinematic

$$
\begin{align}
x &= r_1\cdot\cos(\theta_1)+r_2\cdot\cos(\theta_1+\theta_2)\phantom{12345}\\
y &= r_1\cdot\sin(\theta_1)+r_2\cdot\sin(\theta_1+\theta_2)\phantom{12345}
\end{align}
$$

## Inverse Kinematic

First we need to find the angle between $r_1$ and $r_2$ ($\alpha$).

![Picture]()

As on the picture, imagine $r_1$ and $r_2$ were two edges of a triangle, and the other edge ($C$) is the hypotenuse.

Because $\alpha$ is not $90^\circ$, we cannot find $C$ using ordinary Pythagoras. Instead, we are going to use the Law of Cosines:

$$
C^2 = A^2 + B^2 - 2AB \cdot \cos(\alpha)
$$

Substitute this with our variables:

$$
C^2 = r_1^2 + r_2^2 - 2r_1r_2 \cdot \cos(\alpha) \phantom{123456}(3)
$$

We know that $C$ is the distance between the base and the tip of the arm. Using the Pythagorean theorem:

$$
C^2 = x^2 + y^2
$$

We can substitute $C^2$ in equation (2.3) with those theorem:

$$
x^2 + y^2 = r_1^2 + r_2^2 - 2r_1r_2 \cdot \cos(\alpha) \tag{2.3.1}
$$

We want to calculate $\theta_2$, not $\alpha$. From the geometry, we know that:

$$
\alpha = 180^\circ - \theta_2
$$

Put it in the last equation:

$$
x^2 + y^2 = r_1^2 + r_2^2 - 2r_1r_2 \cdot \cos(180^\circ - \theta_2) \tag{2.3.2}
$$

Using the trigonometric identity $\cos(180^\circ - \theta) = -\cos(\theta)$, we get:

$$
x^2 + y^2 = r_1^2 + r_2^2 + 2r_1r_2 \cdot \cos(\theta_2) \tag{2.3.3}
$$

ai suggestions
$$
\begin{aligned}
  P_x &= \cos(\theta) \quad &\dots\dots [1.1] \\
  P_y &= \sin(\theta) \quad &\dots\dots [1.2]
\end{aligned}
$$