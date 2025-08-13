<script lang="ts">
  import * as Accordion from "$lib/components/ui/accordion/index.js";
</script>

<div class="bg-neutral-950 min-h-screen sm:min-h-[165vh] xl:min-h-screen flex flex-col items-center relative" style="background-image: url(/bgstoryretroclassic.png); background-size: cover; background-position: center; background-repeat: no-repeat; font-family: 'Jomolhari', serif;">
    <div class="absolute inset-0 bg-neutral-700" style="opacity:0.7;"></div>
        <!-- CONTENT HEADER -->
    <div class="relative w-full pt-4 md:pt-8 px-6 lg:px-10 text-center">
        <div class="text-neutral-50 text-base lg:text-xl tracking-widest mb-1 lg:mb-2" style="font-family: 'Jomolhari', serif;">OUR LOVE</div>
        <div class="text-neutral-50 text-4xl lg:text-7xl tracking-[0.2em] mb-2" style="font-family: 'Jomolhari', serif;">STORY</div>
    </div>
    <!-- ACCORDION SHADCN -->
    <Accordion.Root type="single" class="text-white relative w-full max-w-[90%]" value="item-1">
        <Accordion.Item value="item-1">
            <Accordion.Trigger class="md:text-2xl border-b-2 md:border-b-3 border-white mb-1 md:mb-4">WHERE IT ALL BEGAN</Accordion.Trigger>
            <Accordion.Content class="flex flex-col gap-4 text-balance text-justify text-[16px] md:text-[20px] lg:text-[22.5px]" style="font-family: 'Baskervville', serif;">
            <p>
                Destiny brought us together in a place we never expected. Like something out of a fairy tale, our eyes met for the first time and time seemed to stand still. We may not have immediately realized that this simple encounter would change our lives forever, but there was something magical about that first smile, that casual conversation that lasted longer than it should have, and the warm feeling that grew as we got to know each other. 
            </p>
            </Accordion.Content>
        </Accordion.Item>
        <Accordion.Item value="item-2">
            <Accordion.Trigger class="md:text-2xl border-b-2 md:border-b-3 border-white mb-1 md:mb-4">DISCOVERING EACH OTHER</Accordion.Trigger>
            <Accordion.Content class="flex flex-col gap-4 text-balance text-justify text-[16px] md:text-[20px] lg:text-[22.5px]" style="font-family: 'Baskervville', serif;">
            <p>
                Destiny brought us together in a place we never expected. Like something out of a fairy tale, our eyes met for the first time and time seemed to stand still. We may not have immediately realized that this simple encounter would change our lives forever, but there was something magical about that first smile, that casual conversation that lasted longer than it should have, and the warm feeling that grew as we got to know each other. 
            </p>
            </Accordion.Content>
        </Accordion.Item>
        <Accordion.Item value="item-3">
            <Accordion.Trigger class="md:text-2xl border-b-2 md:border-b-3 border-white mb-1 md:mb-4">WHEN HEARTS CONNTECTED</Accordion.Trigger>
            <Accordion.Content class="flex flex-col gap-4 text-balance text-justify text-[16px] md:text-[20px] lg:text-[22.5px]" style="font-family: 'Baskervville', serif;">
            <p>
               Destiny brought us together in a place we never expected. Like something out of a fairy tale, our eyes met for the first time and time seemed to stand still. We may not have immediately realized that this simple encounter would change our lives forever, but there was something magical about that first smile, that casual conversation that lasted longer than it should have, and the warm feeling that grew as we got to know each other. 
            </p>
            </Accordion.Content>
        </Accordion.Item>
        <Accordion.Item value="item-4">
            <Accordion.Trigger class="md:text-2xl border-b-2 md:border-b-3 border-white mb-1 md:mb-4">GROWING TOGETHER</Accordion.Trigger>
            <Accordion.Content class="flex flex-col gap-4 text-balance text-justify text-[16px] md:text-[20px] lg:text-[22.5px]" style="font-family: 'Baskervville', serif;">
            <p>
                Destiny brought us together in a place we never expected. Like something out of a fairy tale, our eyes met for the first time and time seemed to stand still. We may not have immediately realized that this simple encounter would change our lives forever, but there was something magical about that first smile, that casual conversation that lasted longer than it should have, and the warm feeling that grew as we got to know each other. 
            </p>
            </Accordion.Content>
        </Accordion.Item>
    </Accordion.Root>
</div>