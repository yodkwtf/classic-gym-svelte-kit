<script>
  import ProductCard from '../ProductCard.svelte';
  import SectionWrapper from '../common/SectionWrapper.svelte';

  import { productFeatures } from '../../lib/data';
</script>

<SectionWrapper id="product">
  <div
    class="flex flex-col gap-10 sm:gap-14 md:gap-24 flex-1 items-center justify-center pb-10 md:pb-14 text-white"
  >
    <div class="flex flex-col gap-2">
      <p class="opacity-60 text-base sm:text-lg md:text-xl text-center">
        Start your lifetime <span class="text-yellow-400">gym streak</span> today
      </p>
      <h3
        class="text-3xl sm:text-4xl md:text-5xl max-w-[1000px] mx-auto w-full font-semibold text-center"
      >
        Fitness For <span class="text-yellow-400">Everyone</span>
      </h3>
    </div>

    {#each productFeatures as feature, index}
      <ProductCard productFeature={feature} {index}>
        {#if index === 0}
          Experience a beginner exercise <span
            class="text-yellow-400 font-medium">master</span
          > class
        {:else if index === 1}
          Lay the foundations for <span class="text-yellow-400 font-medium"
            >routine</span
          > and consistency
        {:else}
          Workouts specific to your <span class="text-yellow-400 font-medium"
            >environment</span
          >
          and
          <span class="text-yellow-400 font-medium">expertise</span>
        {/if}
      </ProductCard>
    {/each}
  </div>
</SectionWrapper>
