## In this short tutorial you will learn to setup a new Eclipse project that imports Processing 4 as a Java package.

---

- Download and install Processing 4 (alpha 3 at https://processing.org/download/)

- Download and install current Ecplise IDE (2021-03 at https://www.eclipse.org/downloads/)

- Create a new JavaSE-11 project
  
![JavaSE-11](/imgs/eclipse/ecplipse1.png "JavaSE-11")

- Configure build paths
  
![build paths](/imgs/eclipse/ecplipse2.png "build paths")

- select 'Add External JARs...'

![jars](/imgs/eclipse/ecplipse3.png "jars")

- browse to processing/core/library and select all .jar files

![processing/core/library](/imgs/eclipse/ecplipse4.png "processing/core/library")

- add a class with the following code as an example
```java
import processing.core.*; //import processing

public class HelloWorld extends PApplet {

	float r; // rotation
	// The argument passed to main must match the class name

	public static void main(String[] args) {
		PApplet.main("HelloWorld");
	}

	public void settings() { // startup settings
		size(1920, 1080, P3D);
	}

	public void setup() { // setup called after settings
		stroke(255, 0, 0, 255); // set stroke color and weight
		strokeWeight(5.0f);
	}

	public void draw() { // draw loop is calling every frame
		background(0); // clear background
		translate(width / 3, height / 3, 0); // translate and rotate the coord system
		rotateY(r);
		noFill();
		box(width / 10, width / 13, width / 7); // draw a box
	}

	public void mouseClicked() // mouse event hook
	{
		if (mouseButton == LEFT) { // mouse button variable and enum
			r = r + 0.1f;
		} else if (mouseButton == RIGHT) { // mouse button variable and enum
			r = r - 0.1f;
		}
	}
}
```
- Done. You are now ready to use processing within ecplise as you see fit. Happy coding.

$$x = {-b \pm \sqrt{b^2-4ac} \over 2a}$$