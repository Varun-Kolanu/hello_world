<template>
  <div>
    <pre>
      {{ JSON.stringify(formValues, null, 2) }}
    </pre>
  </div>
  <form @submit.prevent="submitHandler"> <!-- or by using event.preventDefault() -->
    <div>
      <label for="name">Name</label>
      <input type="text" placeholder="Name" id="name" v-model="formValues.name"> <!-- v-model for 2 way data binding -->
    </div>
    <div>
      <label for="profile">Profile</label>
      <textarea name="profile" id="profile" cols="30" rows="10" v-model="formValues.profile"></textarea>
    </div>
    <div>
      <label for="country">Country</label>
      <select name="country" id="country" v-model="formValues.country">
        <option value="">Select</option>
        <option value="India">India</option>
        <option value="China">China</option>
      </select>
    </div>
    <div>
      <label for="job-location">Job Location</label>
      <select name="job-location" id="country" multiple v-model="formValues.jobLocation">
        <option value="India">India</option>
        <option value="China">China</option>
      </select>
    </div>
    <div>
      <label for="major">Major?</label>
      <input type="checkbox" id="major" v-model="formValues.major">
    </div>
    <div>
      <label for="remote">Open to remote work?</label>
      <input type="checkbox" id="remote" v-model="formValues.remote" true-value="yes" false-value="no">
    </div>
    <div>
      <label for="html">Html</label>
      <input type="checkbox" id="html" v-model="formValues.skills" value="html">

      <label for="css">CSS</label>
      <input type="checkbox" id="css" v-model="formValues.skills" value="css">

      <label for="js">JS</label>
      <input type="checkbox" id="js" v-model="formValues.skills" value="js">
    </div>

    <button type="submit">Submit</button>
  </form>
  <button @click="formValues.name = 'Varun'">Click</button>
</template>

<script>
export default {
  name: 'App',
  data() {
    return {
      formValues: {
        name: '',
        profile: '',
        country: '',
        jobLocation: [],
        major: false,
        remote: "no",
        skills: []
      }
    };
  },
  methods: {
    submitHandler() {
      console.log(this.formValues)
    }
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
