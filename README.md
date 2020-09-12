# Development Process
1. HTML template
2. Declare canvas tag 
```
<canvas id="gameCanvas" height="500" width="500"></canvas>
```
3. Declare global variables and constants (for convention)
   - Fundamental: canvas, canvas context, FPS, background color, mouse positions, etc.
   - Game elements: X/Y position, X/Y speed, color, etc.
4. Setup script
   - Use ```window.onload``` function (to load script only after HTML page finishes loading)
   - Get canvas: ```document.getElementById("gameCanvas")``` (to get canvas.width/height, add  events)
   - Get canvas context: ```canvasContext = canvas.getContext("2d")``` (for drawing)
   - Init code: initialize states of game elements
   - Set interval for animation/drawing: ```setInterval(updateFunction, 1000 / fps)```
5. Drawing code (interval)
   - Draw big frame (to clear screen and create effect of animation)
   - Draw game elements
6. Motion code (interval)
   - Update element position
   - Set boundations (collision with big frame)
7. Event code
8. Collision code (interval)
   - Determine edge coordinates of each element
   - Compare coordinates (collision happens when element coordinates overlap)
   - Update speeds, states when collision
9. Game over and game restart containing init code

# Notes and Tips
- [VSCode - JS] Declare type to enable code completion feature: ```/** @type {<type_name>} */```
  - Canvas: HTMLCanvasElement
  - Canvas context: CanvasRenderingContext2D
- 30 FPS prefer
- [Refactor] Create drawing helpers
- [Event] Get ```mousemove``` position when page is scrolled
```
var rect = canvas.getBoundingClientRect();
var root = document.documentElement;
var mouseX = event.clientX - rect.left- root.scrollLeft;
var mouseY = event.clientY - rect.top - root.scrollTop;
```
- [Debug] Dislay mouse coordinate
- Init only (mostly) constants' values in declaration section, for variables' values, init in initialization code






























