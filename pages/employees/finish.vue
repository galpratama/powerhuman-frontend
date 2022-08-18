<template>
  <section class="py-[70px] flex flex-col items-center justify-center px-4">
    <div class="text-[32px] font-semibold text-dark">Finalizing Profile</div>
    <p class="mt-4 text-base leading-7 text-center mb-[50px] text-grey">
      Complete the information to make it more <br />
      easier when introduce to team
    </p>
    <form class="w-full card">
      <div class="flex flex-col items-center mb-[14px]">
        <img src="/assets/images/user-f-1.png" width="70" alt="" />
        <div class="mt-6 mb-1 text-lg font-semibold">Andini Danna</div>
        <p class="text-base text-grey">ke@manasihhbang.com</p>
      </div>
      <div class="form-group">
        <label for="" class="text-grey">Phone Number</label>
        <input type="number" class="input-field" />
      </div>
      <a href="employee_create-3.html" class="w-full btn btn-primary mt-[14px]">
        Continue
      </a>
    </form>
  </section>
</template>

<script>
export default {
  layout: 'form',
}
</script>