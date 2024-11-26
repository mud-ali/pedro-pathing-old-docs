# Setting Up Your Pinpoint Localizer

## Prerequisites
* Pinpoint module connected to an I2C port.
* Dead wheel encoder wires properly connected to the Pinpoint module.

---

## Steps
### 1. Setup

Open the file `PinpointLocalizer.java` and configure the following:

1. **Pinpoint Port**: Replace the `deviceName` parameter with the name of the I2C port connected to the Pinpoint module.
2. **Odometry Measurements**: Follow the instructions in the `TODO` comment to enter the odometry measurements in millimeters or inches. Conversion rates are provided in the comments.

### 2. Verifying Pinpoint Connection

Run the `SensorGoBildaPinpointExample.java` file located in the `tuning` folder. This will ensure the Pinpoint is correctly connected and operational.

---

## Testing Your Localizer

After completing the setup:

1. Go to Localization Test and drive your robot around.
2. Open the FTC Dashboard at [http://192.168.43.1:8080/dash](http://192.168.43.1:8080/dash).
3. Switch the view to "field view" from the top-right corner dropdown.
4. Observe if the robot's movements appear accurate on the dashboard. Re-run the setup if necessary.

---

## Congratulations on successfully setting up your localizer!
