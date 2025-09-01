<script lang="ts">
    import { ScrollArea } from "$lib/components/ui/scroll-area";
</script>

<div class="min-h-screen relative overflow-hidden">
    <img src="/coverimgclassicnatural.png" 
         class="absolute inset-0 w-full h-full object-cover object-bottom" 
         alt="">
    
    <h1 class="relative z-20 text-5xl tracking-[0.2em] translate-y-5 translate-x-10" style="font-family: 'Kenia Regular';">
        Gallery
    </h1>
    <ScrollArea class="sm:hidden absolute z-10 w-full h-screen top-0 left-0"> 
            <div class="flex flex-row gap-3">
                <div class="flex flex-row gap-3">
                    <div class="sm:w-[220px] h-[301px]">
                        <img src="/coverimgclassicnatural.png" alt="" class="w-full h-full object-cover">
                    </div>
                    <div class="w-[197px] h-[265px]">
                        <img src="/coverimgclassicnatural.png" alt="" class="w-full h-full object-cover">
                    </div>
                </div>
            </div>
            <div class="flex flex-row gap-3">
                <div class="w-[197px] h-[265px]">
                    <img src="/coverimgclassicnatural.png" alt="" class="w-full h-full object-cover">
                </div>
                <div class="w-[201px] h-[301px] translate-y-3">
                    <img src="/coverimgclassicnatural.png" alt="" class="w-full h-full object-cover">
                </div>
            </div>
            <div class="flex flex-row gap-3 items-end -translate-y-5">
                <div class="flex flex-row gap-3">
                    <div class="w-[220px] h-[258px]">
                        <img src="/coverimgclassicnatural.png" alt="" class="w-full h-full object-cover">
                    </div>
                    <div class="w-[201px] h-[301px]">
                        <img src="/coverimgclassicnatural.png" alt="" class="w-full h-full object-cover">
                    </div>
                </div>
            </div>
            <div class="flex flex-row gap-3 -translate-y-3">
                <div class="flex flex-col gap-3">
                    <div class="w-[200px] h-[225px]">
                        <img src="/coverimgclassicnatural.png" alt="" class="w-full h-full object-cover">
                    </div>
                    <div class="w-[200px] h-[220px] sm:w-[271px] sm:h-[225px]">
                        <img src="/coverimgclassicnatural.png" alt="" class="w-full h-full object-cover">
                    </div>
                </div>
                <div class="flex flex-col gap-3 justify-end">
                    <div class="w-[230px] h-[260px]">
                        <img src="/coverimgclassicnatural.png" alt="" class="w-full h-full object-cover">
                    </div>
                    <div class="w-[230px] h-[300px] sm:w-[359px] sm:h-[166px]">
                        <img src="/coverimgclassicnatural.png" alt="" class="w-full h-full object-cover">
                    </div>
                </div>
            </div>
    </ScrollArea>
    
    <div class="hidden sm:flex flex-col w-full items-center absolute top-30 z-10">
        <div class="flex flex-row gap-3">
            <div class="w-[220px] h-[301px]">
                <img src="/coverimgclassicnatural.png" alt="" class="w-full h-full object-cover">
            </div>
            <div class="w-[197px] h-[265px]">
                <img src="/coverimgclassicnatural.png" alt="" class="w-full h-full object-cover">
            </div>
            <div class="w-[197px] h-[265px]">
                <img src="/coverimgclassicnatural.png" alt="" class="w-full h-full object-cover">
            </div>
        </div>
        <div class="flex flex-row gap-3 items-end -translate-y-5">
            <div class="w-[220px] h-[258px]">
                <img src="/coverimgclassicnatural.png" alt="" class="w-full h-full object-cover">
            </div>
            <div class="w-[201px] h-[301px]">
                <img src="/coverimgclassicnatural.png" alt="" class="w-full h-full object-cover">
            </div>
            <div class="w-[201px] h-[301px] translate-y-3">
                <img src="/coverimgclassicnatural.png" alt="" class="w-full h-full object-cover">
            </div>
        </div>
        <div class="flex flex-row gap-3 -translate-y-3">
            <div class="flex flex-col gap-3">
                <div class="w-[271px] h-[225px]">
                    <img src="/coverimgclassicnatural.png" alt="" class="w-full h-full object-cover">
                </div>
                <div class="w-[271px] h-[225px]">
                    <img src="/coverimgclassicnatural.png" alt="" class="w-full h-full object-cover">
                </div>
            </div>
            <div class="flex flex-col gap-3 justify-end">
                <div class="w-[359px] h-[272px]">
                    <img src="/coverimgclassicnatural.png" alt="" class="w-full h-full object-cover">
                </div>
                <div class="w-[359px] h-[166px]">
                    <img src="/coverimgclassicnatural.png" alt="" class="w-full h-full object-cover">
                </div>
            </div>
        </div>
    </div>
</div>