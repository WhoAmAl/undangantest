<script lang="ts">
  import * as Accordion from "$lib/components/ui/accordion/index.js";
  let contents =[
    {   
        id : 1,
        title : 'Where It All Began',
        desc : 'Destiny brought us together in a place we never expected. Like something out of a fairy tale, our eyes met for the first time and time seemed to stand still. We may not have immediately realized that this simple encounter would change our lives forever, but there was something magical about that first smile, that casual conversation that lasted longer than it should have, and the warm feeling that grew as we got to know each other. ',   
    },
    {   
        id : 2,
        title : 'When Hearts Connected',
        desc : 'Destiny brought us together in a place we never expected. Like something out of a fairy tale, our eyes met for the first time and time seemed to stand still. We may not have immediately realized that this simple encounter would change our lives forever, but there was something magical about that first smile, that casual conversation that lasted longer than it should have, and the warm feeling that grew as we got to know each other. ',   
    },
    {   
        id : 3,
        title : 'Growing Together',
        desc : 'Destiny brought us together in a place we never expected. Like something out of a fairy tale, our eyes met for the first time and time seemed to stand still. We may not have immediately realized that this simple encounter would change our lives forever, but there was something magical about that first smile, that casual conversation that lasted longer than it should have, and the warm feeling that grew as we got to know each other. ',   
    }
  ];
</script>

<div class="min-h-screen sm:min-h-[1195px] text-neutral-950 flex flex-col items-center px-5 sm:px-10 justify-end relative" style="background-image: url(/coverimgclassicnatural.png); background-repeat: no-repeat; background-position: center; background-size: cover;">
    <h1 class="tracking-[0.25em] text-4xl sm:text-5xl text-center mb-10" style="font-family: 'Kenia Regular';">Our Love Story</h1>
    <Accordion.Root type="single" class="w-full mb-15" value="item-1">
        <Accordion.Item value="item-1" class='border-b-1 border-neutral-950 mb-4'>
            <Accordion.Trigger dontshowIcon={true} iconRotation={`-rotate-90`}
                class='uppercase text-xl border-b-1 border-neutral-950 px-5'>
                {contents[0].title}
                <svg width="18" height="18" viewBox="0 0 18 18" fill="none" xmlns="http://www.w3.org/2000/svg">
                    <path d="M-7.03744e-08 1.052L1.052 0L16.4732 15.3906V1.20468H18V18H1.20468V16.4732H15.3921L-7.03744e-08 1.052Z" 
                    fill="currentColor"/>
                </svg>
            </Accordion.Trigger>
            <Accordion.Content class="flex flex-col gap-4 text-center text-base sm:text-xl px-5">
            {contents[0].desc}
            </Accordion.Content>
        </Accordion.Item>
        <Accordion.Item value="item-2" class='border-b-1 border-neutral-950 mb-4'>
            <Accordion.Trigger dontshowIcon={true} iconRotation={`-rotate-90`}
                class='uppercase text-xl border-b-1 border-neutral-950 px-5'>
                {contents[1].title}
                <svg width="18" height="18" viewBox="0 0 18 18" fill="none" xmlns="http://www.w3.org/2000/svg">
                    <path d="M-7.03744e-08 1.052L1.052 0L16.4732 15.3906V1.20468H18V18H1.20468V16.4732H15.3921L-7.03744e-08 1.052Z" 
                    fill="currentColor"/>
                </svg>
            </Accordion.Trigger>
            <Accordion.Content class="flex flex-col gap-4 text-center text-base sm:text-xl px-5">
            {contents[1].desc}
            </Accordion.Content>
        </Accordion.Item>
        <Accordion.Item value="item-3" class='border-b-1 border-neutral-950'>
            <Accordion.Trigger dontshowIcon={true} iconRotation={`-rotate-90`}
                class='uppercase text-xl border-b-1 border-neutral-950 px-5 transition'>
                {contents[2].title}
                <svg width="18" height="18" viewBox="0 0 18 18" fill="none" xmlns="http://www.w3.org/2000/svg">
                    <path d="M-7.03744e-08 1.052L1.052 0L16.4732 15.3906V1.20468H18V18H1.20468V16.4732H15.3921L-7.03744e-08 1.052Z" 
                    fill="currentColor"/>
                </svg>
            </Accordion.Trigger>
            <Accordion.Content class="flex flex-col gap-4 text-center text-base sm:text-xl px-5">
            {contents[2].desc}
            </Accordion.Content>
        </Accordion.Item>
    </Accordion.Root>
</div>