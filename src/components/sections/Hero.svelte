<script>
  import CTAs from '../common/CTAs.svelte';
  import Header from '../layout/Header.svelte';
  import SectionWrapper from '../common/SectionWrapper.svelte';
  import Stars from '../common/Stars.svelte';
</script>

<SectionWrapper>
  <Header />
  <div
    class="flex flex-col gap-10 flex-1 items-center justify-center pb-10 md:pb-14 text-white"
  >
    <h2
      class="text-4xl sm:text-5xl md:text-6xl lg:text-7xl mx-auto w-full text-center max-w-[1200px] font-bold"
    >
      <span class="text-yellow-400">Gym</span> Training
      <span class="text-gray-400 line-through">Is Hard</span><br />
      <div class="mt-2"
        >Just Got <span class="text-yellow-400">Easier</span></div
      >
    </h2>

    <p
      class="text-lg sm:text-xl md:text-2xl mx-auto w-full text-center max-w-[1000px]"
    >
      Less thinking, more lifting. Get the best results with a professional
      trainer full of <span class="italic"
        >personalized workouts, exercise explanations, diet plans</span
      > and much more.
    </p>

    <CTAs />
    <Stars />
  </div>
</SectionWrapper>
