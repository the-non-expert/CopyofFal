<script>
  import HomeHero from "../lib/HomePageComponents/HomeHero.svelte";
  import left1 from "$lib/Images/left-1.png";
  import left3 from "$lib/svgImages/left-3.svg";
  import right2 from "$lib/Images/right-2.png";
  import AccessAndCarousel from "../lib/HomePageComponents/AccessAndCarousel.svelte";
</script>

<svg
  width="332"
  height="209"
  viewBox="0 0 332 209"
  fill="none"
  xmlns="http://www.w3.org/2000/svg"
  class="pointer-events-none absolute left-[235px] top-[40px] hidden lg:block"
  ><path
    id="path1"
    d="M167.01 47.7147L30.3829 158.403L301.547 98.772"
    stroke="#AB77FF"
    stroke-width="59.5056"
    stroke-linecap="round"
    stroke-linejoin="round"
  ></path><animate
    xlink:href="#path1"
    attributeName="stroke-dasharray"
    from="0, 1000"
    to="1000, 0"
    dur="2s"
    repeatCount="1"
    begin="2"
  ></animate><path
    id="path2"
    d="M42.4192 30.5587L280.114 155.909"
    stroke="#FFFF00"
    stroke-width="59.5056"
    stroke-linecap="round"
    stroke-linejoin="round"
  ></path><animate
    xlink:href="#path2"
    attributeName="stroke-dasharray"
    from="0, 1000"
    to="1000, 0"
    dur="2s"
    begin="2"
    repeatCount="1"
  ></animate></svg
>
<img
  src={left1}
  class="pointer-events-none absolute left-0 top-[119px] h-[226px] max-w-[457px] lg:h-auto"
  alt=""
/>

<img
  src={left3}
  class="pointer-events-none absolute left-0 top-[758px] h-[534px] mix-blend-multiply lg:top-[600px] lg:h-auto"
  alt=""
/>
<svg
  width="263"
  height="472"
  viewBox="0 0 263 472"
  fill="none"
  xmlns="http://www.w3.org/2000/svg"
  class="pointer-events-none absolute right-0 top-[250px] hidden lg:block"
  ><path
    id="xpath1"
    d="M204.727 441.572L118.595 187.027"
    stroke="#AB77FF"
    stroke-width="59.5056"
    stroke-linecap="round"
    stroke-linejoin="round"
  ></path><animate
    xlink:href="#xpath1"
    attributeName="stroke-dasharray"
    from="0, 1000"
    to="1000, 0"
    dur="2s"
    repeatCount="1"
    begin="1s"
  ></animate><path
    id="xpath2"
    d="M368.876 145.251L100.651 161.58"
    stroke="#FFFF00"
    stroke-width="59.5056"
    stroke-linecap="round"
    stroke-linejoin="round"
  ></path><animate
    xlink:href="#xpath2"
    attributeName="stroke-dasharray"
    from="0, 1000"
    to="1000, 0"
    dur="2s"
    begin="1s"
    repeatCount="1"
  ></animate></svg
>

<img
  src={right2}
  class="pointer-events-none absolute right-0 top-[779px] h-[277px] max-w-[404px] lg:h-auto"
  alt=""
/>

<div class="bg-[#99edff]">
  <HomeHero />
</div>

<div class="flex h-2 w-full justify-center">
  <div class="h-full w-[5%] bg-[#AB77FF]"></div>
  <div class="h-full w-[50%] bg-[#ADFF00]"></div>
  <div class="h-full w-[20%] bg-[#99EDFF]"></div>
</div>

<div>
  <AccessAndCarousel />
</div>
