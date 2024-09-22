<script>
  import feature2 from "$lib/Images/feature-2.png";
  import feature3 from "$lib/Images/feature-3.png";
  import FeatureTabs from "../CommonComponents/FeatureTabs.svelte";
  import ThirdFeature from "../CommonComponents/ThirdFeature.svelte";
</script>

<div
  class="mx-auto my-28 flex w-full max-w-[1680px] flex-col p-4 lg:my-[242px] lg:flex-row"
>
  <div class="flex">
    <div class="mb-4 w-[268px] p-4">
      <h4 class="mb-3 font-focal text-2xl font-medium">Features</h4>
      <div class="font-hal">
        Where developer experience meets the fastest AI.
      </div>
    </div>
  </div>

  <div
    class="grid grid-cols-1 gap-4 lg:ml-auto lg:mr-[133px] xl:grid-cols-2 xl:gap-14"
  >
    <!-- 1st Feature  -->
    <div
      class="ml-auto flex h-[788px] w-full max-w-[549px] flex-col overflow-hidden border border-stroke-light bg-[#F4F4F4] lg:ml-0"
    >
      <div
        class="flex aspect-square w-full items-center justify-center bg-white p-10 shadow-md"
      >
        <img src={feature3} alt="" />
      </div>
      <div class="max-w-[444px] flex-1 px-5 py-7">
        <h5 class="mb-5 font-focal text-4xl">
          Inference for Your Private Diffusion Model
        </h5>
        <p class="font-hal">
          If you are training your own diffusion transformer model, we would
          like to partner with you to run inference on your model. Fal's
          inference engine can run your model up to 50% faster and cost
          effective. Scale to thousands of GPUs when needed and pay only for
          what you use.
        </p>
      </div>
    </div>

    <!-- 2nd Feature  -->
    <div
      class="ml-auto flex h-[788px] w-full max-w-[549px] flex-col overflow-hidden border border-stroke-light bg-[#F4F4F4] lg:ml-0"
    >
      <div
        class="flex aspect-square w-full items-center justify-center bg-white p-10 shadow-md"
      >
        <img src={feature2} alt="" />
      </div>
      <div class="max-w-[444px] flex-1 px-5 py-7">
        <h5 class="mb-5 font-focal text-4xl">
          Blazing Fast Inference Engine for Diffusion Models
        </h5>
        <p class="font-hal">
          We have built world's fastest inference engine for diffusion models.
          We can run the FLUX models up to 400% faster than other alternatives.
        </p>
      </div>
    </div>

    <!-- 3rd Feature  -->
    <div
      class="ml-auto flex aspect-square h-[788px] w-full max-w-[549px] flex-col overflow-hidden border border-stroke-light bg-[#F4F4F4] lg:ml-0"
    >
      <ThirdFeature />
    </div>

    <!-- 4th Feature  -->
    <div
      class="ml-auto flex h-[788px] w-full max-w-[549px] flex-col overflow-hidden border border-stroke-light bg-[#F4F4F4] lg:ml-0"
    >
      <div class="flex flex-col aspect-square w-full bg-white p-3 shadow-md">
        <FeatureTabs />
      </div>

      <div class="max-w-[444px] flex-1 px-5 py-7">
        <h5 class="mb-5 font-focal text-4xl">
          World class developer experience
        </h5>
        <p class="font-hal">
          Use one of our client libraries to integrate fal directly into your
          applications.
        </p>
      </div>
    </div>
  </div>
</div>
