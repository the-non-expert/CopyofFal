<script>
  let sliderValue = 20; // Set the default value to $20

  const buttons = [1.0, 5.69, 20.0, 50.0, 100.0, 200.0, "custom"];

  function setSlider(button) {
    sliderValue = button !== "custom" ? button : sliderValue;
  }
</script>

<div class="w-full text-content-light">
  <div
    class="mb-4 flex w-fit flex-row items-center justify-between rounded border border-stroke-base px-2"
  >
    <div class="text-md font-hal">Choose a budget</div>
  </div>

  <div class="mb-8 flex h-12 w-fit items-center">
    <div
      class="flex flex-wrap p-2 bg-transparent border border-stroke-light rounded text-sm font-hal"
    >
      {#each buttons as button}
        <button
          class="inline-flex items-center justify-center whitespace-nowrap px-6 py-1.5 transition-all min-w-fit md:min-w-[6rem] font-medium text-content-strong rounded group/tab focus:bg-[#5D4AD9] focus:text-white"
          on:click={() => setSlider(button)}
        >
          {#if button === "custom"}
            custom
          {:else}
            ${button}
          {/if}

          <!-- Highlight if the current button matches the sliderValue -->
          {#if button === sliderValue}
            <span class="text-primary bg-[#5D4AD9]"></span>
          {/if}
        </button>
      {/each}
    </div>
  </div>

  <div
    class="flex w-full flex-col items-center justify-between border-stroke-blue-200 bg-[#F4F4F4] p-5 lg:!mt-[unset] lg:h-40 lg:flex-row lg:rounded lg:border"
  >
    <span class="flex h-4 w-full max-w-4xl items-center bg-[#99EDFF] p-3">
      <input
        type="range"
        min="1"
        max="500"
        bind:value={sliderValue}
        class="slider w-full max-w-4xl h-10 bg-black"
      />
    </span>

    <!-- Display the slider value -->
    <div
      class="mt-5 text-right text-4xl font-medium opacity-40 lg:ml-40 lg:mt-0 lg:w-56"
    >
      ${sliderValue.toFixed(2)}
    </div>
  </div>
</div>

<style>
  /* Custom styles for the range input */
  input[type="range"] {
    -webkit-appearance: none;
    appearance: none;
    width: 100%;
    height: 5px;
    background-color: #000;
    outline: none;
    opacity: 1;
    transition: opacity 0.15s ease-in-out;
  }

  /* Thumb (handle) */
  input[type="range"]::-webkit-slider-thumb {
    -webkit-appearance: none;
    appearance: none;
    width: 10px;
    height: 36px;
    background: black; /* Thumb color */
    transition: background 0.15s ease-in-out;
  }
</style>
