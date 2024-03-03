<script>
  import { openModal } from '../../store';
  import Logo from '../common/Logo.svelte';
</script>

<header class="flex flex-col relative z-20">
  <div
    class="flex items-center max-w-[1400px] mx-auto w-full justify-between p-4 py-6"
  >
    <a href="/">
      <Logo />
    </a>

    <button
      on:click={() => ($openModal = true)}
      class="md:hidden grid place-items-center"
    >
      <i class="fa-solid fa-bars"></i>
    </button>

    <nav class="hidden md:flex items-center gap-4 lg:gap-6">
      <a
        class="duration-20 hover:text-indigo-400 cursor-pointer"
        href="#product">Product</a
      >
      <a
        class="duration-20 hover:text-indigo-400 cursor-pointer"
        href="#reviews">Reviews</a
      >
      <a class="duration-20 hover:text-indigo-400 cursor-pointer" href="#faqs"
        >FAQs</a
      >
      <button class="specialBtn">
        <p>Join Now</p>
      </button>
    </nav></div
  >
</header>
