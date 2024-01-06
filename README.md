# Calculating Trajectory Line
Exam Assignment - Research Topic: Trajectory Line

# Intro
First of all, what is line trajectory?
In the context of physics, particularly projectile motion, the trajectory of a projectile (like a thrown ball or a launched projectile) is often described as a curved path. However, if we focus on a specific plane, such as the horizontal plane, the trajectory can be represented as a line. This line represents the path the object would follow if there were no external forces acting on it, like air resistance.

# Calculation with maths
Calculating the trajectory of an object involves predicting its path through space over time. This is a common concept in physics and is often used in various fields, such as physics, engineering, astronomy, and ballistics. The trajectory of an object can be influenced by factors like initial velocity, launch angle, air resistance, and gravitational forces.

One of the main formulas that I used is: d = x+ u*t+1/2*g*t^2
(Impleneted: point.y = pos.y + startVelocity.y * time + (Physics.gravity.y * time * time)/2;)
But this is just for a normal calculation, without any bounces.

# Calculation with/in Unity
While researching about how I would implement those calculations in Unity, I've read that Unity has already inbuild functions to do this. How nice! But that was too simple...

# Source
* https://en.wikipedia.org/wiki/Trajectory#:~:text=A%20trajectory%20or%20flight%20path,by%20position%20and%20momentum%2C%20simultaneously
* https://phys.libretexts.org/Bookshelves/University_Physics/Physics_(Boundless)/3%3A_Two-Dimensional_Kinematics/3.3%3A_Projectile_Motion
* https://www.youtube.com/watch?v=cuFd7QaG6Rs&ab_channel=SkyroraLimited
* https://www.youtube.com/watch?v=8mGZBYsSXcQ&ab_channel=LlamAcademy
