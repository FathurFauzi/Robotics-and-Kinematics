## Forward Kinematic

Our first equations was:
$$
 \quad x = r_1\cdot\cos(\theta_1)+r_2\cdot\cos(\theta_1+\theta_2)
$$

$$
 \quad y = r_1\cdot\sin(\theta_1)+r_2\cdot\sin(\theta_1+\theta_2)
$$

We will seperate $\theta_1$ and $\theta_2$ for further calculations. to seperate them, we're gonna use the equation below:
$$
\cos(\theta_1+\theta_2)=cos(\theta_1)\cdot\cos(\theta_2)-sin(\theta_1)\cdot\sin(\theta_2)
$$
$$
\sin(\theta_1+\theta_2)=\cos(\theta_1)\cdot\cos(\theta_2)-sin(\theta_1)\cdot\sin(\theta_2)
$$
put it on the equations:

<div style="overflow-y:scroll;">

$$
 \quad x = r_1\cdot\cos(\theta_1)+r_2\cdot\left({\color{27AE60}{cos(\theta_1)\cdot\cos(\theta_2)-sin(\theta_1)\cdot\sin(\theta_2)}}\right)
$$

$$
 \quad y = r_1\cdot\sin(\theta_1)+r_2\cdot\left({\color{27AE60}{\cos(\theta_1)\cdot\cos(\theta_2)-sin(\theta_1)\cdot\sin(\theta_2)}}\right)
$$
 
</div>


<div style="overflow-y:scroll;">

$$
 \quad x = r_1\cdot\cos(\theta_1)+r_2\cdot\left({\color{27AE60}{cos(\theta_1)\cdot\cos(\theta_2)-sin(\theta_1)\cdot\sin(\theta_2)}}\right)
$$

$$
 \quad y = r_1\cdot\sin(\theta_1)+r_2\cdot\left({\color{27AE60}{\cos(\theta_1)\cdot\cos(\theta_2)-sin(\theta_1)\cdot\sin(\theta_2)}}\right)
$$
 
</div>


Now we do the inverse of putting $r_2$ to $\cos(\theta_1)$ and $\sin(\theta_1)$

<div style="overflow-y:scroll;">

$$
 \quad x = r_1\cdot\cos(\theta_1)+{\color{27AE60}{r_2}}\cdot\cos(\theta_1)\cdot\cos(\theta_2)-{\color{27AE60}{r_2}}\cdot\sin(\theta_1)\cdot\sin(\theta_2)
$$

$$
 \quad y = r_1\cdot\sin(\theta_1)+{\color{27AE60}{r_2}}\cdot\cos(\theta_1)\cdot\cos(\theta_2)-{\color{27AE60}{r_2}}\cdot\sin(\theta_1)\cdot\sin(\theta_2)
$$

</div>

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
\text{[3]} \quad C^2 = {\color{#27AE60}{ r_1^2 + r_2^2 - 2r_1r_2}} \cdot \cos(\alpha)
$$

We know that $C$ is the distance between the base and the tip of the arm. Using the Pythagorean theorem:

$$
\text{[2.2]} \quad C^2 = x^2 + y^2
$$

We can substitute $C^2$ in equation [3] with those theorem:

$$
\text{[2.3.1]} \quad {\color{#27AE60}{x^2 + y^2}} = r_1^2 + r_2^2 - 2r_1r_2 \cdot \cos(\alpha)
$$

We want to calculate $\theta_2$, not $\alpha$. From the geometry, we know that:

$$
\text{[2.3.2a]} \quad \alpha = 180^\circ - \theta_2
$$

Put it in the previous equation:

$$
\text{[2.3.2]} \quad x^2 + y^2 = r_1^2 + r_2^2 - 2r_1r_2 \cdot \cos({\color{27AE60}{180^\circ - \theta_2}})
$$

Using the trigonometric identity $\cos(\text{180°} - \theta) = -\cos(\theta)$, we get:

$$
\text{[2.3.3]} \quad x^2 + y^2 = r_1^2 + r_2^2 {\color{#27AE60}{ + 2r_1r_2 \cdot \cos(\theta_2)}}
$$

Now, our goal is to turn the equations to find $\theta_2$, to find it, we subtract both side of equation with $r_1^2+r_2^2$ first:

$$
\text{[2.3.3]} \quad {\color{#27AE60}{(- r_1^2 - r_2^2)}}+x^2 + y^2 = {\color{#27AE60}{(- r_1^2 - r_2^2)}} + r_1^2 + r_2^2 { + 2r_1r_2 \cdot \cos(\theta_2)}
$$

Now we'll get

$$
\text{[2.3.3]} \quad x^2 + y^2 {\color{#27AE60}{- r_1^2 - r_2^2}} = { 2r_1r_2 \cdot \cos(\theta_2)}
$$

Divided both sides with $2r_1r_2$:

$$
\text{[2.3.3]} \quad \frac{x^2 + y^2 {- r_1^2 - r_2^2}}{\color{#27AE60}{2r_1r_2}} = \frac{{ 2r_1r_2 \cdot \cos(\theta_2)}}{\color{#27AE60}{2r_1r_2}}
$$

the equation will be:

$$
\text{[2.3.3]} \quad \frac{x^2 + y^2 {- r_1^2 - r_2^2}}{\color{#27AE60}{2r_1r_2}} ={ \cos(\theta_2)}
$$

To calculate the angle of $\theta_2$, we will use $\cos^{-1}$:

$$
\text{[2.3.3]} \quad {\color{27AE60}{\cos^{-1}}} \left(\frac{x^2 + y^2 {- r_1^2 - r_2^2}}{2r_1r_2}\right) = {\color{27AE60}{\cos^{-1}}}( \cos(\theta_2))
$$

Finally we'll get:

>$$
\color{D35400}{\text{[2.3.3]} \quad  {\color{27AE60}{\theta_2}}= {\color{27AE60}{\cos^{-1}}} \left(\frac{x^2 + y^2 {- r_1^2 - r_2^2}}{2r_1r_2}\right)}
$$

We're gonna use this equation from now on, so i hope you can get along with this.
