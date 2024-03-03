<script>
  import CTAs from '../common/CTAs.svelte';
  import Header from '../layout/Header.svelte';
  import SectionWrapper from '../common/SectionWrapper.svelte';
  import Stars from '../common/Stars.svelte';
</script>

<SectionWrapper>
  <Header />
  <div
    class="flex flex-col gap-10 flex-1 items-center justify-center pb-10 md:pb-14"
  >
    <h2
      class="text-5xl sm:text-6xl md:text-7xl lg:text-8xl mx-auto w-full text-center max-w-[1200px] font-bold"
    >
      <span class="text-indigo-400">Gym</span> Training
      <span class="text-slate-600 line-through">Is Hard</span><br />
      Just Got <span class="text-indigo-400">Easier</span>
    </h2>

    <p
      class="text-xl sm:text-2xl md:text-3xl mx-auto w-full text-center max-w-[1000px]"
    >
      Less thinking, more lifting. Get the best results with our personal
      trainers full of <span class="italic"
        >personalized workouts, exercise explantions, analytics</span
      > and much more.
    </p>

    <CTAs />
    <Stars />
  </div>
</SectionWrapper>
