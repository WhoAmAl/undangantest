<div class="flex flex-col items-center justify-center relative max-w-2xl mx-auto" style="min-height: 100vh;">
  <div class="absolute inset-0 -z-10 w-full h-full">
    <div style="position: absolute; inset: 0; background-image: url('/backgroundstorypinkcherish.png'); background-size: cover; background-position: center;"></div>
    <div style="position: absolute; inset: 0; background: #9D174D; opacity: 0.15;"></div>
  </div>
  <div class="absolute top-5 left-0 w-full flex justify-center items-center py-1 md:py-4 bg-[#FECACA] bg-opacity-95">
    <span class="text-[rgb(10,10,10)] text-[20px] md:text-4xl font-serif font-semibold italic" style="font-family: 'Playfair Display', serif;">-Our Love Story-</span>
  </div>
  <!-- Story Cards -->
    <div class="absolute sm:bottom-8 left-[20%] right-0 flex flex-col sm:gap-3 mt-10">
      <div class="flex flex-col gap-3 sm:gap-8 w-full">
        {#each [
          { title: 'Where it All Begin', text: 'Destiny brought us together in a place we never expected. Like something out of a fairy tale, our eyes met for the first time and time seemed to stand still. We may not have immediately realized that this simple encounter would change our lives forever.' },
          { title: 'Discovering Each Other', text: 'Destiny brought us together in a place we never expected. Like something out of a fairy tale, our eyes met for the first time and time seemed to stand still. We may not have immediately realized that this simple encounter would change our lives forever.' },
          { title: 'When Hearts Connected', text: 'Destiny brought us together in a place we never expected. Like something out of a fairy tale, our eyes met for the first time and time seemed to stand still. We may not have immediately realized that this simple encounter would change our lives forever.' },
          { title: 'Growing Together', text: 'Destiny brought us together in a place we never expected. Like something out of a fairy tale, our eyes met for the first time and time seemed to stand still. We may not have immediately realized that this simple encounter would change our lives forever.' }
        ] as card}
          <div class="flex flex-col items-start w-full">
            <span class="text-gray-100 text-[15px] md:text-2xl mb-1" style="line-height:1.1; font-family: 'Bodoni Moda', serif;">{card.title}</span>
            <div class="flex flex-col items-start justify-center py-2 px-3 sm:py-6 sm:px-8 max-w-fit bg-[#9D174D] bg-opacity-95 w-full">
              <span class="text-gray-50 text-[9px] md:text-lg italic leading-tight text-justify w-full block" style="font-family: 'Justink', serif;">{card.text}</span>
            </div>
          </div>
        {/each}
      </div>
    </div>
</div>