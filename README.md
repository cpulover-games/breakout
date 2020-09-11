# Development Process
1. HTML template
2. Declare canvas tag 
```
<canvas id="gameCanvas" height="500" width="500"></canvas>
```
3. Setup script
   - Use ```window.onload``` function (to load script only after HTML page finishes loading)
   - Declare variables and constans (for convention)
     - Fundamental: canvas, canvas context, FPS, background color, etc.
     - Game elements: X/Y position, X/Y speed, color, etc.
   - Get canvas: ```document.getElementById("gameCanvas")``` (to get canvas.width/height, add events)
   - Get canvas context: ```canvasContext = canvas.getContext("2d")``` (for drawing)
   - Set interval for animation: ```setInterval(updateFunction, 1000 / fps)```
4. Drawing code (interval)
   - Draw big frame (to clear screen and create effect of animation)
   - Draw game elements
5. Motion code (interval)
   - Update element position
   - Set boundations (collision with big frame)
6. Event code
7. Collision code (interval)
   - Determine edge coordinates of each element
   - Compare coordinates (collision happens when element coordinates overlap)
   - Update speeds when collision

# Notes and Tips
- [VSCode - JS] Declare type to enable code completion feature: ```/** @type {<type_name>} */```
  - Canvas: HTMLCanvasElement
  - Canvas context: CanvasRenderingContext2D
- 30 FPS prefer
- [Refactor] Create drawing helpers
- [Event] Fix mousemove position when page is scrolled
```
var rect = canvas.getBoundingClientRect();
var root = document.documentElement;
var mouseX = event.clientX - rect.left- root.scrollLeft;
```
- [Debug] Dislay mouse coordinate






























