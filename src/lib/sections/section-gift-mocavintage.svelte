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


<div class="bg-orange-100 min-h-screen flex flex-col items-center pt-8 px-5 md:px-16 font-serif max-w-2xl mx-auto">
  <h1 class="text-4xl md:text-5xl text-center text-yellow-950 opacity-80 mb-10" style="font-family: 'Fleischman', serif;">GIFT & WISH</h1>
  <p class="text-xl text-center text-yellow-950 opacity-80 mb-8" style="font-family: 'Foglihten', serif;">
    If you would like to give a gift as a symbol of blessing and support for our household journey, some of the following options may be helpful
  </p>
  <!-- SECTION GIFTS -->
  <div class="relative w-full flex md:flex-row flex-col justify-center items-stretch mb-6" style="min-height: 1px;">
    <div class="absolute left-1/2 top-0 h-full md:border-l-3 border-yellow-950 opacity-80" style="transform: translateX(-50%);"></div>
    <div class="flex-1 flex flex-col items-center border-t-3 md:border-b-3 border-yellow-950 py-6">
      <h2 class="text-2xl font-serif text-lime-800 opacity-85 mb-2" style="font-family: 'Libre Caslon', serif;">Cashless</h2>
      <div class="flex flex-col items-center mb-6">
        <img src="/BCA.png" alt="BCA" class="w-20 mb-2" />
        <div class="text-lg font-serif text-yellow-950 opacity-80" style="font-family: 'Foglihten', serif;">Hinata</div>
        <div class="text-base font-serif text-yellow-950 opacity-80 mb-2" style="font-family: 'Foglihten', serif;">123456789</div>
        <button class="bg-yellow-950 opacity-80 text-orange-100 px-6 py-1 rounded-full shadow-lg font-serif text-base" style="box-shadow: 2px 4px 10px #a48c74;font-family: 'Foglihten', serif;" on:click={() => navigator.clipboard.writeText('123456789')}>Copy to clipboard</button>
      </div>
      <div class="flex flex-col items-center">
        <img src="/BCA.png" alt="BCA" class="w-20 mb-2" />
        <div class="text-lg font-serif text-yellow-950 opacity-80" style="font-family: 'Foglihten', serif;">Naruto</div>
        <div class="text-base font-serif text-yellow-950 opacity-80 mb-2" style="font-family: 'Foglihten', serif;">123456789</div>
        <button class="bg-yellow-950 opacity-80 text-orange-100 px-6 py-1 rounded-full shadow-lg font-serif text-base" style="box-shadow: 2px 4px 10px #a48c74;font-family: 'Foglihten', serif;" on:click={() => navigator.clipboard.writeText('123456789')}>Copy to clipboard</button>
      </div>
    </div>
    <div class="flex-1 flex flex-col items-center border-t-3 border-b-3 border-yellow-950 py-6">
      <h2 class="text-2xl font-serif text-lime-800 opacity-85 mb-5" style="font-family: 'Libre Caslon', serif;">Gift</h2>
      <div class="text-lg font-serif text-yellow-950 opacity-80 text-center mb-6 px-3" style="font-family: 'Foglihten', serif;">Orchid Streat Number 15, West Jakarta</div>
      <button class="bg-yellow-950 opacity-80 text-orange-100 px-9 py-1 rounded-full shadow-lg font-serif text-base" style="box-shadow: 2px 4px 10px #a48c74;font-family: 'Foglihten', serif;" on:click={() => navigator.clipboard.writeText('Orchid Streat Number 15, West Jakarta')}>Copy address</button>
    </div>
  </div>
  <!-- SECTION WISHES -->
  <div class="w-full mb-6">
    <div class="text-yellow-950 opacity-80 mb-2" style="font-family: 'Foglihten', serif;">Give us your best wish for our wedding</div>
    <form class="flex flex-col gap-4">
      <div class="flex flex-col md:flex-row items-start md:items-center gap-1 md:gap-4">
        <label class="text-yellow-950 opacity-80 min-w-[140px] text-base" style="font-family: 'Foglihten', serif;">Nama Pengirim</label>
        <input type="text" placeholder="Nama Tamu" class="flex-1 px-4 w-full py-2 rounded-2xl bg-yellow-950 opacity-30 text-orange-100 placeholder:text-orange-100" />
      </div>
      <div class="flex flex-col md:flex-row items-start gap-1 md:gap-4">
        <label class="text-yellow-950 opacity-80 min-w-[140px] text-base" style="font-family: 'Foglihten', serif;">Message</label>
        <textarea placeholder="Kirim Ucapan" class="flex-1 px-4 py-2 w-full rounded-2xl bg-yellow-950 opacity-30 text-orange-100 placeholder:text-orange-100 md:h-24"></textarea>
      </div>
      <div class="flex justify-end">
        <button type="submit" class="bg-yellow-950 opacity-80 text-orange-100 px-14 py-1 rounded-full shadow-md" style="font-family: 'Libre Caslon', serif;">Kirim</button>
      </div>
    </form>
  </div>
  <div class="w-full border-t-3 border-yellow-950 opacity-80 pt-4">
    <div class="flex flex-col gap-2">
        <ScrollArea class="h-[200px] w-full rounded-md" orientation="both">
            {#each wishes as wish}
            <div class="mb-4 text-left">
                <h4 class="text-xl text-lime-800" style="font-family: 'Libre Caslon', serif;">{wish.name}</h4>
                <p class="text-yellow-950" style="font-family: 'Foglihten', serif;">{wish.message}</p>
            </div>
            {/each}
        </ScrollArea>
    </div>
  </div>
</div>