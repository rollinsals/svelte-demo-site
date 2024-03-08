<script>
    import CtAs from "./CTAs.svelte";
    import Header from "./Header.svelte";
    import SectionWrapper from "./SectionWrapper.svelte";
</script>

<SectionWrapper>
    <Header />
    <div
        class="flex flex-col gap-10 flex-1 items-center justify-center pb-10 md:pb-14"
    >
        <h2
            class="text-5xl sm:text-6xl md:text-7xl lg:text-8xl max-w-[1200px] mx-auto w-full text-center"
        >
            Unlovable Fools <br /> Unforgettable
            <span class="text-teal-600">Lives</span>
        </h2>
        <p
            class="text-xl sm:text-2xl md:text-3xl text-center max-w-[[1000px] mx-auto w-full"
        >
            These bast*rds won't sleep. We can't wrangle them at all.
        </p>
        <CtAs />
        <div class="flex items-center justify-center gap-2 text-base">
            <p>4.3</p>
            {#each [0, 1, 2, 3, 4] as index}
                <div class="grid place-items-center relative">
                    <i class="fa-solid fa-eye opacity-0"></i>
                    <div
                        class={"absolute top-0 left-0 grid place-items-center " +
                            (index === 4 ? "w-[60%] overflow-hidden" : " ")}
                    >
                        <i class="fa-solid fa-eye text-amber-400"></i>
                    </div>
                </div>
            {/each}
            <p>We're watching</p>
        </div>
    </div></SectionWrapper
>
