# Development Process
1. HTML template
2. Declare canvas tag 
```
<canvas id="gameCanvas" height="500" width="500"></canvas>
```
3. Setup script
   - Declare variables and constans (for convention)
     - Fundamental: canvas, canvas contest, FPS, background color, etc.
     - Game elements: X/Y position, X/Y speed, color, etc.
   - Get canvas: ```document.getElementById("gameCanvas")``` (to get canvas.width/height)
   - Get canvas context: ```canvasContext = canvas.getContext("2d")``` (for drawing)
   - Set interval for animation: ```setInterval(updateFunction, 1000 / fps)```
4. Drawing code with canvas context
   - Draw big frame (to clear screen and create effect of animation)
   - Draw game elements
5. Motion code
   - Update element position
   - Set boundations (collision with big frame)

# Notes and Tips
- [VSCode] Declare type to enable autofilling feature: ```/** @type {CanvasRenderingContext2D} */```
- 30 FPS prefer
- [Refactor] Create drawing helpers










