Course Materials:

1.	Where is everything : goo.gle/3iTdWbP
2.	Pathways/CodeLabs: goo.gle/3xwL2Xq


Step 1: 
1.	Create a Google developer profile : goo.gle/30orQvC
2.	Make your profile public.
a.	Click on gear icon settings.
b.	Select profile visibility: Update it to Public.

Prerequisite: 
System : Windows, MAC, Linux
RAM: Min 8 GB
Storage: SSD preferred
Processor: i5

Tools:
1.	IntelliJ : Working with Kotlin : https://www.jetbrains.com/idea/download/download-thanks.html?platform=windows&code=IIC

2.	Android Studio: Work with Android : https://developer.android.com/studio


Demo: Create Hello World with Kotlin

1.	Open IntelliJ
2.	Create a new project
a.	Project Name: Hello Kotlin
b.	Category: Kotlin
c.	Template: JVM template
d.	Select the JDK version.
e.	Finish to create the same.
3.	It will take time to build the project ( first time)

4.	Tools Menu > Kotlin > REPL 
a.	Provide below details.
print(“Hello world”)

b.	To run the same, click play icon / CTRL + ENTER.



Variable & Constant

The keyword “var” is used to create variables.
Variables,data are allowed to manipulate.
It is also known as mutable (changeable).


The keyword “val” is used to create a constant.
Constant values are not allowed to be manipulated.
It is also known as Immutable (unchanged)


Working with Functions
1.	Select Project >src>main>kotlin : Right Click > New > kotlin file/class
a.	Name: Hello.kt
b.	Type: File
2.	Add below statement for main function.
fun main(args: Array<String>) {
   print("Hello This is Main function Kotlin")

   }


Day 02: Class & Objects
1.	class  keyword is used to create a class.
2.	To create instances we don’t use new  keywords.


Working with Constructor:
1.	Class with Parameters			: Used
2.	Init						: Used
3.	constructor keyword


Inheritance:
Make sure Base class/ Parent Class/ Super Class must be as Open. Else default type is as final.

