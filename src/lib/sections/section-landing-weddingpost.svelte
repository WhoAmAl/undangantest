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

<div class="w-full md:max-w-2xl mx-auto bg-[#dcdcdc] md:border md:border-black md:rounded-none md:px-4" style="font-family: 'Times New Roman', Times, serif;">

    <!-- Header Koran -->
    <div class="px-4 pt-3 text-center font-serif">
      <p class="uppercase text-[14px] md:text-[24px] tracking-widest">THE BIGGEST WEDDING OF THE YEAR</p>
      <hr class="border-black border-[1.5px]" />
      <p class="text-[14px] md:text-[24px]">12 Juni 2025</p>
      <hr class="border-black border-[1.5px]" />
      <h1 class="text-[25px] md:text-[46px]" style="font-family: 'Fleischman', serif;">THE WEDDING TIMES</h1>
      <hr class="border-black border-t-2" />
      <hr class="border-black border-t-[1.5px] mt-0.5" />
    </div>

    <!-- Gambar + Overlay -->
    <div class="relative w-full p-4 md:px-4 mt-2">
      <img src="/landing.png" alt="Wedding Image" class="w-full object-cover" />

      <!-- Overlay -->
      <div class="absolute inset-0 flex flex-col justify-end text-white font-serif px-6 pb-6 md:rounded-md rounded-md">
        <h2 class="text-center text-[24px] md:text-[36px] tracking-wide mb-2">HINATA &amp; NARUTO</h2>

        <!-- Garis hiasan -->
        <div class="border-t-[3px] border-white mb-[2px]"></div>
        <div class="border-t-[2px] border-white mb-2"></div>

        <!-- Undangan -->
        <div class="flex justify-between text-[12px] md:text-[18px] px-10 md:px-35">
          <span>Dear</span>
          <span>Alan and Partner</span>
        </div>

        <div class="border-t-[2px] border-white mt-2 mb-[2px]"></div>
        <div class="border-t-[3px] border-white mb-4"></div>

        <!-- Tombol -->
        <div class="flex justify-center">
          <button
            on:click={handleRedirect}
            class="mb-10 bg-white border text-black border-white rounded-lg md:rounded-2xl px-3 md:px-6 py-1 md:py-2 text-sm shadow-sm hover:bg-gray-200 transition-all duration-200"
          >
            Open Invitation
          </button>
        </div>
      </div>
    </div>
</div>
