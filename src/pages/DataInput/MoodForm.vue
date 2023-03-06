<template>
  <card>
    <h4 slot="header" class="card-title">How have you felt today?</h4>
    <form>
      <div class="row">
        <div class="col-md-5">
          <base-input type="number"
                    min="0"
                    max="5"
                    label="Mood rating (0-5)"
                    :disabled="false"
                    placeholder="Mood Rating"
                    v-model="rating">
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
          rating: ''
        }
    },
    methods: {
      updateProfile () {
        alert('Thank you, you have given a rating of: ' + JSON.stringify(this.rating))
      }
    }
  }

</script>
<style>

</style>
