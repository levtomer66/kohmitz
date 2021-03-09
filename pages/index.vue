<template>
  <div  class="content countdown-timer">
    <h1>{{ name }}</h1>
    <button @click="generate_name">תן בי</button>
  </div>
</template>

<style scoped>
.content {
  max-width: 500px;
  margin: auto;
  text-align: right;
}
</style>

<script>
  export default {
    data() {
    return {
        name: "כוחמיץ"
    }
  },
  created() {
    
  },
  methods: {
    generate_name: function() {
      var output1 = "אבגדהזחטכלמנסעפצקרשת".split('');
      var output2 = "בגדזחטכלמנסעפצקרשת".split('');
      var output3 = "בגדזחטכלמנסעפצקרשת".split('');
      var output4 = "בגדזחטךלםןסףצקרשת".split('');
      const let1 = Math.floor(Math.random() * output1.length);
      const let2 = Math.floor(Math.random() * output2.length);
      const let3 = Math.floor(Math.random() * output3.length);
      const let4 = Math.floor(Math.random() * output4.length);

      this.name = output1[let1] + "ו" + output2[let2] + output3[let3] + "י" + output4[let4]
    }
  }

  }
</script>
