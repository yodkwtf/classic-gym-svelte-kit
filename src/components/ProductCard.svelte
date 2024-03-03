<script>
  export let index;
  export let productFeature;
</script>

<div
  class="grid grid-cols-1 md:grid-cols-2 gap-14 md:gap-14 lg:gap-20 relative text-base text-white place"
>
  <div
    class={'flex flex-col gap-8 md:gap-10 pt-8 sm:pt-10 ' +
      (index % 2 === 1 ? ' md:order-2' : ' ')}
  >
    <h4
      class="text-xl sm:text-2xl md:text-3xl max-w-[1000px] w-full font-medium relative pr-10 after:absolute after:top-full after:left-0 after:w-1/5 after:h-1.5 after:mt-1 after:bg-yellow-400"
    >
      <slot />
    </h4>

    <p>{productFeature.description}</p>
    <div class="flex flex-col gap-3">
      {#each productFeature.featureList as listItem}
        <div class="flex gap-2 items-center">
          <div
            class="grid place-items-center px-1.5 text-xs sm:text-sm aspect-square rounded-full border-[1.5px] bg-black border-solid border-yellow-400"
          >
            <i class="fa-solid fa-bolt text-yellow-400"></i>
          </div>
          <p>{listItem}</p>
        </div>
      {/each}
    </div>

    <div class="flex items-center">
      <button class="specialBtn mr-auto font-semibold">
        <a href="tel:+91 9899195018" target="_blank">Try free today &rarr;</a>
      </button>
    </div>
  </div>

  <div class={'flex flex-col dropShadow overflow-hidden rounded-b-lg'}>
    <div
      class="flex flex-col overflow-hidden rounded-b-lg h-[16rem] sm:h-[20rem] md:h-[24rem] lg:h-[28rem] xl:h-[32rem]"
    >
      <img
        src={productFeature.imgUrl}
        class={'w-full h-full ' +
          (index === 2 ? 'object-contain' : 'object-cover')}
        alt="product-img"
      />
    </div>
  </div>
</div>
