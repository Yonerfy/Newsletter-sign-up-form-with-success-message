<script setup>

</script>
<template>

  <div class="newsletter-container flex ">
    <div class="form-container lg:mr-[4em] flex flex-col justify-center">
      <h1 class="text-preset-1 md:mb-[1em] mb-[.8em] blue-800">Stay updated!</h1>
      <p class="text-preset-2 mb-[2em] blue-800">Join 60,000+ product managers receiving monthly<br> updates on:</p>
      <ul class="text-preset-2 mb-[2em] list-inside blue-800">
        <li class="flex items-center mb-[1em]">
          <img src="../assets/icon-list.svg" class="w-6 h-6 mr-2" />
          Product discovery and building what matters
        </li>
        <li class="flex items-center mb-[1em]">
          <img src="../assets/icon-list.svg" class="w-6 h-6 mr-2" />
          Measuring to ensure updates are a success
        </li>
        <li class="flex items-center mb-[1em]">
          <img src="../assets/icon-list.svg" class="w-6 h-6 mr-2" />
          And much more!
        </li>
      </ul>
      <form action="">
        <div class="form-element flex flex-col">
          <label for="email" class="text-preset-3 mb-[.5em] blue-800">Email address</label>
          <input class="mb-[1.5em] border-solid border-1 border-[#949494] rounded-lg p-4" type="email" placeholder="email@company.com" required />
          <button type="submit" class="bg-[#242742] p-5 text-white rounded-lg text-preset-2-bold">Subscribe to monthly newsletter</button>
        </div>
      </form>
    </div>
    <div class="img-container">
      <img src="../assets/illustration-sign-up-desktop.svg" class="w-full hidden lg:flex" alt="" />
      <img src="../assets/illustration-sign-up-mobile.svg" class="w-full lg:hidden md:rounded-[2.2em] mb-[2.5em]" alt="" />
    </div>
  </div>
</template>

<style scoped>

  @media(max-width: 768px) {
    .newsletter-container {
      display: grid;
      grid-template-columns: 1fr;
      grid-template-rows: 1fr 1fr;
      grid-template-areas:
        "img-container"
        "form-container";
    }
    .img-container{
      grid-area: img-container;
    }
    .form-container{
      grid-area: form-container;
    }
  }

  @media(max-width:450px) {
    .form-container{
      padding: 0 2em;
      margin-top: -4.5em;
    }
  }



</style>
