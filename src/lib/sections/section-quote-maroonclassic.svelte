<script>
  // Props untuk customization jika diperlukan
  export let title = "QS. AR-RUM : 21";
  export let quote = "Di antara tanda-tanda (kebesaran)-Nya ialah bahwa dia menciptakan pasangan-pasangan untukmu dari (jenis) dirimu sendiri agar kamu merasa tenteram kepadanya. Dia menjadikan di antaramu rasa cinta dan kasih sayang. Sesungguhnya pada yang demikian itu benar-benar terdapat tanda-tanda (kebesaran Allah) bagi kaum yang berpikir.";
</script>

<section class="max-w-2xl mx-auto relative w-full min-h-screen bg-cover bg-center bg-no-repeat flex items-center justify-center overflow-hidden" style="background-image: url('/backgroundquotemaroonclassic.png');">
  <!-- Overlay with specified color and opacity -->
  <!-- <div class="absolute inset-0 bg-zinc-300 opacity-50 z-10"></div> -->
  
  <!-- Quote container with responsive dimensions -->
  <div class="relative z-20 bg-white/35 rounded-none shadow-2xl w-full h-full min-h-screen flex items-center justify-center">
    <div class="relative flex flex-col items-center justify-center px-4 sm:px-8 md:px-12 lg:px-20 py-8 sm:py-12 md:py-16 text-center max-w-4xl mx-auto">
      <!-- Quote text -->
      <p class="animate-fade-in-up font-times text-base sm:text-lg md:text-xl lg:text-2xl leading-relaxed text-center mb-6 sm:mb-8 md:mb-10 lg:mb-12 w-full" style="color: #450A0A;">
        {quote}
      </p>
      
      <!-- Quote source -->
      <h3 class="animate-fade-in-up font-cinzel text-lg sm:text-xl md:text-xl lg:text-2xl font-bold tracking-wider uppercase text-center" style="color: #450A0A;">
        {title}
      </h3>
    </div>
  </div>
</section>

<style>
  @import url('https://fonts.googleapis.com/css2?family=Cinzel:wght@400;600&display=swap');
  
  /* Custom font classes for Tailwind */
  .font-cinzel {
    font-family: 'Cinzel', serif;
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
</style>
