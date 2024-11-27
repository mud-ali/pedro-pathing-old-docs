# Forward Zero Power Acceleration Tuner

## Purpose

The **Forward Zero Power Acceleration Tuner** measures how your robot decelerates when moving forward and power is cut from the drivetrain. This value is critical for improving motion accuracy in Pedro Pathing.

---

## Setup and Instructions

1. Open the `ForwardZeroPowerAccelerationTuner.java` OpMode.
2. Ensure your robot has enough space to accelerate to **30 inches/second** forward. You can adjust this velocity in the FTC Dashboard under the `ForwardZeroPowerAccelerationTuner` dropdown.
3. Run the OpMode.

---

## Output

* **Deceleration**: After the robot reaches the target velocity and power is cut, telemetry will display the robot’s deceleration rate.
* Ensure the robot drifts to a complete stop for accurate measurements.

---

## Inputting the Results

1. Open the `FollowerConstants` class.
2. Replace the value of the `forwardZeroPowerAcceleration` variable on **line 94** with the deceleration rate output from the tuner.

Congratulations, you’ve completed the forward zero power acceleration tuning!
