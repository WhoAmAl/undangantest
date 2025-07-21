<script>
  import { goto } from '$app/navigation';

  function handleRedirect() {
    goto('/pinkmarble');
  }
</script>

<style>
  @import url('https://fonts.googleapis.com/css2?family=Playfair+Display:wght@500;700&family=Great+Vibes&display=swap');

  .font-script {
    font-family: 'Great Vibes', cursive;
  }
</style>

<!-- WRAPPER UTAMA agar card center horizontal dan vertical -->
<div class="min-h-screen flex items-center justify-center bg-white px-4 py-6">
  <!-- Card -->
  <div
    class="w-full md:max-w-[420px] bg-[#FFF1F2] flex items-center justify-center md:border md:border-black md:rounded-none min-h-screen md:px-4 md:py-10 px-0 py-0"
    style="background-image: url('/pinkmarblebg.png'); background-size: cover; background-position: center;"
  >
    <!-- Konten -->
    <div class="text-center text-[#781c3e] space-y-4 max-w-xl w-full">
      <p class="text-sm tracking-wide font-medium">We’re Getting Married</p>
      <h1 class="text-4xl font-script">Hinata</h1>
      <p class="text-lg font-medium">&</p>
      <h1 class="text-4xl font-script">Naruto</h1>
      <p class="text-sm italic font-light px-2">
        With a great joy, we are pleased to cordially invite you to our wedding
      </p>
      <div class="mt-6 space-y-1">
        <p class="text-sm font-semibold">Dear</p>
        <p class="text-base italic">Alan and Partner</p>
      </div>
      <div class="mt-4 mb-0">
        <button
          on:click={handleRedirect}
          class="bg-white text-[#781c3e] px-5 py-2 text-sm rounded-full shadow-md hover:bg-pink-100 transition-all duration-200"
        >
          Open Invitation
        </button>
      </div>
    </div>
  </div>
</div>
