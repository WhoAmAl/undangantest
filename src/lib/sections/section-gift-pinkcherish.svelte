<script>
  import { ScrollArea } from "$lib/components/ui/scroll-area/index.js";
  let wishes = [
    { name: "Sendvitation", message: "Selamat ya, bahagia selalu" },
    { name: "Sendvitation2", message: "Semoga pernikahan kalian selalu penuh cinta dan berkah" },
    { name: "DindaSaputra", message: "Turut berbahagia! Semoga langgeng dan selalu rukun" },
    { name: "RamaYusuf", message: "Congratulations! Wishing you a lifetime of happiness together." },
    { name: "TamuUndangan123", message: "Selamat menempuh hidup baru 🎉" },
    { name: "NinaM", message: "Lorem ipsum dolor sit amet, consectetur adipiscing elit." },
    { name: "FikriAF", message: "Vivamus luctus urna sed urna ultricies ac tempor dui sagittis." },
    { name: "GuestA", message: "Doa terbaik untuk kalian berdua. Semoga bahagia hingga akhir hayat." },
    { name: "GuestB", message: "May your journey ahead be filled with love and laughter ❤️" },
    { name: "DewiAnggraini", message: "Semoga jadi keluarga yang sakinah, mawaddah, warahmah." },
    { name: "BayuSetiawan", message: "Lorem ipsum dolor sit amet, happy wedding pokoknya!" },
    { name: "Sendvitation3", message: "Best wishes! ❤️💍🎉" },
    { name: "AnantaRey", message: "Semoga cepat diberi momongan yaa 😄" },
    { name: "Hamba Allah", message: "Selamat ya, semoga lancar sampai hari H!" },
    { name: "TamuVirtual", message: "Nullam ut metus id sapien dictum hendrerit nec nec elit." }
  ];
</script>
<div class="bg-[#FECACA] flex flex-col max-w-2xl mx-auto min-h-[1195px]">
  <!-- HEADER SECTION -->
  <div class="bg-[#500724]">
    <h2 class="text-white text-2xl md:text-5xl italic py-3 sm:py-6 font-bold text-center"  style="font-family: 'Bodoni Moda', serif;">-Gift & Wish-</h2>
  </div>

  <!-- Subheader -->
  <div class="py-6 px-4 text-center">
    <p class="italic text-[12px] sm:text-lg text-[#500724]" style="font-family: 'Justink', serif;">
      If you would like to give a gift as a symbol of blessing and support for our household journey, some of the following options may be helpful
    </p>
  </div>

  <!-- Gift & Cashless Section -->
  <div class="flex flex-col md:flex-row justify-center items-stretch gap-8 px-4 py-6 bg-[#9D174D]">
    <!-- Cashless -->
    <div class="flex-1 flex flex-col items-center md:border-r md:border-[#FECACA] md:pr-4 md:mb-0 mb-8">
      <h3 class="text-white text-2xl mb-4" style="font-family: 'Bodoni Moda', serif;">Cashless</h3>
      <!-- BCA Hinata -->
      <div class="flex flex-col items-center mb-6">
        <img src="/BCA.png" alt="BCA" class="h-8 mb-2" />
        <span class="italic text-white text-lg" style="font-family: 'Justink', serif;">Hinata</span>
        <span class="text-white text-xl" style="font-family: 'Justink', serif;">123456789</span>
        <button class="mt-2 px-4 py-1 rounded-full bg-[#FECACA] text-[#500724] font-semibold shadow-md hover:bg-[#fbb6ce] transition" style="font-family: 'Bodoni Moda', serif;">
          Copy to clipboard
        </button>
      </div>
      <!-- BCA Naruto -->
      <div class="flex flex-col items-center">
        <img src="/BCA.png" alt="BCA" class="h-8 mb-2" />
        <span class="italic text-white text-lg" style="font-family: 'Justink', serif;">Naruto</span>
        <span class="text-white text-xl" style="font-family: 'Justink', serif;">123456789</span>
        <button class="mt-2 px-4 py-1 rounded-full bg-[#FECACA] text-[#500724] font-semibold shadow-md hover:bg-[#fbb6ce] transition" style="font-family: 'Bodoni Moda', serif;">
          Copy to clipboard
        </button>
      </div>
    </div>
    <!-- Gift -->
    <div class="flex-1 flex flex-col items-center sm:justify-center md:pl-4">
      <h3 class="text-white text-2xl mb-4" style="font-family: 'Bodoni Moda', serif;">Gift</h3>
      <p class="text-white text-xl font-serif italic text-center mb-4">
        <span style="font-family: 'Justink', serif;">Orchid Streat Number 15,<br />
        West Jakarta</span>
      </p>
      <button class="px-4 py-1 rounded-full bg-[#FECACA] text-[#500724] font-serif font-semibold shadow-md hover:bg-[#fbb6ce] transition">
        <span style="font-family: 'Bodoni Moda', serif;">Copy address</span>
      </button>
    </div>
  </div>

  <!-- Wish Form -->
  <div class="bg-[#FECACA] px-8 py-8">
    <p class="italic text-lg text-[#500724] font-serif mb-4">
      <span style="font-family: 'Justink', serif;">Give us your best wish for our wedding</span>
    </p>
    <form class="flex flex-col gap-4">
      <div class="flex flex-col md:flex-row md:items-center gap-2">
        <label class="font-serif text-xl text-[#500724] md:w-1/3 mb-1 md:mb-0">Nama Pengirim</label>
        <input type="text" placeholder="Nama Tamu" class="rounded-lg px-4 py-2 bg-[#C77990] text-white font-serif placeholder-white focus:outline-none md:w-2/3" />
      </div>
      <div class="flex flex-col md:flex-row gap-2">
        <label class="font-serif text-xl text-[#500724] md:w-1/3 mb-1 md:mb-0">Message</label>
        <textarea rows="4" placeholder="Kirim Ucapan" class="rounded-lg px-4 py-2 bg-[#C77990] text-white font-serif placeholder-white focus:outline-none md:w-2/3"></textarea>
      </div>
      <button type="submit" class="self-end mt-2 px-8 sm:px-16 py-2 rounded-2xl bg-[#500724] text-white font-serif shadow-md hover:bg-[#8B1C4A] transition">
        Kirim
      </button>
    </form>
  </div>

  <!-- Divider -->
  <div class="px-8">
    <hr class="border-t-2 border-[#8B1C4A] my-6" />
  </div>

  <!-- Wish List Scroll Area -->
  <div class="px-8 pb-8">
    <ScrollArea class="h-[200px] w-full rounded-md bg-[#FECACA]" orientation="both">
      {#each wishes as wish}
        <div class="mb-4 text-left">
          <h4 class="font-serif text-xl text-[#500724]">{wish.name}</h4>
          <p class="italic text-[#500724]">{wish.message}</p>
        </div>
      {/each}
    </ScrollArea>
  </div>
</div>