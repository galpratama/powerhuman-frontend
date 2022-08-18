<template>
  <section class="py-[70px] flex flex-col items-center justify-center px-4">
    <div class="text-[32px] font-semibold text-dark">Build New Team</div>
    <p class="mt-4 text-base leading-7 text-center mb-[50px] text-grey">
      Team that can bring your company <br />
      growing bigger and bigger
    </p>
    <form class="w-full card">
      <div class="mb-[2px] mx-auto">
        <img src="/assets/svgs/ric-box.svg" alt="" />
      </div>
      <div class="form-group">
        <label for="" class="text-grey">Email Address</label>
        <input
          type="email"
          class="input-field disabled:bg-grey disabled:outline-none"
          value="angga@yourcompany.com"
          disabled
        />
      </div>
      <div class="form-group">
        <label for="" class="text-grey">Team Name</label>
        <input type="text" class="input-field" value="Growth Marketing" />
      </div>
      <div class="form-group">
        <label for="" class="text-grey">Status</label>
        <select
          name=""
          id=""
          class="appearance-none input-field form-icon-chevron_down"
        >
          <option value="" selected>Active</option>
          <option value="">Inactive</option>
        </select>
      </div>
      <a href="my_teams.html" class="w-full btn btn-primary mt-[14px]">
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