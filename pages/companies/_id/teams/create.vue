<template>
    <section class="py-[70px] flex flex-col items-center justify-center px-4">
        <div class="text-[32px] font-semibold text-dark">Build New Team</div>
        <p class="mt-4 text-base leading-7 text-center mb-[50px] text-grey">
            Team that can bring your company <br />
            growing bigger and bigger
        </p>
        <form class="w-full card"  @submit.prevent="createTeam">
            <div class="mb-[2px] mx-auto">
                <img src="/assets/svgs/ric-box.svg" alt="" />
            </div>
            <div class="form-group">
                <label for="" class="text-grey">Email Address</label>
                <input type="email" class="input-field disabled:bg-grey disabled:outline-none"
                       :value="this.$auth.user.email" disabled />
            </div>
            <div class="form-group">
                <label for="" class="text-grey">Team Name</label>
                <input type="text" class="input-field" value="Growth Marketing" v-model="team.name" />
            </div>
            <div class="form-group">
                <label for="" class="text-grey">Status</label>
                <select name="" id="" class="appearance-none input-field form-icon-chevron_down">
                    <option value="" selected>Active</option>
                    <option value="">Inactive</option>
                </select>
            </div>
            <button type="submit" class="w-full btn btn-primary mt-[14px]">
                Continue
            </button>
        </form>
    </section>
</template>

<script>
export default {
    layout: 'form',
    middleware: 'auth',
    data() {
        return {
            team: {
                name: '',
                company_id: this.$route.params.id,
            },
        }
    },
    methods: {
        async createTeam() {
            try {
                // Send Registration Data to Server
                let response = await this.$axios.post('/team', this.team)

                // Redirect to My Teams Page
                this.$router.push({ name: 'companies-id-teams' })

                console.log(response)
            } catch (error) {
                console.log(error)
            }
        },
    },
}
</script>