<script>
  import "../app.css";
  import DesktopHeader from "../lib/DesktopHeader.svelte";
  import Footer from "../lib/Footer.svelte";
</script>

<div class="bg-[#99edff]">
  <DesktopHeader />
</div>
<div>
  <slot />
</div>

<div class="bg-[#99EDFF]">
  <Footer />
</div>
