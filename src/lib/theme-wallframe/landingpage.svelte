<script>
    import LandingPage from '../sections/section-landing-wallframe.svelte';
    function handleRedirect (){
        window.location.href = '/wallframe';
    }
</script>

<main id="wallframe" class="max-w-2xl mx-auto relative bg-[#B0A695] text-[#EBE3D5]" on:click={handleRedirect}>
    <img src="/texturewallframe.png" alt="" class="w-full h-full absolute object-cover z-100">
    <LandingPage />
</main>