<script>
  let images = [
    "/bridegallerypinkmarble.png",
    "/bridegallerypinkmarble.png",
    "/bridegallerypinkmarble.png",
    "/bridegallerypinkmarble.png",
    "/bridegallerypinkmarble.png",
    "/bridegallerypinkmarble.png",
  ];
</script>

<section>
  <div class="bg-[url('/giftbgpinkmarble.png')] bg-cover max-w-2xl mx-auto px-4">
    <!-- Judul -->
    <h2 class="text-left text-5xl pl-6 py-10 font-[Great_Vibes] text-[#6b0f1a]">
      Our Story In Gallery
    </h2>

    <!-- Video Cover -->
    <div class="rounded-xl overflow-hidden shadow-lg relative mb-8 aspect-video">
      <img
        src="/briderectangle.png"
        alt="Cover"
        class="w-full h-full object-cover"
      />
      <!-- Tombol Play -->
      <div class="absolute inset-0 flex items-center justify-center">
        <div class="bg-white rounded-full p-3 shadow-md">
          <svg
            xmlns="http://www.w3.org/2000/svg"
            class="h-8 w-8 text-pink-500"
            fill="currentColor"
            viewBox="0 0 24 24"
          >
            <path d="M8 5v14l11-7z" />
          </svg>
        </div>
      </div>
    </div>

    <!-- Grid Gallery -->
    <div class="grid grid-cols-3 gap-3">
      {#each images as img}
        <div class="rounded-xl overflow-hidden shadow-md">
          <img
            src={img}
            alt="Gallery"
            class="w-full h-full object-cover"
          />
        </div>
      {/each}
    </div>
  </div>
</section>

<style>
  @import url('https://fonts.googleapis.com/css2?family=Great+Vibes&display=swap');
</style>
