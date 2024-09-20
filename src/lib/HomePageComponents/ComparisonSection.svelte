<script>
  import right3 from "$lib/Images/right-3.png";
  import right31 from "$lib/Images/right-3-1.png";
  import rightm31 from "$lib/Images/right-m-3-1.png";
  import right32 from "$lib/Images/right-3-2.png";
</script>

<div
  class="relative my-[200px] flex flex-col justify-center gap-6 bg-[#D5BBFF] p-3 py-[205px] lg:pl-[296px]"
>
  <img
    src={right3}
    class="pointer-events-none absolute bottom-10 left-0 z-50 h-[160px] lg:h-[345px]"
    alt=""
  /><img
    src={right31}
    class="pointer-events-none absolute left-0 top-2 z-50 h-36 lg:h-auto"
    alt=""
  /><img
    src={rightm31}
    class="pointer-events-none absolute right-0 top-2 z-50 lg:hidden lg:h-auto"
    alt=""
  /><img
    src={right32}
    class="pointer-events-none absolute bottom-2 right-0 z-50 hidden lg:block lg:h-auto"
    alt=""
  />
  <div class="flex flex-col">
    <div class="flex flex-col items-start">
      <div class="z-30 flex flex-col" style="width: 25%;">
        <span class="flex w-full justify-between text-sm lg:text-2xl"
          ><span>fal</span><span>2.5s</span></span
        >
        <div class="h-[35px] w-full bg-[#5718C0] md:h-[60px]"></div>
      </div>
      <div class="relative z-20 flex flex-col" style="width: 50%;">
        <div
          class="flex h-[35px] w-full items-end justify-end overflow-hidden bg-[#E5ECE7] md:h-[60px]"
        >
          <span
            class="md:text-md ml-auto flex min-w-28 shrink-0 justify-between px-1 text-xs opacity-90 lg:-top-7 lg:w-40 lg:text-lg"
            ><span>alternative 1 </span><span>5s</span></span
          >
        </div>
      </div>
      <div class="relative z-10 flex flex-col" style="width: 90%;">
        <div
          class="flex h-[35px] w-full items-end justify-end overflow-hidden bg-[#FFC4D8] md:h-[60px]"
        >
          <span
            class="md:text-md ml-auto flex min-w-28 shrink-0 justify-between px-1 text-xs opacity-90 lg:-top-7 lg:w-40 lg:text-lg"
            ><span>alternative 2</span><span>9.0s</span></span
          >
        </div>
      </div>
    </div>
    <div class="mb-10 mt-2 font-hal text-sm lg:mb-[124px]">
      flux[dev] inference speed
    </div>
  </div>
  <p
    class="font-focal text-3xl font-medium text-content-strong md:text-5xl lg:text-[72px] lg:leading-[69px]"
  >
    fal Inference Engine™ is<br />the fastest way to run<br />diffusion models
  </p>
  <p class="max-w-[212px] font-hal font-light text-content-strong">
    Run diffusion models up to 4x faster. Enable new user experiences leveraging
    our real time infrastructure.
  </p>
</div>
