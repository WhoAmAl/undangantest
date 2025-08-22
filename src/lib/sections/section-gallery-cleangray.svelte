<script lang="ts">
    import { ScrollArea } from "$lib/components/ui/scroll-area";
</script>

<div class="min-h-screen sm:min-h-[1195px] relative py-15 
    bg-cover bg-center bg-no-repeat" 
    style="background-image: url(/covercleangray.png)">
    
    <!-- overlay -->
    <div class="absolute inset-0 bg-neutral-100/64 flex flex-col items-center p-3 sm:p-6"></div>

    <!-- versi mobile: ScrollArea -->
    <div class="relative block sm:hidden">
        <h1 class="text-center text-plate-700 text-5xl" style="font-family: 'Tangerine';">Our Gallery</h1>
        <ScrollArea class="w-full h-[500px] px-2">
            <div class="flex flex-col gap-2">
                <!-- baris 1 -->
                <div class="flex flex-row items-end gap-2">
                    <div class="w-[162px] h-[192px] -translate-y-5">
                        <img src="/gallery1cleangray.png" class="h-full w-full object-cover" />
                    </div>
                    <div class="w-[200px] h-[250px]">
                        <img src="/covercleangray.png" class="h-full w-full object-cover">
                    </div>
                </div>
                <!-- baris 2 -->
                <div class="flex flex-row items-start gap-2">
                    <div class="w-[148px] h-[145px] -translate-y-10 translate-x-4">
                        <img src="/gallery3cleangray.png" class="h-full w-full object-cover">
                    </div>
                    <div class="w-[258px] h-[172px] -translate-y-4">
                        <img src="/covercleangray.png" class="h-full w-full object-cover">
                    </div>
                </div>
                <!-- baris 3 -->
                <div class="flex flex-col items-center gap-2 -translate-y-6">
                    <div class="flex flex-row items-start gap-2">
                        <div class="w-[148px] h-[145px]">
                            <img src="/gallery5cleangray.png" class="h-full w-full object-cover">
                        </div>
                        <div class="w-[193px] h-[234px]">
                            <img src="/covercleangray.png" class="h-full w-full object-cover">
                        </div>
                    </div>
                    <div class="w-[247px] h-[172px] -translate-y-12">
                        <img src="/gallery7cleangray.png" class="h-full w-full object-cover">
                    </div>
                </div>
                <!-- baris 4 -->
                <div class="flex flex-col items-center gap-2 -translate-y-20">
                    <div class="flex flex-row justify-center items-start gap-6">
                        <div class="w-[181px] h-[177px]">
                            <img src="/gallery8cleangray.png" class="h-full w-full object-cover">
                        </div>
                        <div class="w-[171px] h-[202px] translate-x-2">
                            <img src="/gallery10cleangray.png" class="h-full w-full object-cover">
                        </div>
                    </div>
                    <div class="w-[205px] h-[234px] -translate-y-8">
                        <img src="/covercleangray.png" class="h-full w-full object-cover">
                    </div>
                </div>
                <!-- baris 5 -->
                <div class="flex flex-row justify-between items-center -translate-y-25 gap-2">
                    <div class="w-[200px] h-[200px]">
                        <img src="/covercleangray.png" class="h-full w-full object-cover">
                    </div>
                    <div class="w-[200px] h-[200px]">
                        <img src="/covercleangray.png" class="h-full w-full object-cover">
                    </div>
                </div>
            </div>
        </ScrollArea>
    </div>

    <!-- versi desktop: layout asli -->
    <div class="relative hidden sm:flex flex-col">
        
        <!-- baris pertama -->
        <div class="flex flex-row justify-center gap-4">
            <div class="flex flex-row items-end justify-center">
                <div class="w-[162px] h-[192px] translate-x-8 -translate-y-6">
                    <img src="/gallery1cleangray.png" class="h-full w-full object-cover">
                </div>
                <div class="w-[250px] h-[333px] translate-x-12">
                    <img src="/covercleangray.png" class="h-full w-full object-cover">
                </div>
            </div>
            <div class="flex flex-col gap-4 items-center">
                <div class="w-[148px] h-[145px] translate-y-10">
                    <img src="/gallery3cleangray.png" class="h-full w-full object-cover">
                </div>
                <div class="w-[258px] h-[172px] translate-y-15 -translate-x-6">
                    <img src="/covercleangray.png" class="h-full w-full object-cover">
                </div>
            </div>
        </div>

        <!-- baris kedua -->
        <div class="flex flex-row justify-center items-end gap-4 translate-y-2">
            <div class="w-[148px] h-[145px]">
                <img src="/gallery5cleangray.png" class="h-full w-full object-cover">
            </div>
            <div class="w-[193px] h-[234px]">
                <img src="/covercleangray.png" class="h-full w-full object-cover">
            </div>
            <div class="w-[247px] h-[172px] translate-y-10">
                <img src="/gallery7cleangray.png" class="h-full w-full object-cover">
            </div>
        </div>

        <!-- baris ketiga -->
        <div class="flex flex-row justify-center items-end gap-4 translate-y-8">
            <div class="flex flex-row justify-center items-start gap-6">
                <div class="w-[181px] h-[177px]">
                    <img src="/gallery8cleangray.png" class="h-full w-full object-cover">
                </div>
                <div class="w-[205px] h-[234px]">
                    <img src="/covercleangray.png" class="h-full w-full object-cover">
                </div>
            </div>
            <div class="w-[171px] h-[202px] translate-x-2">
                <img src="/gallery10cleangray.png" class="h-full w-full object-cover">
            </div>
        </div>

        <!-- baris keempat -->
        <div class="flex flex-row justify-center items-end gap-6">
            <div class="w-[257px] h-[277px]">
                <img src="/covercleangray.png" class="h-full w-full object-cover">
            </div>
            <div class="w-[333px] h-[222px]">
                <img src="/covercleangray.png" class="h-full w-full object-cover">
            </div>
        </div>
    </div>
</div>
