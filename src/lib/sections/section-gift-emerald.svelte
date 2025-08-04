<div class="min-h-screen bg-[#0a2d2b] flex flex-col items-center py-10 px-2 max-w-2xl mx-auto">
  <div class="w-full max-w-xl flex flex-col items-center">
    <h2 class="text-[56px] font-cursive text-[#f6b93b] mb-2 mt-4">Gift <span class="font-cursive">&amp;</span> Wish</h2>
    <p class="text-center text-[#f6f6f6] text-lg mb-8 mt-2 font-light">
      If you would like to give a gift as a symbol of blessing and support for our household journey, some of the following options may be helpful
    </p>
    <div class="w-full flex flex-col items-center">
      <h3 class="text-3xl text-[#f6b93b] font-cursive mb-2">Cashless</h3>
      <div class="flex flex-row justify-center items-start w-full gap-8 mb-8">
        <div class="flex-1 flex flex-col items-center">
          <img src="/BCA.png" alt="BCA" class="h-8 mb-1" />
          <div class="text-[#f6f6f6] text-lg">Hinata</div>
          <div class="text-[#f6f6f6] text-2xl tracking-widest mb-2">123456789</div>
          <button class="bg-[#0a2d2b] border border-[#1abc9c] text-[#f6f6f6] rounded-full px-6 py-2 shadow-md hover:bg-[#1abc9c] hover:text-[#0a2d2b] transition mb-2" on:click={() => copyToClipboard('123456789')}>Copy to clipboard</button>
        </div>
        <div class="h-24 w-px bg-[#f6b93b] mx-2"></div>
        <div class="flex-1 flex flex-col items-center">
          <img src="/BCA.png" alt="BCA" class="h-8 mb-1" />
          <div class="text-[#f6f6f6] text-lg">Naruto</div>
          <div class="text-[#f6f6f6] text-2xl tracking-widest mb-2">123456789</div>
          <button class="bg-[#0a2d2b] border border-[#1abc9c] text-[#f6f6f6] rounded-full px-6 py-2 shadow-md hover:bg-[#1abc9c] hover:text-[#0a2d2b] transition mb-2">Copy to clipboard</button>
        </div>
      </div>
      <h3 class="text-3xl text-[#f6b93b] font-cursive mb-2">Gift</h3>
      <div class="text-[#f6f6f6] text-xl mb-2 text-center">Orchid Streat Number 15, West Jakarta</div>
      <button class="bg-[#0a2d2b] border border-[#1abc9c] text-[#f6f6f6] rounded-full px-6 py-2 shadow-md hover:bg-[#1abc9c] hover:text-[#0a2d2b] transition mb-8" >Copy address</button>
    </div>
    <div class="w-full mt-4">
      <div class="text-[#f6f6f6] text-xl mb-2">Send your best wish for our wedding day</div>
      <div class="flex justify-center w-full">
        <form class="w-full max-w-xl bg-[#064E3B] rounded-2xl shadow-lg p-6 flex flex-col gap-4 mb-8">
          <div>
            <label class="text-[#f6f6f6] mb-1 block" for="nama-pengirim">Nama Pengirim</label>
            <input id="nama-pengirim" type="text" class="w-full rounded-2xl px-4 py-2 bg-[#8ca7a1] text-[#0a2d2b] placeholder-[#0e3a36] focus:outline-none" placeholder="Nama Tamu"/>
          </div>
          <div>
            <label class="text-[#f6f6f6] mb-1 block" for="pesan">Pesan</label>
            <textarea id="pesan" class="w-full rounded-2xl px-4 py-2 bg-[#8ca7a1] text-[#0a2d2b] placeholder-[#0e3a36] focus:outline-none" rows="4" placeholder="Kirim Ucapan"></textarea>
          </div>
          <div class="flex justify-center mt-2">
            <button type="submit" class="bg-[#0a2d2b] text-[#f6f6f6] rounded-full px-16 py-2 shadow-lg hover:bg-[#1abc9c] hover:text-[#0a2d2b] transition" style="box-shadow: 0 6px 24px 0 #0a2d2b80;">Kirim</button>
          </div>
          <!-- Sendvitation Section -->
            <div class="mt-2">
                <div class="mb-6">
                    <div class="text-2xl text-[#f6b93b] font-cursive mb-1">Sendvitation</div>
                    <div class="text-[#f6f6f6] text-lg">Selamat ya, bahagia selalu</div>
                </div>
                <div class="mb-6">
                    <div class="text-2xl text-[#f6b93b] font-cursive mb-1">Sendvitation</div>
                    <div class="text-[#f6f6f6] text-lg">Selamat ya, bahagia selalu</div>
                </div>
            </div>
        </form>
      </div>
    </div>
    
  </div>
</div>

<style>
  @import url('https://fonts.googleapis.com/css2?family=Great+Vibes&display=swap');
  .font-cursive {
    font-family: 'Great Vibes', cursive;
  }
</style>
