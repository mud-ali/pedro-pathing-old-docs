# Setup your Localizer

---
## Setup Pose Updater
Go to line `70` in the `PoseUpdater` class, and replace the `new ThreeWheelLocalizer(hardwareMap)`
with the localizer that applies to you:
* If you're using drive encoders, put `new DriveEncoderLocalizer(hardwareMap)`
* If you're using two wheel odometry, put `new TwoWheelLocalizer(hardwareMap)`
* If you're using three wheel odometry, put `new ThreeWheelLocalizer(hardwareMap)`, so basically
  don't change it from the default
* If you're using three wheel odometry with the IMU, put `new ThreeWheelIMULocalizer(hardwareMap)`
* If you're using OTOS, put `new OTOSLocalizer(hardwareMap)`
* If you're using Pinpoint, put `new PinpointLocalizer(hardwareMap)`

---
## Access
To start, you'll want to open the file (.java) of your localizer of choice (They are located in the [localization folder](https://github.com/AnyiLin/Pedro-Pathing-Quickstart/tree/master/TeamCode/src/main/java/org/firstinspires/ftc/teamcode/pedroPathing/localization/localizers) within the pedroPathing package) 

From there, continue the steps for your localizer in the linked pages:
- [Drive Encoder Localizer](./setup/driveEncoder.md)
- [Two Wheel Localizer](./setup/twoWheel.md)
- [Three Wheel Localizer](./setup/threeWheel.md)
- [Three Wheel + IMU Localizer](./setup/threeWheelImu.md)
- [OTOS Localizer](./setup/otos.md)
- [Pinpoint Localizer](./setup/pinpoint.md)
- [Roadrunner 0.5 to Pedro Localizer](./setup/rrToPedro.md)




---


