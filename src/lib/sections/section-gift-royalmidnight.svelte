<script lang="ts">
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
<!-- <div class="max-w-2xl mx-auto min-h-screen relative flex flex-col items-center px-2 sm:px-0"> -->
<div class="     max-w-2xl mx-auto min-h-screen relative flex flex-col items-center px-6 sm:px-15" style="background-image: url('/backgroundopeningroyalmidnight.png'); background-size: cover; background-repeat: no-repeat;">
    <!-- CARD CONTENT -->
    <div class="bg-transparant rounded-[10px] sm:rounded-[20px] shadow-2xl w-full min-h-screen sm:min-h-[900px] h-full flex flex-col items-center justify-between py-2.5 px-3 sm:py-4 sm:px-4 border-x-8 sm:border-x-16 border-y-14 sm:border-y-25 border-[#172554] my-10">
        <div class="bg-[#172554] rounded-[10px] sm:rounded-[20px] shadow-2xl w-full h-full flex flex-col items-centersm:py-8 sm:px-4 border-x-16 border-y-25 border-[#172554]">
        <!-- Title -->
        <h2 class="text-white text-[12px] sm:text-4xl font-serif tracking-[0.3em] text-center mb-4">GIFT AND WISH</h2>
        <!-- Subtitle -->
        <p class="text-white md:px-4 text-[9px] sm:text-lg font-serif text-center mb-6 max-w-md">If you would like to give a gift as a symbol of blessing and support for our household journey, some of the following options may be helpful</p>
        <!-- Cashless -->
        <div class="w-full flex flex-col items-center justify-center sm:mb-4">
            <span class="text-white text-[10px] sm:text-xl font-serif mb-2">Cashless</span>
            <div class="flex flex-row justify-center gap-8 w-full mb-2">
            <!-- BCA 1 -->
            <div class="flex flex-col items-center scale-90 sm:scale-105 gap-0">
                <img src="/BCA.png" alt="BCA" class="h-5 sm:h-10 mb-0.5" />
                <span class="text-white font-serif text-[8px] sm:text-xs -mt-1">Hinata</span>
                <span class="text-white font-mono text-[8px] sm:text-xs">123456789</span>
                <button class="mt-1 px-2 py-0.5 bg-white rounded-full shadow text-[#172554] text-[8px] sm:text-xs font-serif hover:bg-gray-200 transition min-w-[70px]">Copy to clipboard</button>
            </div>
            <!-- BCA 2 -->
            <div class="flex flex-col items-center scale-90 sm:scale-105 gap-0">
                <img src="/BCA.png" alt="BCA" class="h-5 sm:h-10 mb-0.5" />
                <span class="text-white font-serif text-[8px] sm:text-xs -mt-1">Naruto</span>
                <span class="text-white font-mono text-[8px] sm:text-xs">123456789</span>
                <button class="mt-1 px-2 py-0.5 bg-white rounded-full shadow text-[#172554] text-[8px] sm:text-xs font-serif hover:bg-gray-200 transition min-w-[70px]">Copy to clipboard</button>
            </div>
            </div>
        </div>
        <!-- Gift Address -->
        <div class="w-full flex flex-col items-center sm:mb-6">
            <span class="text-white text-[8px] sm:text-xl font-serif mb-1 sm:mb-2">Gift</span>
            <span class="text-white font-serif text-[8px] sm:text-base text-center mb-1 sm:mb-2">Orchid Streat Number 15, West Jakarta</span>
            <button class="px-3 py-0.5 bg-white rounded-full shadow text-[#172554] text-[8px] sm:text-sm font-serif hover:bg-gray-200 transition min-w-[70px] sm:min-w-[120px]">Copy address</button>
        </div>
        <!-- Wish Form -->
        <div class="w-full flex flex-col items-center sm:mb-4">
          <span class="text-white text-[8px] sm:text-xl font-serif mb-1 sm:mb-2">Give us your best wish</span>
          <form class="w-full max-w-2xl flex flex-row gap-2 sm:gap-6 items-start">
            <div class="flex flex-col gap-2 sm:gap-6 w-1/3 min-w-[90px] sm:min-w-[120px]">
              <label class="text-white font-serif text-[8px] sm:text-base mt-0.5 sm:mt-1">Nama Pengirim</label>
              <label class="text-white font-serif text-[8px] sm:text-base mt-6 sm:mt-3">Message</label>
            </div>
            <!-- INPUT PESAN -->
            <div class="flex flex-col gap-2 sm:gap-4 w-2/3">
              <input type="text" placeholder="Nama Tamu" class="rounded-xl px-2 py-1 sm:px-4 sm:py-2 bg-[#aeb3c2] text-[#172554] font-serif w-full outline-none text-[8px] sm:text-base" />
              <textarea rows="3" placeholder="Kirim Ucapan" class="rounded-xl px-2 py-1 sm:px-4 sm:py-2 bg-[#aeb3c2] text-[#172554] font-serif w-full outline-none resize-none text-[8px] sm:text-base"></textarea>
              <div class="flex justify-end mt-1 sm:mt-2">
                <button type="submit" class="px-6 py-0.5 sm:px-12 sm:py-1 bg-white rounded-full shadow text-[#172554] text-[8px] sm:text-base font-serif hover:bg-gray-200 transition">Kirim</button>
              </div>
            </div>
          </form>
        </div>

        <!-- Wishes List -->
            <ScrollArea
            class="h-[200px] w-full rounded-md"
            orientation="both"
            >
                {#each wishes as wish}
                <div class="text-left">
                    <h3 class="font-semibold text-[12px] sm:text-xl text-white">{wish.name}</h3>
                    <p class="italic text-[12px] sm:text-lg text-gray-200">{wish.message}</p>
                </div>
                {/each}
            </ScrollArea>
        </div>
    </div>
</div>