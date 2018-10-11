<template>
  <div>
    <h1>Kaalu teisendamine</h1>
    <h4>Sisesta kaal kilogrammides:</h4>
    <input type="number" min="0" v-model="kg">
    <table v-if="kg !== '' " id="output">
      <tr id="alloutputs">
        <td>Grammid</td>
        <td>{{ convertKg(1000) + 'g'}}</td>
      </tr>
      <tr>
        <td>Naelad</td>
        <td>{{ convertKg(2.20462262) + 'lb' }}</td>
      </tr>
      <tr>
        <td>Untsid</td>
        <td>{{ convertKg(35.2739619) + 'oz'}}</td>
      </tr>
    </table>
  </div>
</template>

<script>
export default {
  name: 'Konventer',
  data () {
    return {
        kg: ''
    }
  },
  methods: {
     convertKg(multiplier) {
        /*if (this.kg !== 0) {
          return (this.kg * multiplier).toFixed(2)
        } else {
          return 0
        }*/
        return (this.kg !==0) ? (this.kg * multiplier).toFixed (2) : 0
     }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
    
    #output {
      text-align: center;
      margin-left: auto;
      margin-right: auto;
      margin-top: 20px;
    }
    input {
      border: 1px solid black;
    }

    h1 {
      margin-top: 50px;
    }
</style>
