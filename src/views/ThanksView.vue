<script>

</script>

<template>
  <div class="thank-conteiner">
    <div class="thanks-page w-[24.5em] mt-[4em] md:mt-[0]">
        <img src="../assets/icon-success.svg" alt="Thank You" class="thank-you-image mb-[2em]" />
        <h1 class="text-preset-1 blue-800 md:mb-[.5em] mb-[1em]">Thank you for<br/>subscribing!</h1>
        <p class="text-preset-2 blue-800 md:mb-[2.5em] mb-[16em] thank-parragraf">
          A confirmation email has been sent to <span class="text-preset-2-bold">ash@loremcompany.com</span>.
          Please open it and click the button inside to confirm your subscription.
        </p>
        <button type="submit" class="bg-[#242742] p-5 text-white rounded-lg text-preset-2-bold w-full thank-submit">Dismiss message</button>
      </div>
    </div>
  <div class="body-container">

  </div>
</template>

<style scoped>

 /* I need to solved this problem with the flexbox */
 @media (max-width: 768px) {

  }

 @media(max-width:450px) {

  .thanks-page{
    .text-preset-1{
      font-size: 3rem;
    }
  }
 }
 @media(max-width:380px) {
  .thank-parragraf {
    width: 80%;
  }
  .thank-submit {
    width: 80%;
  }
  .thank-conteiner{
    padding: 0 2em;
  }
}
</style>
