# Tuning Centripetal Force Correction

## Purpose

The centripetal force correction corrects deviations from curved paths, ensuring the robot maintains an optimal trajectory.

---

## Setup

1. Open FTC Dashboard and go to the **Follower** tab.
2. Enable all checkboxes.
3. Run the `CurvedBackAndForth` OpMode.
4. Ensure the timer for autonomous OpModes is **disabled**.

---

## Tuning Process

1. Observe the robot’s path:
    - If the robot corrects towards the **inside** of the curve, increase `centripetalScaling`.
    - If the robot corrects towards the **outside** of the curve, decrease `centripetalScaling`.

2. Adjust the value of `centripetalScaling` (line 89 in `FollowerConstants`).

---

## Testing

Run additional tests with curved paths like `CurvedBackAndForth` or custom paths. Fine-tune the scaling value for smooth and accurate performance.
