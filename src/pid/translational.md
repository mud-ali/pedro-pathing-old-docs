# Tuning the Translational PID

## Purpose

The translational PID ensures the robot follows a straight path without lateral deviation. It corrects the robot’s position along an imaginary forward line from its starting position.

---

## Setup

1. Open FTC Dashboard and go to the **Follower** tab.
2. Enable `useTranslational` and disable all other checkboxes.
3. Run the `StraightBackAndForth` OpMode.
4. Ensure the timer for autonomous OpModes is **disabled**.

---

## Tuning Process

1. Push the robot laterally (left or right) to test its correction response.
    - The robot should return to its path without rotating.
    - If the robot rotates, disable `useHeading`.
2. Adjust the PID constants (`translationalPIDF`) in the **FollowerConstants** tab of FTC Dashboard.
    - **Goal**: Minimize oscillations while maintaining accuracy.

---

## Feedforward Adjustments

If additional feedforward is needed, use `translationalPIDFFeedForward` for corrections in the robot’s movement direction. Avoid modifying the feedforward term directly in the PIDF.

---

## Testing

Test by pushing the robot with varying force and from different directions. Observe its ability to correct smoothly and accurately without oscillations.
