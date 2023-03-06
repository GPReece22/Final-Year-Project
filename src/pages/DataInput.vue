<template>
  <div class="content">
    <div class="container-fluid">
      <div class="row">
        <div class="col-12">
          <mood-form>
          </mood-form>
          <exercise-form>
          </exercise-form>
        </div>
      </div>
    </div>
  </div>
</template>
<script>
  import LTable from 'src/components/Table.vue'
  import Card from 'src/components/Cards/Card.vue'
  import MoodForm from './DataInput/MoodForm.vue'
  import ExerciseForm from "@/pages/DataInput/ExerciseForm.vue";

  export default {
    components: {
      LTable,
      Card,
      MoodForm,
      ExerciseForm
    },
    data () {
      return {
        table1: {
          columns: [...tableColumns],
          data: [...tableData]
        },
        table2: {
          columns: [...tableColumns],
          data: [...tableData]
        }
      }
    }
  }
</script>
<style>
</style>
