<script>
  let senderName = '';
  let message = '';
</script>

<section class="w-full min-h-screen px-4 sm:px-6 lg:px-8">
  <div class="max-w-2xl mx-auto py-8 sm:py-12 lg:py-16">
    <!-- Header -->
    <div class="text-center mb-8 sm:mb-12">
      <h2 class="text-[#450A0A] px-6 text-3xl sm:text-4xl md:text-5xl font-serif mb-4 sm:mb-6 text-left sm:text-left" style="background-color: #FAFAFA; font-family: 'Kleymissky', serif;">
        GIFT AND WISH
      </h2>
      <p class="text-base sm:text-lg md:text-xl leading-relaxed max-w-2xl mx-auto" style="color: #450A0A; font-family: 'Times New Roman', serif;">
        If you would like to give a gift as a symbol of blessing and support 
        for our household journey, some of the following options may be helpful
      </p>
    </div>

    <!-- Gift Section -->
    <div class="rounded-xl shadow-lg overflow-hidden mb-8 sm:mb-12 mx-auto flex flex-col" style="background-color: rgba(76, 5, 25, 0.5); width: 90vw; max-width: 542px; height: calc(90vw * 0.677); max-height: 367px;">
      <!-- Top Section - Cashless -->
      <div class="px-4 sm:px-6 md:px-8 pt-4 sm:pt-6 md:pt-8 pb-3 sm:pb-4 md:pb-6" style="height: 65.4%;">
        <h3 class="text-base sm:text-lg md:text-xl font-serif text-center mb-2 sm:mb-3 md:mb-4" style="color: #450A0A;">
          CASHLESS
        </h3>
        
        <!-- Top horizontal line -->
        <div class="w-full h-0.5 bg-white mb-0.5"></div>
        <div class="w-full h-0.5 bg-white mb-2 sm:mb-3 md:mb-4"></div>
        
        <div class="grid grid-cols-2 gap-0 relative">
          <!-- Vertical divider line - extends from top line to bottom line -->
          <div class="absolute left-1/2 bg-white transform -translate-x-1/2" style="width: 2px; top: -14px; bottom: -8px;"></div>
          
          <!-- BCA Hinata -->
          <div class="pr-3 sm:pr-4 md:pr-6 text-center mb-1">
            <div class="flex justify-center">
              <img src="/BCA.png" alt="BCA Logo" class="h-4 sm:h-6 md:h-8 w-auto mb-0.5 sm:mb-0.5 md:mb-1">
            </div>
            <h4 class="text-xs sm:text-sm md:text-base font-medium text-white" style="font-family: 'Times New Roman', serif;">Hinata</h4>
            <p class="text-xs sm:text-xs md:text-sm text-white/90 mb-0.5 sm:mb-0.5 md:mb-1" style="font-family: 'Times New Roman', serif;">123456789</p>
            <button class="text-white px-2 sm:px-3 md:px-4 py-1 sm:py-1.5 md:py-2 rounded-full text-xs" style="background-color: #450A0A; font-family: 'Libre Caslon Text', serif; font-size: 8px; line-height: 1;">
              Copy to clipboard
            </button>
          </div>

          <!-- BCA Naruto -->
          <div class="pl-3 sm:pl-4 md:pl-6 text-center mb-1">
            <div class="flex justify-center">
              <img src="/BCA.png" alt="BCA Logo" class="h-4 sm:h-6 md:h-8 w-auto mb-0.5 sm:mb-0.5 md:mb-1">
            </div>
            <h4 class="text-xs sm:text-sm md:text-base font-medium text-white" style="font-family: 'Times New Roman', serif;">Naruto</h4>
            <p class="text-xs sm:text-xs md:text-sm text-white/90 mb-0.5 sm:mb-0.5 md:mb-1" style="font-family: 'Times New Roman', serif;">123456789</p>
            <button class="text-white px-2 sm:px-3 md:px-4 py-1 sm:py-1.5 md:py-2 rounded-full text-xs" style="background-color: #450A0A; font-family: 'Libre Caslon Text', serif; font-size: 8px; line-height: 1;">
              Copy to clipboard
            </button>
          </div>
        </div>
        
        <!-- Bottom horizontal line -->
        <div class="w-full h-0.5 bg-white mt-1 sm:mt-1.5 md:mt-2"></div>
        <div class="w-full h-0.5 bg-white mt-0.5"></div>
      </div>

      <!-- Bottom Section - Gift Address -->
      <div class="px-4 sm:px-6 md:px-8 pb-4 sm:pb-6 md:pb-8 pt-0 text-center flex-1 flex flex-col justify-center">
        <h3 class="text-base sm:text-lg md:text-xl font-serif mb-1.5 sm:mb-2 md:mb-3" style="color: #450A0A;">
          GIFT
        </h3>
        <p class="text-xs sm:text-xs md:text-sm text-white mb-1.5 sm:mb-1.5 md:mb-2" style="font-family: 'Times New Roman', serif;">
          Orchid Street Number 15, West Jakarta
        </p>
        <button class="text-white px-3 sm:px-4 md:px-6 py-1 sm:py-1.5 md:py-2 rounded-full mx-auto" style="background-color: #450A0A; font-family: 'Libre Caslon Text', serif; font-size: 8px; line-height: 1;">
          Copy address
        </button>
      </div>
    </div>

    <!-- Wish Section -->
    <div class="text-left mb-6 sm:mb-8">
      <p class="px-10 text-lg sm:text-xl md:text-2xl" style="color: #450A0A; font-family: 'Times New Roman', serif;">
        Send your best wish for our wedding day
      </p>
    </div>

    <!-- Message Form -->
    <div class="rounded-xl shadow-lg mx-auto" style="background-color: #450A0A; width: 90vw; max-width: 542px;">
      <div class="px-3 sm:px-5 md:px-8 py-4 sm:py-6 md:py-8">
        <div class="mb-4 sm:mb-5 md:mb-6">
          <label for="senderName" class="block text-white text-sm sm:text-sm md:text-base font-medium mb-2 sm:mb-2 md:mb-3" style="font-family: 'Times New Roman', serif;">
            Nama Pengirim
          </label>
          <input 
            id="senderName"
            type="text" 
            bind:value={senderName}
            placeholder="Nama Tamu"
            class="w-full px-3 sm:px-3 md:px-4 py-2 sm:py-2.5 md:py-3 rounded-2xl text-black placeholder-[#450A0A] border-0 focus:outline-none text-sm sm:text-sm md:text-base"
            style="background-color: #9F8282; font-family: 'Times New Roman', serif;"
          >
        </div>

        <div class="mb-5 sm:mb-6 md:mb-8">
          <label for="message" class="block text-white text-sm sm:text-sm md:text-base font-medium mb-2 sm:mb-2 md:mb-3" style="font-family: 'Times New Roman', serif;">
            Pesan
          </label>
          <textarea 
            id="message"
            bind:value={message}
            placeholder="Kirim Ucapan"
            rows="4"
            class="w-full px-3 sm:px-3 md:px-4 py-2 sm:py-2.5 md:py-3 rounded-2xl text-black placeholder-[#450A0A] border-0 focus:outline-none resize-none text-sm sm:text-sm md:text-base"
            style="background-color: #9F8282; font-family: 'Times New Roman', serif; height: 80px;"
          ></textarea>
        </div>

        <div class="text-center mb-5 sm:mb-6 md:mb-8">
          <button class="bg-white text-[#450A0A] px-6 sm:px-8 md:px-12 py-0.5 sm:py-0.5 md:py-1 rounded-full font-medium hover:bg-gray-100 transition-colors duration-300 text-sm sm:text-sm md:text-base" style="font-family: 'Libre Caslon Text', serif;">
            Kirim
          </button>
        </div>

        <!-- Send Invitation Text -->
        <div class="text-left space-y-3 sm:space-y-4 md:space-y-6">
          <div>
            <h4 class="text-sm sm:text-base md:text-lg font-semibold text-white mb-1 sm:mb-1.5 md:mb-2" style="font-family: 'Cinzel', serif;">
              SENDVITATION
            </h4>
            <p class="text-white/90 text-xs sm:text-xs md:text-sm" style="font-family: 'Times New Roman', serif;">
              Selamat ya, bahagia selalu
            </p>
          </div>
          
          <div>
            <h4 class="text-sm sm:text-base md:text-lg font-semibold text-white mb-1 sm:mb-1.5 md:mb-2" style="font-family: 'Cinzel', serif;">
              SENDVITATION
            </h4>
            <p class="text-white/90 text-xs sm:text-xs md:text-sm" style="font-family: 'Times New Roman', serif;">
              Selamat ya, bahagia selalu
            </p>
          </div>
        </div>
      </div>
    </div>
  </div>
</section>