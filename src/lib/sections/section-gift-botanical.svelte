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

<div class="bg-neutral-50 relative flex flex-col items-center pt-8 pb-16">
	<!-- Bunga kiri -->
	<img src="/bungamapsbotanical.png" alt="Bunga kiri" class="absolute left-0 top-0 w-25 md:w-40 lg:w-48 scale-x-[-1] translate-y-15 md:-translate-y-0" style="z-index:1;" />

	<!-- Pembungkus judul dan card rata kanan -->
	<div class="flex flex-col items-center max-w-xl ml-auto">
		<!-- Judul -->
		<h2 class="text-3xl md:text-4xl text-fuchsia-900 mt-2 mb-6" style="font-family: 'Oleo Script Swash Regulars', cursive;">Gift &amp; Wish</h2>

		<!-- Card foto pengantin dan deskripsi rata kanan, teks p menempel di bawah -->
		<div class="rounded-l-4xl shadow-md flex flex-col justify-between items-end p-4 md:p-6 w-[280px] md:w-[450px] h-50 md:h-70 ml-auto" style="background-image: url('/picturegiftbotanical.png'); background-size: cover; background-repeat: no-repeat; margin-top:-12px;">
			<div class="w-full flex-grow"></div>
			<p class="text-center text-fuchsia-900 text-xs md:text-lg leading-relaxed px-2 mb-0">
				If you would like to give a gift as a symbol of blessing and support for our household journey, some of the following options may be helpful
			</p>
		</div>
	</div>

	<!-- Wrapper untuk Cashless, Gift, Wish, dan Sendvitation section -->
	<div class="w-full max-w-2xl mx-auto flex flex-col items-center px-5 md:px-30">
		<!-- Cashless Section -->
		<div class="w-full max-w-lg mx-auto mt-8 ">
			<h2 class="text-center text-3xl font-cursive text-fuchsia-900 mb-6" style="font-family: 'Uchen Regular', cursive;">Cashless</h2>
			<div class="flex flex-row justify-center gap-8 mb-2">
				<!-- BCA Hinata -->
				<div class="flex flex-col items-center w-full">
					<div class="flex flex-col items-center gap-2 mb-1">
						<img src="/BCA.png" alt="BCA" class="w-auto h-8" />
						<span class="font-bold text-lg text-fuchsia-900">Hinata</span>
					</div>
					<span class="text-fuchsia-900 text-lg cursor-pointer" id="hinata-rek">123456789</span>
					<button class="mt-2 px-12 md:px-6 py-1 rounded-full bg-fuchsia-900 text-gray-50 text-xs md:text-base" on:click={() => copyToClipboard('123456789')}>Copy to clipboard</button>
				</div>
				<!-- BCA Naruto -->
				<div class="flex flex-col items-center w-full">
					<div class="flex flex-col items-center gap-2 mb-1">
						<img src="/BCA.png" alt="BCA" class="w-auto h-8" />
						<span class="font-bold text-lg text-fuchsia-900">Naruto</span>
					</div>
					<span class="text-fuchsia-900 text-lg cursor-pointer" id="naruto-rek">123456789</span>
					<button class="mt-2 px-12 md:px-6 py-1 rounded-full bg-fuchsia-900 text-gray-50 text-xs md:text-base" on:click={() => copyToClipboard('123456789')}>Copy to clipboard</button>
				</div>
			</div>
		</div>
		<!-- Gift Section -->
		<div class="w-full max-w-lg mx-auto mt-8">
			<h2 class="text-center text-2xl md:text-3xl text-fuchsia-900 mb-2" style="font-family: 'Uchen Regular', cursive;">Gift</h2>
			<div class="text-center text-lg md:text-lg text-fuchsia-900 mb-2">Orchid Streat Number 15, West Jakarta</div>
			<button class="block mx-auto px-8 md:px-8 py-1 rounded-full bg-fuchsia-900 text-white mb-4" on:click={() => copyToClipboard('Orchid Streat Number 15, West Jakarta')}>Copy address</button>
		</div>
		<!-- Wish Section -->
		<div class="w-full max-w-lg mx-auto mt-8">
			<h2 class="text-center text-xl md:text-2xl text-fuchsia-900 mb-4">Give us your best wish</h2>
			<form class="flex flex-col gap-4">
				<div class="flex flex-col md:flex-row md:items-center gap-2">
					<label for="sender" class="text-fuchsia-900 w-40">Nama Pengirim</label>
					<input id="sender" type="text" placeholder="Nama Tamu" class="flex-1 rounded-2xl px-4 py-2 bg-fuchsia-900/40 text-white placeholder:text-purple-200" />
				</div>
				<div class="flex flex-col md:flex-row md:items-start gap-2">
					<label for="message" class="text-fuchsia-900 w-40">Message</label>
					<textarea id="message" rows="4" placeholder="Kirim Ucapan" class="flex-1 rounded-2xl px-4 py-2 bg-fuchsia-900/40 text-white placeholder:text-purple-200 resize-none" />
				</div>
				<button type="submit" class="rounded-xl self-end px-14 py-1 bg-fuchsia-900 text-white">Kirim</button>
			</form>
		</div>
        
		<!-- Sendvitation Section -->
		<div class="w-full max-w-lg mx-auto mt-8">
            <ScrollArea class="h-75 md:h-65 w-full rounded-md" orientation="both">
                {#each wishes as wish}
                <div class="mb-4 text-left">
                    <h4 class="text-xl text-fuchsia-900" style="font-family: 'Uchen Regular', cursive;">{wish.name}</h4>
                    <p class="text-fuchsia-900">{wish.message}</p>
                </div>
                {/each}
            </ScrollArea>
		</div>
	</div>
</div>