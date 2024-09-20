<script>
  import { onMount } from "svelte";

  let strip1Time = 0;
  let strip2Time = 0;
  let strip3Time = 0;

  // Helper function to increment the time
  function incrementTime(targetTime, setTime) {
    let currentTime = 0;
    const interval = setInterval(() => {
      currentTime = parseFloat((currentTime + 0.1).toFixed(1));
      setTime(currentTime);

      if (currentTime >= targetTime) {
        clearInterval(interval); // Stop once the target time is reached
      }
    }, 100); // 100ms interval to increment by 0.1s
  }

  const observeStrips = () => {
    const strips = document.querySelectorAll(".strip");

    const observer = new IntersectionObserver(
      (entries) => {
        entries.forEach((entry) => {
          if (entry.isIntersecting) {
            const strip = entry.target;
            const time = parseFloat(strip.getAttribute("data-time"));
            const width = strip.getAttribute("data-width");

            // Start incrementing time for the visible strip
            if (strip.dataset.index === "1")
              incrementTime(time, (val) => (strip1Time = val));
            if (strip.dataset.index === "2")
              incrementTime(time, (val) => (strip2Time = val));
            if (strip.dataset.index === "3")
              incrementTime(time, (val) => (strip3Time = val));

            // Animate the width
            strip.style.transition = `width ${time}s linear`;
            strip.style.width = width;

            // Unobserve after animation starts
            observer.unobserve(strip);
          }
        });
      },
      { threshold: 0.1 }
    );

    strips.forEach((strip) => observer.observe(strip));
  };

  onMount(() => {
    observeStrips();
  });
</script>

<div class="flex flex-col items-start">
  <!-- First Strip -->
  <div
    class="z-30 flex flex-col strip"
    data-time="2.5"
    data-width="25%"
    data-index="1"
    style="width: 0%"
  >
    <span class="flex w-full justify-between text-sm lg:text-2xl"
      ><span>fal</span><span>{strip1Time.toFixed(1)}s</span></span
    >
    <div class="h-[35px] w-full bg-[#5718C0] md:h-[60px]"></div>
  </div>

  <!-- Second Strip -->
  <div
    class="relative z-20 flex flex-col strip"
    data-time="5"
    data-width="50%"
    data-index="2"
    style="width: 0%"
  >
    <div
      class="flex h-[35px] w-full items-end justify-end overflow-hidden bg-[#E5ECE7] md:h-[60px]"
    >
      <span
        class="md:text-md ml-auto flex min-w-28 shrink-0 justify-between px-1 text-xs opacity-90 lg:-top-7 lg:w-40 lg:text-lg"
        ><span>alternative 1</span><span>{strip2Time.toFixed(1)}s</span></span
      >
    </div>
  </div>

  <!-- Third Strip -->
  <div
    class="relative z-10 flex flex-col strip"
    data-time="9"
    data-width="90%"
    data-index="3"
    style="width: 0%"
  >
    <div
      class="flex h-[35px] w-full items-end justify-end overflow-hidden bg-[#FFC4D8] md:h-[60px]"
    >
      <span
        class="md:text-md ml-auto flex min-w-28 shrink-0 justify-between px-1 text-xs opacity-90 lg:-top-7 lg:w-40 lg:text-lg"
        ><span>alternative 2</span><span>{strip3Time.toFixed(1)}s</span></span
      >
    </div>
  </div>
  <div class="mb-10 mt-2 font-hal text-sm lg:mb-[124px]">
    flux[dev] inference speed
  </div>
</div>
