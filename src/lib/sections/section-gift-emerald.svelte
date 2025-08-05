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

<div class="bg-[#0a2d2b] flex flex-col items-center py-10 px-4 max-w-2xl mx-auto">
  <div class="w-full max-w-xl flex flex-col items-center">
    <h2 class="text-[30px] sm:text-[40px] font-cursive text-[#CA8A04] mb-9 mt-7" style="font-family: 'Emotional Use', cursive;">Gift &amp; Wish</h2>
    <p class="text-center text-[#FEF3C7] text-lg mb-8 mt-2 font-light">
      If you would like to give a gift as a symbol of blessing and support for our household journey, some of the following options may be helpful
    </p>
    <div class="w-full flex flex-col items-center">
      <h3 class="text-3xl text-[#CA8A04] font-caslon mb-2">Cashless</h3>
      <div class="flex flex-col sm:flex-row justify-center items-center sm:items-start w-full gap-8 mb-8">
        <div class="flex-1 flex flex-col items-center">
          <img src="/BCA.png" alt="BCA" class="h-7 mb-1" />
          <div class="text-[#FAFAFA] text-lg font-oblata">Hinata</div>
          <div class="text-[#FAFAFA] text-2xl tracking-widest mb-2 font-oblata">123456789</div>
          <button class="bg-[#064E3B] text-[#FEF3C7] rounded-full px-6 py-1 shadow-md hover:bg-[#1abc9c] hover:text-[#0a2d2b] transition mb-2 font-oblata" >Copy to clipboard</button>
        </div>
        <!-- TIANG SEPARATOR -->
        <div class="h-38 w-px bg-[#CA8A04] mx-2 hidden sm:block"></div>
        <div class="flex-1 flex flex-col items-center">
          <img src="/BCA.png" alt="BCA" class="h-7 mb-1" />
          <div class="text-[#FAFAFA] text-lg font-oblata">Naruto</div>
          <div class="text-[#FAFAFA] text-2xl tracking-widest mb-2 font-oblata">123456789</div>
          <button class="bg-[#064E3B] text-[#FEF3C7] rounded-full px-6 py-1 shadow-md hover:bg-[#1abc9c] hover:text-[#0a2d2b] transition mb-2 font-oblata">Copy to clipboard</button>
        </div>
      </div>
      <h3 class="text-3xl text-[#CA8A04] font-caslon mb-2">Gift</h3>
      <div class="text-[#FAFAFA] text-xl mb-2 text-center font-oblata">Orchid Streat Number 15, West Jakarta</div>
      <button class="bg-[#064E3B] text-[#FEF3C7] rounded-full px-9 py-1 shadow-md hover:bg-[#1abc9c] hover:text-[#0a2d2b] transition mb-8 font-oblata" >Copy address</button>
    </div>
    <div class="w-full mt-4">
      <div class="text-[#FEF3C7] text-xl mb-2 font-oblata">Send your best wish for our wedding day</div>
      <div class="flex justify-center w-full">
        <form class="w-full max-w-xl bg-[#064E3B] rounded-2xl shadow-lg p-6 flex flex-col gap-4 mb-8">
          <div>
            <label class="text-[#FEF3C7] mb-1 block font-oblata" for="nama-pengirim">Nama Pengirim</label>
            <input id="nama-pengirim" type="text" class="w-full rounded-2xl px-4 py-2 bg-[#8ca7a1] text-[#0a2d2b] placeholder-[#0e3a36] focus:outline-none font-oblata" placeholder="Nama Tamu"/>
          </div>
          <div>
            <label class="text-[#FEF3C7] mb-1 block font-oblata" for="pesan">Pesan</label>
            <textarea id="pesan" class="w-full rounded-2xl px-4 py-2 bg-[#8ca7a1] text-[#0a2d2b] placeholder-[#0e3a36] focus:outline-none font-oblata" rows="4" placeholder="Kirim Ucapan"></textarea>
          </div>
          <div class="flex justify-center mt-2">
            <button type="submit" class="bg-[#0a2d2b] text-[#f6f6f6] rounded-full px-16 py-2 shadow-lg hover:bg-[#1abc9c] hover:text-[#0a2d2b] transition font-oblata" style="box-shadow: 0 6px 24px 0 #0a2d2b80;">Kirim</button>
          </div>
          <!-- Sendvitation Section -->
            <div class="mt-2">
                  <ScrollArea class="h-[200px] w-full rounded-md" orientation="both">
                    {#each wishes as wish}
                      <div class="mb-4 text-left">
                        <h4 class="font-caslon text-xl text-[#CA8A04]">{wish.name}</h4>
                        <p class="italic text-[#FAFAFA] font-oblata">{wish.message}</p>
                      </div>
                    {/each}
                </ScrollArea>
            </div>
        </form>
      </div>
    </div>
  </div>
</div>

<style>
  @import url('https://fonts.googleapis.com/css2?family=Great+Vibes&display=swap');
  .font-cursive {
    font-family: 'Great Vibes', cursive;
  }
  .font-oblata {
    font-family: 'Oblata-Regular', serif;
  }
  .font-caslon {
    font-family: 'Caslon Regular', serif;
  }
</style>
