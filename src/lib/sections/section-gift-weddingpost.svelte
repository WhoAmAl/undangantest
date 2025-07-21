<script>
  let senderName = '';
  let message = '';
  let wishes = [
    { name: "Sendvitation", message: "Selamat ya, bahagia selalu" },
    { name: "Sendvitation", message: "Selamat ya, bahagia selalu" },
    { name: "Sendvitation", message: "Selamat ya, bahagia selalu" }
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
    <h2 class="text-4xl font-bold tracking-widest m-2">GIFT AND WISH</h2>
    <div class="border-t-3 border-black mb-0.5"></div>
    <div class="border-t-4 border-black mb-1"></div>

  <!-- Subtext -->
  <p class="italic text-gray-700">
    If you would like to give a gift as a symbol of blessing and support for our household journey, some of the following options may be helpful
  </p>

  <!-- Gift Options -->
  <div class="grid grid-cols-1 md:grid-cols-2 divide-x divide-black border-t border-b border-black py-6">
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
  <div class="border-t border-black pt-6 space-y-6 text-left">
    {#each wishes as wish}
      <div>
        <h3 class="font-semibold">{wish.name}</h3>
        <p class="italic text-gray-700">{wish.message}</p>
      </div>
    {/each}
  </div>
</div>
