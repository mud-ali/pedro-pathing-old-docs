# Setting Up Your Drive Encoder Localizer

## Prerequisites
* Encoders attached to all drive motors.

---
## Steps 
### 1. Encoder Setup

Open the file `DriveEncoderLocalizer.java`. The motor names are already defined, so you don't need to modify them here.

### 2. Encoder Direction Calibration

Ensure all encoders tick up when the robot moves forward. Reverse the direction of any encoders that don't follow this convention.

### 3. Localizer Tuning

We need to adjust multipliers that convert encoder ticks into real-world measurements (inches or radians). This ensures your localizer's readings are accurate.

#### a) Turn Localizer Tuner

1. Position your robot facing a recognizable landmark, like a field tile edge.

2. Spin the robot counterclockwise for one full rotation (or your desired angle).

3. The tuner will display two numbers:

   * First number: Distance the robot thinks it has spun.

   * Second number (multiplier): This is the value you need to replace `TURN_TICKS_TO_RADIANS` in the localizer. Replace the entire value, don't add or multiply it.

4. (Optional) Run multiple tests and average the multipliers for better accuracy.

#### b) Forward Localizer Tuner

1. Position a ruler alongside your robot.

2. Push the robot forward by the desired distance (default is 30 inches).

3. The tuner will display two numbers:

   * First number: Distance the robot thinks it has traveled.

   * Second number (multiplier): This is the value you need to replace `FORWARD_TICKS_TO_INCHES` in the localizer. Replace the entire value, don't add or multiply it.

4. (Optional) Run multiple tests and average the multipliers for better accuracy.

#### c) Lateral Localizer Tuner

1. Position a ruler alongside your robot.

2. Push the robot sideways (strafing) by the desired distance (default is 30 inches).

3. The tuner will display two numbers:

   * First number: Distance the robot thinks it has traveled laterally.

   * Second number (multiplier): This is the value you need to replace `STRAFE_TICKS_TO_INCHES` in the localizer. Replace the entire value, don't add or multiply it.

4. (Optional) Run multiple tests and average the multipliers for better accuracy.

---

## Testing Your Localizer

After completing the tuning steps, you can test your localizer's accuracy.



1. Go to `Localization Test` and drive your robot around.

2. Open the FTC Dashboard at http://192.168.43.1:8080/dash.

3. Switch the view to "field view" from the top right corner dropdown.

4. The dashboard should display the robot's position on the field. Observe if the movements seem accurate.

5. If the movements appear inaccurate, re-run some of the tuning steps.



--- 

## Congratulations on successfully tuning your localizer!