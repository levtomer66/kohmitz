<template>
  <div  class="content countdown-timer">
    <p>{{ name }}</p>
    <button class="big-button" @click="generate_name">תן בי</button>
  </div>
</template>

<style>
@import url('https://fonts.googleapis.com/css2?family=Amatic+SC&display=swap');
.content {
  max-width: 500px;
  margin: auto;
  text-align: right;
}
:root {
  --backgroundColor: rgba(246, 241, 209);
  --colorShadeA: rgb(106, 163, 137);
  --colorShadeB: rgb(121, 186, 156);
  --colorShadeC: rgb(150, 232, 195);
  --colorShadeD: rgb(187, 232, 211);
  --colorShadeE: rgb(205, 255, 232);
}
* {
  box-sizing: border-box;
}
*::before, *::after {
  box-sizing: border-box;
}
body {
  font-family: 'Amatic SC', 'OpenSans', sans-serif;
  font-size: 7rem;
  line-height: 2;
  display: flex;
          align-items: center;
          justify-content: center;
  margin: 0;
  min-height: 100vh;
  background: var(--backgroundColor);
}
button {
  position: relative;
  display: inline-block;
  cursor: pointer;
  outline: none;
  border: 0;
  vertical-align: middle;
  text-decoration: none;
  font-size: 1.5rem;
    color:var(--colorShadeA);
  font-weight: 700;
  text-transform: uppercase;
  font-family: inherit;
}

button.big-button {
   padding: 1em 2em;
   border: 2px solid var(--colorShadeA);
  border-radius: 1em;
  background: var(--colorShadeE);
transform-style: preserve-3d;
   transition: all 175ms cubic-bezier(0, 0, 1, 1);
}
button.big-button::before {
  position: absolute;
  content: '';
  width: 100%;
  height: 100%;
  top: 0;
  left: 0;
  right: 0;
  bottom: 0;
  background: var(--colorShadeC);
  border-radius: inherit;
    box-shadow: 0 0 0 2px var(--colorShadeB), 0 0.75em 0 0 var(--colorShadeA);
 transform: translate3d(0, 0.75em, -1em);
     transition: all 175ms cubic-bezier(0, 0, 1, 1);
}


button.big-button:hover {
  background: var(--colorShadeD);
  transform: translate(0, 0.375em);
}

button.big-button:hover::before {
  transform: translate3d(0, 0.75em, -1em);
}

button.big-button:active {
            transform: translate(0em, 0.75em);
}

button.big-button:active::before {
  transform: translate3d(0, 0, -1em);
  
      box-shadow: 0 0 0 2px var(--colorShadeB), 0 0.25em 0 0 var(--colorShadeB);

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
