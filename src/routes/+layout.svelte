<script>
  import "../app.css";
  import DesktopHeader from "../lib/DesktopHeader.svelte";
  import Footer from "../lib/Footer.svelte";
  import MobileHeader from "../lib/MobileHeader.svelte";
</script>

<div class="bg-[#99edff]">
  <DesktopHeader />
  <MobileHeader />
</div>
<div>
  <slot />
</div>

<div class="bg-[#99EDFF]">
  <Footer />
</div>
<div class="flex h-2 w-full justify-end">
  <div class="h-full w-[5%] bg-[#AB77FF]"></div>
  <div class="h-full w-[40%] bg-[#99EDFF]"></div>
  <div class="h-full w-[7%] bg-[#AB77FF]"></div>
  <div class="h-full w-[25%] bg-black"></div>
  <div class="h-full w-[10%] bg-[#ADFF00]"></div>
</div>
