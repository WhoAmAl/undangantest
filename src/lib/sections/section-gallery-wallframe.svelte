<script lang="ts">
    import * as Carousel from "$lib/components/ui/carousel/index.js";

    let pictures = [
        {
            id:1,
            icon: "/gallerypic1wallframe.png"
        },
        {
            id:2,
            icon: "/gallerypic1wallframe.png"
        },
        {
            id:3,
            icon: "/gallerypic1wallframe.png"
        },
        {
            id:4,
            icon: "/gallerypic1wallframe.png"
        },
        {
            id:5,
            icon: "/gallerypic1wallframe.png"
        },
        {
            id:6,
            icon: "/gallerypic1wallframe.png"
        }
    ];
</script>

<div class="min-h-screen sm:min-h-[1070px] flex flex-col items-end relative">
    <div class="w-[85%] h-[25%] sm:w-[85%] sm:h-[441px] shadow-2xl relative mt-3 z-1" style="background-image: url(/livestreampict1wallframe.png); background-repeat: no-repeat; background-position: center;">
        <img src="/galleryframewallframe.png" alt="" class="w-full h-full top-0 absolute object-cover z-2">
        <div class="w-full h-full absolute bg-[#A29683]/30"></div>
        <img src="/galleryvidwallframe.png" alt="" class="h-full w-full object-cover object-top">
        <button class="text-[#B0A695] absolute left-1/2 top-1/2 -translate-x-1/2 -translate-y-1/2 rounded-full p-1 hover:bg-black/20 transition z-10" aria-label="Play Video">
            <svg class="w-full h-auto max-w-[39px]" viewBox="0 0 39 39" fill="none" xmlns="http://www.w3.org/2000/svg" aria-hidden="true">
                <path d="M34.7747 7.38404C31.2086 2.88617 25.6875 0 19.4998 0C8.7311 0 0 8.73204 0 19.5C0 30.2688 8.73196 39 19.4998 39C26.5847 39 32.7861 35.2211 36.1965 29.5704C37.9776 26.6322 39 23.1829 39 19.4991C39 14.923 37.4229 10.7103 34.775 7.38249L34.7747 7.38404ZM27.2094 20.5698L16.9593 27.9354C16.7325 28.0983 16.4677 28.184 16.1932 28.184C15.4652 28.184 14.8731 27.5923 14.8731 26.8653V12.1347C14.8731 11.4076 15.4651 10.8159 16.1932 10.8159C16.4681 10.8159 16.7328 10.9016 16.9593 11.0642L27.2094 18.4301C27.5531 18.6771 27.758 19.0772 27.758 19.4999C27.7577 19.923 27.5524 20.3226 27.2094 20.5698Z" 
                fill="currentColor" />
            </svg>
        </button>
    </div>

    <div class="absolute left-0 top-1/2 -translate-y-15/24">
        <div class="w-full h-full absolute bg-[#A29683]/30"></div>
        <img src="/galleryimg1wallframe.png" alt="">
    </div>

    <div class="h-[380px] w-full sm:w-[89%] bg-[#776B5D] z-3 relative sm:ml-15 mt-6 sm:mt-10 px-6 py-7">
        <Carousel.Root class="w-full">
            <Carousel.Content>
                {#each pictures as item (item.id)}
                <Carousel.Item class=" basis-[200px] mx-2 flex flex-col items-center">
                    <div class="flex h-[320px] w-[200px] items-center justify-center overflow-hidden shadow">
                        <div class="bg-[#A29683]/30 w-[200px] h-[320px] absolute"></div>
                        <img src={item.icon} alt="" class="w-full h-full object-cover" />
                    </div>
                </Carousel.Item>
                {/each}
            </Carousel.Content>
        </Carousel.Root>
    </div>

    <div class="hidden sm:block absolute bottom-20 left-10 w-[442px] h-[142px]">
        <div class="w-full h-full absolute bg-[#A29683]/30"></div>
        <img src="/galleryimg2wallframe.png" alt="" class="w-full h-full object-cover">
    </div>
</div>