<template>
  <div class="lg:pr-[70px] py-[50px] lg:ml-[320px] xl:ml-[365px] px-4 lg:pl-0">
    <!-- Top Section -->
    <section
      class="flex flex-col flex-wrap justify-between gap-6 md:items-center md:flex-row"
    >
      <div class="flex items-center justify-between gap-4">
        <a href="#" id="toggleOpenSidebar" class="lg:hidden">
          <svg
            class="w-6 h-6 text-dark"
            fill="none"
            stroke="currentColor"
            viewBox="0 0 24 24"
            xmlns="http://www.w3.org/2000/svg"
          >
            <path
              stroke-linecap="round"
              stroke-linejoin="round"
              stroke-width="2"
              d="M4 6h16M4 12h16M4 18h7"
            ></path>
          </svg>
        </a>
        <div class="text-[32px] font-semibold text-dark">My Teams</div>
      </div>
      <div class="flex items-center gap-4">
        <form class="shrink md:w-[516px] w-full">
          <input
            type="text"
            name=""
            id=""
            class="
              input-field
              !outline-none
              !border-none
              italic
              form-icon-search
              ring-indigo-200
              focus:ring-2
              transition-all
              duration-300
              w-full
            "
            placeholder="Search people, team, project"
          />
        </form>
        <a
          href="#"
          class="
            flex-none
            w-[46px]
            h-[46px]
            bg-white
            rounded-full
            p-[11px]
            relative
            notification-dot
          "
        >
          <img src="/assets/svgs/ic-bell.svg" alt="" />
        </a>
      </div>
    </section>

    <section class="pt-[50px]">
      <!-- Section Header -->
      <div class="mb-[30px]">
        <div
          class="flex flex-col justify-between gap-6 sm:items-center sm:flex-row"
        >
          <div>
            <div class="text-xl font-medium text-dark">Available</div>
            <p class="text-grey">Empower company</p>
          </div>
          <NuxtLink :to="{ name: 'companies-id-teams-create' }"  class="btn btn-primary"
            >Build New Team</NuxtLink
          >
        </div>
      </div>

      <div
        class="grid grid-cols-2 gap-4 sm:grid-cols-3 lg:grid-cols-4 xl:gap-10 lg:gap-3"
      >
      <p v-if="$fetchState.pending">Fetching teams...</p>
        <div class="items-center card py-6 md:!py-10 md:!px-[38px] !gap-y-0" v-else v-for="team in teams.data.result.data">
          <a
            href="#"
            class="absolute inset-0 focus:ring-2 ring-primary rounded-[26px]"
          ></a>
          <img :src="team.icon" alt="" />
          <div class="mt-6 mb-1 font-semibold text-center text-dark">
            {{ team.name }}
          </div>
          <p class="text-center text-grey">{{ team.employees_count }} People</p>
        </div>
      </div>
    </section>
  </div>
</template>
<script>
export default {
    layout: 'dashboard',
    middleware: 'auth',
    data() {
      return {
          teams: [],
      }
    }, 
    async fetch() {
        this.teams = await this.$axios.get('/team', {
            params: {
                company_id: this.$route.params.id,
                limit: 100,
            }
      })
    }
}
</script>