# Manim Animation Prompts

> Prompts for generating Manim (Mathematical Animation Engine) code — create stunning math visualizations, algorithm animations, and educational content.

**Best with:** Claude, ChatGPT (GPT-4), Cursor, Claude Code

---

## Basic Mathematical Concepts

### 1. Function Plotting
```
Write a Manim scene that plots the function f(x) = sin(x) on a coordinate plane.
Add axes with labels, draw the curve with a smooth animation using Create,
then add a dot that traces along the curve. Use blue for the curve and yellow for the dot.
Show the x-axis from -2π to 2π and y-axis from -1.5 to 1.5.
```

### 2. Derivative Visualization
```
Create a Manim scene showing the geometric meaning of a derivative.
Plot f(x) = x² on axes. Animate a secant line between two points on the curve,
then smoothly move the points closer together until the secant becomes a tangent line.
Display the slope value updating in real-time using a DecimalNumber.
Use colors: curve=BLUE, secant=YELLOW, tangent=GREEN.
```

### 3. Integration Area
```
Write a Manim scene that visualizes definite integration as area under a curve.
Plot f(x) = x² from 0 to 3. Start with 4 Riemann sum rectangles, then animate
increasing to 8, 16, 32, and finally show the smooth filled area.
Display the approximate area value updating with each step.
Use BLUE for the curve and BLUE with 0.3 opacity for the filled area.
```

### 4. Taylor Series Expansion
```
Create a Manim animation showing Taylor series approximation of sin(x).
Start with the first term (x), then progressively add terms (x - x³/3! + x⁵/5! - ...).
Show each polynomial approximation in a different color overlaid on the actual sin(x) curve.
Display the current polynomial equation using MathTex at the top of the screen.
Animate up to the 7th order approximation.
```

### 5. Vector Field
```
Write a Manim scene displaying a 2D vector field for F(x,y) = (-y, x).
Use ArrowVectorField to show the rotation pattern. Then animate a particle
(small dot) following the field lines in a circular path.
Use a color gradient based on vector magnitude.
```

## Linear Algebra

### 6. Matrix Transformation
```
Create a Manim scene showing how a 2x2 matrix transforms the unit square.
Start with a grid and the unit square highlighted. Apply the transformation
matrix [[2, 1], [0, 1]] (shear transformation). Show basis vectors e1 and e2
as colored arrows, and animate how they transform. Display the matrix
equation using MathTex.
```

### 7. Eigenvalue Visualization
```
Write a Manim animation that shows eigenvectors of a 2x2 matrix.
Use the matrix [[3, 1], [0, 2]]. Show multiple random vectors being transformed,
then highlight the eigenvectors (which only scale, not rotate) in a bright color.
Display eigenvalues next to each eigenvector.
```

### 8. SVD Decomposition
```
Create a Manim scene that visually decomposes a matrix using SVD.
Show a 2D shape (unit circle). Apply transformations step by step:
first rotation (V^T), then scaling (Σ), then rotation (U).
Show each step separately with labels U, Σ, V^T.
```

### 9. Dot Product Geometry
```
Write a Manim scene showing the geometric interpretation of the dot product.
Draw two vectors a and b from the origin. Show the projection of a onto b
as a dashed line. Animate the angle between them changing and update
the dot product value (|a||b|cos θ) in real-time.
```

## Calculus

### 10. Gradient Descent
```
Create a Manim animation of gradient descent on f(x) = x⁴ - 3x² + 2.
Plot the function. Place a ball at x=2. Animate the ball rolling downhill
following the negative gradient with learning rate 0.1. Show the gradient
arrow at each step, and display the current x value and f(x) value.
Run for 20 iterations. Use red for the ball and green for gradient arrows.
```

### 11. Chain Rule Visualization
```
Write a Manim scene explaining the chain rule visually.
Show three number lines representing x, u=g(x), and y=f(u).
Animate how a small change dx maps to du via g'(x) and then to dy via f'(u).
Show the equation dy/dx = (dy/du)(du/dx) with animated arrows connecting them.
Use g(x) = x² and f(u) = sin(u) as examples.
```

### 12. Fourier Series
```
Create a Manim animation building a square wave from Fourier series.
Start with the fundamental sine wave, then progressively add harmonics
(3rd, 5th, 7th, 9th, 11th). Show each harmonic being added with a different
color, and the sum getting closer to a square wave. Display the partial
sum formula at the top using MathTex.
```

