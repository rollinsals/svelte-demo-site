<script>
    import CtAs from "./CTAs.svelte";
    import SectionWrapper from "./SectionWrapper.svelte";

    let faqs = [
        {
            question: "Really?",
            ans: "Yeah, absolutely",
        },
        {
            question: "No, but seriously",
            ans: "It's true",
        },
        {
            question: "I can't believe it",
            ans: "That isn't a question",
        },
        {
            question: "How do I get out of here?",
            ans: "You can't",
        },
    ];
</script>

<SectionWrapper id="part3">
    <div
        class="flex flex-1 flex-col items-center justify-center gap-10 py-20 sm:gap-14 md:gap-24"
    >
        <div class="flex flex-col gap-2">
            <p>Now onto more</p>
            <h3
                class="mx-auto w-full max-w-[1000px] text-center text-4xl font-semibold sm:text-5xl md:text-6xl"
            >
                Gross Misconduct
            </h3>
        </div>
        <div class="flex w-full flex-col gap-8 sm:gap-10 md:gap-14">
            {#each faqs as faq}
                <div
                    class="relative mx-auto flex w-full max-w-[800px] flex-col gap-2 px-6 text-left"
                >
                    <div
                        class="absolute left-0 top-0 h-[1px] w-1/3 -translate-x-4"
                    >
                        <i class="fa-solid fa-circle-question text-teal-800"
                        ></i>
                    </div>
                    <div
                        class="absolute left-0 top-0 h-full w-[1px] translate-x-2 bg-slate-950"
                    ></div>
                    <h4 class="pt-2 text-lg sm:text-xl md:text-2xl">
                        {faq.question}
                    </h4>
                    <p class="pl-2">{faq.ans}</p>
                </div>
            {/each}
        </div>
    </div>
</SectionWrapper>
