<script>
  const time = {
    days: 10,
    hours: 20,
    minutes: 18,
    seconds: 6,
  };
</script>

<main class="bg-gray-200 text-black font-serif flex justify-center">
  <div class="w-full max-w-2xl bg-gray-200 text-center border-x border-black p-4">
    <!-- Tanggal -->
    <div class="text-sm mb-2">12 Juni 2025</div>

    <!-- Double Border Header -->
    <div class="border-t-4 border-black mb-0.5"></div>
    <div class="border-t-3 border-black mb-1"></div>
    <h1 class="text-4xl font-bold tracking-widest">THE WEDDING POST</h1>
    <div class="border-b-3 border-black mt-1"></div>
    <div class="border-b-4 border-black mt-0.5 mb-6"></div>

    <!-- Baris nama tamu -->
    <div class="flex justify-between text-sm mt-2 mb-4 px-30">
      <span>Dear</span>
      <span>Alan and Partner</span>
    </div>

    <!-- Gambar dan Overlay -->
    <div class="relative">
      <img src="/opening.png" alt="Wedding Couple" class="w-full h-auto object-cover object-center" />
      <div class="absolute inset-0 bg-opacity-50 flex flex-col justify-end items-center pb-8 text-white">
        <!-- Nama pasangan -->
        <h2 class="text-xl md:text-2xl mb-4">HINATA &amp; NARUTO</h2>

        <!-- Countdown -->
        <div class="flex space-x-6 text-center">
          <div>
            <div class="text-xl md:text-2xl">{time.days}</div>
            <div class="italic text-sm">Days</div>
          </div>
          <div>
            <div class="text-xl md:text-2xl">{time.hours}</div>
            <div class="italic text-sm">Hours</div>
          </div>
          <div>
            <div class="text-xl md:text-2xl">{time.minutes}</div>
            <div class="italic text-sm">Minutes</div>
          </div>
          <div>
            <div class="text-xl md:text-2xl">{time.seconds}</div>
            <div class="italic text-sm">Seconds</div>
          </div>
        </div>
      </div>
    </div>
  </div>
</main>
