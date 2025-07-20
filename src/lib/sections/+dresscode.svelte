<script>
  const dontUseItems = [
    "Pakaian berwarna Gold",
    "Kaos Oblong",
    "Short Pants",
    "Sendal Jepit"
  ];
</script>

<div class="bg-gray-200 px-4 mx-auto max-w-2xl text-center border-x border-black p-4">
  <div class="border-t-4 border-black mb-0.5"></div>
    <div class="border-t-3 border-black mb-1"></div>
    <h1 class="text-4xl font-bold tracking-widest">DRESSCODE</h1>
  <div class="border-b-3 border-black mt-1"></div>
    <div class="border-b-4 border-black mt-0.5 mb-6"></div>

  <p class="italic text-left text-sm md:text-base mt-4 pl-6">
    Kami harap Anda dapat mengenakan apa pun yang Anda suka. Jika Anda memiliki permintaan khusus, silakan beritahu kami.
  </p>

  <div class="mt-10 flex flex-col md:flex-row items-center justify-center gap-12">
    <div class="text-center scale-120">
      <h2 class="text-sm font-semibold mb-3">Color Recommendation</h2>
      <div class="flex items-center justify-center gap-4">
        <div class="w-8 h-8 rounded-full bg-gray-300"></div>
        <div class="w-8 h-8 rounded-full bg-black"></div>
        <div class="w-8 h-8 rounded-full bg-gray-500"></div>
      </div>
    </div>

    <div class="border-l-3 border-black h-16 hidden md:block"></div>

    <div class="ml-10 text-center items-center scale-120">
      <h2 class="text-sm font-semibold mb-3">Theme Recommendation</h2>
      <div class="flex gap-4 justify-center">
        <img src="/women.png" alt="White Theme" class="w-20 h-24 object-cover rounded" />
        <img src="/men.png" alt="Black Theme" class="w-20 h-24 object-cover rounded" />
      </div>
    </div>
  </div>

  <div class="border-t-3 border-black mt-10 pt-0.5">
    <div class="border-t-4 border-black pt-6"></div>
    <h2 class="font-semibold text-lg mb-4">Don’t Use</h2>
    <div class="flex flex-wrap justify-center gap-4">
      {#each dontUseItems as item}
        <div class="bg-black text-white px-4 py-2 rounded-full text-sm">
          {item}
        </div>
      {/each}
    </div>
  </div>

  <div class="border-t-3 border-black mt-10"></div>
  <div class="border-t-4 border-black mt-0.5"></div>
</div>

<style>
  /* You can place this in a global stylesheet or use Tailwind's plugin for custom font if needed */
  @import url('https://fonts.googleapis.com/css2?family=Playfair+Display:wght@400;700&display=swap');

  .font-serif {
    font-family: 'Playfair Display', serif;
  }
</style>
