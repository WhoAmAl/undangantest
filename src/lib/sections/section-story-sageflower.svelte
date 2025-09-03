<script lang="ts">
    import {
        Carousel,
        CarouselContent,
        CarouselItem,
    } from "@/components/ui/carousel";

    let slides = [
        {
            title: "Where It All Began",
            content: `Destiny brought us together in a place we never expected. Like something out of a fairy tale, our eyes met for the first time and time seemed to stand still. We may not have immediately realized that this simple encounter would change our lives forever, but there was something magical about that first smile, that casual conversation that lasted longer than it should have, and the warm feeling that grew as we got to know each other.`
        },
        {
            title: "Where It All Began 2",
            content: `Destiny brought us together in a place we never expected. Like something out of a fairy tale, our eyes met for the first time and time seemed to stand still. We may not have immediately realized that this simple encounter would change our lives forever, but there was something magical about that first smile, that casual conversation that lasted longer than it should have, and the warm feeling that grew as we got to know each other.`
        },
        {
            title: "Where It All Began 3",
            content: `Destiny brought us together in a place we never expected. Like something out of a fairy tale, our eyes met for the first time and time seemed to stand still. We may not have immediately realized that this simple encounter would change our lives forever, but there was something magical about that first smile, that casual conversation that lasted longer than it should have, and the warm feeling that grew as we got to know each other.`
        },
        {
            title: "Where It All Began 4",
            content: `Destiny brought us together in a place we never expected. Like something out of a fairy tale, our eyes met for the first time and time seemed to stand still. We may not have immediately realized that this simple encounter would change our lives forever, but there was something magical about that first smile, that casual conversation that lasted longer than it should have, and the warm feeling that grew as we got to know each other.`
        },
        {
            title: "Where It All Began 5",
            content: `Destiny brought us together in a place we never expected. Like something out of a fairy tale, our eyes met for the first time and time seemed to stand still. We may not have immediately realized that this simple encounter would change our lives forever, but there was something magical about that first smile, that casual conversation that lasted longer than it should have, and the warm feeling that grew as we got to know each other.`
        },
    ];

    import type { CarouselAPI } from "$lib/components/ui/carousel/context.js";
    let carouselapi = $state<CarouselAPI>();
    // const count = $derived(api ? api.scrollSnapList().length : 0);
    let current = $state(0);
    $effect(() => {
    if (carouselapi) {
        current = carouselapi.selectedScrollSnap() + 1;
        carouselapi.on("select", () => {
            current = carouselapi!.selectedScrollSnap() + 1;
        });
        }
    });

    function handleCarouselAPI (api: any) {
        carouselapi = api;
        if( !carouselapi ) {
            return; 
        }
        carouselapi.on("select", () => {
            current = carouselapi!.selectedScrollSnap();
        });
        current = carouselapi.selectedScrollSnap();
    }
</script>

