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

![Picture K1](../../Media/K1%20and%20K2%20versions.PNG)

While k1 is x parameters but rotated by $\theta_1$, and k2 is y parameters but rotated by $\theta_2$..

Now compare to this picture :
![Picture k, but in different aproach](../../Media/X%20and%20Y%20version.PNG)

k1 and k2 was sharing the same hipotenuse and El2, their difference was only in red and green line.. Simply, k1 is $X_s$, but was rotated by $\theta_1$, and so does k2. This explanations will be important, because we can calculate angle of $\theta_1$ by subtracting k1 and k2 angle with x and y angle.. 

## Inverse Kinematic

First we need to find the angle between $r_1$ and $r_2$ ($\alpha$).

![Picture](../../Media/angle%20definition.PNG)

As on the prior picture, imagine $r_1$ and $r_2$ were two edges of a triangle, and the other edge ($C$) is the hypotenuse.

Because $\alpha$ (angle in the middle of r1 and r2) is not **90°**, we cannot find $C$ or hypotenuse using ordinary Pythagoras. Instead, we are going to use the Law of Cosines:

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

We want to calculate $\theta_2$, not $\alpha$. From the picture, we know that:

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
>\theta_1 = \tan^{-1}(\frac{y}{x})-\tan^{-1}(\frac{k_2}{k_1})
>$$

To help you understand why it subtracted, see this figure:

![Angle Subtraction](../../Media/polar%20and%20rect%20subtraction.PNG)
$\theta_{pol} $ is result of $\tan^{-1}(\frac{k_2}{k_1})$, while $\theta_{rect}$ is result of $\tan^{-1}(\frac{y}{x})$. To find $\theta_1$, whic is the difference between $\theta_{rect}$ and $\theta_{pol}$ we can subtract them.

So, the summary of this subject is:
- we can turn coordinate into angles using inverse Kinematics
- to turn it, we must find $\theta_2$ first.
- $\theta_2$ formula is 

$$
\cos^{-1} \left(\frac{x^2 + y^2 - r_1^2 - r_2^2}{2r_1r_2}\right)
$$

- then we need to find $\theta_1$. But to find it, we find k1 and k2 first.
- k1 formula is 

$$
r_1+r2\cdot\cos(\theta_2)
$$

- while k2 formula is 

$$
r2\cdot\sin(\theta_2)
$$

- Hence $\theta_1$ is
$$
\tan^{-1}(\frac{y}{x})-\tan^{-1}(\frac{k_2}{k_1})
$$

>[!:bulb:tip]
>you can multiply $\theta_2$ by (-1), Because it will make node between $r_1$ and $r_2$ higher than its Hipotenuse.. this layout was a standard to make a robot.

this is $\theta_2$ when positive:
![theta2 positive](../../Media/theta%202%20normally.PNG)

and this is when $\theta_2$ negative:
![theta2 negative](../../Media/theta%202%20when%20multiply%20by%20-1.PNG)..

Now we Know how to make 2-dof Robot. Now we make it so we can manage ourselves the slope of the target [(3-DOF)](../3-DOF/3-dof-Kinematics.md).




