<script>
  import ReviewCard from '../ReviewCard.svelte';
  import SectionWrapper from '../common/SectionWrapper.svelte';
  import Stars from '../common/Stars.svelte';

  let lim = true;

  import { reviewsList } from '../../lib/data';
</script>

<SectionWrapper id="reviews">
  <div
    class="flex flex-col gap-10 sm:gap-14 md:gap-24 py-20 flex-1 items-center justify-center text-white"
  >
    <div class="flex flex-col gap-2">
      <p class="opacity-60 text-base sm:text-lg md:text-xl text-center">
        Don't just take our word for it
      </p>
      <h3
        class="text-3xl sm:text-4xl md:text-5xl max-w-[1000px] mx-auto w-full font-semibold text-center"
      >
        See What <span class="text-yellow-400">Others</span> Have To Say
      </h3>
    </div>
    <div class="flex flex-col md:flex-row gap-8 w-fit mx-auto">
      <div class="flex flex-col gap-8">
        {#each lim ? reviewsList.slice(0, 4) : reviewsList as reviewItem, index}
          <ReviewCard {reviewItem} left={true} {index} />
        {/each}
      </div>
      <div class="w-[1px] bg-gray-700 hidden md:flex"></div>
      <div class="flex flex-col gap-8">
        {#each lim ? reviewsList.slice(0, 4) : reviewsList as reviewItem, index}
          <ReviewCard {reviewItem} {index} />
        {/each}
      </div>
    </div>
    <button on:click={() => (lim = !lim)} class="specialBtn">
      <p>{lim ? 'Show More' : 'Show Less'}</p>
    </button>
    <div class="flex flex-col gap-10">
      <p class="mx-auto text-lg sm:text-xl md:text-2xl font-semibold">
        Trusted by 100+ Members
      </p>
      <Stars />
    </div>
  </div>
</SectionWrapper>
