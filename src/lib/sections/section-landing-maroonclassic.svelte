<script>
	import { goto } from '$app/navigation';

	function handleRedirect() {
		goto('/maroonclassic');
	}
</script>

<!-- Import Google Fonts -->
<svelte:head>
	<link rel="preconnect" href="https://fonts.googleapis.com">
	<link rel="preconnect" href="https://fonts.gstatic.com">
	<link href="https://fonts.googleapis.com/css2?family=Cinzel:wght@400;500;600&display=swap" rel="stylesheet">
	<link href="https://fonts.googleapis.com/css2?family=Kleymissky&display=swap" rel="stylesheet">
	<link href="https://fonts.googleapis.com/css2?family=Justink&display=swap" rel="stylesheet">
</svelte:head>

<section class="w-full mx-auto sm:mt-18 max-w-[460px] h-[820px] relative overflow-hidden font-serif bg-red-950">
	<div class="relative w-full h-full flex flex-col items-center p-6">
		<!-- Background dengan frame bunga -->
		<div class="absolute top-0 left-0 w-full h-full flex items-center justify-center">
			<img src="/coverframemaroonclassic.png" alt="Frame" class="object-contain transform -translate-y-[75px] sm:-translate-y-[28px]" />
		</div>
		
		<!-- Konten utama -->
		<div class="relative z-20 flex flex-col items-center h-full justify-between text-center">
			<!-- Title -->
			<h1 class="text-2xl font-reguler tracking-[6px] text-white m-0 mt-18 uppercase" style="font-family: 'Cinzel', serif;">PLEASE JOIN US !</h1>
			
			<!-- Photo container dengan frame oval -->
			<div class="relative flex flex-col items-center flex-1 justify-center -translate-y-[70px] sm:-translate-y-[20px]">
				<div class="relative w-[225px] sm:w-[280px] overflow-hidden shadow-xl">
					<img src="/coverimagemaroonclassic.png" alt="Wedding Couple" class="w-full h-full object-cover object-center" />
				</div>
				
				<!-- Nama pengantin overlay di atas foto -->
				<div class="absolute top-1/2 left-1/2 transform -translate-x-1/2 -translate-y-[160px] z-30 ">
					<h2 class="text-2xl text-white m-0 tracking-[2px] italic drop-shadow-lg" style="font-family: 'Kleymissky', cursive;">HINATA & NARUTO</h2>
				</div>
			</div>
			
			<!-- Tanggal -->
			<p class="text-base font-light text-white my-3 tracking-[2px] italic -translate-y-[130px] sm:-translate-y-[20px]" style="font-family: 'Kleymissky', cursive;">12 June 2025</p>

			<!-- Button -->
			<button 
				on:click={handleRedirect}
				class="bg-white text-red-900 border-none px-8 py-3 rounded-2xl text-sm font-medium tracking-wider cursor-pointer transition-all duration-300 mb-6 shadow-lg hover:bg-gray-100 hover:-translate-y-1 hover:shadow-xl active:translate-y-0 -translate-y-[130px] sm:-translate-y-[20px]" 
				style="font-family: 'Justink', cursive;"
			>
				Open Invitation
			</button>
		</div>
	</div>
</section>

