<template>
    <section class="py-[200px] flex flex-col items-center justify-center px-4">
        <div class="text-[32px] font-semibold text-dark mb-4">Create Companies</div>
        <form class="w-full card" @submit.prevent="createCompany">
            <div class="form-group">
                <label for="" class="text-grey">Name</label>
                <input type="text" class="input-field" name="name" v-model="company.name" />
            </div>
            <button type="submit" class="w-full btn btn-primary mt-[14px]">
                Save
            </button>
        </form>
    </section>
</template>

<script>
export default {
    middleware: 'auth',
    data() {
        return {
            company: {
                name: '',
            }
        }
    },
    methods: {
        async createCompany() {
            try {
                this.$axios.post('/company', this.company)
                    .then(response => {
                        console.log(response)
                        this.$router.push({
                            name: 'companies-id',
                            params: {
                                id: response.data.result.id,
                            },
                        })
                    })
            } catch (error) {
                console.log(error)
            }
        },
    }
}
</script>