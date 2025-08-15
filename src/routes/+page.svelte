<script lang="ts">
  import Sidebar from '$lib/components/ui/sidebar/sidebar.svelte';
  import { landingpages } from '$lib/landingpages.js';
  import { onMount } from 'svelte';

  let components: any[] = [];

  onMount(async () => {
    components = await Promise.all(
      landingpages.map(lp => lp.component().then(mod => mod.default))
    );
  });
</script>

<main class="flex min-h-screen">
  <Sidebar />
  <div class="flex flex-1 items-center justify-center">
    <div class="max-w-2xl w-full">
      {#each components as Comp, i}
        <svelte:component this={Comp} />
      {/each}
    </div>
  </div>
</main>