# Development Process
1. HTML template
2. Declare canvas tag 
```
<canvas id="gameCanvas" height="500" width="500"></canvas>
```
3. Setup script
   - Declare variables (for convention)
   - Get canvas: ```document.getElementById("gameCanvas")``` (to get canvas.width/height)
   - Get canvas context: ```canvasContext = canvas.getContext("2d")``` (for drawing)
   - Set interval for animation: ```setInterval(updateFunction, 1000 / fps)```
4. Drawing code with canvas context
   - Draw big frame (to create effect of animation)
   - Draw game elements

# Notes and Tips
- [VSCode] Declare type to enable autofilling feature: ```/** @type {CanvasRenderingContext2D} */```











