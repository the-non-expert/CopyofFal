<script>
  import { onMount } from "svelte";

  let canvas;
  let ctx;
  let pixelData = [];
  let animationId; // To store the requestAnimationFrame ID
  const canvasWidth = 250; // Set the canvas width to match the display size
  const canvasHeight = 250; // Set the canvas height to match the display size
  const pixelSize = 12; // Size of each pixel
  const totalPixels = (canvasWidth / pixelSize) * (canvasHeight / pixelSize); // Total number of pixels

  let lastTime = 0;
  const frameDelay = 300; // Delay in milliseconds (100ms = 10fps)

  const colorDistribution = {
    "#99EDFF": Math.floor(totalPixels * 0.85),
    "#A15DF9": Math.floor(totalPixels * 0.14),
    "#F7EC37": Math.floor(totalPixels * 0.01),
  };

  // Initialize pixels with specific color distribution
  function initPixels() {
    addPixels("#99EDFF", colorDistribution["#99EDFF"]);
    addPixels("#A15DF9", colorDistribution["#A15DF9"]);
    addPixels("#F7EC37", colorDistribution["#F7EC37"]);

    pixelData = shuffle(pixelData); // Shuffle the pixelData array to randomize color positions
  }

  // Add pixels of a specific color to the pixelData array
  function addPixels(color, count) {
    for (let i = 0; i < count; i++) {
      pixelData.push({ color });
    }
  }

  // Fisher-Yates shuffle to randomize pixel placement
  function shuffle(array) {
    let currentIndex = array.length,
      randomIndex;

    while (currentIndex !== 0) {
      randomIndex = Math.floor(Math.random() * currentIndex);
      currentIndex--;

      // Swap the elements
      [array[currentIndex], array[randomIndex]] = [
        array[randomIndex],
        array[currentIndex],
      ];
    }
    return array;
  }

  // Draw pixels on the canvas
  function drawPixels() {
    ctx.clearRect(0, 0, canvasWidth, canvasHeight); // Clear the canvas before redrawing
    let index = 0;
    for (let i = 0; i < canvasWidth / pixelSize; i++) {
      for (let j = 0; j < canvasHeight / pixelSize; j++) {
        const pixel = pixelData[index];
        if (pixel) {
          // Check if the pixel data exists
          ctx.fillStyle = pixel.color;
          ctx.fillRect(i * pixelSize, j * pixelSize, pixelSize, pixelSize);
        }
        index++;
      }
    }
  }

  function animatePixels(timestamp) {
    // Check if enough time has passed since the last frame
    if (timestamp - lastTime > frameDelay) {
      pixelData = shuffle(pixelData); // Shuffle the pixels
      drawPixels(); // Redraw the shuffled pixels
      lastTime = timestamp; // Update lastTime to the current timestamp
    }
    animationId = requestAnimationFrame(animatePixels); // Continue animation
  }

  // Mount the canvas and start the animation
  onMount(() => {
    if (canvas) {
      canvas.width = canvasWidth; // Ensure canvas internal width matches display
      canvas.height = canvasHeight; // Ensure canvas internal height matches display
      ctx = canvas.getContext("2d");

      initPixels(); // Initialize the pixel data
      drawPixels(); // Draw the initial state
      animationId = requestAnimationFrame(animatePixels); // Start the animation loop

      // Stop the animation after 4 seconds
      setTimeout(() => {
        cancelAnimationFrame(animationId); // Stop the animation
        console.log("Animation stopped");
      }, 2000); // 4000 ms = 4 seconds
    }
  });
</script>

<!-- Canvas HTML -->
<div
  class="pointer-events-none absolute right-0 top-5 lg:top-7 flex h-16 w-16 items-end lg:right-10 lg:h-72 lg:w-72"
>
  <canvas
    bind:this={canvas}
    style="image-rendering: pixelated;"
    class="w-[100px] h-[100px] lg:w-[250px] lg:h-[250px]"
  ></canvas>
</div>
