<script setup>
import { ref } from 'vue'
import { useRouter } from 'vue-router'
const emailError = ref(false)
const email = ref('')
const emailRegex = /^[^\s@]+@[^\s@]+\.[^\s@]+$/
const router = useRouter()

function handleEmailChange(event) {
  email.value = event.target.value
  emailError.value = !emailRegex.test(email.value)
}
function onSubmit(){
  if(!emailError.value && emailRegex.test(email.value)) {
    router.push('/thanks')
  }
}

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
      <form @submit.prevent="onSubmit" action="">
        <div class="form-element flex flex-col">
          <div class="labels-container flex justify-between">
            <label for="email" class="text-preset-3 mb-[.5em] blue-800">Email address</label>
            <label for="email" class="text-preset-3 mb-[.5em] text-red-600" v-if="emailError">Valid email required</label>
          </div>
          <input class="mb-[1.5em] border-solid border-1 border-[#949494] rounded-lg p-4 " :class="{error : emailError}" type="email" @change="handleEmailChange"  :email="email" placeholder="email@company.com" required />
          <button type="submit" class="bg-[#242742] p-5 text-white rounded-lg text-preset-2-bold" id="sub-btn" >Subscribe to monthly newsletter</button>
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

  .error, .error:focus{
    border-color: oklch(0.577 0.245 27.325) !important;
    color: oklch(0.577 0.245 27.325) !important;
    background-color: #ff61551c;
  }
  .error:focus{
    outline: none;
  }
  .error::placeholder{
    color: oklch(0.577 0.245 27.325);
  }
  #sub-btn {
    transition: all 2s ease-out;
  }
  #sub-btn:hover {
    background: linear-gradient(90deg, #FF6155 0%, #FF8B00 100%);
    cursor: pointer;
  }
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
