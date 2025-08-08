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

<div class="bg-neutral-50 max-w-2xl mx-auto py-8 px-6 md:px-18" style="font-family: 'Questrial', serif;">
  <h2 class="text-4xl text-lime-950 mb-4 text-left" style="font-family: 'Rouge Script', serif;">Gift and Wish</h2>
  <p class="text-center text-[14px] md:text-[20px] text-lime-950 mb-8">
    If you would like to give a gift as a symbol of blessing and support for our household journey, some of the following options may be helpful
  </p>

  <div class="flex flex-col md:flex-row md:justify-center items-center mb-8 gap-3 md:gap-0">
    <div class="flex flex-col md:gap-8 px-8">
        <div class="flex flex-col items-center">
            <div>
                <img src="/creditcardblackskeleton.png" alt="Credit Card" class="w-12 h-12 object-contain" />
            </div>
            <div class="text-center mb-3">
                <div class="font-medium text-lime-950 ">BCA an Hinata</div>
                <div class="text-lime-950">123456789</div>
            </div>
            <button class="bg-lime-900 text-white rounded-full px-7 py-0.5">Copy to clipboard</button>
            </div>
            <div class="flex flex-col items-center">
                <div>
                    <img src="/creditcardblackskeleton.png" alt="Credit Card" class="w-12 h-12 object-contain" />
                </div>
                <div class="text-center mb-3">
                    <div class="font-medium text-lime-950">BNI an Naruto</div>
                    <div class="text-lime-950">123456789</div>
                </div>
            <button class="bg-lime-900 text-white rounded-full px-7 py-0.5">Copy to clipboard</button>
        </div>
    </div>
    <div class="flex flex-col items-center gap-1">
      <div class="font-medium text-lime-950 text-2xl">Gift</div>
      <p class="text-lime-950 text-center">Orchid Streat Number 15, West Jakarta</p>
      <button class="bg-lime-900 text-white rounded-full px-7 py-0.5 mt-2">Copy address</button>
    </div>
  </div>

  <div class="mt-8">
    <h3 class="text-[14px] md:text-[21.5px] text-lime-950 text-left mb-4">Give your best wish for us. We will so appreciate for that</h3>
    <!-- Form Submit -->
    <form class="flex flex-col gap-4 items-start w-full">
      <div class="flex flex-col md:flex-row itesm-start md:items-center gap-4 w-full">
        <label class="text-lime-950 text-base md:text-xl min-w-[140px]">Nama Pengirim</label>
        <input class="flex-1 rounded-xl bg-lime-900 opacity-45 px-6 py-2 text-white placeholder:text-white text-lg" type="text" placeholder="Nama Tamu" />
      </div>
      <div class="flex flex-col md:flex-row items-start gap-4 w-full">
        <label class="text-lime-950 text-base md:text-xl min-w-[140px]">Message</label>
        <textarea class="flex-1 rounded-xl bg-lime-900 opacity-45 px-6 py-2 text-white placeholder:text-white text-lg w-full" rows="4" placeholder="Kirim Ucapan"></textarea>
      </div>
      <button type="submit" class="bg-lime-900 text-white rounded-full px-12 py-1 mt-1 self-end">Kirim</button>
    </form>
  </div>

  <!-- WISHES LIST -->
  <div class="mt-8">
    <ScrollArea class="h-[250px] w-full rounded-md" orientation="both">
        {#each wishes as wish}
        <div class="mb-4 text-left">
            <h4 class="text-xl text-lime-800" style="font-family: 'Libre Caslon', serif;">{wish.name}</h4>
            <p class="text-yellow-950">{wish.message}</p>
        </div>
        {/each}
    </ScrollArea>
  </div>
</div>