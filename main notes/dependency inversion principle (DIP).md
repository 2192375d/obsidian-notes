---
title: dependency inversion principle (DIP)
created: Monday 10th November 2025 20:32
last_modified: Monday 10th November 2025 20:32
aliases: []
tags:
  - computer-science/software-development/SOLID
course:
  - CSCB07
LEC:
  - "8"
---
# dependency inversion principle (DIP)
- High-level modules should not depend on low-level modules, both should depend on abstractions.
- Abtractions should not depend on details. Details should depend on abstractions.

Consider this code:
```java
class Lamp {
	public void turnOn() {
		System.out.println("Lamp turned on");
	}
	
	//...
}

class ConstrolSystem {
	InfraredSensor sensor;
	Lamp lamp;
	
	public ControlSystem(InfraredSensor sensor, Lamp lamp) {
		while (true) {
			double  sensorReading = sensor.read();
			
			if (sensorReading > 0.5) {
				lamp.turnOn();
			} else {
				lamp.turnOff();
			}
			try {
				Thread.sleep(1000);
			} catch (InterruptedException e) {
				e.printStackTrace();
			}
		}
	}
}
```

This violates DIP
To conform to DIP, we should have something like:
![[Pasted image 20251110204138.png]]