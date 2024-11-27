# Tuning the Heading PID

## Purpose

The heading PID ensures the robot maintains its rotational alignment, correcting deviations from its desired heading.

---

## Setup

1. Open FTC Dashboard and go to the **Follower** tab.
2. Enable `useHeading` and disable all other checkboxes.
3. Run the `StraightBackAndForth` OpMode.
4. Ensure the timer for autonomous OpModes is **disabled**.

---

## Tuning Process

1. Rotate the robot manually from one corner and observe its correction response.
    - The robot should correct its heading smoothly without moving laterally.
2. Adjust the PID constants (`headingPIDF`) in the **FollowerConstants** tab of FTC Dashboard.
    - **Goal**: Reduce oscillations while maintaining precise alignment.

---

## Testing

Repeat the tuning process with varying rotation angles and directions to ensure consistent performance.
