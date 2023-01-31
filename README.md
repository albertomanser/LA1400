# LA1400
ROBOCODE
Code:
```java
package AM;
import robocode.*;
import java.lang.Math;
// API help : https://robocode.sourceforge.io/docs/robocode/robocode/JuniorRobot.html

/**
 * ManserAlberto_REEEEE - a robot by Alberto Manser
 */
public class ManserAlberto_REEEEE extends JuniorRobot{

	public void run() {
		
		setColors(orange, blue, white, yellow, black);
		ahead(100);
		back(100);
		turnGunRight(360);
	}
	
	public void survival(){
		int energy_ = energy;
		if(energy_ < 21){
			turnAheadLeft(90, 90);
			turnAheadRight(90, 90);
			
		}
	}
	
	public void onScannedRobot() {
		//defining the Variables 
		int scannedDistance_ = scannedDistance;
		turnGunTo(scannedAngle);
		if(scannedDistance_ < 200){
			fire(3);
		}
		else{
			fire(2);
		}
		ahead(100);
		back(100);
	}

	public void onHitByBullet() {
	//When Robot gets hit by a Bullet it tries to dodge the following few Bullets
	turnAheadLeft(100, 90 - hitByBulletBearing);
	}
	
	
	public void onHitWall() {
		turnRight(90);
		ahead(60);
	}	
}
```
