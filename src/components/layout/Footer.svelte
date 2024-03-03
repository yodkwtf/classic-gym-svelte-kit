<script>
  import Logo from '../common/Logo.svelte';
</script>

<footer class="py-16 sm:py-20 md:py-24 px-4 md:px-8 bg-black text-white">
  <div
    class="max-w-[1200px] mx-auto w-full grid grid-cols-1 sm:grid-cols-2 md:grid-cols-5 gap-8 text-base"
  >
    <div class="flex flex-col gap-4 md:col-span-2">
      <Logo />
      <p>©2023 CLASSIC GYM LTD. All rights reserved.</p>
      <p class="mt-4"
        >SCO No. 11, 1st and 2nd floor, Near NCU University,<br />Sec 23A
        Gurgaon
      </p>
    </div>
    <div class="flex flex-col gap-4">
      <p class="font-bold poppins text-base sm:text-lg">Support</p>
      <a
        href="tel:+91 9899195018"
        target="_blank"
        class="cursor-pointer hover:text-yellow-400 duration-200"
      >
        Contact Us</a
      >
      <a
        href="https://maps.app.goo.gl/FQebfRcBEUGAZjmVA"
        target="_blank"
        class="cursor-pointer hover:text-yellow-400 duration-200"
      >
        Google Maps</a
      >
    </div>
    <div class="flex flex-col gap-4">
      <p class="font-bold poppins text-base sm:text-lg">Research</p>
      <a
        href="https://youtu.be/0_Of-5nPI7s?si=eM6kuLDUvdJcM0ZA"
        target="_blank"
        class="cursor-pointer hover:text-yellow-400 duration-200"
      >
        Gym Tour</a
      >
      <a
        href="http://www.fitarrow.in/product/gym/classic-gym-sec-23a-gurgaon/"
        target="_blank"
        class="cursor-pointer hover:text-yellow-400 duration-200"
      >
        About Us</a
      >
    </div>
    <div class="flex flex-col gap-4">
      <p class="font-bold poppins text-base sm:text-lg">Follow Us</p>
      <a
        href="https://www.instagram.com/sonu_tyagi_mr_world_2018"
        target="_blank"
        class="cursor-pointer hover:text-yellow-400 duration-200"
      >
        <i class="fa-brands fa-instagram pr-2" />
        Instagram</a
      >
      <a
        href="https://www.youtube.com/@jonyverma0602/featured"
        target="_blank"
        class="cursor-pointer hover:text-yellow-400 duration-200"
      >
        <i class="fa-brands fa-youtube pr-2" />
        YouTube</a
      >
      <a
        href="https://www.facebook.com/people/Sonu-Tyagi/100069974058731/"
        target="_blank"
        class="cursor-pointer hover:text-yellow-400 duration-200"
      >
        <i class="fa-brands fa-facebook pr-2" />
        Facebook</a
      >
    </div>
  </div>
</footer>
