<script>
    import { goto } from '$app/navigation';
    function handleRedirect() {
        goto('/violetvintage');
    }
</script>

<div class="bg-white min-h-screen flex items-center justify-center px-0 py-0">
  <div class="w-full md:max-w-[460px] bg-[#f7f5f2] md:border md:border-[#4B217A] md:rounded-none relative flex flex-col items-center justify-center" style="height: 820px; padding:0;">

    <!-- Ornamen Atas & Bawah -->
    <img src="/covertopvioletvintage.png" alt="Ornament Top Left" class="absolute top-0 left-0 z-10 h-[90px] w-auto object-contain pointer-events-none" />
    <img src="/covertopvioletvintage.png" alt="Ornament Top Right" class="absolute top-0 right-0 z-10 h-[90px] w-auto object-contain transform scale-x-[-1] pointer-events-none" />
    <img src="/coverbottomvioletvintage.png" alt="Ornament Bottom Left" class="absolute bottom-0 left-0 z-10 h-[90px] w-auto object-contain pointer-events-none" />
    <img src="/coverbottomvioletvintage.png" alt="Ornament Bottom Right" class="absolute bottom-0 right-0 z-10 h-[90px] w-auto object-contain transform scale-x-[-1] pointer-events-none" />

    <!-- Konten utama -->
    <div class="flex flex-col items-center justify-center absolute left-1/2 top-1/2 -translate-x-1/2 -translate-y-1/2 w-[85%] bg-[#f7f5f2] border-2 border-[#4B217A] rounded-xl shadow-lg py-8 px-4 text-center" style="min-height: 340px;">
      <h2 class="text-2xl sm:text-3xl font-serif text-[#4B217A] mb-6">PLEASE JOIN US !</h2>
      <div class="text-2xl sm:text-3xl font-serif text-[#4B217A] mb-6">
        HINATA<br />
        <span class="text-xl sm:text-2xl">&</span><br />
        NARUTO
      </div>
      <div class="text-base text-[#4B217A] mb-2">12 Juni 2025</div>
    </div>

    <!-- Tombol -->
    <div class="absolute left-1/2 -translate-x-1/2 bottom-[90px] flex justify-center">
      <button
        class="bg-[#4B217A] text-white rounded-2xl px-6 py-2 text-sm shadow-lg font-medium transition hover:bg-[#6d3bbd]"
        on:click={handleRedirect}
      >
        Open Invitation
      </button>
    </div>
  </div>
</div>