<script>
  import '../app.css';
  import CTAs from '../components/common/CTAs.svelte';
  import Footer from '../components/layout/Footer.svelte';
  import Header from '../components/layout/Header.svelte';
  import Logo from '../components/common/Logo.svelte';

  import { openModal } from '../store';

  let y;
  $: outerHeight = 0;

  function reroute(href) {
    $openModal = false;
    window.location.href = href;
  }
</script>

{#if $openModal}
  <div
    class="fixed top-0 left-0 w-screen h-screen border-b bg-white z-50 flex flex-col gap-8 md:hidden"
  >
    <div
      class="flex items-center justify-between gap-4 border-b bg-black py-2 px-8"
    >
      <Logo />
      <button
        on:click={() => ($openModal = false)}
        class="outline-none border-none"
      >
        <i class="fa-solid fa-xmark text-2xl"></i>
      </button>
    </div>
    <div class="flex flex-col gap-4 flex-1">
      <button
        on:click={() => reroute('#product')}
        class="border-none outline-none duration-200 cursor-pointer text-left rounded-none bg-white text-black pt-0"
      >
        <p class="duration-200 poppins font-semibold pb-4 border-b">
          Features <i class="fa-solid fa-chevron-right pl-4" />
        </p>
      </button>
      <button
        on:click={() => reroute('#reviews')}
        class="border-none outline-none duration-200 cursor-pointer text-left rounded-none bg-white text-black pt-0"
      >
        <p class="duration-200 poppins font-semibold pb-4 border-b">
          Reviews <i class="fa-solid fa-chevron-right pl-4" />
        </p>
      </button>
      <button
        on:click={() => reroute('#faqs')}
        class="border-none outline-none duration-200 cursor-pointer text-left rounded-none bg-white text-black pt-0"
      >
        <p class="duration-200 poppins font-semibold">
          FAQs <i class="fa-solid fa-chevron-right pl-4" />
        </p>
      </button>
    </div>
    <div class="flex flex-col items-center pb-12 justify-center">
      <CTAs />
    </div>
  </div>
{/if}

{#if y > outerHeight}
  <div class="bg-white fixed top-0 left-0 w-full flex flex-col z-20 fadeIn">
    <Header />
  </div>
{/if}

<slot />
<Footer />

<svelte:window bind:scrollY={y} bind:outerHeight />
