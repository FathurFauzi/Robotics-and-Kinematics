## Forward Kinematic

$$
\text{[1.1]} \quad x = r_1\cdot\cos(\theta_1)+r_2\cdot\cos(\theta_1+\theta_2)
$$

$$
\text{[1.2]} \quad y = r_1\cdot\sin(\theta_1)+r_2\cdot\sin(\theta_1+\theta_2)
$$

## Inverse Kinematic

First we need to find the angle between $r_1$ and $r_2$ ($\alpha$).

![Picture]()

As on the picture, imagine $r_1$ and $r_2$ were two edges of a triangle, and the other edge ($C$) is the hypotenuse.

Because $\alpha$ is not **90°**, we cannot find $C$ using ordinary Pythagoras. Instead, we are going to use the Law of Cosines:

$$
\text{[2.1]} \quad C^2 = A^2 + B^2 - 2AB \cdot \cos(\alpha)
$$

Substitute this with our variables:

$$
\text{[3]} \quad C^2 = r_1^2 + r_2^2 - 2r_1r_2 \cdot \cos(\alpha)
$$

We know that $C$ is the distance between the base and the tip of the arm. Using the Pythagorean theorem:

$$
\text{[2.2]} \quad C^2 = x^2 + y^2
$$

We can substitute $C^2$ in equation [3] with those theorem:

$$
\text{[2.3.1]} \quad x^2 + y^2 = r_1^2 + r_2^2 - 2r_1r_2 \cdot \cos(\alpha)
$$

We want to calculate $\theta_2$, not $\alpha$. From the geometry, we know that:

$$
\text{[2.3.2a]} \quad \alpha = 180^\circ - \theta_2
$$

Put it in the last equation:

$$
\text{[2.3.2]} \quad x^2 + y^2 = r_1^2 + r_2^2 - 2r_1r_2 \cdot \cos(180^\circ - \theta_2)
$$

Using the trigonometric identity $\cos(\text{**180°**} - \theta) = -\cos(\theta)$, we get:

$$
\text{[2.3.3]} \quad x^2 + y^2 = r_1^2 + r_2^2 + 2r_1r_2 \cdot \cos(\theta_2)
$$