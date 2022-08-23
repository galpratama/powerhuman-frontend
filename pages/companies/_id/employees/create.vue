<template>
  <section class="py-[70px] flex flex-col items-center justify-center px-4">
    <div class="text-[32px] font-semibold text-dark">Empower Your Team</div>
    <p class="mt-4 text-base leading-7 text-center mb-[50px] text-grey">
      Add your new people to grow the <br />
      company reaching their goals
    </p>
    <form class="w-full card">
      <div class="form-group">
        <label for="" class="text-grey">Complete Name</label>
        <input type="text" class="input-field" />
      </div>
      <div class="form-group">
        <label for="" class="text-grey">Email Address</label>
        <input type="email" class="input-field" />
      </div>
      <div class="form-group">
        <label for="" class="text-grey">Gender</label>
        <select
          name=""
          id=""
          class="appearance-none input-field form-icon-chevron_down"
        >
          <option value="" selected>Male</option>
          <option value="">Female</option>
        </select>
      </div>
      <div class="form-group">
        <label for="" class="text-grey">Age</label>
        <input type="number" class="input-field" />
      </div>
      <a href="employee_create-2.html" class="w-full btn btn-primary mt-[14px]">
        Continue
      </a>
    </form>
  </section>
</template>

<script>
export default {
    layout: 'form',
  middleware: 'auth',
}
</script>