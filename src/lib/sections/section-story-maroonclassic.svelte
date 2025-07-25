<script>
  // Props untuk customization jika diperlukan
  export let title = "OUR LOVE STORY";
  export let stories = [
    {
      image: "/lovestorypict1maroonclassic.png",
      text: "Tatapan pertama yang tidak sengaja bertukar di sebuah kafe kecil pinggir kota menjadi awal dari segalanya. Percakapan singkat yang terasa begitu panjang mengawali perjalanan yang tak pernah kami bayangkan sebelumnya."
    },
    {
      image: "/lovestorypict2maroonclassic.png", 
      text: "Hari-hari berlalu dengan pesan-pesan yang tidak pernah berhenti hingga larut malam, berbagi mimpi dan ketakutan yang selama ini tersimpan rapat. Pertengkaran kecil dan perbedaan pandangan justru membuat kami semakin memahami satu sama lain dengan cara yang tidak terduga."
    },
    {
      image: "/lovestorypict3maroonclassic.png",
      text: "Jarak yang memisahkan selama dua tahun mengajarkan kami tentang kesabaran dan kepercayaan yang sesungguhnya. Air mata berlining setiap kali panggilan video terputus di tengah kerinduan yang menghimpit dada."
    }
  ];
</script>

<section class="max-w-2xl mx-auto relative w-full bg-cover bg-center bg-no-repeat overflow-hidden min-h-[700px] sm:min-h-[1195px]" style="background-image: url('/backgroundstorymaroonclassic.png');">
  <!-- Overlay with specified color and opacity -->
  <div class="absolute inset-0 bg-[#D4D4D8]/50 z-10"></div>
  
  <!-- Story container -->
  <div class="relative z-20 w-full h-full flex flex-col min-h-[700px] sm:min-h-[1195px]">
    <!-- Title -->
    <div class="flex items-center justify-center pt-8 pb-0 sm:pt-16 sm:pb-12">
      <h2 class="animate-fade-in-up font-kleymissky text-4xl font-semibold italic tracking-wider text-center mb-4 sm:mb-0" style="color: #450A0A;">
        {title}
      </h2>
    </div>
    
    <!-- Story items container -->
    <div class="flex-1 flex flex-col justify-center px-3 sm:px-6 md:px-8 lg:px-12 space-y-4 sm:space-y-16 md:space-y-20 pb-16">
      
      <!-- Story 1 - Image left, text right -->
      <div class="animate-fade-in-up">
        <div class="bg-white/90 rounded-2xl shadow-2xl overflow-hidden flex flex-row max-h-[200px] sm:max-h-[278px]">
          <div class="flex-shrink-0">
            <div class="w-[150px] sm:w-[212px] h-[200px] sm:h-[278px]">
              <img src={stories[0].image} alt="Story 1" class="w-full h-full object-cover" />
            </div>
          </div>
          <div class="flex-1 px-3 py-6 sm:px-4 sm:py-7 flex items-start">
            <p class="font-times text-xs sm:text-sm md:text-base leading-relaxed text-justify" style="color: #450A0A;">
              {stories[0].text}
            </p>
          </div>
        </div>
      </div>
      
      <!-- Story 2 - Text left, image right -->
      <div class="animate-fade-in-up">
        <div class="bg-white/90 rounded-2xl shadow-2xl overflow-hidden flex flex-row-reverse max-h-[200px] sm:max-h-[278px]">
          <div class="flex-shrink-0">
            <div class="w-[150px] sm:w-[212px] h-[200px] sm:h-[278px]">
              <img src={stories[1].image} alt="Story 2" class="w-full h-full object-cover" />
            </div>
          </div>
          <div class="flex-1 px-3 py-6 sm:px-4 sm:py-7 flex items-start">
            <p class="font-times text-xs sm:text-sm md:text-base leading-relaxed text-justify" style="color: #450A0A;">
              {stories[1].text}
            </p>
          </div>
        </div>
      </div>
      
      <!-- Story 3 - Image left, text right -->
      <div class="animate-fade-in-up">
        <div class="bg-white/90 rounded-2xl shadow-2xl overflow-hidden flex flex-row max-h-[200px] sm:max-h-[278px]">
          <div class="flex-shrink-0">
            <div class="w-[150px] sm:w-[212px] h-[200px] sm:h-[278px]">
              <img src={stories[2].image} alt="Story 3" class="w-full h-full object-cover" />
            </div>
          </div>
          <div class="flex-1 px-3 py-6 sm:px-4 sm:py-7 flex items-start">
            <p class="font-times text-xs sm:text-sm md:text-base leading-relaxed text-justify" style="color: #450A0A;">
              {stories[2].text}
            </p>
          </div>
        </div>
      </div>
      
    </div>
  </div>
</section>

<style>
  @import url('https://fonts.googleapis.com/css2?family=Cinzel:wght@400;600&display=swap');
  
  /* Custom font classes for Tailwind */
  .font-cinzel {
    font-family: 'Cinzel', serif;
  }
  
  .font-kleymissky {
    font-family: 'Kleymissky', serif;
  }
  
  .font-times {
    font-family: 'Times New Roman', serif;
  }
  
  /* Custom animation */
  .animate-fade-in-up {
    animation: fadeInUp 1s ease-out;
  }
  
  @keyframes fadeInUp {
    from {
      opacity: 0;
      transform: translateY(30px);
    }
    to {
      opacity: 1;
      transform: translateY(0);
    }
  }

  /* Mobile optimizations */
  @media (max-width: 640px) {
    section {
      background-attachment: scroll !important;
    }
    
    .font-times {
      line-height: 1.4;
      word-break: break-word;
    }
    
    .font-cinzel {
      letter-spacing: 0.05em;
    }
  }

  /* Tablet optimizations */
  @media (min-width: 641px) and (max-width: 1024px) {
    .font-times {
      line-height: 1.5;
    }
  }

  /* Ensure proper text scaling */
  @media (max-width: 480px) {
    .font-times {
      hyphens: auto;
      word-wrap: break-word;
      overflow-wrap: break-word;
    }
  }

  /* Responsive image adjustments */
  @media (max-width: 480px) {
    .w-48 {
      width: 12rem;
      height: 12rem;
    }
  }
</style>
