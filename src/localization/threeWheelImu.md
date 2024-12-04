# Setting Up Your Three Wheel Localizer with IMU

## Prerequisites
* Three odometry wheels connected to motor encoder ports on a hub.
* A properly configured IMU.

---

## Steps
### 1. Setup

Open the file `ThreeWheelIMULocalizer.java` and configure the following:

1. **Tracking Wheel Positions**: Enter the positions of your tracking wheels relative to the robot's center. Use inches for measurements.
2. **Encoder Ports**: Replace the `deviceName` parameters with the names of the ports connected to your encoders.
3. **IMU Orientation**: Adjust the IMU's orientation to match your robot.

### 2. Encoder Direction Calibration

Ensure the following:

* Forward encoder ticks up when the robot moves forward.
* Strafe encoder ticks up when the robot moves to the left.

### 3. Localizer Tuning

#### a) Turn Localizer Tuner (without IMU)

1. Open FTC Dashboard and deselect the `useIMU` option in the `ThreeWheelIMULocalizer` dropdown.
2. Position your robot facing a recognizable landmark, such as a field tile edge.
3. Spin the robot counterclockwise for one full rotation (or a custom angle).
4. The tuner will display two numbers:

   * First number: Distance the robot thinks it has spun.
   * Second number (multiplier): Replace `TURN_TICKS_TO_RADIANS` in the localizer with this value.

5. (Optional) Run multiple tests and average the multipliers for better accuracy.

#### b) Forward and Lateral Tuning (with IMU)

1. Re-enable `useIMU` in the FTC Dashboard.

2. Forward Tuning:
   * Position a ruler alongside your robot.
   * Push the robot forward by 30 inches (default distance).
   * The tuner will display the forward multiplier: Replace `FORWARD_TICKS_TO_INCHES` in the localizer with this value.

3. Lateral Tuning:
   * Position a ruler alongside your robot.
   * Push the robot sideways (strafing) by 30 inches (default distance).
   * The tuner will display the lateral multiplier: Replace `STRAFE_TICKS_TO_INCHES` in the localizer with this value.

4. (Optional) Run multiple tests and average the multipliers for better accuracy.

---

## Testing Your Localizer

After completing the tuning steps, test the localizer as follows:

1. Go to Localization Test and drive your robot around.
2. Open the FTC Dashboard at [http://192.168.43.1:8080/dash](http://192.168.43.1:8080/dash).
3. Switch the view to "field view" from the top-right corner dropdown.
4. Observe if the robot's movements appear accurate on the dashboard. Re-run tuning if necessary.

---

## Congratulations on successfully tuning your localizer!
