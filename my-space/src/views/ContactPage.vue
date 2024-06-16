<template>
  <div id="contactPage">
    <h1>Contact Page</h1>

    <form>
        <div>
            <label for="first_name">Firstname : </label>
            <input type="text" name="first_name" v-model.trim.lazy="applicant['first_name']">
        </div>
        <br>
        <div>
            <label for="e_mail">E mail : </label>
            <input type="text" name="e_mail" v-model.trim.lazy="applicant['e_mail']">
        </div>
        <br>
        <div>
            <label for="age">age : </label>
            <input type="number" name="age" v-model.number.lazy="applicant['age']">
        </div>


        <br>
        <button type="button" @click="submitForm">Submit</button>
        <button type="button" @click="clearApplicant">Clear</button>
    </form>

    <div style="margin-top: 20px; color:brown">#spy {{ JSON.stringify(applicant) }}</div>

  </div>
</template>

<script>
export default {
    name: "contactPage",
    methods: {
        submitForm() {
            console.log("submit !", this.applicant['first_name'])
        },
        clearApplicant() {
            this.applicant = {
                first_name : "",
                e_mail : 0
            }
        }
    },
    data() {
        return {
            applicant: {
                first_name : "",
                e_mail : "",
                age : 0
            }
        }
    },
}
</script>

<style>

</style>