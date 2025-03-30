# Bresenham's Circle Drawing Algorithm

1. **Initialize the following variables:**
   - Center of the circle: \((cx, cy)\)
   - Radius: \(r\)
   - Starting point: \((x, y) = (0, r)\)
   - Decision parameter \(p = 3 - 2r\) (Initial decision value)

2. **Plot the initial points:**
   Using the symmetry of the circle, plot the eight symmetrical points:
   \[
   (cx + x, cy + y), (cx - x, cy + y), (cx + x, cy - y), (cx - x, cy - y)
   \]
   \[
   (cx + y, cy + x), (cx - y, cy + x), (cx + y, cy - x), (cx - y, cy - x)
   \]

3. **Loop until \(x < y\):**
   - Increase \(x\) by 1.
   - If \(p \leq 0\), update the decision parameter as:
     \[
     p = p + 4x + 6
     \]
     This means you move horizontally.
   - If \(p > 0\), update the decision parameter as:
     \[
     p = p + 4(x - y) + 10
     \]
     Then, decrease \(y\) by 1 (move diagonally).

4. **Plot the new points** after each update using symmetry.

5. **Repeat steps 3 and 4** until \(x\) is greater than or equal to \(y\).

6. **End the algorithm** once all points have been plotted.
