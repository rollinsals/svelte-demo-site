<script>
    import CtAs from "./CTAs.svelte";
    import ProductCard from "./ProductCard.svelte";
    import SectionWrapper from "./SectionWrapper.svelte";
    let productFeatures = [
        {
            featureList: ["Bad breath", "Terrible manners", "Wretched"],
            description: "Can't get in their range",
            imgURL: "assets/pic.jpeg",
        },
        {
            featureList: ["Total square", "Mundane taste"],
            description: "Middlebrow at best",
            imgURL: "assets/pic.jpeg",
        },
        {
            featureList: ["Good lord", "Horrible", "Can't stand"],
            description: "Unpleasant",
            imgURL: "assets/pic.jpeg",
        },
    ];
</script>

<SectionWrapper id="part1">
    <div
        class="flex flex-1 flex-col items-center justify-center gap-10 pb-10 sm:gap-14 md:gap-24 md:pb-14"
    >
        <div class="flex flex-col gap-2">
            <p class="text-center text-base opacity-60 sm:text-lg md:text-xl">
                We've got the <span class="font-semibold text-teal-600">
                    receipts
                </span>
            </p>
            <h3
                class="mx-auto w-full max-w-[1000px] text-center text-4xl font-semibold sm:text-5xl md:text-6xl"
            >
                Undeniable Allegations
            </h3>
        </div>

        {#each productFeatures as productFeature, index}
            <ProductCard {productFeature} {index}>
                {#if index === 0}
                    Truly Some Sordid <span class="font-medium text-teal-600"
                        >Business</span
                    >
                {:else if index === 1}
                    Total and Utter <span class="italic text-teal-600"
                        >Lechery</span
                    >
                {:else}
                    Completely Unbearable
                {/if}
            </ProductCard>
        {/each}
    </div>
</SectionWrapper>
