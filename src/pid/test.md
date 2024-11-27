# Testing Your Tuned PID Controllers

## Purpose

After completing the tuning of all PIDs, it’s important to validate the overall performance of your robot under real-world conditions. This step ensures that your robot follows paths accurately and smoothly.

---

## Recommended Tests

### 1. StraightBackAndForth
- This test evaluates the robot’s ability to move forward and backward in a straight line without deviating laterally or rotating unnecessarily.
- Look for:
    - Minimal oscillations.
    - Accurate stopping points.

### 2. CurvedBackAndForth
- This test assesses the robot’s handling of curved paths, focusing on centripetal corrections.
- Look for:
    - Smooth trajectory along the curve.
    - Proper centripetal corrections (neither over-correcting nor under-correcting).

### 3. Circle
- The **Circle** test is primarily for fun but can also be used to observe the robot’s handling of continuous curves.
- Look for:
    - Smooth and consistent movement along the circular trajectory.

### 4. Custom Paths
- Create custom paths to test the robot’s performance in scenarios closer to match conditions.
- Look for:
    - Consistency across different types of paths.
    - Smooth transitions between path segments.
###

---

## Fine-Tuning Tips

1. Observe the robot’s performance during each test.
2. If you notice any issues (e.g., overshooting, slow corrections, oscillations), revisit the corresponding PID and make small adjustments.
3. Alternate between different tests to ensure the robot performs well in diverse scenarios.

---

## Documentation and Support

If further improvements are needed or you encounter issues, please join the [Pedro Pathing Discord Server](https://discord.gg/2GfC4qBP5s) to ask questions!

---

## Final Thoughts

Congratulations on completing your PID tuning and testing! Best of luck to your team this season!
