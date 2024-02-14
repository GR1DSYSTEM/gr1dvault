---
{"dg-publish":true,"permalink":"/lab/itct-111/"}
---

# Midterm
- Match datatype and data
- Expression → Relational + logical → `if (temp>35) return boolean` → Flowchart
- Class-object
		- properties (variables)
		- behaviour (action) → method (function in the class)
- Code → Explain the result
	- Shape + Transformation
- Flowchart + Loop

# Processing

[Reference / Processing.org](https://processing.org/reference/)

![Pasted image 20240214224423.png](/img/user/Utilities/Attachments/Pasted%20image%2020240214224423.png)
![Pasted image 20240214233419.png](/img/user/Utilities/Attachments/Pasted%20image%2020240214233419.png)

Functions: specific and small tasks
Classes: organize related functions and variables into a single unit

## Functions
```processing
void draw() {
	background(220);
	drawCircle(50, 50, 50, color(255, 0, 0));
	drawCircle(150, 100, 75, color(0, 255, 0));
	drawCircle(250, 150, 100, color(0, 0, 255));
	drawCircle(100, 250, 125, color(255, 255, 0));
	drawCircle(200, 300, 150, color(0, 255, 255));
}
void drawCircle(float x, float y, float radius, color c) {
	fill(c);
	ellipse(x, y, radius, radius);
}
```
## Class-Object

```processing
// Define a class
class Ball {

	// Properties
	float x;
	float y;
	float size;

	// Constructor
	Ball(float xpos, float ypos, float s) {
	x = xpos;
	y = ypos;
	size = s;
	}

	// Method 
	void display() {
	ellipse(x, y, size, size);
	}
}
```

```processing
// Create an object
Ball b = new Ball(100, 100, 50);
```

```processing
// Use the object
b.x = 200; // Changes the x position of the ball
b.display(); // Displays the ball on the canvas
```
