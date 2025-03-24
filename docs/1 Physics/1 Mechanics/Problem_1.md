# Problem 1

# Investigating the Range as a Function of the Angle of Projection
## Introduction
Projectile motion, while seemingly simple, offers a rich playground for exploring fundamental principles of physics. This report investigates how the range of a projectile depends on its angle of projection.

## Theoretical Foundation
In the foundation of projectile movement lie the Laws of Newton:

### First Law
An object at rest will stay at rest, and an object in motion will continue moving with constant velocity unless acted upon by a net external force. In terms of projectile motion, this means that once an object is in motion (like a ball thrown in the air), it will keep moving at a constant velocity in a straight line unless a force (like gravity or air resistance) acts on it.

### Second Law
This law states that the acceleration of an object is directly proportional to the net force acting on it and inversely proportional to its mass: 

$F=ma$ 

Where:

* F is the net force 
* m is the mass of the object
* a is the acceleration

In projectile motion, gravity provides a constant downward force that accelerates the object downward at a rate of approximately 
$9.8 \frac{m}{s^2}$ (on Earth).

### Third Law

This law states that for every action, there is an equal and opposite reaction. In projectile motion, this law isn't as directly involved in the motion of the object but can be observed in other interactions.

### Motion Components
A projectile moves under the influence of gravity, meaning its horizontal and vertical motions are independent except for the time variable. The acceleration due to gravity acts only in the vertical direction, making the motion two-dimensional.

**Horizontal Motion**: The object moves horizontally with a constant velocity (since there is no force acting horizontally, assuming no air resistance).

**Vertical Motion**: The object moves vertically with constant acceleration due to gravity, starting with an initial velocity in the upward direction (if thrown upward) or zero velocity (if dropped).

### Main formulas:

* $x(t) = v_0\cos(θ)t$ - horizontal displacement

This equation comes from the definition of constant velocity motion:

The horizontal component of velocity is \( v_0 \cos(\theta) \) (initial velocity times the cosine of the launch angle).

There is no acceleration in the x-direction (ignoring air resistance), so distance is simply velocity times time.


* $y(t) = v_0\sin(θ)t-\frac{1}{2}gt^2$ - vertical displacement

This equation follows from the kinematic equation for motion under constant acceleration:

$$
y = v_0 t + \frac{1}{2} a t^2
$$

Since gravity acts downward with acceleration \( g \), we replace \( a \) with \( -g \), leading to the negative term.


From the two formulas a single formula for the distance can be derived:

###### 1. Determine the Total Time of Flight

The vertical displacement equation for projectile motion is:  
   $$
   y(t) = v_0 \sin(\theta) t - \frac{1}{2} g t^2
   $$
Since the projectile returns to the ground, we set \( y = 0 \) and solve for \( t \):  
   $$
   0 = v_0 \sin(\theta) t - \frac{1}{2} g t^2
   $$  
Factor out \( t \):  
   $$
   t \left( v_0 \sin(\theta) - \frac{1}{2} g t \right) = 0
   $$  
This gives two solutions:  
   $$
   t = 0  \quad \text{(initial time)}
   $$  
   $$
   t = \frac{2 v_0 \sin(\theta)}{g}
   $$  
Thus, the **total time of flight** is:  
   $$
   T = \frac{2 v_0 \sin(\theta)}{g}
   $$

###### 2. Use the Horizontal Displacement Formula

The horizontal displacement is given by:  
   $$
   x = v_0 \cos(\theta) t
   $$  
Since range \( R \) is the total horizontal distance when the projectile lands, we substitute \( t = T \):

   $$
   R = v_0 \cos(\theta) \cdot \frac{2 v_0 \sin(\theta)}{g}
   $$

###### 3. Simplify Using Trigonometric Identity

Using the identity \( \sin(2\theta) = 2 \sin(\theta) \cos(\theta) \), we get:

   $$
   R = \frac{v_0^2 \sin(2\theta)}{g}
   $$

###### Conclusion

Thus, the **range formula** for projectile motion is:  
   $$
   R = \frac{v_0^2 \sin(2\theta)}{g}
   $$

## Analyzing the Range with regard to Angle

To analyze, at what angle does the object cross the largest distance, one can calculate the Range for different angles.

Let's take the angles $15°, 30°, 45°, 60°$ and $75°$

For this example, let's take the initial velocity for 10 m/s.

###### $15°$

$$
R = \frac{v_0^2 \sin(2*15°)}{g} = 5 m
$$


###### $30°$

$$
R = \frac{v_0^2 \sin(2*30°)}{g} = 8,66 m
$$


###### $45°$

$$
R = \frac{v_0^2 \sin(2*45°)}{g} = 10 m
$$

###### $60°$

$$
R = \frac{v_0^2 \sin(2*60°)}{g} = 8,66 m
$$


###### $75°$

$$
R = \frac{v_0^2 \sin(2*75°)}{g} = 5 m
$$


As a result, the object increases it's range of flight when the angle approaches 45°. The further the angle from this number, the less distance it travels.


However, angle is not a single parameter that determines the range - there is also velocity and gravitational acceleration:

1. Velocity is proportional to the range, as it stands in the numerator of the equation. The higher the velocity - the higher the distance that the object is able to travel.

2. Gravitational acceleration is antiproportional to the range, as it stands in the denomenator of the equation. The higher the gravitational acceleration - the faster the object is gonna fall, and hence, the less distance it will be able to travel.

## Practical applications

Projectile motion lies at the foundation of mechanics and has countless applications in real life. It can be seen in something as simple as children throwing snowballs in winter or as complex as launching a missile to another country. However, real-life applications are more complex than a simple formula. We must account for air resistance, uneven terrain, and other forces that could affect the flight.

For example, air resistance slows down the object by absorbing some of its energy. Additionally, an object may land higher or lower than its initial position depending on the terrain, which would influence its flight range.

## Implementation

The following code shows the trajectory of the object depending on the angle:

https://github.com/OlehVorobiov/solutions_repo/blob/main/docs/1%20Physics/1%20Mechanics/Implementation.ipynb

The representation clearly shows the same results as the analysis: the longest distance traveled by the object happens at 45°.


## Conclusion

In this report, we investigated projectile motion, explored its theoretical foundation, analyzed the function's range, discussed practical applications, and implemented its trajectory using Python code.