<script>
  import { onMount } from "svelte";

  let canvas;
  let ctx;
  let pixelData = [];
  let animationId; // To store the requestAnimationFrame ID
  const canvasWidth = 100;
  const canvasHeight = 100;
  const pixelSize = 6;

  // Initialize the pixels
  function initPixels() {
    for (let i = 0; i < canvasWidth / pixelSize; i++) {
      for (let j = 0; j < canvasHeight / pixelSize; j++) {
        pixelData.push({
          x: i * pixelSize,
          y: j * pixelSize,
          color: randomColor(),
        });
      }
    }
  }

  // Generate a random color
  function randomColor() {
    const colors = [
      "#A15DF9",
      "#A15DF9",
      "#A15DF9",
      "#A15DF9",
      "#F7EC37",
      "#99EDFF",
      "#99EDFF",
      "#99EDFF",
      "#99EDFF",
      "#99EDFF",
      "#99EDFF",
      "#99EDFF",
      "#99EDFF",
      "#99EDFF",
      "#99EDFF",
      "#99EDFF",
      "#99EDFF",
      "#99EDFF",
      "#99EDFF",
      "#99EDFF",
      "#99EDFF",
      "#99EDFF",
      "#99EDFF",
      "#99EDFF",
      "#99EDFF",
    ]; // Purple, Yellow, Cyan
    return colors[Math.floor(Math.random() * colors.length)];
  }

  // Draw pixels on the canvas
  function drawPixels() {
    ctx.clearRect(0, 0, canvasWidth, canvasHeight);
    for (const pixel of pixelData) {
      ctx.fillStyle = pixel.color;
      ctx.fillRect(pixel.x, pixel.y, pixelSize, pixelSize);
    }
  }

  // Animate pixels
  function animatePixels() {
    for (let pixel of pixelData) {
      if (Math.random() > 0.99) {
        pixel.color = randomColor();
      }
    }
    drawPixels();
    animationId = requestAnimationFrame(animatePixels); // Save the requestAnimationFrame ID
  }

  // Mount the canvas and start the animation
  onMount(() => {
    if (canvas) {
      ctx = canvas.getContext("2d");
      initPixels(); // Initialize the pixel data
      drawPixels(); // Draw the initial state
      animationId = requestAnimationFrame(animatePixels); // Start the animation loop

      // Stop the animation after 4 seconds
      setTimeout(() => {
        cancelAnimationFrame(animationId); // Stop the animation
        console.log("Animation stopped");
      }, 4000); // 4000 ms = 4 seconds
    }
  });
</script>

<!-- Canvas HTML -->
<div
  class="hidden md:inline pointer-events-none absolute right-0 top-16 flex h-40 w-40 items-end lg:right-10 lg:h-72 lg:w-72"
>
  <canvas
    bind:this={canvas}
    width="100"
    height="100"
    style="width: 250px; height: 250px; image-rendering: pixelated;"
  ></canvas>
</div>

<!-- Optional styles -->
<style>
</style>