<div class="flex flex-col items-center relative pb-20">
    <div class="h-auto w-[190px] sm:h-[387px] sm:w-[267px] absolute bottom-0 left-0 z-10">
        <img src="/leftwishsageflower.png" alt="" class="w-full h-full object-cover">
    </div>
    <div class="h-auto w-[190px] sm:h-[387px] sm:w-[267px] absolute bottom-0 right-0 z-10">
        <img src="/wishrightsageflower.png" alt="" class="w-full h-full object-cover">
    </div>
    <h1 class="text-5xl sm:text-[64px] pt-15" style="font-family: 'Manstein Regular';">Our Love Story</h1>
    
    <Carousel setApi={handleCarouselAPI}>
        <CarouselContent>
            {#each slides as slide}
            <CarouselItem>
                <h1 class="text-2xl mt-15 mb-10 tracking-[0.2em] w-full text-center" style="font-family: 'Cinzel Bold';">{slide.title}</h1>
                <div class="w-full relative flex flex-col items-center">
                    <svg viewBox="0 0 586 419" fill="none" xmlns="http://www.w3.org/2000/sv"
                        class="w-full h-[280px] sm:h-[419px]"
                    >
                        <mask id="mask0_1253_2263" style="mask-type:luminance" maskUnits="userSpaceOnUse" x="0" y="0" width="586" height="419">
                            <path d="M586 0V419H0.138V0H586Z" 
                            fill="currentColor"/>
                        </mask>
                        <g mask="url(#mask0_1253_2263)">
                            <path fill-rule="evenodd" clip-rule="evenodd" d="M69.3235 349.45V387.338L73.0366 391.407C85.6776 392.568 95.7589 402.65 96.9238 415.287L97.2648 419H488.868L489.209 415.287C490.374 402.65 500.451 392.568 513.1 391.407L516.809 391.066V349.45C523.553 344.974 585.957 301.38 585.957 221.093V197.903C585.957 117.62 523.553 74.0259 516.809 69.5504V27.9336L513.1 27.5926C500.451 26.4315 490.374 16.354 489.209 3.71298L488.868 0H485.139C452.47 0 133.659 0 100.989 0H97.2648L96.9238 3.71298C95.7589 16.354 85.6776 26.4315 73.0366 27.5926L69.3235 27.9336V69.5504C62.5797 74.0259 0.175476 117.62 0.175476 197.903V221.093C0.175476 301.38 62.5797 344.974 69.3235 349.45ZM77.4929 383.817V348.771C77.4929 346.396 76.2744 344.185 74.2627 342.92C74.2627 342.92 8.34479 301.384 8.34479 221.093V197.903C8.34479 117.616 74.2627 76.0798 74.2627 76.0798C76.2744 74.8114 77.4929 72.6043 77.4929 70.2286V35.1833C91.0612 32.4283 101.759 21.7338 104.515 8.16933C104.515 8.16933 443.258 8.16933 481.618 8.16933C484.373 21.7338 495.071 32.4283 508.64 35.1833C508.64 46.7093 508.64 70.2286 508.64 70.2286C508.64 72.6043 509.858 74.8114 511.87 76.0798C511.87 76.0798 577.784 117.616 577.784 197.903V221.093C577.784 301.384 511.87 342.92 511.87 342.92C509.858 344.185 508.64 346.396 508.64 348.771V383.817C495.071 386.576 484.373 397.266 481.618 410.827H104.515C101.759 397.266 91.0612 386.576 77.4929 383.817ZM109.91 405.378C108.626 391.461 97.5292 380.364 83.6046 379.084V342.307C83.6046 341.38 83.1294 340.518 82.3439 340.023C82.3439 340.023 17.6675 299.303 17.6675 220.557V198.443C17.6675 119.697 82.3439 78.9766 82.3439 78.9766C83.1294 78.4823 83.6046 77.6201 83.6046 76.6928V39.9155C97.5292 38.6357 108.626 27.5389 109.91 13.6219C141.062 13.6219 445.071 13.6219 476.227 13.6219C477.507 27.5389 488.603 38.6357 502.528 39.9155C502.528 48.6596 502.528 76.6928 502.528 76.6928C502.528 77.6201 503.003 78.4823 503.789 78.9766C503.789 78.9766 568.465 119.697 568.465 198.443V220.557C568.465 299.303 503.789 340.023 503.789 340.023C503.003 340.518 502.528 341.38 502.528 342.307V379.084C488.603 380.364 477.507 391.461 476.227 405.378H109.91ZM112.749 402.11C110.304 389.02 99.97 378.69 86.873 376.245V342.307C86.873 340.257 85.8193 338.349 84.0835 337.261C84.0835 337.261 20.936 297.472 20.936 220.557V198.443C20.936 121.528 84.0835 81.7393 84.0835 81.7393C85.8193 80.6472 86.873 78.7428 86.873 76.6928V42.7549C99.97 40.314 110.304 29.9798 112.749 16.8866H473.384C475.828 29.9798 486.162 40.314 499.259 42.7549C499.259 53.5451 499.259 76.6928 499.259 76.6928C499.259 78.7428 500.313 80.6472 502.049 81.7393C502.045 81.7393 565.197 121.528 565.197 198.443V220.557C565.197 297.472 502.045 337.261 502.045 337.261C500.313 338.349 499.259 340.257 499.259 342.307V376.245C486.162 378.686 475.828 389.02 473.384 402.11H112.749Z" 
                            fill="currentColor"/>
                        </g>
                    </svg>
                    <h1 class="absolute text-[14px] sm:text-[20px] text-center top-12 sm:top-20 px-40 sm:px-31.5" style="font-family: 'Times New Roman', Times, serif; font-style: italic;">{slide.content}</h1>
                </div>
            </CarouselItem>
            {/each}
        </CarouselContent>
    </Carousel>

    <!-- pagination dot -->
    <div class="flex justify-center gap-2 md:gap-2 my-5 sm:my-10">
        {#each slides as _, index}
            <button
                class="w-2 h-2 md:w-3 md:h-3 rounded-full transition-all duration-300 focus:outline-none focus:ring-2
                    {index === current - 1
                        ? 'bg-green-950 scale-110'
                        : 'bg-[#F6F1DE] hover:bg-gray-700 hover:scale-105'}"
                onclick={() => carouselapi && carouselapi.scrollTo(index)}
                aria-label={`Go to story ${index + 1}`}
            ></button>
        {/each}
    </div>
</div>
