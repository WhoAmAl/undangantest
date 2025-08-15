<script>
  import Marquee from "../Marquee.svelte";

  function handleRedirect() {
  window.location.href = "/cleanelegance";
  }
</script>

<div class="bg-neutral-50 w-full overflow-hidden py-5 text-yellow-950" style="font-family: 'Cormorant Garamond Regular', serif;">
  <Marquee pauseOnHover>
    <div class="text-2xl pl-15" style="font-family: 'Cinzel', serif;">THE WEDDING OF</div>
  </Marquee>
  <div class="flex flex-col items-center justify-center mb-5">
    <div class="flex justify-center mt-3 px-8 max-h-[880px] overflow-hidden">
      <img src="/bgcovercleanelegance.png" alt="Bride" class="h-full w-full shadow-lg" />
    </div>
    <h1 class="text-4xl mt-12" style="font-family: 'Tangerine Regular', serif;">Dear,</h1>
    <h2 class="text-xl">Alan and Partner</h2>
    <button class="mt-8 px-6 py-2 bg-yellow-950 text-neutral-50 transition" on:click={handleRedirect}>OPEN INVITATION</button>
  </div>
</div>