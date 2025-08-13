<script lang="ts">
  import { ScrollArea } from "$lib/components/ui/scroll-area/index.js";
  	function copyToClipboard(text: string) {
		navigator.clipboard.writeText(text);
	}
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
</script>

<div class="bg-neutral-950 px-4 md:px-7 lg:px-10 min-h-screen sm:min-h-[165vh] xl:min-h-screen flex flex-col items-center" style="background-image: url(/landingopeningretroclassic.png); background-size: cover; background-position: center; background-repeat: no-repeat; font-family: 'Jomolhari', serif;">
	<!-- HeaDER -->
    <div class="w-full flex flex-col items-center justify-center text-neutral-50">
        <div class="w-full text-center pt-8">
            <div class="text-neutral-50 text-4xl lg:text-7xl tracking-[0.2em] mb-2" style="font-family: 'Jomolhari', serif;">WISH</div>
            <div class="border-t-3 border-white w-full my-2"></div>
        </div>
    </div>

    <!-- BODY CONTENT -->
    <div class="flex flex-col justify-center items-center w-full mt-5 md:mt-15 gap-8">
        <!-- Wishes Form -->
        <div class="bg-neutral-700/70 w-full">
            <form class="w-full max-w-xl mx-auto pt-6 px-6 rounded-lg shadow-lg flex flex-col gap-1">
                <label class="text-neutral-50 text-lg" for="nama">Nama Pengirim :</label>
                <input id="nama" name="nama" type="text" placeholder="Nama Tamu" class="w-full p-3 rounded-md bg-neutral-200/60 text-neutral-900 focus:outline-none focus:ring-2 focus:ring-white mb-6" />

                <label class="text-neutral-50 text-lg mb-1" for="pesan">Pesan / Message :</label>
                <textarea id="pesan" name="pesan" rows="5" placeholder="Kirim Ucapan" class="w-full p-3 rounded-md bg-neutral-200/60 text-neutral-900 focus:outline-none focus:ring-2 focus:ring-white"></textarea>

                <div class="flex justify-center my-8">
                    <button type="submit" class="px-12 py-1 rounded-xl bg-white text-neutral-900 shadow hover:bg-neutral-200 transition">Kirim</button>
                </div>
            </form>
        </div>
        <!-- Wishes List -->
         <div class="bg-neutral-700/70 w-full px-8 p-8 mb-10">
            <h3 class="text-neutral-50 text-base md:text-lg mb-3">Give us your best wish for our wedding</h3>
            <ScrollArea class="h-75 md:h-100 w-full rounded-md" orientation="both">
                {#each wishes as wish}
                <div class="mb-4 md:mb-8 text-left">
                    <h4 class="text-base md:text-xl text-neutral-50 uppercase">{wish.name}</h4>
                    <p class="text-neutral-50" style="font-family: 'Baskervville', cursive;">{wish.message}</p>
                </div>
                {/each}
            </ScrollArea>
         </div>
    </div>
</div>