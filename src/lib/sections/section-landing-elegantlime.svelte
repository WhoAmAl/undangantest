<script>
  let scrolled = false;
  function scrollSvgUp() {
    scrolled = true;
    setTimeout(() => {
      handleRedirect();
    }, 800);
  }
  function handleRedirect() {
    window.location.href = '/elegantlime';
  }

</script>

<style>

.svg-scroll {
    transition: transform 0.9s cubic-bezier(0,0,0,0);
    will-change: transform;
  }
  .svg-scrolled {
    transform: translateY(-700px);
  }
  .dear-container {
    position: absolute;
    bottom: 0;
    right: 0;
    padding: 2.5rem;
    text-align: right;
    z-index: 30;
    width: auto;
    transition: all 0.9s cubic-bezier(0,0,0,0);
    display: flex;
    flex-direction: column;
    align-items: flex-end;
  }
  .dear-container.centered {
    left: 50%;
    bottom: 0;
    right: auto;
    transform: translateX(-50%);
    align-items: center;
    text-align: center;
  }
  .dear-text.gray {
    color: #f9fafb;
    transition: color 0.9s cubic-bezier(0,0,0,0);
    }
  .dear-text.lime {
    color: #365314;
    transition: color 0.9s cubic-bezier(0,0,0,0);
  }
</style>

<div class="bg-gray-50 mx-auto max-w-2xl min-h-screen relative" style="background-image: url(/landingelegantlime.png); background-size: cover; background-position: center; bg-repeat: no-repeat;">
    <!-- layer svg inverted rounded + konten judul ikut scroll -->
    <div class="relative w-full max-w-2xl mx-auto svg-scroll {scrolled ? 'svg-scrolled' : ''}">
        <div class="absolute top-0 left-0 w-full flex flex-col items-center justify-center pt-16 z-20 pointer-events-none">
            <div class="text-center">
                <div class="text-xl text-lime-950 tracking-wide mb-0">THE</div>
                <div class="text-3xl text-lime-950 tracking-wide mb-13">WEDDING</div>
                <div class="text-2xl text-lime-950">Naruto &amp; Hinata</div>
            </div>
        </div>
        <svg
            class="w-full h-auto z-10"
            viewBox="0 0 672 614"
            fill="none"
            xmlns="http://www.w3.org/2000/svg"
            style="pointer-events: none; display: block;"
        >
            <path
                d="M672 614H671.954C671.984 612.17 672 610.337 672 608.5C672 423.208 521.568 273 336 273C150.432 273 0 423.208 0 608.5C0 610.337 0.0164441 612.17 0.0458984 614H0V0H672V614Z"
                fill="#FAFAFA"
            />
        </svg>

        <!-- layer svg bawah -->
        <svg
            class="w-full h-auto translate-y-365 md:translate-y-380 svg-scroll {scrolled ? 'svg-scrolled' : ''}"
            viewBox="0 0 672 473"
            fill="none"
            xmlns="http://www.w3.org/2000/svg"
            style="pointer-events: none;"
        >
            <path
                d="M672 0C672 185.568 521.568 336 336 336C150.432 336 0 185.568 0 0V473H672V0Z"
                fill="#FAFAFA"
            />
        </svg>
    </div>
    <div class="dear-container {scrolled ? 'centered' : ''}">
        <div class="dear-text text-lg leading-tight {scrolled ? 'lime' : 'gray'}">Dear</div>
        <div class="dear-text text-xl font-serif leading-tight {scrolled ? 'lime' : 'gray'}">Alan and Partner</div>
    </div>
    {#if !scrolled}
    <button
        class="absolute left-1/2 transform -translate-x-1/2 bottom-10 z-40 focus:outline-none"
        style="width:80px; height:80px; background:transparent;"
        aria-label="Play"
        on:click={scrollSvgUp}
    >
        <svg width="60" height="60" viewBox="0 0 80 80" fill="none" xmlns="http://www.w3.org/2000/svg">
            <circle cx="40" cy="40" r="38" fill="#FAFAFA"/>
            <circle cx="40" cy="40" r="38" fill="#FAFAFA"/>
            <polygon points="34,28 34,52 54,40" fill="#8A963A"/>
            <circle cx="40" cy="40" r="22" fill="transparent"/>
        </svg>
    </button>
    {/if}
</div>