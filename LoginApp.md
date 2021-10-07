Working with Layout Constraints:


Constraint Layout,  is a layout that allows to place UI components + fix the position of UI Component based on constraints. 

There are four constraints that can be added. 
-	Minimum 2 constraints can be added to UI Element ( X , Y position)
-	Maximum 3 constraints can be added.
-	Rare Cases, we can go for 4 constraints.


Demo: 
Create an application named “Login App.
Update the User interface as per fig.
![image](https://user-images.githubusercontent.com/46557268/136403796-cadd3443-f5c6-470c-8f4d-663c69aac59f.png)


app>layout>activity_main.xml
1.	Drag below of UI Components.
a.	Text View: Display Value as text
b.	PlainText: To take input as text
c.	Password: To take input as text, to display with dotted values.
d.	Button : Handling Login Event
e.	Button : Handle Register event.

2.	Constraint Addition:
a.	Login Panel
i.	Top	: 16
ii.	Left	: 16
iii.	Right	: 16

b.	Plain Text, Password
i.	Top: 	40
ii.	Left:	16
iii.	Right: 16
iv.	layout_width= 0dp match_constraint
v.	layout_height=50dp

c.	Button Login
i.	Top: 20
ii.	Right : 16

d.	Button Register
i.	Top : 20
ii.	Left: 16

