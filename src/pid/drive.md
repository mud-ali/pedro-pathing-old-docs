# Tuning the Drive PID

## Purpose

The drive PID manages acceleration and braking along a path, ensuring smooth motion and minimizing overshoot.

---

## Setup

1. Open FTC Dashboard and go to the **Follower** tab.
2. Enable `useDrive`, `useHeading`, and `useTranslational`.
3. Run the `StraightBackAndForth` OpMode.
4. Ensure the timer for autonomous OpModes is **disabled**.

---

## Tuning Process

1. Adjust the PID constants (`drivePIDF`) in the **FollowerConstants** tab of FTC Dashboard.
    - **Proportional (P)**: Start with very low values (e.g., hundredths or thousandths).
    - **Derivative (D)**: Use small values (e.g., hundred-thousandths or millionths).
    - **Integral (I)**: Avoid using this term; it can cause accumulated errors and oscillations.

2. Test the response during braking:
    - Reduce oscillations for smoother stops.

---

## Zero Power Acceleration Multiplier

Before tuning, set the `zeroPowerAccelerationMultiplier` (line 107 in `FollowerConstants`). This value determines deceleration speed:
- Higher values: Faster braking but more oscillations.
- Lower values: Slower braking with fewer oscillations.

---

## Kalman Filter Adjustments (Optional)

The drive PID uses a Kalman filter to smooth error responses:
- Model Covariance: Default is `6`.
- Data Covariance: Default is `1`.
- Adjust the time constant (default `0.6`) to change the weighted average of derivatives.

Feel free to experiment with these settings for optimal performance.