### 13. Multivariable Calculus — 3D Surface
```
Write a Manim scene using ThreeDScene to plot the surface z = sin(x)*cos(y).
Rotate the camera smoothly around the surface. Add contour lines at the base
plane. Use a color gradient based on z-value (blue for low, red for high).
Add axes labels x, y, z.
```

## Probability & Statistics

### 14. Central Limit Theorem
```
Create a Manim animation demonstrating the Central Limit Theorem.
Start with a uniform distribution. Show sampling: take samples of size n,
compute means, and build a histogram. Animate n increasing from 1 to 5 to 30.
Show the histogram morphing toward a normal distribution.
Overlay the theoretical normal curve. Display n and sample count.
```

### 15. Bayes' Theorem
```
Write a Manim scene visualizing Bayes' theorem with a medical test example.
Use rectangles/areas to show: P(Disease)=1%, P(Positive|Disease)=99%,
P(Positive|No Disease)=5%. Animate highlighting the true positive area
vs false positive area. Calculate and display P(Disease|Positive) step by step.
```

### 16. Normal Distribution
```
Create a Manim animation of a normal distribution that shows the 68-95-99.7 rule.
Draw the bell curve. Progressively shade the area within 1σ (68%), 2σ (95%),
and 3σ (99.7%) using different colors. Label each percentage.
Animate the mean and standard deviation shifting to show how the curve changes.
```

## Neural Networks & ML

### 17. Neural Network Forward Pass
```
Write a Manim scene showing a forward pass through a neural network.
Draw a network with architecture [3, 4, 4, 2] (input, two hidden, output).
Animate data flowing from input to output — light up each neuron as data
passes through. Show weights as colored lines (red=negative, green=positive).
Display activation values inside each neuron.
```

### 18. Backpropagation
```
Create a Manim animation showing backpropagation in a simple 2-layer network.
First show the forward pass with values. Then show the loss computation.
Animate the error signal flowing backward through the network with red arrows.
Display the gradient computation at each step using the chain rule.
Show weight updates with before/after values.
```

### 19. Convolution Operation
```
Write a Manim scene showing how 2D convolution works in a CNN.
Show a 5x5 input grid with numbers, a 3x3 kernel/filter, and the output grid.
Animate the kernel sliding across the input, highlighting the current receptive
field, computing the dot product, and writing the result in the output.
Use colors to highlight the active computation region.
```

### 20. Loss Landscape
```
Create a Manim 3D scene showing a loss landscape with multiple local minima.
Plot a surface with several valleys. Animate two gradient descent paths:
one getting stuck in a local minimum, another reaching the global minimum.
Use different colors for each path. Show how learning rate affects the trajectory.
```

## Algorithm Visualizations

### 21. Sorting Algorithm — Merge Sort
```
Write a Manim scene visualizing merge sort on an array [38, 27, 43, 3, 9, 82, 10].
Show bars representing values. Animate the divide step (splitting into halves),
then the merge step (comparing and combining). Color-code: unsorted=BLUE,
comparing=YELLOW, sorted=GREEN. Show the current operation at the top.
```

### 22. Binary Search
```
Create a Manim animation of binary search on a sorted array.
Show 15 sorted numbers as labeled boxes. Search for a target value.
Animate highlighting the search range, computing the midpoint, comparing,
and eliminating half the array each step. Show low, mid, high pointers.
Color eliminated elements gray.
```

### 23. Graph BFS/DFS
```
Write a Manim scene showing BFS traversal on a graph with 8 nodes.
Draw the graph with nodes as circles and edges as lines. Animate BFS:
start from a source node, show the frontier expanding level by level.
Color nodes: unvisited=WHITE, in queue=YELLOW, visited=GREEN.
Show the queue state at the bottom updating in real-time.
```

### 24. Dynamic Programming — Fibonacci
```
Create a Manim animation showing the recursion tree for Fibonacci(6),
then show how memoization eliminates redundant computations.
First draw the full recursion tree with repeated subproblems highlighted in red.
Then animate the memoized version where cached results are looked up (GREEN)
instead of recomputed. Show the memoization table building up.
```

## Physics & Engineering

