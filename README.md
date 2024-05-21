# 3DPole

10.04.2024 -> Added a full 3D Cad Model ( dimensions might differ in real life, components might differ in real life, no wiring and / or animations have been done in the 3D Cad)

11.04.2024 -> Added component manual, wiring diagrams and / or other legal information.

21.05.2024 Added the full Wiring Diagram ( I don't know how I missed that:3 );


A Polar - based 3D printer made from off-the-shelf parts.

Designed by Szilagyi Luca with the coordination of Maidan Alin.

All the files for the 3D Printable files are provided in the 3DCAD folder with a full build file coming soon.
This project required custom-made 3DPrinted Parts as well as custom crimped cables and configurable firmware based on Marlin.

!! The printer does have Thermal Runaway Protection but it's still a prototype so be aware of the risks!

!! The system uses a 24V 12.4A Power supply. While the metal of the cable of the wires is not exposed, it's still dangerous!


# Polar Printers

Most people have heard of Carthesian 3D printers and others also know about CoreXY printers.
The truth is, all of the 3d printing industry has changed a lot the past 20 years or so. We have seemingly endless types of 3D printers.

There are the normal Cartesian printers that spiked up with the chinese production of 3D printers after the patent expired, there is also CoreXY printers that became more popular mid 2020 and Delta printers that have seen a spike in 2011 and another one in 2024 with the launch of speedy printers from Flsun.

Each type of printer has its own flaws and sellpoints, the Cartesian type of printer is cheap and easy to maintain, it’s also easy to build if you’d like that, but it’s not fast and many quality of life problems occur with time. CoreXY are (most often) big, fast and overall wood, their drawback is the price and the complex movement system. Delta printers are tall and thin, scary looking at first sight but in fact they are faster than Cartesian printers (and newer models are even faster then CoreXY ones), easy to maintain, but the printspace is limited and they tend to be quite lod and easy to fit in a normal space.

Besides these 3 major types of printers (when speaking of FDM type machines) there comes 5 Axis machines, CoreXZ, Industrial grade machines, and my personal favorite, Polar Printers.

Polar Printers borrow something from all of the 3 big types of FDM printers. They are cheap and easy to assemble like Chartesian printers, fast* and reliable as their CoreXY brothers, easy to scale up and scary looking (when it comes to the math) just like the Delta printers.

*While they can be fast, this prototype is not any of that, we chose slow and sturdy as it gives the best results, with lots of tuning you can turn this into a fast machine though.

Traditional Cartesian printers use (as the name implies) a standard 3 axis cartesian system, you have the X value that tells you how left or right is a point, and Y value that determines the back and forth motion and the Z variable that dictates the height. CoreXY is somewhat the same but X and Y are a 2 in 1 system made using an ingenious routing of bets that move the printhead precisely with the Z axis moving the entire bed up and down. Delta printers have a fixed bed and only don’t seem to have 3 different axis, they have 3 parallel axis connected to the printhead with 3 arms, by moving those 3 axis in various ways you can reach any point in the printspace, though the printspace is not a cylinder but more of a cone at its peak due to this system of motion.

Polar Printers look like Cartesian printers (solely on looks) with 3 separate axes, but a keen eye will see that the X axis is shorter than usual. Due to a polar movement system, the X axis only needs to be half the size of the bed, thus reducing material costs, weight on the print axis and making a full travel faster.

![image](https://github.com/lucagavril0307/3DPole/assets/163439407/a331d722-1aea-4a5b-ba6b-b6945ba8e72c)

To get the position of a point in the XY plane you will need and angle and a distance (r and Θ) the distance takes values from 0 (the middle point of the circle) and the radius of the circle (half the bed size, so it will be the X axis) while Θ is an angle ( so from 0 to 360 <or 2π in radians>, aka the rotation of the bed, so the Y axis). The Z axis only dictates how high is said point.

