<script>
  function handleRedirect() {
    window.location.href = '/mocavintage';
  }
</script>

<div class="bg-orange-100 min-h-screen max-w-2xl mx-auto flex items-center justify-center relative overflow-hidden" style="font-family: serif;">
  <img src="/landingmocavintage.png" alt="" class="absolute inset-0 w-full h-full object-cover max-h-[580px] md:max-h-[1024px] pb-12 rounded-b-[18%] md:rounded-b-[145px] z-0 select-none pointer-events-none" draggable="false">
  <div class="absolute top-0 left-0 w-full h-full flex flex-col justify-between items-center z-10">
    <div class="w-full flex flex-col items-center pt-8">
      <div class="text-[16px] md:text-[30px] tracking-widest text-yellow-950 opacity-[80%] md:mb-2" style="font-family: 'Fleischman', serif;">04|08|2025</div>
      <div class="text-[26px] md:text-[45px] tracking-wide text-yellow-950 opacity-[80%] mb-2" style="font-family: 'Fleischman', serif;">HINATA &amp; NARUTO</div>
    </div>
    <div class="flex-1"></div>
    <div class="w-full flex flex-col items-center mb-8 md:mb-12">
      <div class="text-[22px] md:text-[35px] text-yellow-950 opacity-80 mb-3" style="font-family: 'Libre Caslon', serif;">We're Getting Married</div>
      <button class="bg-yellow-950 opacity-80 text-[#FFEDD5B2] text-[12px] md:text-[16px] px-2 py-1 rounded-[8px] md:rounded-lg shadow-md hover:scale-105 transition-all duration-150" style="font-family: 'Libre Caslon', serif;" onclick={handleRedirect}>Open Invitation</button>
    </div>
  </div>
</div>