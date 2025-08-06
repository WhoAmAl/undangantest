<script lang="ts">
  import { ScrollArea } from "$lib/components/ui/scroll-area/index.js";
  let senderName = '';
  let message = '';
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

  const copyToClipboard = (text) => {
    navigator.clipboard.writeText(text);
    alert('Copied to clipboard');
  };

  const sendWish = () => {
    if (senderName && message) {
      wishes = [...wishes, { name: senderName, message }];
      senderName = '';
      message = '';
    }
  };
</script>

<div class="bg-gray-200 max-w-2xl mx-auto px-4 py-10 space-y-6 text-center font-serif border-x border-black text-gray-900">
  <!-- Title -->
    <div class="border-t-4 border-black mb-0.5"></div>
    <div class="border-t-3 border-black mb-1"></div>
    <h2 class="text-3xl md:text-4xl font-bold tracking-widest m-2">GIFT AND WISH</h2>
    <div class="border-t-3 border-black mb-0.5"></div>
    <div class="border-t-4 border-black mb-1"></div>

  <!-- Subtext -->
  <p class="italic text-gray-700 mt-6 md:mt-10 text-left">
    If you would like to give a gift as a symbol of blessing and support for our household journey, some of the following options may be helpful
  </p>

  <!-- Gift Options -->
  <div class="grid grid-cols-1 md:grid-cols-2 md:divide-x divide-black border-t border-b border-black py-6">
    <!-- Cashless -->
    <div class="space-y-6">
      <h2 class="text-xl font-medium">Cashless</h2>

      <!-- Hinata -->
      <div class="space-y-2">
        <img src="/BCA.png" alt="BCA" class="h-6 mx-auto" />
        <div>Hinata</div>
        <div>123456789</div>
        <button on:click={() => copyToClipboard('123456789')} class="bg-black text-white px-4 py-2 rounded-2xl shadow-md hover:opacity-80">
          Copy to clipboard
        </button>
      </div>

      <!-- Naruto -->
      <div class="space-y-2">
        <img src="/BCA.png" alt="BCA" class="h-6 mx-auto" />
        <div>Naruto</div>
        <div>123456789</div>
        <button on:click={() => copyToClipboard('123456789')} class="bg-black text-white px-4 py-2 rounded-2xl shadow-md hover:opacity-80">
          Copy to clipboard
        </button>
      </div>
    </div>

    <!-- Gift Address -->
    <div class="space-y-6 pt-6 md:pt-0">
      <h2 class="text-xl font-medium">Gift</h2>
      <div>
        Orchid Streat Number 15,<br />West Jakarta
      </div>
      <button on:click={() => copyToClipboard('Orchid Streat Number 15, West Jakarta')} class="bg-black text-white px-4 py-2 rounded-2xl shadow-md hover:opacity-80">
        Copy address
      </button>
    </div>
  </div>

  <!-- Wish Form -->
  <div class="text-left mt-10">
    <p class="italic">Give us your best wish for our wedding</p>

    <div class="mt-4 space-y-4">
      <div class="flex flex-col md:flex-row md:items-center md:gap-4">
        <label class="w-40">Nama Pengirim</label>
        <input bind:value={senderName} placeholder="Nama Tamu" class="flex-1 px-4 py-2 bg-gray-500 text-white rounded" />
      </div>

      <div class="flex flex-col md:flex-row md:items-start md:gap-4">
        <label class="w-40 mt-2">Message</label>
        <textarea bind:value={message} rows="4" placeholder="Kirim Ucapan" class="flex-1 px-4 py-2 bg-gray-500 text-white rounded"></textarea>
      </div>

      <div class="flex justify-end">
        <button on:click={sendWish} class="bg-black text-white px-10 py-2 rounded-2xl shadow-md hover:opacity-80">
          Kirim
        </button>
      </div>
    </div>
  </div>

  <!-- Wishes List -->
  <ScrollArea
    class="h-[200px] w-[350px] rounded-md border p-4"
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
