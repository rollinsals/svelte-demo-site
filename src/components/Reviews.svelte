<script>
    import CtAs from "./CTAs.svelte";
    import ReviewCard from "./ReviewCard.svelte";
    import SectionWrapper from "./SectionWrapper.svelte";

    let lim = true;
    let reviewsList = [
        {
            name: "Lil Baphomet",
            review: "Real nasty stuff. I wouldn't touch it with a 5 foot pole.",
        },
        { name: "Rootin' Tootin' Randal", review: "Not so bad. 5 stars" },
        {
            name: "Qi Gon Jerk",
            review: "Lambast them. Tear them asunder. May the fires of hell consumes theme",
        },
        { name: "Goochi", review: "Excellent content here" },
        {
            name: "Rumplestiltzkin",
            review: "You'll never find me here",
        },
    ];
</script>

<SectionWrapper id="part2">
    <div
        class="flex flex-1 flex-col items-center justify-center gap-10 py-20 sm:gap-14 md:gap-24"
    >
        <div class="flex flex-col gap-2">
            <p>Don't just take our word for it</p>
            <h3
                class="mx-auto w-full max-w-[1000px] text-center text-4xl font-semibold sm:text-5xl md:text-6xl"
            >
                Just check out this hot gossip
            </h3>
        </div>
        <div class="mx-auto flex w-fit flex-col gap-8 md:flex-row">
            <div class="flex flex-col gap-8">
                {#each lim ? reviewsList.slice(0, 4) : reviewsList as reviewItem, index}
                    <ReviewCard {reviewItem} left={true} {index} />
                {/each}
            </div>
            <div class="hidden w-[1px] bg-slate-950 md:flex"></div>
            <div class="flex flex-col gap-8">
                {#each lim ? reviewsList.slice(0, 4) : reviewsList as reviewItem, index}
                    <ReviewCard {reviewItem} {index} />
                {/each}
            </div>
        </div>
        <button on:click={() => (lim = !lim)} class="spbtn"
            ><p>{lim ? "Show More" : "Show Less"}</p>
        </button>
    </div>
</SectionWrapper>
