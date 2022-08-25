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
                <input type="text" class="input-field" :value="name" @input="updateName" />
            </div>
            <div class="form-group">
                <label for="" class="text-grey">Email Address</label>
                <input type="email" class="input-field"  :value="email" @input="updateEmail" />
            </div>
            <div class="form-group">
                <label for="" class="text-grey">Gender</label>
                <select name="" id="" class="appearance-none input-field form-icon-chevron_down" :value="gender" @change="updateGender">
                    <option value="MALE" selected>Male</option>
                    <option value="FEMALE">Female</option>
                </select>
            </div>
            <div class="form-group">
                <label for="" class="text-grey">Age</label>
                <input type="number" class="input-field" :value="age" @input="updateAge" />
            </div>
            <NuxtLink :to="{name: 'companies-id-employees-finish'}" href="employee_create-2.html" class="w-full btn btn-primary mt-[14px]">
                Continue
            </NuxtLink>
        </form>
    </section>
</template>

<script>
export default {
    layout: 'form',
    middleware: 'auth',
    computed: {
        /* Use a computed property instead */
        name() {
            return this.$store.state.employee.name
        },
        email() {
            return this.$store.state.employee.email
        },
        gender() {
            return this.$store.state.employee.gender
        },
        age() {
            return this.$store.state.employee.age
        },
    },
    methods: {
        updateName(event) {
            this.$store.commit('employee/updateName', event.target.value)
        },
        updateEmail(event) {
            this.$store.commit('employee/updateEmail', event.target.value)
        },
        updateGender(event) {
            this.$store.commit('employee/updateGender', event.target.value)
        },
        updateAge(event) {
            this.$store.commit('employee/updateAge', event.target.value)
        },
    }
}
</script>