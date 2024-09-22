<script>
  import falIconGreen from "$lib/svgImages/fal-gpu-icon-green.svg";
  import falIconBlue from "$lib/svgImages/fal-gpu-icon-blue.svg";
  import Slider from "$lib/CommonComponents/Slider.svelte";
</script>

<div class="bg-dots bg-surface-300 py-12">
  <div class="ml-auto w-full lg:mr-[133px]">
    <div class="container mx-auto">
      <div class="flex flex-col items-start space-y-12 mx-auto max-w-[1200px]">
        <div class="w-full space-y-8">
          <Slider />
        </div>
        <div class="w-full">
          <div class="flex items-start space-x-6 py-4 text-content-light">
            <img
              src={falIconGreen}
              alt="GPU A100 icon"
              class="mb-4 h-16 w-16 md:mb-0"
            />
            <div class="flex w-full flex-col items-start text-content-light">
              <div
                class="grid w-fit grid-cols-3 gap-6 font-medium text-content-strong md:grid-cols-5"
              >
                <div class="flex flex-col space-y-1">
                  <span class="text-xs">GPU</span><span
                    class="text-lg text-content-strong">A100</span
                  >
                </div>
                <div class="flex flex-col space-y-1">
                  <span class="text-sm">VRAM</span><span
                    class="text-lg text-content-strong">40GB</span
                  >
                </div>
                <div class="flex flex-col space-y-1">
                  <span class="text-sm">CPUs</span><span
                    class="text-lg text-content-strong">10</span
                  >
                </div>
                <div class="flex flex-col space-y-1">
                  <span class="text-sm">CPU Memory</span><span
                    class="text-lg text-content-strong">4GB</span
                  >
                </div>
                <div class="flex flex-col space-y-1">
                  <span class="text-sm">Price per second</span><span
                    class="text-lg text-content-strong">$0.00111/s</span
                  >
                </div>
              </div>
              <div
                class="mt-4 flex w-full flex-1 flex-row md:mt-0 lg:justify-end"
              ></div>
              <div class="mt-8 flex w-full flex-col gap-4 md:gap-8">
                <div class="mb-8 w-full">
                  <div
                    class="flex w-full flex-col items-center justify-between space-y-4 md:flex-row"
                  >
                    <div
                      class="w-full flex-1 shrink-0 font-focal text-lg text-content-strong"
                    >
                      SDXL with defaults
                    </div>
                    <div class="flex-1 font-hal text-sm text-content-light">
                      With <span class="font-medium text-content-strong"
                        >$20.00</span
                      >, run this model with
                      <span class="font-medium text-content-strong"
                        >20 inference steps</span
                      >
                      approximately
                      <span class="font-medium text-content-strong">10,296</span
                      >
                      times.
                      <div class="pt-2">
                        That's about <span
                          class="font-medium text-content-strong">$0.00194</span
                        > per inference.
                      </div>
                    </div>
                    <div
                      class="flex w-full flex-1 items-center justify-start md:justify-end"
                    >
                      <a
                        href="/models/fal-ai/fast-sdxl"
                        class="inline-flex items-center justify-center whitespace-nowrap rounded border font-heading font-medium transition-all focus-ring disabled:pointer-events-none disabled:opacity-50 bg-surface-alpha text-content-base border-transparent hover:bg-surface-alpha-strong hover:text-content-strong data-[state=open]:bg-surface-alpha-strong h-8 px-2.5 text-sm"
                        >View</a
                      >
                    </div>
                  </div>
                </div>
                <div class="mb-8 w-full">
                  <div
                    class="flex w-full flex-col items-center justify-between space-y-4 md:flex-row"
                  >
                    <div
                      class="w-full flex-1 shrink-0 font-focal text-lg text-content-strong"
                    >
                      SDXL Lightning
                    </div>
                    <div class="flex-1 font-hal text-sm text-content-light">
                      With <span class="font-medium text-content-strong"
                        >$20.00</span
                      >, run this model with
                      <span class="font-medium text-content-strong"
                        >4 inference steps</span
                      >
                      approximately
                      <span class="font-medium text-content-strong">47,415</span
                      >
                      times.
                      <div class="pt-2">
                        That's about <span
                          class="font-medium text-content-strong">$0.00042</span
                        > per inference.
                      </div>
                    </div>
                    <div
                      class="flex w-full flex-1 items-center justify-start md:justify-end"
                    >
                      <a
                        href="/models/fal-ai/fast-lightning-sdxl"
                        class="inline-flex items-center justify-center whitespace-nowrap rounded border font-heading font-medium transition-all focus-ring disabled:pointer-events-none disabled:opacity-50 bg-surface-alpha text-content-base border-transparent hover:bg-surface-alpha-strong hover:text-content-strong data-[state=open]:bg-surface-alpha-strong h-8 px-2.5 text-sm"
                        >View</a
                      >
                    </div>
                  </div>
                </div>
                <div class="mb-8 w-full">
                  <div
                    class="flex w-full flex-col items-center justify-between space-y-4 md:flex-row"
                  >
                    <div
                      class="w-full flex-1 shrink-0 font-focal text-lg text-content-strong"
                    >
                      Whisper v3
                    </div>
                    <div class="flex-1 font-hal text-sm text-content-light">
                      With <span class="font-medium text-content-strong"
                        >$20.00</span
                      >, run this model with
                      <span class="font-medium text-content-strong"
                        >a 10 minute audio clip</span
                      >
                      approximately
                      <span class="font-medium text-content-strong">3,677</span>
                      times.
                      <div class="pt-2">
                        That's about <span
                          class="font-medium text-content-strong">$0.00544</span
                        > per inference.
                      </div>
                    </div>
                    <div
                      class="flex w-full flex-1 items-center justify-start md:justify-end"
                    >
                      <a
                        href="/models/fal-ai/whisper"
                        class="inline-flex items-center justify-center whitespace-nowrap rounded border font-heading font-medium transition-all focus-ring disabled:pointer-events-none disabled:opacity-50 bg-surface-alpha text-content-base border-transparent hover:bg-surface-alpha-strong hover:text-content-strong data-[state=open]:bg-surface-alpha-strong h-8 px-2.5 text-sm"
                        >View</a
                      >
                    </div>
                  </div>
                </div>
              </div>
              <div class="mt-4 border-b border-stroke-light"></div>
            </div>
          </div>
          <div class="flex items-start space-x-6 py-4 text-content-light">
            <img
              src={falIconBlue}
              alt="GPU A6000 icon"
              class="mb-4 h-16 w-16 md:mb-0"
            />
            <div
              class="flex w-full flex-col items-start text-content-light lg:flex-row"
            >
              <div
                class="grid w-fit grid-cols-3 gap-6 font-medium text-content-strong md:grid-cols-5"
              >
                <div class="flex flex-col space-y-1">
                  <span class="text-xs">GPU</span><span
                    class="text-lg text-content-strong">A6000</span
                  >
                </div>
                <div class="flex flex-col space-y-1">
                  <span class="text-sm">VRAM</span><span
                    class="text-lg text-content-strong">48GB</span
                  >
                </div>
                <div class="flex flex-col space-y-1">
                  <span class="text-sm">CPUs</span><span
                    class="text-lg text-content-strong">14</span
                  >
                </div>
                <div class="flex flex-col space-y-1">
                  <span class="text-sm">CPU Memory</span><span
                    class="text-lg text-content-strong">100GB</span
                  >
                </div>
                <div class="flex flex-col space-y-1">
                  <span class="text-sm">Price per second</span><span
                    class="text-lg text-content-strong">$0.000575/s</span
                  >
                </div>
              </div>
              <div
                class="mt-4 flex w-full flex-1 flex-row md:mt-0 lg:justify-end"
              >
                <button
                  class="inline-flex items-center justify-center whitespace-nowrap rounded border font-heading font-medium transition-all focus-ring disabled:pointer-events-none disabled:opacity-50 bg-surface-alpha text-content-base border-transparent hover:bg-surface-alpha-strong hover:text-content-strong data-[state=open]:bg-surface-alpha-strong h-9 px-3 text-sm"
                  >see examples</button
                >
              </div>
            </div>
          </div>
        </div>
        <div class="w-full">
          <div
            data-layout="default"
            class="flex flex-col rounded border border-stroke-light bg-surface group"
          >
            <div class="p-6 flex flex-col gap-2">
              <h3
                class="font-heading text-lg leading-none tracking-tight text-content-base lg:text-xl"
              >
                Billing Based on Model Output
              </h3>
              <div class="text-content-light">
                The models below are billed by model output, instead of compute
                seconds.
              </div>
            </div>
            <div
              class="flex-1 group-data-[layout=compact]:m-0 group-data-[layout=compact]:p-0 group-data-[layout=compact]:rounded-xl group-data-[layout=compact]:border-none overflow-y-auto p-0"
            >
              <div class="w-full">
                <table class="caption-bottom w-full">
                  <thead
                    class="[&amp;_tr]:border-b border-b border-stroke-light"
                    ><tr
                      class="border-b border-stroke-light transition-colors group-hover/tbody:hover:bg-surface-alpha-light data-[state=selected]:hover:bg-surface-alpha-light"
                      ><th
                        class="h-12 px-4 align-middle uppercase text-xs font-bold text-content-lighter [&amp;:has([role=checkbox])]:pr-0 w-64 text-left"
                        >Model Name</th
                      ><th
                        class="h-12 px-4 align-middle uppercase text-xs font-bold text-content-lighter [&amp;:has([role=checkbox])]:pr-0 text-left"
                        >Unit Price (USD)</th
                      ><th
                        class="h-12 px-4 text-center align-middle uppercase text-xs font-bold text-content-lighter [&amp;:has([role=checkbox])]:pr-0"
                      ></th></tr
                    ></thead
                  ><tbody class="[&amp;_tr:last-child]:border-0 group/tbody"
                    ><tr
                      class="border-b border-stroke-light transition-colors group-hover/tbody:hover:bg-surface-alpha-light data-[state=selected]:hover:bg-surface-alpha-light w-full"
                      ><td
                        class="p-4 align-middle [&amp;:has([role=checkbox])]:pr-0"
                        >FLUX.1 [dev]</td
                      ><td
                        class="p-4 align-middle [&amp;:has([role=checkbox])]:pr-0"
                        >0.025 per megapixel</td
                      ><td
                        class="p-4 align-middle [&amp;:has([role=checkbox])]:pr-0 flex-1 shrink-0 whitespace-nowrap"
                        >Billed by the size of generated images.</td
                      ></tr
                    ><tr
                      class="border-b border-stroke-light transition-colors group-hover/tbody:hover:bg-surface-alpha-light data-[state=selected]:hover:bg-surface-alpha-light w-full"
                      ><td
                        class="p-4 align-middle [&amp;:has([role=checkbox])]:pr-0"
                        >FLUX.1 [schnell]</td
                      ><td
                        class="p-4 align-middle [&amp;:has([role=checkbox])]:pr-0"
                        >0.003 per megapixel</td
                      ><td
                        class="p-4 align-middle [&amp;:has([role=checkbox])]:pr-0 flex-1 shrink-0 whitespace-nowrap"
                        >Billed by the size of generated images.</td
                      ></tr
                    ><tr
                      class="border-b border-stroke-light transition-colors group-hover/tbody:hover:bg-surface-alpha-light data-[state=selected]:hover:bg-surface-alpha-light w-full"
                      ><td
                        class="p-4 align-middle [&amp;:has([role=checkbox])]:pr-0"
                        >FLUX.1 [pro]</td
                      ><td
                        class="p-4 align-middle [&amp;:has([role=checkbox])]:pr-0"
                        >0.05 per megapixel</td
                      ><td
                        class="p-4 align-middle [&amp;:has([role=checkbox])]:pr-0 flex-1 shrink-0 whitespace-nowrap"
                        >Billed by the size of generated images.</td
                      ></tr
                    ><tr
                      class="border-b border-stroke-light transition-colors group-hover/tbody:hover:bg-surface-alpha-light data-[state=selected]:hover:bg-surface-alpha-light w-full"
                      ><td
                        class="p-4 align-middle [&amp;:has([role=checkbox])]:pr-0"
                        >Stable Diffusion 3 - Medium</td
                      ><td
                        class="p-4 align-middle [&amp;:has([role=checkbox])]:pr-0"
                        >0.035 per image</td
                      ><td
                        class="p-4 align-middle [&amp;:has([role=checkbox])]:pr-0 flex-1 shrink-0 whitespace-nowrap"
                      ></td></tr
                    ><tr
                      class="border-b border-stroke-light transition-colors group-hover/tbody:hover:bg-surface-alpha-light data-[state=selected]:hover:bg-surface-alpha-light w-full"
                      ><td
                        class="p-4 align-middle [&amp;:has([role=checkbox])]:pr-0"
                        >Stable Video</td
                      ><td
                        class="p-4 align-middle [&amp;:has([role=checkbox])]:pr-0"
                        >0.075 per video</td
                      ><td
                        class="p-4 align-middle [&amp;:has([role=checkbox])]:pr-0 flex-1 shrink-0 whitespace-nowrap"
                      ></td></tr
                    ></tbody
                  >
                </table>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</div>
