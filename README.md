# Calculating Trajectory Line
Exam Assignment - Research Topic: Trajectory Line by Vryens Sebastiaan

# Intro
First of all, what is line trajectory?
In the context of physics, particularly projectile motion, the trajectory of a projectile (like a thrown ball or a launched projectile) is often described as a curved path. However, if we focus on a specific plane, such as the horizontal plane, the trajectory can be represented as a line. This line represents the path the object would follow if there were no external forces acting on it, like air resistance.
Here is a simple example of how it works.

![Figure_03_04_05a](https://github.com/SebaTheProgrammer/Trajectory/assets/119673781/79dcda9c-a632-436a-91c1-dd4469235330)


# Calculation with maths
Calculating the trajectory of an object involves predicting its path through space over time. This is a common concept in physics and is often used in various fields, such as physics, engineering, astronomy, and ballistics. The trajectory of an object can be influenced by factors like initial velocity, launch angle, air resistance, and gravitational forces.

One of the main formulas that I used is: d = x+ u*t+1/2*g*t^2

Implemented:

<img width="517" alt="Screenshot 2024-01-06 164952" src="https://github.com/SebaTheProgrammer/Trajectory/assets/119673781/e0913bd7-c83b-4ea1-9dbf-fa059b791d2b">

# Calculation with Unity
While researching about how I would implement those calculations in Unity, I've read that Unity has already inbuild functions to do this. How nice! But was that too simple?

<img width="629" alt="Screenshot 2024-01-06 172217" src="https://github.com/SebaTheProgrammer/Trajectory/assets/119673781/45c0aefb-686a-456f-9217-901cf3855f2d">

Like here above, I started with an extra physics scene. That is needed for those calculations.
But for the actual trajectory calculations in Unity, I spawn an extra ghost ball every update! Damn! Wonderfull performance :D.
That is not the way to go. So I tried my own way.

<img width="482" alt="Screenshot 2024-01-06 172232" src="https://github.com/SebaTheProgrammer/Trajectory/assets/119673781/20477a72-4acf-472b-8cdd-da0685db8fc8">

# Implementing in Unity

As you can see, it's simpler do it in on paper then in Unity. Here I had hundreds of ball, with no trajectory lines.

<img width="913" alt="Screenshot 2024-01-06 171322" src="https://github.com/SebaTheProgrammer/Trajectory/assets/119673781/820fb9f4-1088-40ef-84b6-3d3207b398ac">

# Source

* https://en.wikipedia.org/wiki/Trajectory#:~:text=A%20trajectory%20or%20flight%20path,by%20position%20and%20momentum%2C%20simultaneously
* https://phys.libretexts.org/Bookshelves/University_Physics/Physics_(Boundless)/3%3A_Two-Dimensional_Kinematics/3.3%3A_Projectile_Motion
* https://www.youtube.com/watch?v=cuFd7QaG6Rs&ab_channel=SkyroraLimited
* https://www.youtube.com/watch?v=8mGZBYsSXcQ&ab_channel=LlamAcademy
