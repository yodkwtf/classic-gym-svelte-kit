<script>
  import SectionWrapper from '../common/SectionWrapper.svelte';

  import { faqs } from '../../lib/data';
</script>

<SectionWrapper id="faqs">
  <div
    class="flex flex-col gap-10 sm:gap-14 md:gap-24 py-20 flex-1 items-center justify-center text-white"
  >
    <div class="flex flex-col gap-2">
      <p class="opacity-60 text-base sm:text-lg md:text-xl text-center">
        For all your questions, qualms & queries
      </p>
      <h3
        class="text-4xl sm:text-5xl md:text-6xl max-w-[1000px] mx-auto w-full font-semibold text-center"
      >
        Frequently Asked Questions
      </h3>
    </div>
    <div class="flex flex-col gap-8 sm:gap-10 md:gap-14 w-full">
      {#each faqs as faq}
        <div
          class="flex flex-col gap-2 text-left max-w-[800px] w-full mx-auto relative p-4 px-6 border border-solid border-gray-700 rounded"
        >
          <div
            class="absolute top-0 left-0 w-1/3 h-[1px] bg-gray-700 -translate-x-4"
          ></div>
          <div
            class="absolute top-0 left-0 h-2/3 w-[1px] bg-gray-700 -translate-y-4"
          ></div>
          <h4 class="text-lg sm:text-xl md:text-2xl pt-2">
            {faq.question}
          </h4>
          <p class="pl-2">{faq.ans}</p>
        </div>
      {/each}
    </div>
  </div>
</SectionWrapper>
