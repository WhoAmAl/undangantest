<script>
  import { goto } from '$app/navigation';

  function handleRedirect() {
    goto('/weddingpost');
  }
</script>

<style>
  @import url('https://fonts.googleapis.com/css2?family=Playfair+Display:wght@500;700&display=swap');
  .font-playfair {
    font-family: 'Playfair Display', serif;
  }
</style>

<!-- Warna latar di luar box hanya aktif di md ke atas -->
<!-- <div class="bg-black min-h-screen flex items-center justify-center md:px-4 md:py-10 px-0 py-0"> -->
  <div class="w-full md:max-w-2xl mx-auto bg-[#dcdcdc] md:border md:border-black md:rounded-none px-4">

    <!-- Header Koran -->
    <div class="px-4 pt-3 text-center font-serif">
      <p class="uppercase text-[24px] tracking-widest">THE BIGGEST WEDDING OF THE YEAR</p>
      <hr class="border-black border-[1.5px]" />
      <p class="text-[24px]">12 Juni 2025</p>
      <hr class="border-black border-[1.5px]" />
      <h1 class="md:text-[46px]" style="font-family: 'Fleischman', serif;">THE WEDDING TIMES</h1>
      <hr class="border-black border-t-2" />
      <hr class="border-black border-t-[1.5px] mt-0.5" />
    </div>

    <!-- Gambar + Overlay -->
    <div class="relative w-full p-4 md:px-4 mt-2">
      <img src="/landing.png" alt="Wedding Image" class="w-full object-cover" />

      <!-- Overlay -->
      <div class="absolute inset-0 flex flex-col justify-end text-white font-serif px-6 pb-6 md:rounded-md rounded-md">
        <h2 class="text-center text-[36px] tracking-wide mb-2">HINATA &amp; NARUTO</h2>

        <!-- Garis hiasan -->
        <div class="border-t-[3px] border-white mb-[2px]"></div>
        <div class="border-t-[2px] border-white mb-2"></div>

        <!-- Undangan -->
        <div class="flex justify-between text-[18px] px-35">
          <span>Dear</span>
          <span>Alan and Partner</span>
        </div>

        <div class="border-t-[2px] border-white mt-2 mb-[2px]"></div>
        <div class="border-t-[3px] border-white mb-4"></div>

        <!-- Tombol -->
        <div class="flex justify-center">
          <button
            on:click={handleRedirect}
            class="mb-10 bg-white border text-black border-white rounded-2xl px-6 py-2 text-sm shadow-sm hover:bg-gray-200 transition-all duration-200"
          >
            Open Invitation
          </button>
        </div>
      </div>
    </div>
  </div>
<!-- </div> -->
