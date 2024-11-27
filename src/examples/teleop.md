# Setting Up Your OTOS Localizer

## Prerequisites
* OTOS connected to an I2C port on a hub.
* Ensure the protective film is removed from the sensor.

---

## Steps
### 1. Setup

Open the file `OTOSLocalizer.java` and configure the following:

1. **OTOS Port**: Replace the `deviceName` parameter with the name of the port connected to your OTOS.
2. **Sensor Position**: Enter the OTOS position relative to the robot's center. Use inches for measurements.

### 2. Localizer Tuning

#### a) Angular Scalar

1. Position your robot facing a recognizable landmark, such as a field tile edge.
2. Spin the robot counterclockwise for one full rotation (or a custom angle).
3. The tuner will display two numbers:

   * First number: Distance the robot thinks it has spun.
   * Second number (angular scalar): Replace the scalar value on line `78` in the localizer with this value.

4. (Optional) Run multiple tests and average the scalars for better accuracy.

#### b) Linear Scalar (Forward or Lateral Tuning)

Choose either forward or lateral tuning:

* **Forward Tuning**:
   1. Position a ruler alongside your robot.
   2. Push the robot forward by 30 inches (default distance).
   3. The tuner will display the linear scalar: Replace the scalar value on line `77` in the localizer with this value.

* **Lateral Tuning**:
   1. Position a ruler alongside your robot.
   2. Push the robot sideways by 30 inches (default distance).
   3. The tuner will display the linear scalar: Replace the scalar value on line `77` in the localizer with this value.

4. (Optional) Run multiple tests and average the scalars for better accuracy.

---

## Testing Your Localizer

1. Go to Localization Test and drive your robot around.
2. Open the FTC Dashboard at [http://192.168.43.1:8080/dash](http://192.168.43.1:8080/dash).
3. Switch the view to "field view" from the top-right corner dropdown.
4. Observe if the robot's movements appear accurate on the dashboard. Re-run tuning if necessary.

---

## Congratulations on successfully tuning your localizer!
