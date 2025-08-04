<script>
  function handleRedirect() {
    window.location.href = '/pinkcherish';
  }
</script>

<div class="relative max-w-2xl mx-auto w-full min-h-screen flex flex-col justify-between items-center bg-[#9D174D]" on:click={handleRedirect}>
  <!-- Header -->
  <div class="w-full pt-4 md:pt-8 pb-4 text-center">
    <h1 class="text-gray-50 text-xl md:text-4xl font-serif italic tracking-wide">We're Getting Married</h1>
  </div>

  <!-- Main Image + Date Bar Overlay -->
  <div class="relative flex-1 w-full flex justify-center items-center">
    <img src="/coverpinkcherish.jpg" alt="Wedding Couple" class="object-cover w-full max-h-[72vh] md:max-h-[80vh] rounded-none shadow-lg" />
    <!-- Date Bar Overlay -->
    <div class="absolute bottom-2 left-0 w-full flex justify-center items-center py-1 md:py-2 bg-[#FECACA] bg-opacity-95">
      <span class="text-[#0A0A0A] text-[13px] md:text-xl font-serif italic">12 July 2025</span>
    </div>
  </div>

  <!-- Footer -->
  <div class="w-full pb-8 pt-4 text-center">
    <h2 class="text-white text-xl md:text-4xl font-serif italic font-semibold tracking-wide my-5">Hinata &amp; Naruto</h2>
  </div>
</div>
