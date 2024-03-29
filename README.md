# Calculating Trajectory Line
Exam Assignment - Research Topic: Trajectory Line by Vryens Sebastiaan 2GD18N

# Intro
First of all, what is line trajectory?
In the context of physics, particularly projectile motion, the trajectory of a projectile (like a thrown ball or a launched projectile) is often described as a curved path. However, if we focus on a specific plane, such as the horizontal plane, the trajectory can be represented as a line. This line represents the path the object would follow if there were no external forces acting on it, like air resistance.
Here is a simple example of how it works.

![Ideal_projectile_motion_for_different_angles svg](https://github.com/SebaTheProgrammer/Trajectory/assets/119673781/52aa4b02-f13d-4bc3-a652-1ff296c70d42)

# Calculation with Unity
While researching about how I would implement those calculations in Unity, I've read that Unity has already inbuild functions to do this. How nice, right?

<img width="629" alt="Screenshot 2024-01-06 172217" src="https://github.com/SebaTheProgrammer/Trajectory/assets/119673781/45c0aefb-686a-456f-9217-901cf3855f2d">

Like here above, I started with an extra physics scene. That is needed for those calculations.
But for the actual trajectory calculations in Unity, I spawn extra 'ghost' balls every update where their trajectory gets used! Damn, there goes the performance...

<img width="482" alt="Screenshot 2024-01-06 172232" src="https://github.com/SebaTheProgrammer/Trajectory/assets/119673781/20477a72-4acf-472b-8cdd-da0685db8fc8">

# Implementing in Unity

As you can see, it's simpler do it in on paper then in Unity. Here I had hundreds of ball, with no trajectory lines...

<img width="913" alt="Screenshot 2024-01-06 171322" src="https://github.com/SebaTheProgrammer/Trajectory/assets/119673781/820fb9f4-1088-40ef-84b6-3d3207b398ac">

So due to the low performance and Unity that is strange, this is not the way to go. So I tried my own.

# Calculation with maths
Calculating the trajectory of an object involves predicting its path through space over time. This is a common concept in physics and is often used in various fields, such as physics, engineering, astronomy, and ballistics. The trajectory of an object can be influenced by factors like initial velocity, launch angle, air resistance, and gravitational forces.

One of the main formulas that I used is: d = x+ u*t+1/2*g*t^2

Implemented:

<img width="517" alt="Screenshot 2024-01-06 164952" src="https://github.com/SebaTheProgrammer/Trajectory/assets/119673781/e0913bd7-c83b-4ea1-9dbf-fa059b791d2b">

But this was only for one line, or one bounce.

<img width="177" alt="Screenshot 2024-01-06 175154" src="https://github.com/SebaTheProgrammer/Trajectory/assets/119673781/0088c537-6061-4193-a40b-407e742d180f">

This was also not the answer. I was so close. 
I look into the Unity engine if those lines had a collision/overlapping event. Sadly, this wasn't the case. Then how could I ever know/check when the ball collides with an object?
Well, I have no idea. On paper it's easy, but in Unity it is different. I can fix it by using Unity's way so that is also my result.

# End Result

![Untitled video - Made with Clipchamp (2)](https://github.com/SebaTheProgrammer/Trajectory/assets/119673781/b8010051-f108-445a-8172-1060f91919b3)


# Self Reflection
This is also important. I learned a lot, new stuff about Unity, how trajectory actually works, code optimasation, and more.
But one of the main things that I would've done different, is thinking about which engine is better for what I need. 
In Game Mechanics I loved working with Unity because there was so much 'new' stuff for me to find out. (I always worked in UE4-5 before.) So I was happy we could choose it ourself.

After this assignment I would 2 main things different:
* choosing the right engine
* choosing something more complex, eventho I know already how it works.

Still I'm happy about this learning curve.


# Source

* https://en.wikipedia.org/wiki/Trajectory#:~:text=A%20trajectory%20or%20flight%20path,by%20position%20and%20momentum%2C%20simultaneously
* https://phys.libretexts.org/Bookshelves/University_Physics/Physics_(Boundless)/3%3A_Two-Dimensional_Kinematics/3.3%3A_Projectile_Motion
* https://www.youtube.com/watch?v=cuFd7QaG6Rs&ab_channel=SkyroraLimited
* https://www.youtube.com/watch?v=8mGZBYsSXcQ&ab_channel=LlamAcademy
