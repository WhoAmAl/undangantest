<script>
  function joinInstagram() {
    window.open('https://instagram.com/hinata_hyuga', '_blank');
  }
</script>

<style>
  @import url('https://fonts.googleapis.com/css2?family=Great+Vibes&family=Playfair+Display:wght@500&display=swap');
</style>

<div class="bg-cover bg-center flex flex-col items-center justify-start text-center">
  <div
    class="max-w-2xl w-full flex flex-col items-center space-y-6 text-[#611717] px-6 md:px-10 py-12"
    style="background-image: url('/giftbgpinkmarble.png');"
  >
    <!-- Judul -->
    <h2 class="text-3xl md:text-4xl text-[#611717] font-[Great_Vibes] mb-6">
      Live Stream
    </h2>

    <p class="text-xl text-[#611717]">
      Distance won't keep us apart on our special day. We've <br class="hidden md:block" />
      arranged a live stream so that all our loved ones can witness <br class="hidden md:block" />
      our joy, no matter where you are.
    </p>

    <!-- Grid dengan Sekat -->
    <div class="relative grid md:grid-cols-2 gap-8 items-center justify-center text-[#611717] w-full max-w-md md:max-w-full">
      <!-- Instagram -->
      <div class="flex flex-col items-center">
        <img src="/instagram.png" alt="Instagram" class="w-10 h-10 mb-2" />
        <p class="text-[#881337] text-md font-semibold">@hinata_hyuga</p>
        <button
          on:click={joinInstagram}
          class="mt-3 px-5 py-1.5 bg-pink-100 text-[#BE123C] text-sm rounded-full shadow hover:bg-pink-200 transition"
        >
          Join Live Streaming
        </button>
      </div>

      <!-- Sekat vertikal -->
      <div class="hidden md:block absolute top-0 bottom-0 w-px bg-[#9D174D] left-1/2 -translate-x-1/2"></div>

      <!-- Zoom -->
      <div class="flex flex-col items-center">
        <img src="/zoom.png" alt="Zoom" class="w-10 h-10 mb-2" />
        <p class="text-md">ID Meeting : <span class="font-semibold">123456789</span></p>
        <p class="text-md">Password : <span class="font-semibold">hariBahagia</span></p>
      </div>
    </div>
  </div>
</div>
