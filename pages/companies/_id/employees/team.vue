<template>
  <section class="py-[70px] flex flex-col items-center justify-center px-4">
    <div class="text-[32px] font-semibold text-dark">Add to Team</div>
    <p class="mt-4 text-base leading-7 text-center mb-[50px] text-grey">
      Add your new people to grow the <br />
      company reaching their goals
    </p>
    <div
      class="
        w-full
        card
        !max-w-[560px]
        sm:!flex-row
        items-center
        justify-between
      "
    >
      <div class="flex flex-row items-center gap-4">
        <img src="/assets/images/user-f-1.png" width="70" alt="" />
        <div>
          <div class="text-lg font-semibold">Andini Danna</div>
          <p class="text-base text-grey">ke@manasihhbang.com</p>
        </div>
      </div>
      <p class="text-right text-grey">Product Designer</p>
    </div>

    <!-- Your Teams -->
    <section class="pt-[50px]">
      <!-- Section Header -->
      <div class="mb-[30px]">
        <div class="flex items-center justify-between gap-6">
          <div>
            <div class="text-xl font-medium text-dark">Your Teams</div>
            <p class="text-grey">Improve your growth</p>
          </div>
        </div>
      </div>

      <form>
        <div
          class="
            grid grid-cols-2
            gap-4
            sm:grid-cols-3
            lg:grid-cols-4
            xl:gap-10
            lg:gap-3
            mb-[50px]
          "
        >
          <div class="items-center card py-6 md:!py-10 md:!px-[38px] !gap-y-0">
            <input
              type="radio"
              name="productGrowth"
              id="productGrowth"
              class="
                absolute
                inset-0
                checked:ring-2
                ring-primary
                rounded-[26px]
                appearance-none
              "
            />
            <img src="/assets/svgs/ric-box.svg" alt="" />
            <div class="mt-6 mb-1 font-semibold text-center text-dark">
              Product Growth
            </div>
            <p class="text-center text-grey">810 People</p>
          </div>
          <div class="items-center card py-6 md:!py-10 md:!px-[38px] !gap-y-0">
            <input
              type="radio"
              name="marketing"
              id="marketing"
              class="
                absolute
                inset-0
                checked:ring-2
                ring-primary
                rounded-[26px]
                appearance-none
              "
            />
            <img src="/assets/svgs/ric-target.svg" alt="" />
            <div class="mt-6 mb-1 font-semibold text-center text-dark">
              Marketing
            </div>
            <p class="text-center text-grey">15,810 People</p>
          </div>
          <div class="items-center card py-6 md:!py-10 md:!px-[38px] !gap-y-0">
            <input
              type="radio"
              name="globalization"
              id="globalization"
              class="
                absolute
                inset-0
                checked:ring-2
                ring-primary
                rounded-[26px]
                appearance-none
              "
            />
            <img src="/assets/svgs/ric-globe.svg" alt="" />
            <div class="mt-6 mb-1 font-semibold text-center text-dark">
              Globalization
            </div>
            <p class="text-center text-grey">300 People</p>
          </div>
          <div class="items-center card py-6 md:!py-10 md:!px-[38px] !gap-y-0">
            <input
              type="radio"
              name="gamification"
              id="gamification"
              class="
                absolute
                inset-0
                checked:ring-2
                ring-primary
                rounded-[26px]
                appearance-none
              "
            />
            <img src="/assets/svgs/ric-award.svg" alt="" />
            <div class="mt-6 mb-1 font-semibold text-center text-dark">
              Gamification
            </div>
            <p class="text-center text-grey">25 People</p>
          </div>
        </div>
        <div class="flex justify-center">
          <a href="employees.html" id="continueBtn" class="btn btn-primary">
            Continue
          </a>
        </div>
      </form>
    </section>
  </section>
</template>

<script>
export default {
    layout: 'form',
  middleware: 'auth',
}
</script>