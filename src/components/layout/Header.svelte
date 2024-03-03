<script>
  import { openModal } from '../../store';
  import Logo from '../common/Logo.svelte';
</script>

<header class="flex flex-col relative z-20 bg-black">
  <div
    class="flex items-center max-w-[1400px] mx-auto w-full justify-between p-4 py-6 text-white"
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
        class="duration-20 hover:text-yellow-400 cursor-pointer"
        href="#product">Features</a
      >
      <a
        class="duration-20 hover:text-yellow-400 cursor-pointer"
        href="#reviews">Reviews</a
      >
      <a class="duration-20 hover:text-yellow-400 cursor-pointer" href="#faqs"
        >FAQs</a
      >
      <button class="specialBtn">
        <a href="tel:+91 9899195018" target="_blank">Join Now</a>
      </button>
    </nav>
  </div>
</header>
