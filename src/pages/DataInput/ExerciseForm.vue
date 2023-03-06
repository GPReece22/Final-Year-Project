<template>
  <card>
    <h4 slot="header" class="card-title">Data</h4>
    <form>
      <div class="row">
        <div class="col-md-5">
          <base-input type="number"
                    min="0"
                    label="Steps Today"
                    :disabled="false"
                    placeholder="Number of Steps"
                    v-model="user.numberOfSteps">
          </base-input>
          <base-input type="time"
                      min="0"
                      label="Time slept (HH:mm)"
                      :disabled="false"
                      placeholder="0"
                      v-model="user.timeSlept">
          </base-input>
          <base-input type="time"
                      min="0"
                      label="Social Time (HH:mm)"
                      :disabled="false"
                      placeholder="0"
                      v-model="user.socialTime">
          </base-input>
        </div>
      </div>
      <div class="text-center">
        <button type="submit" class="btn btn-info btn-fill float-right" @click.prevent="updateProfile">
          Submit
        </button>
      </div>
      <div class="clearfix"></div>
    </form>
  </card>
</template>
<script>
  import Card from 'src/components/Cards/Card.vue'

  export default {
    components: {
      Card
    },
    data () {
      return {
        user: {
          numberOfSteps: '',
          timeSlept: '',
          socialTime: ''
        }
      }
    },
    methods: {
      updateProfile () {
        alert('Thank you, you have given a rating of: ' + JSON.stringify(this.user))
      }
    }
  }

</script>
<style>

</style>
