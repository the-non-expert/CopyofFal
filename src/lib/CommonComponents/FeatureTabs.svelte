<script>
  import { onMount } from "svelte";
  import hljs from "highlight.js";
  import "highlight.js/styles/github.css"; // You can change the theme here.

  // Define the tabs and the active tab
  let tabs = ["JavaScript", "Python", "Swift"];
  let activeTab = tabs[0]; // Default active tab is JavaScript

  // Sample code for each language
  const codeSnippets = [
    {
      language: "JavaScript",
      code: `import * as fal from "@fal-ai/serverless-client";

const result = await fal.subscribe("fal-ai/fast-sdxl", {
  input: {
    prompt: "photo of a cat wearing a kimono"
  },
  logs: true,
  onQueueUpdate: (update) => {
    if (update.status === "IN_PROGRESS") {
      update.logs.map((log) => log.message).forEach(console.log);
    }
  },
});`,
    },
    {
      language: "Python",
      code: `import fal_client

        handler = await fal_client.submit_async(
            "fal-ai/fast-sdxl",
        arguments={
            "prompt": "photo of a cat wearing a kimono"
        },
    )

    async for event in handler.iter_events(with_logs=True):
    if isinstance(event, fal_client.InProgress):
        print(event)

    result = await handler.get()`,
    },
    {
      language: "Swift",
      code: `import FalClient

let result = try await fal.subscribe(
    to: "fal-ai/fast-sdxl",
    input: [
        "prompt": "photo of a cat wearing a kimono"
    ],
    includeLogs: true
) { update in
    if case let .inProgress(logs) = update {
        print(logs)
    }
}`,
    },
  ];

  let activeSnippet = codeSnippets.find(
    (snippet) => snippet.language === activeTab
  ).code;

  // Set the active tab
  function setActiveTab(tab) {
    activeTab = tab;

    console.log(activeTab);
    // Update the active snippet based on the active tab
    activeSnippet = codeSnippets.find(
      (snippet) => snippet.language === activeTab
    ).code;
    // Re-highlight the code after switching tabs
    highlightCode();
  }

  // Function to highlight code using highlight.js
  //   function highlightCode() {
  //     const codeBlock = document.querySelector("pre code");
  //     hljs.highlightElement(codeBlock);
  //   }

  // Highlight code initially when the component mounts
  onMount(() => {
    highlightCode();
  });
</script>

<!-- Tabs -->
<div class="inline-flex w-fit p-0.5 border bg-gray-200">
  {#each tabs as tab}
    <button
      class="px-4 py-2 text-xs font-bold rounded-sm transition duration-150 ease-in-out {activeTab ===
      tab
        ? 'bg-purple-600 text-white'
        : 'text-gray-700'}"
      on:click={() => setActiveTab(tab)}
    >
      {tab}
    </button>
  {/each}
</div>

<!-- Code snippet display -->
<div
  class="mt-2 p-5 h-full bg-white border border-gray-300 text-sm overflow-y-auto"
>
  <pre>
<code class="{activeTab} text-wrap">{activeSnippet}</code>
</pre>
</div>
