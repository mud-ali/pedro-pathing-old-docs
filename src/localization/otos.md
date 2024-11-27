# Setting Up Your OTOS Localizer

## Prerequisites
* Ensure the **OTOS sensor** is connected to an **I2C port** on your control hub.
* Verify the protective film on the sensor is **removed** before use.

---

## Steps

### 1. Setup

1. Open the file `OTOSLocalizer.java`.
2. In the **constructor**:
    - Locate the section where the `deviceName` parameter is defined and replace it with the **port name** connected to your OTOS sensor.  
      Example: If your port is labeled `I2C1`, replace the `deviceName` with `"I2C1"`.
3. Define the **sensor's position** relative to the **center of the robot**:
    - Measure the X, Y coordinates (in inches) and update them in the constructor.
    - Use the comment above the class declaration as guidance for coordinate updates.

---

### 2. Localizer Tuning

#### a) Angular Scalar (Turn Tuning)

1. Place your robot, so it faces a fixed, recognizable reference point (e.g., aligning an edge with a field tile).
2. Run the **Turn Localizer Tuner**:
    - By default, rotate the robot counterclockwise **one full rotation**.
    - Alternatively, you can set a **custom angle** in the tuner.
3. After the rotation:
    - **First number**: The distance the robot estimates it has rotated.
    - **Second number**: The **angular scalar** you need to input.
4. Replace the angular scalar value in `OTOSLocalizer.java` (line **78**) with the new scalar:
    - Ensure you **replace** the value, not add to or multiply the existing one.
5. (Optional): Run multiple tests to average the scalars for improved accuracy.

---

#### b) Linear Scalar (Forward or Lateral Tuning)

Since OTOS has only one linear scalar, you can run **either Forward or Lateral Localizer Tuner**. The result should be very similar, but not the same as there will be very small, negligible differences.

##### **Option 1: Forward Tuning**
1. Align a ruler alongside your robot.
2. Push the robot forward by the default distance (**30 inches**) or a custom set value.
3. Observe the tuner outputs:
    - **First number**: The distance the robot estimates it has moved.
    - **Second number**: The **linear scalar** to update.

##### **Option 2: Lateral Tuning**
1. Align a ruler alongside your robot.
2. Push the robot **30 inches laterally to the right** (default distance) or a custom set value.
3. Observe the tuner outputs:
    - **First number**: The distance the robot estimates it has moved.
    - **Second number**: The **linear scalar** to update.

4. Replace the linear scalar value in `OTOSLocalizer.java` (line **77**) with the new scalar:
    - Ensure you **replace** the value, not add to or multiply the existing one.
5. (Optional): Run multiple tests and average the scalars for better accuracy.

---

### 3. Testing Your Localizer

1. Go to the **Localization Test** and move your robot (either manually or using the drivetrain).
2. Access the **FTC Dashboard** at [http://192.168.43.1:8080/dash](http://192.168.43.1:8080/dash).
3. Change the view to **Field View** (dropdown menu in the top-right corner).
4. Observe the robot's movements:
    - If movements are accurate, you are done.
    - If movements are not aligned with reality, revisit the tuning steps.

---

## Congratulations!

You have successfully tuned your OTOS Localizer. If you encounter any issues, revisit the steps above or reach out for support.