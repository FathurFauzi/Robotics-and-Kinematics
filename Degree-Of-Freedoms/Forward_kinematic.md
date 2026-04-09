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
\cos(\theta_1+\theta_2) = \cos(\theta_1)\cdot\cos(\theta_2) - \sin(\theta_1)\cdot\sin(\theta_2)
$$

$$
\sin(\theta_1+\theta_2) = \sin(\theta_1)\cdot\cos(\theta_2) + \cos(\theta_1)\cdot\sin(\theta_2)
$$

Put it on the equations:

<div style="overflow-x: auto;">

$$
\text{[4.1a]} \quad x = r_1\cdot\cos(\theta_1)+r_2\cdot\left({\color{#27AE60}{\cos(\theta_1)\cdot\cos(\theta_2)-\sin(\theta_1)\cdot\sin(\theta_2)}}\right)
$$

$$
\text{[4.1b]} \quad y = r_1\cdot\sin(\theta_1)+r_2\cdot\left({\color{#27AE60}{\sin(\theta_1)\cdot\cos(\theta_2)+\cos(\theta_1)\cdot\sin(\theta_2)}}\right)
$$

</div>

Then we're gonna multiply $r_2$ to the brackets:

<div style="overflow-x: auto;">

$$
\text{[4.2a]} \quad x = r_1\cdot\cos(\theta_1)+{\color{#27AE60}{r_2}}\cdot\cos(\theta_1)\cdot\cos(\theta_2)-{\color{#27AE60}{r_2}}\cdot\sin(\theta_1)\cdot\sin(\theta_2)
$$

$$
\text{[4.2b]} \quad y = r_1\cdot\sin(\theta_1)+{\color{#27AE60}{r_2}}\cdot\sin(\theta_1)\cdot\cos(\theta_2)+{\color{#27AE60}{r_2}}\cdot\cos(\theta_1)\cdot\sin(\theta_2)
$$

</div>

We need to isolate the terms containing $\theta_1$ to simplify the expression

<div style="overflow-x: auto;">

$$
\text{[4.3a]} \quad x = \left(r_1+r_2\cdot\cos(\theta_2)\right)\cdot{\color{#27AE60}{\cos(\theta_1)}}-\left(r_2\cdot\sin(\theta_2)\right)\cdot{\color{#27AE60}{\sin(\theta_1)}}
$$

$$
\text{[4.3b]} \quad y = \left(r_1+r_2\cdot\cos(\theta_2)\right)\cdot{\color{#27AE60}{\sin(\theta_1)}}+\left(r_2\cdot\sin(\theta_2)\right)\cdot{\color{#27AE60}{\cos(\theta_1)}}
$$

</div>

Now you can see that under bracets in both x and y functions ? $( r_1+r_2\cdot\cos(\theta_2) )$ and $(r_2\cdot\sin(\theta_2))$.. they have the same function. we will gonna use this function far later, so i'm gonna keep it as:

><div style="overflow-x: auto; padding: 10px 0;">
>
>$$
\boxed{
>(  r_1+r_2\cdot\cos(\theta_2) ) ={\color{#D35400}{k_1}}}
>$$
>
>$$
\boxed{
>\quad(r_2\cdot\sin(\theta_2))\quad={\color{#D35400}{k_2}}}
>$$

></div>

Geometrically, k1 and k2 will look like this

![Picture K1]()
This equations is one of the fundamental of robotics. So, i hope you can get along with this as soon as possible...

## Inverse Kinematic

First we need to find the angle between $r_1$ and $r_2$ ($\alpha$).

![Picture]()

As on the picture, imagine $r_1$ and $r_2$ were two edges of a triangle, and the other edge ($C$) is the hypotenuse.

Because $\alpha$ is not **90°**, we cannot find $C$ using ordinary Pythagoras. Instead, we are going to use the Law of Cosines:

$$
\quad C^2 = A^2 + B^2 - 2AB \cdot \cos(\alpha)
$$

Substitute this with our variables:

$$
 \quad C^2 = {\color{#27AE60}{ r_1^2 + r_2^2 - 2r_1r_2}} \cdot \cos(\alpha)
$$

We know that $C$ is the distance between the base and the tip of the arm. Using the Pythagorean theorem:

$$
 \quad C^2 = x^2 + y^2
$$

We can substitute $C^2$ in equation [3] with those theorem:

$$
 \quad {\color{#27AE60}{x^2 + y^2}} = r_1^2 + r_2^2 - 2r_1r_2 \cdot \cos(\alpha)
$$

We want to calculate $\theta_2$, not $\alpha$. From the geometry, we know that:

$$
 \quad \alpha = 180^\circ - \theta_2
$$

Put it in the previous equation:

$$
 \quad x^2 + y^2 = r_1^2 + r_2^2 - 2r_1r_2 \cdot \cos({\color{27AE60}{180^\circ - \theta_2}})
$$

Using the trigonometric identity $\cos(\text{180°} - \theta) = -\cos(\theta)$, we get:

$$
 \quad x^2 + y^2 = r_1^2 + r_2^2 {\color{#27AE60}{ + 2r_1r_2 \cdot \cos(\theta_2)}}
$$

Now, our goal is to turn the equations to find $\theta_2$, to find it, we subtract both side of equation with $r_1^2+r_2^2$ first:

$$
\quad {\color{#27AE60}{(- r_1^2 - r_2^2)}} + x^2 + y^2 = {\color{#27AE60}{(- r_1^2 - r_2^2)}} + r_1^2 + r_2^2 + 2r_1r_2 \cdot \cos(\theta_2)
$$

$$
\downarrow
$$

$$
\quad x^2 + y^2 {\color{#27AE60}{- r_1^2 - r_2^2}} = 2r_1r_2 \cdot \cos(\theta_2)
$$

Divided both sides with $2r_1r_2$:

$$
\quad \frac{x^2 + y^2 {\color{#27AE60}{- r_1^2 - r_2^2}}}{\color{#27AE60}{2r_1r_2}} = \frac{2r_1r_2 \cdot \cos(\theta_2)}{\color{#27AE60}{2r_1r_2}}
$$

$$
\downarrow
$$

$$
\quad \frac{x^2 + y^2 {\color{#27AE60}{- r_1^2 - r_2^2}}}{\color{#27AE60}{2r_1r_2}} = \cos(\theta_2)
$$

To calculate the angle of $\theta_2$, we will use $\cos^{-1}$ to both sides of equations:

$$
 \quad {\color{#27AE60}{\cos^{-1}}} \left(\frac{x^2 + y^2 - r_1^2 - r_2^2}{2r_1r_2}\right) = {\color{#27AE60}{\cos^{-1}}}( \cos(\theta_2))
$$

$$
\downarrow
$$

> <div style="padding: 20px 0; overflow-x: auto;">
> 
>$$
\color{#D35400}\quad
>\boxed{
> {\color{#27AE60}{\theta_2}} = {\color{#27AE60}{\cos^{-1}}} \left(\frac{x^2 + y^2 - r_1^2 - r_2^2}{2r_1r_2}\right)
}
>$$
> 
> </div>

We're gonna use this equation from now on, so I hope you can get along with this.

After we get $\theta_2$, our next steps is to find $\theta_1$ . It actually much simpler than $\theta_2$.

Remember ${\color{#D35400}{k_1}}$ and ${\color{#D35400}{k_2}}$? That formula is for this equations. To find $\theta_1$, we need to subtract angle of x and y resultant, and k1 and k2 resultant.

>$$
>\theta_1 = \tan^{-1}(\frac{k_2}{k_1})-\tan^{-1}(\frac{k_2}{k_1})
>$$
