<script>
  function handleRedirect() {
    window.location.href = '/elegantlime';
  }
</script>

<!-- CONTAINER WORDS -->
<div class="flex flex-col items-center justify-center mx-auto max-w-2xl relative pt-15">
 <div class="text-center mb-8">
     <div class="text-[14px] md:text-xl text-lime-950 tracking-wide mb-0" style="font-family: 'Libre Caslon', serif;">THE</div>
     <div class="text-[23px] md:text-3xl text-lime-950 tracking-wide font-semibold mb-3 md:mb-8" style="font-family: 'Libre Caslon', serif;">WEDDING</div>
     <div class="text-[28px] md:text-5xl text-lime-950" style="font-family: 'Rouge Script', serif;">Naruto &amp; Hinata</div>
 </div>
</div>
<!-- FRAME -->
<div class="mx-auto max-w-2xl min-h-[470px] md:min-h-[945px] relative flex flex-col justify-center rounded-t-[350px] bg-[position:bottom] md:bg-[position:center]" style="background-image: url(/landingelegantlime.png); background-size: contain; background-repeat: no-repeat; background-attachment: fixed; font-family: 'Libre Caslon', serif;">
  <button
        class="absolute left-1/2 transform -translate-x-1/2 bottom-10 z-40 focus:outline-none"
        style="width:80px; height:80px; background:transparent;"
        aria-label="Play"
        on:click={handleRedirect}
    >
        <svg width="60" height="60" viewBox="0 0 80 80" fill="none" xmlns="http://www.w3.org/2000/svg">
            <circle cx="40" cy="40" r="38" fill="#FAFAFA"/>
            <circle cx="40" cy="40" r="38" fill="#FAFAFA"/>
            <polygon points="34,28 34,52 54,40" fill="#8A963A"/>
            <circle cx="40" cy="40" r="22" fill="transparent"/>
        </svg>
  </button>

  <div class="bottom-0 right-0 absolute text-right pb-9 pr-8 text-gray-50">
      <div class="text-[12px] md:text-lg" style="font-family: 'Libre Caslon', serif;">Dear</div>
      <div class="text-[14px] md:text-xl" style="font-family: 'Libre Caslon', serif;">Alan and Partner</div>
  </div>
</div>

<style></style>