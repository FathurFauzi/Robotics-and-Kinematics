## Forward Kinematic
$$x = r_1\cdot\cos(\theta_1)+r2\cdot\cos(\theta_1+\theta_2)\tag{2.1}$$
$$y = r_1\cdot\sin(\theta_1)+r2\cdot\sin(\theta_1+\theta_2)\tag{2.2}$$

## inverse Kinematic
first we need to find the angle between $r_1$ and $r_2$ ($\alpha$)
$$$$
as on the picture, imagine $r_1$ and $r_2$ was 2 edges of the triangle, and the other edges ($C$) are the hipotenuse.

Because of $\alpha$ was not ${90^\circ}$, we cant find $C$ using ordinary phytagoras. Instead, we are gonna using law of cosines which is :
$$C^2=A^2+B^2-2\cdot\cos(\alpha)$$
subtitite this equations with our formula

$$C^2=r_1^2+r_2^2-2\cdot\cos(\alpha)\tag{2.3}$$
We know that $C$ is a distance between the base and the tip of the arm, 

 using Phytagoras teorethm:
 $$C^2 = x^2+y^2$$
 we can subtitute $C^2$ in $(2.3)$ equation with those theoretm. 
$$x^2+y^2=r_1^2+r_2^2-2\cdot\cos(\alpha)\tag{2.3.1}$$

we want to calculate $\theta_2$, not $\alpha$. From the picture, we know that $\theta_2$ is a angle of $r_2$ and a line that parallel with $r_1$

when 2 edges are parallel, we know that the angle between them is ${180^\circ}$. As we seen before, $r_1$ is paralel with those line, and we also know the angle between $r_1$ and $r_2$ is $\alpha$, and it need $\theta_2$ more degree to make $r_1$ and $r_2$ parallel. so the equation is $$180=\alpha+\theta_2$$ 
put $-\theta_2$ to both sides of equations to find the value of $\alpha$
$$180-\theta_2=\alpha+(-\theta_2)+\theta_2$$ 

Same variabels cancel each other, so:
$$180-\theta_2=\alpha$$

Swab both sides of equations so it can be easier to read
$$\alpha=180-\theta_2$$

Put it in the last equations:
$$x^2+y^2=r_1^2+r_2^2-2\cdot\cos(180-\theta_2)\tag{2.3.2}$$
Because we want to find $\theta_2$, we can add $-\alpha$ to both side of equations to determine $\theta_2$ $${180^\circ}+(-\alpha)=\alpha+(-\alpha)+\theta_2$$