### 25. Simple Harmonic Motion
```
Write a Manim scene showing simple harmonic motion of a spring-mass system.
Animate a mass on a spring oscillating left and right. Simultaneously plot
the position x(t) = A*cos(ωt) as a function of time on axes to the right.
Show the velocity and acceleration vectors on the mass. Use a tracer dot
on the plot synchronized with the mass motion.
```

### 26. Wave Interference
```
Create a Manim animation showing two waves interfering. Draw wave 1 and
wave 2 separately at the top, then show their sum (superposition) below.
Animate constructive interference (in phase) transitioning to destructive
interference (out of phase) by shifting one wave's phase. Display the
phase difference angle.
```

### 27. Electric Field Lines
```
Write a Manim scene showing electric field lines between a positive and
negative charge (dipole). Place +q and -q charges. Draw field lines flowing
from positive to negative. Use ArrowVectorField or StreamLines.
Animate a test charge moving along a field line.
```

## Advanced / Creative

### 28. Mandelbrot Set Zoom
```
Create a Manim scene that renders and zooms into the Mandelbrot set.
Start with the full set view, then animate zooming into an interesting
boundary region. Use a color gradient based on iteration count.
Make it smooth with at least 3 zoom levels.
```

### 29. 3D Möbius Strip
```
Write a Manim ThreeDScene that constructs and rotates a Möbius strip.
Parametrize the surface and create it using Surface. Animate the camera
rotating around it. Then animate an ant walking along the surface to show
it has only one side. Use a gradient color for the surface.
```

### 30. Fractal — Koch Snowflake
```
Create a Manim animation that builds a Koch snowflake iteratively.
Start with an equilateral triangle. Animate each iteration: subdivide each
edge into thirds, replace the middle third with an equilateral triangle bump.
Show iterations 0 through 5. Display the current iteration number and
the perimeter length (which increases with each step).
```

## Prompt Templates

### 31. Generic Manim Scene Template
```
Create a Manim scene called [SceneName] that visualizes [concept].
Requirements:
- Use [resolution: 1080p/720p] quality settings
- Animation duration: [X] seconds
- Color scheme: background=[BLACK/WHITE], primary=[COLOR], accent=[COLOR]
- Include title text "[Title]" at the beginning using Write animation
- Add mathematical notation using MathTex for [equations]
- Smooth transitions between steps using [Transform/ReplacementTransform]
- End with a FadeOut of all objects
```

### 32. Step-by-Step Proof Animation
```
Create a Manim animation that proves [theorem name] step by step.
Format each step as:
1. Show the statement using MathTex
2. Animate the algebraic manipulation
3. Highlight the key insight with a colored box (SurroundingRectangle)
4. Transition to the next step using TransformMatchingTex
Use a consistent layout with the current step centered and previous
steps faded above. Include "Q.E.D." at the end.
```

### 33. Comparison Animation
```
Create a Manim scene comparing [Method A] vs [Method B] side by side.
Split the screen vertically. Run both methods simultaneously:
- Left side: [Method A] with label and metrics
- Right side: [Method B] with label and metrics
Show a running counter/metric at the bottom comparing performance.
Use distinct colors for each method. End with a summary comparison table.
```

### 34. Data Visualization Animation
```
Write a Manim scene that creates an animated [bar chart / line chart / pie chart]
showing [data description]. Start with empty axes, then animate bars/lines
growing to their final values. Add value labels above each bar/point.
Include a title, axis labels, and legend. Use the following data:
[provide your data points]
```

## Tips for Better Manim Prompts

### Do's
- Specify exact colors (use Manim color names: BLUE, RED, GREEN, YELLOW, etc.)
- Mention animation types (Create, Write, FadeIn, Transform, etc.)
- Specify duration/run_time when timing matters
- Ask for MathTex for mathematical expressions
- Request specific screen layout (centered, split, top/bottom)

### Don'ts
- Don't ask for interactive elements (Manim generates videos, not apps)
- Don't request real-time user input
- Don't expect photorealistic rendering
- Don't combine too many concepts in one scene (keep it focused)

### Quality Settings
```python
# Add to your prompt for quality control:
# Low quality (fast preview):  manim render -ql scene.py SceneName
# Medium quality:              manim render -qm scene.py SceneName
# High quality (production):   manim render -qh scene.py SceneName
# 4K quality:                  manim render -qk scene.py SceneName
```

---

*40+ Manim prompts — ready to copy and create stunning math animations*
