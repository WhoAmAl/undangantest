<script>
  import { ScrollArea } from "$lib/components/ui/scroll-area/index.js";
  let name = '';
  let message = '';
  let showCashlessModal = false;
  let showGiftModal = false;
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

  function closeModal() {
    showCashlessModal = false;
    showGiftModal = false;
  }
  function handleSubmit() {
    if (name && message) {
      wishes = [...wishes, { name, message }];
      name = '';
      message = '';
    }
  }
</script>

<style>
  @import url('https://fonts.googleapis.com/css2?family=Great+Vibes&family=Playfair+Display:wght@500;700&display=swap');
</style>

<div class="bg-cover bg-center min-h-screen flex flex-col items-center justify-start text-center">
  <div class="min-h-[1160px] max-w-full sm:max-w-2xl w-full flex flex-col items-center space-y-6 text-[#611717] px-4 sm:px-15" style="background-image: url('/giftbgpinkmarble.png');">
    <h1 class="mt-8 text-3xl sm:text-4xl font-[Great Vibes]">Gift And Wishes</h1>
    <p class="text-lg sm:text-xl text-center text-[#611717]">
      If you would like to give a gift as a symbol of blessing and <br />
      support for our household journey, some of the following <br />
      options may be helpful
    </p>

    <!-- Buttons -->
    <div class="flex flex-col sm:flex-row gap-4 sm:gap-40 mt-3 w-full sm:w-auto px-2 sm:px-0">
      <button
        on:click={() => (showCashlessModal = true)}
        class="bg-white px-6 sm:px-16 py-2 rounded-full shadow text-[#BE123C] font-medium w-full sm:w-auto"
      >
        Cashless
      </button>
      <button
        on:click={() => (showGiftModal = true)}
        class="bg-white px-6 sm:px-16 py-2 rounded-full shadow text-[#BE123C] font-medium w-full sm:w-auto"
      >
        Gift
      </button>
    </div>

    <p class="text-lg sm:text-xl text-[#611717] leading-tight mt-8 sm:mt-10">
      Give your best wish for us <br />
      We will so appreciate for that
    </p>

    <!-- Form -->
    <div class="min-h-[400px] sm:min-h-[643px] bg-[#FFF1F2] bg-opacity-50 backdrop-blur-md rounded-2xl p-4 sm:p-6 w-full max-w-full sm:max-w-xl space-y-4 text-left">
      <div class="flex flex-col sm:flex-row items-stretch sm:items-center gap-2 sm:gap-4 mb-2">
        <label class="text-[#881337] font-semibold min-w-[120px] sm:block">Nama Pengirim</label>
        <input bind:value={name} type="text" placeholder="Nama Tamu" class="flex-1 px-4 py-2 text-black bg-pink-100 rounded-md focus:outline-none" />
      </div>
      <div class="flex flex-col sm:flex-row items-stretch sm:items-center gap-2 sm:gap-4 mb-2">
        <label class="text-[#881337] font-semibold min-w-[120px] sm:block">Message</label>
        <textarea bind:value={message} rows="3" placeholder="Kirim Ucapan" class="flex-1 px-4 py-2 bg-pink-100 rounded-md resize-none focus:outline-none"></textarea>
      </div>

      <div class="text-right">
        <button on:click={handleSubmit} class="bg-pink-100 px-6 sm:px-10 py-1 rounded-full text-[#881337]">Kirim</button>
      </div>

      <!-- Wishes List -->
      <ScrollArea
        class="h-[200px] w-full rounded-md border p-4"
        orientation="both"
      >
          {#each wishes as wish}
            <div class="text-left">
              <h3 class="font-semibold">{wish.name}</h3>
              <p class="italic text-gray-700">{wish.message}</p>
            </div>
          {/each}
      </ScrollArea>
    </div>

    {#if showCashlessModal}
    <div
      class="fixed inset-0 z-50 flex items-center justify-center backdrop-blur-sm bg-white/30"
      on:click={closeModal}
    >
      <div
        class="bg-[#FDF2F8] rounded-2xl p-6 w-11/12 max-w-md text-left shadow-lg"
        on:click|stopPropagation
      >
        <!-- Akun 1 -->
        <div class="flex items-center space-x-4 mb-6">
          <img src="/BCA.png" alt="BCA Logo" class="w-14 h-14 object-contain" />
          <div>
            <p class="text-[#BE123C] font-semibold text-lg">Hinata</p>
            <p class="text-[#BE123C] text-md">123456789</p>
            <button
              class="mt-2 px-4 py-1 bg-[#FCE7F3] text-[#BE123C] rounded-full shadow-md text-sm hover:bg-pink-100 transition"
            >
              Copy to clipboard
            </button>
          </div>
        </div>

        <!-- Akun 2 -->
        <div class="flex items-center space-x-4">
          <img src="/BCA.png" alt="BCA Logo" class="w-14 h-14 object-contain" />
          <div>
            <p class="text-[#BE123C] font-semibold text-lg">Naruto</p>
            <p class="text-[#BE123C] text-md">123456789</p>
            <button
              class="mt-2 px-4 py-1 bg-[#FCE7F3] text-[#BE123C] rounded-full shadow-md text-sm hover:bg-pink-100 transition"
            >
              Copy to clipboard
            </button>
          </div>
        </div>
      </div>
    </div>
    {/if}

    {#if showGiftModal}
    <div
      class="fixed inset-0 backdrop-blur-sm bg-white/30 flex items-center justify-center z-50"
      role="dialog"
      tabindex="0"
      aria-modal="true"
      on:click={closeModal}
      on:keydown={(e) => { if (e.key === 'Escape' || e.key === 'Enter' || e.key === ' ') closeModal(); }}
    >
      <div
        class="bg-[#FDF2F8] rounded-xl p-6 w-11/12 max-w-md text-center"
        role="document"
        tabindex="0"
        on:click|stopPropagation
        on:keydown|stopPropagation
      >
        <h2 class="text-xl font-semibold mb-4 text-[#881337]">Kirim Hadiah</h2>
        <p class="text-lg mt-2 font-semibold">Orchid Streat Number 15, West Jakarta</p>
        <button on:click={() => {
          navigator.clipboard.writeText('Orchid Streat Number 15, West Jakarta');
          closeModal();
        }} class="mt-4 px-4 py-1 bg-[#FCE7F3] rounded-full text-[#611717]">Copy Address</button>
      </div>
    </div>
    {/if}

  </div>
</div>