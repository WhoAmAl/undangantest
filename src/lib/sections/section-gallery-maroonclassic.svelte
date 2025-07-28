<section class="max-w-2xl mx-auto relative w-full bg-cover bg-center bg-no-repeat overflow-hidden min-h-[700px] sm:min-h-[1195px]" style="background-image: url('/bggallerymaroonclassic.png');">
  <div class="bg-[#D4D4D8]/40 absolute inset-4 sm:inset-12 z-10 rounded-xl p-4 sm:p-5">
    <div class="flex flex-col gap-4 sm:gap-6 h-full items-center justify-center">
      <!-- Container untuk 2 foto bersebelahan -->
      <div class="flex flex-col sm:flex-row gap-4 sm:gap-6 w-full">
        <!-- Foto 1 -->
        <div class="flex-1 w-full h-48 sm:h-64 lg:h-80">
          <img 
            src="/gallery1maroonclassic.png" 
            alt="Gallery Photo 1" 
            class="w-full h-full object-cover shadow-lg hover:shadow-2xl transition-all duration-300 transform hover:-translate-y-2 hover:scale-105 cursor-pointer"
          />
        </div>
        
        <!-- Foto 2 -->
        <div class="flex-1 w-full h-48 sm:h-64 lg:h-80">
          <img 
            src="/gallery2maroonclassic.png" 
            alt="Gallery Photo 2" 
            class="w-full h-full object-cover shadow-lg hover:shadow-2xl transition-all duration-300 transform hover:-translate-y-2 hover:scale-105 cursor-pointer"
          />
        </div>
      </div>
      
      <!-- Video Player -->
      <div class="w-full h-48 sm:h-64 lg:h-80 relative group">
        <video 
          class="w-full h-full object-cover shadow-lg"
          poster="/gallery5maroonclassic.png"
          id="galleryVideo"
        >
          <source src="/gallery-video-maroonclassic.mp4" type="video/mp4">
          <source src="/gallery-video-maroonclassic.webm" type="video/webm">
          Your browser does not support the video tag.
        </video>
        
        <!-- Custom Play Button -->
        <div class="absolute inset-0 flex items-center justify-center bg-black/20 group-hover:bg-black/30 transition-all duration-300" id="playOverlay">
          <button 
            class="bg-[#450A0A] hover:bg-[#5A0E0E] text-black rounded-full p-4 sm:p-6 shadow-lg hover:shadow-xl transition-all duration-300 transform hover:scale-110"
          >
            <svg xmlns="http://www.w3.org/2000/svg" class="h-8 w-8 sm:h-12 sm:w-12 text-black" fill="currentColor" viewBox="0 0 20 20">
              <path d="M6 4l10 6-10 6V4z" />
            </svg>
          </button>
        </div>
      </div>
      
      <!-- Container untuk 2 foto bersebelahan (bawah) -->
      <div class="flex flex-col sm:flex-row gap-4 sm:gap-6 w-full">
        <!-- Foto 3 -->
        <div class="flex-1 w-full h-48 sm:h-64 lg:h-80">
          <img 
            src="/gallery3maroonclassic.png" 
            alt="Gallery Photo 3" 
            class="w-full h-full object-cover shadow-lg hover:shadow-2xl transition-all duration-300 transform hover:-translate-y-2 hover:scale-105 cursor-pointer"
          />
        </div>
        
        <!-- Foto 4 -->
        <div class="flex-1 w-full h-48 sm:h-64 lg:h-80">
          <img 
            src="/gallery4maroonclassic.png" 
            alt="Gallery Photo 4" 
            class="w-full h-full object-cover shadow-lg hover:shadow-2xl transition-all duration-300 transform hover:-translate-y-2 hover:scale-105 cursor-pointer"
          />
        </div>
      </div>
    </div>
  </div>
</section>

<style>

</style>
