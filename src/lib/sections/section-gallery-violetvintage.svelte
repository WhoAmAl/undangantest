<svelte:head>
    <link href="https://fonts.googleapis.com/css2?family=Foglihten&display=swap" rel="stylesheet">
</svelte:head>

<div class="w-full flex justify-center items-center">
  <div class="w-full max-w-2xl bg-black text-center sm:border-x border-[#4b2e6a] p-0 sm:p-0 flex flex-col relative overflow-hidden" style="background-image: url('/bgvioletvintage.png'); background-size: cover; background-position: center;">
    <!-- Bunga hias atas -->
    <img src="gallerytopvioletvintage.png" alt="" class="absolute top-0 left-0 w-44 sm:w-52 md:w-60 lg:w-68 pointer-events-none select-none" />
      
    <!-- Area konten utama -->
    <div class="flex flex-col px-4 pt-16 pb-4">
       
        <!-- Foto Utama -->
        <div class="flex justify-center mb-6 z-20">
            <div class="border-4 border-[#4b2e6a] shadow-lg p-2 " style="border-radius: 12px; background-image: url('/bgvioletvintage.png'); background-size: cover; background-position: center;">
                <div class="w-80 sm:w-96 md:w-[28rem] lg:w-[32rem] overflow-hidden" style="aspect-ratio: 566/314; border-radius: 8px;">
                    <img src="groomImagevioletvintage.png" alt="Wedding Gallery Main" class="w-full h-full object-cover filter grayscale" />
                </div>
            </div>
        </div>
        
        <!-- Slider untuk 3 foto kecil -->
        <div class="relative w-full select-none z-10" style="touch-action: pan-y; user-select: none; -webkit-user-select: none; -moz-user-select: none;">
            <div class="overflow-hidden rounded-lg">
                <div class="flex space-x-4 snap-x snap-mandatory scroll-smooth overflow-x-auto scrollbar-hide" style="scrollbar-width: none; -ms-overflow-style: none;">
                    <!-- Foto 1 -->
                    <div class="flex-shrink-0 snap-start">
                        <div class="border-4 border-[#4b2e6a] shadow-lg p-2" style="border-radius: 12px; background-image: url('/bgvioletvintage.png'); background-size: cover; background-position: center;">
                            <div class="w-32 sm:w-36 md:w-40 lg:w-44 overflow-hidden" style="aspect-ratio: 245/314; border-radius: 8px;">
                                <img src="groomImagevioletvintage.png" alt="Gallery 1" class="w-full h-full object-cover filter grayscale pointer-events-none select-none" style="user-drag: none; -webkit-user-drag: none;" draggable="false" />
                            </div>
                        </div>
                    </div>
                    
                    <!-- Foto 2 -->
                    <div class="flex-shrink-0 snap-start">
                        <div class="border-4 border-[#4b2e6a] shadow-lg p-2" style="border-radius: 12px; background-image: url('/bgvioletvintage.png'); background-size: cover; background-position: center;">
                            <div class="w-32 sm:w-36 md:w-40 lg:w-44 overflow-hidden" style="aspect-ratio: 245/314; border-radius: 8px;">
                                <img src="groomImagevioletvintage.png" alt="Gallery 2" class="w-full h-full object-cover filter grayscale pointer-events-none select-none" style="user-drag: none; -webkit-user-drag: none;" draggable="false" />
                            </div>
                        </div>
                    </div>
                    
                    <!-- Foto 3 -->
                    <div class="flex-shrink-0 snap-start">
                        <div class="border-4 border-[#4b2e6a] shadow-lg p-2" style="border-radius: 12px; background-image: url('/bgvioletvintage.png'); background-size: cover; background-position: center;">
                            <div class="w-32 sm:w-36 md:w-40 lg:w-44 overflow-hidden" style="aspect-ratio: 245/314; border-radius: 8px;">
                                <img src="groomImagevioletvintage.png" alt="Gallery 3" class="w-full h-full object-cover filter grayscale pointer-events-none select-none" style="user-drag: none; -webkit-user-drag: none;" draggable="false" />
                            </div>
                        </div>
                    </div>
                    
                    <!-- Foto 4 (untuk menambah efek slider) -->
                    <div class="flex-shrink-0 snap-start">
                        <div class="border-4 border-[#4b2e6a] shadow-lg p-2" style="border-radius: 12px; background-image: url('/bgvioletvintage.png'); background-size: cover; background-position: center;">
                            <div class="w-32 sm:w-36 md:w-40 lg:w-44 overflow-hidden" style="aspect-ratio: 245/314; border-radius: 8px;">
                                <img src="groomImagevioletvintage.png" alt="Gallery 4" class="w-full h-full object-cover filter grayscale pointer-events-none select-none" style="user-drag: none; -webkit-user-drag: none;" draggable="false" />
                            </div>
                        </div>
                    </div>
                    
                    <!-- Foto 5 (untuk menambah efek slider) -->
                    <div class="flex-shrink-0 snap-start">
                        <div class="border-4 border-[#4b2e6a] shadow-lg p-2" style="border-radius: 12px; background-image: url('/bgvioletvintage.png'); background-size: cover; background-position: center;">
                            <div class="w-32 sm:w-36 md:w-40 lg:w-44 overflow-hidden" style="aspect-ratio: 245/314; border-radius: 8px;">
                                <img src="groomImagevioletvintage.png" alt="Gallery 5" class="w-full h-full object-cover filter grayscale pointer-events-none select-none" style="user-drag: none; -webkit-user-drag: none;" draggable="false" />
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </div>
        
        <!-- Bunga hias bawah (sesuai dengan gambar) -->
        <div class="flex justify-center space-x-1 -mt-4 relative z-0">
            <img src="gallerybottomvioletvintage.png" alt="" class="w-16 h-16 sm:w-20 sm:h-20 md:w-24 md:h-24 lg:w-28 lg:h-28 pointer-events-none select-none" style="transform: translateY(-8px);" />
            <img src="gallerybottomvioletvintage.png" alt="" class="w-16 h-16 sm:w-20 sm:h-20 md:w-24 md:h-24 lg:w-28 lg:h-28 pointer-events-none select-none" style="transform: translateY(4px);" />
            <img src="gallerybottomvioletvintage.png" alt="" class="w-16 h-16 sm:w-20 sm:h-20 md:w-24 md:h-24 lg:w-28 lg:h-28 pointer-events-none select-none" style="transform: translateY(-12px);" />
            <img src="gallerybottomvioletvintage.png" alt="" class="w-16 h-16 sm:w-20 sm:h-20 md:w-24 md:h-24 lg:w-28 lg:h-28 pointer-events-none select-none" style="transform: translateY(2px);" />
            <img src="gallerybottomvioletvintage.png" alt="" class="w-16 h-16 sm:w-20 sm:h-20 md:w-24 md:h-24 lg:w-28 lg:h-28 pointer-events-none select-none" style="transform: translateY(-6px);" />
        </div>
    </div>
  </div>
</div>
<script lang="ts">
    // Pure CSS slider - no JavaScript needed
</script>

<style>
    :global(.foglihten) { 
        font-family: 'Foglihten', serif; 
    }
    
    :global(.scrollbar-hide::-webkit-scrollbar) {
        display: none;
    }
    
    :global(.scrollbar-hide) {
        scrollbar-width: none;
        -ms-overflow-style: none;
    }
</style>
