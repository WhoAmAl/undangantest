<script>
    function handleRedirect() {
        window.location.href = "/retroclassic";
    }
</script>

<div class="bg-neutral-950 min-h-screen lg:min-h-[165vh] xl:min-h-screen flex flex-col items-center justify-between" style="background-image: url(/landingopeningretroclassic.png); background-size: cover; background-position: center; background-repeat: no-repeat; font-family: 'Jomolhari', serif;">
  <div class="w-full pt-8 px-6 lg:px-10 text-center">
    <div class="text-neutral-50 text-base lg:text-xl tracking-widest mb-1 lg:mb-2" style="font-family: 'Jomolhari', serif;">THE</div>
    <div class="text-neutral-50 text-4xl lg:text-7xl tracking-[0.2em] mb-2" style="font-family: 'Jomolhari', serif;">WEDDING</div>
    <div class="border-t-3 border-white w-full my-2"></div>
    <div class="flex justify-between text-neutral-50 text-[14px] lg:text-xl" style="font-family: 'Jomolhari', serif;">
      <span>DEAR</span>
      <span>ALAN &amp; PARTNER</span>
    </div>
  </div>
  <div class="flex-1 flex flex-col items-center translate-y-3/24">
    <div class="text-neutral-50 text-2xl md:text-3xl tracking-[0.5em] mb-4" style="font-family: 'Jomolhari', serif;">HINATA</div>
    <div class="text-neutral-50 text-4xl md:text-5xl mb-4" style="font-family: 'Jomolhari', serif;">&amp;</div>
    <div class="text-neutral-50 text-2xl md:text-3xl tracking-[0.5em] mb-4" style="font-family: 'Jomolhari', serif;">NARUTO</div>
  </div>
  <div class="pb-25">
    <button class="mt-15 md:mt-25 bg-neutral-50 text-neutral-950 rounded-md md:rounded-xl px-3 md:px-5 py-1 md:py-2 text-[12px] md:text-base shadow-lg hover:bg-neutral-100 transition" style="font-family: 'Baskervville Regular', serif;" on:click={handleRedirect}>Open Invitation</button>
  </div>
</div>