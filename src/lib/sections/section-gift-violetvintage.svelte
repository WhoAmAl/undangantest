<script lang="ts">
  import { ScrollArea } from "$lib/components/ui/scroll-area/index.js";
  let senderName = '';
  let wishMessage = '';
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

  function copyToClipboard(text: string) {
    navigator.clipboard.writeText(text).then(() => {
      alert('Copied to clipboard!');
    });
  }
  
  function copyAddress() {
    const address = 'Orchid Street Number 15, West Jakarta';
    copyToClipboard(address);
  }
  
  function sendWish() {
    if (senderName.trim() && wishMessage.trim()) {
      // Handle sending wish - you can implement your preferred method here
      alert(`Thank you ${senderName} for your wishes!`);
      senderName = '';
      wishMessage = '';
    } else {
      alert('Please fill in both name and message fields');
    }
  }
</script>

<div class="min-h-[100vh] w-full flex justify-center items-center">
  <div class="w-full max-w-2xl bg-[#f7f3f6] text-center border-x border-[#4b2e6a] p-0 flex flex-col justify-between relative overflow-hidden" style="background-image: url('/bgvioletvintage.png'); min-height: 100vh; background-size: cover; background-position: center;">
        
    <!-- Main Content -->
    <div class="flex flex-col my-auto space-y-4 md:space-y-6 lg:space-y-8 px-3 md:px-6 lg:px-8 py-6 md:py-8">
      
      <!-- Title -->
      <div class="text-center font-serif text-[#4b2e6a] tracking-[0.15em] text-2xl md:text-3xl lg:text-4xl mb-3 md:mb-4">
        GIFT AND WISH
      </div>
      
      <!-- Description -->
      <div class="text-center text-[#4b2e6a] text-sm md:text-base lg:text-lg font-normal font-sans max-w-[90%] md:max-w-[85%] mx-auto leading-relaxed px-2" style="line-height:1.6;">
        If you would like to give a gift as a symbol of blessing and support for our household journey, some of the following options may be helpful
      </div>
      
      <!-- Cashless Section -->
      <div class="bg-[#4b2e6a] rounded-lg p-4 md:p-6 lg:p-8 mx-2 md:mx-4 lg:mx-6">
        <div class="text-[#FFF7ED] text-xl md:text-2xl font-serif mb-4 md:mb-6 tracking-wider">Cashless</div>
        
        <!-- Bank Accounts -->
        <div class="grid grid-cols-1 md:grid-cols-2 gap-3 md:gap-4 lg:gap-6 mb-4 md:mb-6">
          <!-- Hinata Account -->
          <div class="text-center">
            <img src="/BCA.png" alt="BCA" class="w-14 md:w-16 lg:w-20 mx-auto mb-2" />
            <div class="text-[#FFF7ED] text-base md:text-lg font-serif mb-1">Hinata</div>
            <div class="text-[#FFF7ED] text-sm md:text-base mb-3">123456789</div>
            <button 
              on:click={() => copyToClipboard('123456789')}
              class="px-4 py-2 rounded-full text-sm font-medium hover:opacity-80 transition-colors text-[#4b2e6a]"
              style="background-image: url('/bgvioletvintage.png'); background-size: cover; background-position: center;"
            >
              Copy to clipboard
            </button>
          </div>
          
          <!-- Naruto Account -->
          <div class="text-center">
            <img src="/BCA.png" alt="BCA" class="w-14 md:w-16 lg:w-20 mx-auto mb-2" />
            <div class="text-[#FFF7ED] text-base md:text-lg font-serif mb-1">Naruto</div>
            <div class="text-[#FFF7ED] text-sm md:text-base mb-3">123456789</div>
            <button 
              on:click={() => copyToClipboard('123456789')}
              class="px-4 py-2 rounded-full text-sm font-medium hover:opacity-80 transition-colors text-[#4b2e6a]"
              style="background-image: url('/bgvioletvintage.png'); background-size: cover; background-position: center;"
            >
              Copy to clipboard
            </button>
          </div>
        </div>
        
        <!-- Separator Lines -->
        <div class="my-4 md:my-6 space-y-1">
          <div class="border-t border-[#FFF7ED]"></div>
          <div class="border-t border-[#FFF7ED]"></div>
        </div>
        
        <!-- Gift Address -->
        <div class="text-center">
          <div class="text-[#FFF7ED] text-xl md:text-2xl font-serif mb-3 md:mb-4 tracking-wider">Gift</div>
          <div class="text-[#FFF7ED] text-sm md:text-base mb-3 md:mb-4">Orchid Street Number 15, West Jakarta</div>
          <button 
            on:click={copyAddress}
            class="px-4 py-2 rounded-full text-sm font-medium hover:opacity-80 transition-colors text-[#4b2e6a]"
            style="background-image: url('/bgvioletvintage.png'); background-size: cover; background-position: center;"
          >
            Copy address
          </button>
        </div>
      </div>
      
      <!-- Wishes Section -->
      <div class="mx-2 md:mx-4 lg:mx-6">
        <div class="text-center text-[#4b2e6a] text-base md:text-lg lg:text-xl font-serif mb-4 md:mb-6">
          Give us your best wish for our wedding day
        </div>
        
        <!-- Wishes Form -->
        <div class="backdrop-blur-sm rounded-2xl p-4 md:p-6 lg:p-8 border-4 border-[#4b2e6a] shadow-lg">
          <!-- Name Input -->
          <div class="mb-3 md:mb-4">
            <label class="block text-[#4b2e6a] text-sm mb-2 text-left" for="senderName" style="font-family: 'Foglihten', serif;">
              Nama Pengirim
            </label>
            <input 
              id="senderName"
              bind:value={senderName}
              type="text" 
              placeholder="Nama Tamu"
              class="w-full px-3 md:px-4 py-2 md:py-3 bg-transparent border-2 border-[#4b2e6a]/40 rounded-xl focus:outline-none focus:ring-0 focus:border-[#4b2e6a] text-[#4b2e6a] placeholder-[#4b2e6a]/60 font-medium text-sm md:text-base"
            />
          </div>
          
          <!-- Message Input -->
          <div class="mb-4 md:mb-6">
            <label class="block text-[#4b2e6a] text-sm mb-2 text-left" for="wishMessage" style="font-family: 'Foglihten', serif;">
              Pesan
            </label>
            <textarea 
              id="wishMessage"
              bind:value={wishMessage}
              rows="4"
              placeholder="Kirim Ucapan"
              class="w-full px-3 md:px-4 py-2 md:py-3 bg-transparent border-2 border-[#4b2e6a]/40 rounded-xl focus:outline-none focus:ring-0 focus:border-[#4b2e6a] text-[#4b2e6a] placeholder-[#4b2e6a]/60 resize-none font-medium text-sm md:text-base"
            ></textarea>
          </div>
          
          <!-- Send Button -->
          <div class="flex justify-start">
            <button 
              on:click={sendWish}
              class="bg-[#4b2e6a] text-white px-6 md:px-8 py-3 md:py-4 rounded-xl font-bold text-sm md:text-base hover:bg-[#3d2454] transition-all duration-200 transform hover:scale-[1.02] shadow-lg"
              style="font-family: 'Foglihten', serif;"
            >
              Kirim
            </button>
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
      </div>
    </div>
  </div>
</div>
