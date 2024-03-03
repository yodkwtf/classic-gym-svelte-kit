<script>
  export let reviewItem;
  export let left;
  export let index;
</script>

<div
  class={'flex flex-col gap-2 w-full max-w-[500px] mx-auto relative text-white ' +
    (left
      ? index % 2 === 1
        ? 'hidden md:flex opacity-0 pointer-events-none max-h-[40px] overflow-hidden'
        : ' '
      : index % 2 === 0
        ? 'hidden md:flex opacity-0 pointer-events-none max-h-[40px] overflow-hidden'
        : ' ')}
>
  <div class="flex relative">
    <div
      class={'absolute rounded-full bg-black aspect-square hidden md:grid place-items-center h-4 top-0 ' +
        (index % 2 === 0
          ? ' right-0 -mr-8 translate-x-1/2'
          : ' left-0 -ml-8 -translate-x-1/2')}
    >
      <div class="rounded-full bg-gray-700 aspect-square h-2" />
    </div>
    <div class="flex items-center gap-2">
      <i class="fa-solid fa-user" />
      <h3 class="text-lg sm:text-xl md:text-2xl">
        {reviewItem.name}
      </h3>
    </div>
  </div>
  <div class="h-[1.5px] bg-gray-700 w-1/4 mr-auto mb-4 mt-2"></div>
  <div class="flex items-center flex-wrap gap-2 text-xs sm:text-sm mb-4">
    {#each reviewItem.features as keyword}
      <div
        class="p-1 py-0.5 rounded-md border border-solid border-yellow-400 bg-yellow-50 text-black"
      >
        <p>{keyword}</p>
      </div>
    {/each}
  </div>
  <p>{reviewItem.review}</p>
</div>
