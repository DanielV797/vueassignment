<template>
  <div class="smurry">
    <h1>Invoer</h1>
    
    <input v-model="code" minlength="6" maxlength="6"/>
    <br>
    <br>
    <button v-on:click="sendCode">Smurrify</button>

    <!-- <h1>Uitvoer</h1> https://youtu.be/fsBJXiP--Jc -->
    <p> Jouw uitvoer is: {{ code }} </p>
        <h5>IJs: {{ flavour }}</h5>
        <h5>Choco: {{ choco }}</h5>
        <h5>Snoep: {{ candy }}</h5>
  </div>
</template>

<script>
export default {
  name: 'Smurry',
  props: {
    msg: String
  },
  data() {
    return {
      code: '',
      flavour: code.slice(0,2),
      choco: code.slice(2,4),
      candy: code.slice(4,6),
      

      ass: {
        flavour: { 12: 'Vanille', 13: 'Chocolade', 21: 'Aardbei', 25: 'Banaan' },
        choco: { 44: 'Mars', 13: 'Twix', 52: 'Snickers', 21: 'Bounty' },
        candy: { 12: 'Kikkertjes', 13: 'Winegums', 23: 'Gummibeertjes', 99: 'Kauwgumballen' },
      }
    }
  },
  methods: {
    sendCode() {
      /* eslint-disable no-debugger */
      //debugger;
      /* eslint-enable no-debugger */
      console.log(this.code);
      console.log(this.code.slice(0,2));
      console.log(this.code.slice(2,4));
      console.log(this.code.slice(4,6));





      
    }
  }

}
</script>