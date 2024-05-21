# 3DPole

10.04.2024 -> Added a full 3D Cad Model ( dimensions might differ in real life, components might differ in real life, no wiring and / or animations have been done in the 3D Cad)

11.04.2024 -> Added component manual, wiring diagrams and / or other legal information.

21.05.2024 Added the full Wiring Diagram ( I don't know how I missed that:3 );


A Polar - based 3D printer made from off-the-shelf parts.

Designed by Szilagyi Luca.

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

 #Printer Specs and Information

 As explained earlier, it's a polar based printer, with some features made using 3D printing.
 
 How could this work?
 
 In early times of 3D printing there was a community named RepRap that wanted to make 3D printing more accessible since at the time, it was meant for only the industry or the rich. They designed printers that could be cheap and good enough for anyone to make, that’s right, make. At that time you couldn’t buy a pre-made printer, you had to build it yourself. During this period is when lots of new discoveries were made that brought 3D Printing to what it is today.
 
The RepRap community were a bunch of enthusiasts that made printer projects with them in mind to be easy to recreate. Since they did not have access to industrial equipment, most parts in a 3d printer needed to be 3d printed themselves. They decided that a 1’s generation of printer should be made with 3d printer parts from industrial machines and the next generation of printers could have all the pieces they need from the 1’st generation machine, so, with only one machine you can make another which can make another and so on. The trend caught up and even reached our days.

The Voron Design Team known for their fast printers has its own “Print it forward” program where (for a sum of money) somebody that already has a Voron printer will print the parts you need (and the estetic parts if you want too) and later, you can print the same parts on your machine for someone else.

I decided to make this project in the same spirit with all the parts 3D printed for this printer being able to be made on the new printer.
Some decisions had to be made in terms of design, I never liked bulky printers (or enclosed ones for my sake - though they do have their many ups - even though I own one). The X axis is inspired by the Ender 3 axis for two big reasons, to make it clear it borrows something from Cartesian printers and because if it’s not broken, why fix it?

The design is time tested and I think it looks good in contrast with the entire printer.

As for the other parts, they are new designs made by me, besides the hotend that is inspired from the HERO ME fan duct.

The color green that you can see everywhere is not random at all. Well, I mean it is random as the filament was a random color, I printed some parts for testing and I thought it looked good with the black. I ended up using 2 kg of this filament since it is high quality and I needed lots of parts. The gray is ABS and it is used due to its high heat resistance.

Otherwise, I don’t have much to say about the design, there are cool design chives and other things, but you’ll have to find them on your own.
