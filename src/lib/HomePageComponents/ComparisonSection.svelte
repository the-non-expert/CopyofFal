<script>
  import right3 from "$lib/Images/right-3.png";
  import right31 from "$lib/Images/right-3-1.png";
  import rightm31 from "$lib/Images/right-m-3-1.png";
  import right32 from "$lib/Images/right-3-2.png";
  import Strips from "../CommonComponents/Strips.svelte";
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
  <Strips />

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

<style>
  .strip {
    transition: width linear;
  }

  [data-time="2.5"] {
    transition-duration: 2.5s;
  }

  [data-time="5"] {
    transition-duration: 5s;
  }

  [data-time="9"] {
    transition-duration: 9s;
  }
</style>
