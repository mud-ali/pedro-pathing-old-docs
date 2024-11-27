# Prerequisites for Pedro Pathing

## Robot and Drive Type

Pedro Pathing is designed to work with **omnidirectional drives**, such as **mecanum drive**. Currently, there is no support for swerve drives. You must have a robot with one of these supported drive systems to use Pedro Pathing.

---

## Localizer

You will need a tuned localizer to use Pedro Pathing effectively.

**Important**: Before tuning Pedro Pathing, ensure your localizer is properly tuned. Check out the localization tuning guide under the localization tab.

---

## FTC Dashboard

Using the [FTC Dashboard](http://192.168.43.1:8080/dash) will greatly aid in tuning your robot. Additionally, Team 16166 Watt'S Up created a **path visualizer**, which you can access [here](https://pedro-path-generator.vercel.app). 

For reference, the older Desmos visualizer is available [here](https://www.desmos.com/calculator/3so1zx0hcd).

---

## Units

Pedro Pathing uses **inches** and **radians** for measurements. If you prefer **centimeters**, you must input all measurements in centimeters. However, note that tuners will still label outputs as "inches" even if you're using centimeters.

---

## Initial Setup

1. **Mass of the Robot**: Input the robot’s mass (in kg) into the `mass` variable on **line 86** in the `FollowerConstants` class under the `tuning` package.

2. **Motor Reversal**: Ensure your motors are properly reversed in the `Follower` class constructor before running any OpModes.

Now you're ready to begin tuning Pedro Pathing!
