# Lateral Zero Power Acceleration Tuner

## Purpose

The **Lateral Zero Power Acceleration Tuner** measures how your robot decelerates when strafing (moving sideways) and power is cut from the drivetrain. This value is critical for improving motion accuracy in Pedro Pathing.

---

## Setup and Instructions

1. Open the `LateralZeroPowerAccelerationTuner.java` OpMode.
2. Ensure your robot has enough space to accelerate to **30 inches/second** laterally. You can adjust this velocity in the FTC Dashboard under the `LateralZeroPowerAccelerationTuner` dropdown.
3. Run the OpMode.

---

## Output

* **Deceleration**: After the robot reaches the target velocity and power is cut, telemetry will display the robot’s deceleration rate.
* Ensure the robot drifts to a complete stop for accurate measurements.

---

## Inputting the Results

1. Open the `FollowerConstants` class.
2. Replace the value of the `lateralZeroPowerAcceleration` variable on **line 98** with the deceleration rate output from the tuner.

Congratulations, you’ve completed the lateral zero power acceleration tuning!
