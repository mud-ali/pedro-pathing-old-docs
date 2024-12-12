# Setup your Localizer

---
## Setup Pose Updater
Go to line `70` in the `PoseUpdater` class, and replace the `new ThreeWheelLocalizer(hardwareMap)`
with the localizer that applies to you:
* If you're using drive encoders, put `new DriveEncoderLocalizer(hardwareMap)`
* If you're using two wheel odometry, put `new TwoWheelLocalizer(hardwareMap)`
* If you're using two wheel odometry + pinpoint imu, put `new TwoWheelPinpointIMULocalizer(hardwareMap)`
* If you're using three wheel odometry, put `new ThreeWheelLocalizer(hardwareMap)`, so basically
  don't change it from the default
* If you're using three wheel odometry with the IMU, put `new ThreeWheelIMULocalizer(hardwareMap)`
* If you're using OTOS, put `new OTOSLocalizer(hardwareMap)`
* If you're using Pinpoint, put `new PinpointLocalizer(hardwareMap)`

---
## Robot Coordinate Grid
Use this diagram to find the offset of your localizer
[](robotCoord.png)

## Access
To start, you'll want to open the file (.java) of your localizer of choice (They are located in the [localization folder](https://github.com/AnyiLin/Pedro-Pathing-Quickstart/tree/master/TeamCode/src/main/java/org/firstinspires/ftc/teamcode/pedroPathing/localization/localizers) within the pedroPathing package) 

From there, continue the steps for your localizer in the linked pages:
- [Drive Encoder Localizer](driveEncoder.md)
- [Two Wheel Localizer](twoWheel.md)
- [TwoWheel + Pinpoint IMU Localizer](twoWheelPinpointImu.md)
- [Three Wheel Localizer](threeWheel.md)
- [Three Wheel + IMU Localizer](threeWheelImu.md)
- [OTOS Localizer](otos.md)
- [Pinpoint Localizer](pinpoint.md)
- [Roadrunner 0.5 to Pedro Localizer](rrToPedro.md)




---


