Android Application Development
-	Create Hello Android 
-	Files & Folder
-	Android Version
-	Lifecycle Methods

Creating Hello World

1.	Open Android Studio
2.	File Menu / Create a new project and provide below of details.
a.	Choose Category: 	Phone and Tablet
i.	Template:	Empty Activity

b.	Project Name: 		Name of Project
c.	Package Name		Package for project (Important part for deployment)
d.	Location			
e.	Language			Kotlin
f.	Min SDK version		4.1
g.	Finish to create project


3.	Execution of Android app
a.	Using Android AVD
b.	Tools Menu > AVD ( Android Virtual Device Manager) -> it will show the list of Virtual devices whichever is available.
i.	If no devices available create a new one.
1.	Select the screen size
2.	Provide Operating system Q
3.	Provide name
4.	Create
ii.	Once Created, From Android Device Manager, we can start the same.


Important Points:
A
B
C		: Cupcake
D		: Donut
E		: Eclairs
F		: Froyo
G		Gingerbread
H		HoneyComb						
I		Ice Cream Sandwich			Android 4.0
J		JellyBean				Android 4.2	: Android Wear
K		Kitkat					Android 4.4
L		Lollypop				Android 5	:  Material Design
M		Marshmallow				Android 6	:  Run time permissions
N		Nougat				Android 7
O		Oreo					Android 8
P		Pie					Android 9
Q							Android 10
R							Android 11


Files & Folder of Android 
1.	manifest
a.	AndroidManifest.xml : It’s a configuration file that will maintain permission, number of activities, launcher activity & others.
2.	Java
It’s also known as the Compiled Zone. Files kept inside will be compiled.
a.	Package Name(default)
i.	MainActivity.kt:  It will be containing information of event handler of UI Components
b.	Package Name UITest: UI Testing (espresso)
c.	Package Name Test	: Unit Testing ( JUnit)

3.	Res
a.	Drawable: Used to place images.
b.	Layout :  User Interface
c.	Mipmap : Used to place images with different resolutions, mostly for application icons.	
d.	Values: Useful for localization



Day 03
Android Components
1.	Activity	: Used to build User Interfaces for end users.
2.	Broadcast Receiver: App to App communication
3.	Services	: Long running background process

Note: For above three, Intent is a class that allows you to perform operations.

4.	Content Provider: Share data 


