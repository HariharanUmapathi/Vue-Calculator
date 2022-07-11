<template>

  <div class="calculator">
    <h1>Interest Calculator</h1>
   <div class='interface'>
     <label>Amount (P)</label>
     <input v-model="amount" type='number' min="0" step="50" /> 
     <label>Months (n)</label>
     <input v-model='months' type='number' />
     <label>Rate Of Interest (p.a)(r)</label>
     <input v-model="roi"  type='number' />
    <label>Simple Interest</label>
     {{(months/12)*(roi/100)*amount}}
     <label>Compound Interest</label>
     {{amount+(1+roi/100)**(months/12)}}
      
      
    
   </div>

  </div>
</template>

<script>
export default {
  name:"Calculator",
  data:()=>{return {months:5,roi:1,amount:1000}},
  methods:()=>{}
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h3 {
  margin: 40px 0 0;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
.calculator{
  display:flex;
  flex-direction:column;
  align-items: center;
}

.interface{
  display:grid;
  grid-auto-rows:auto;
  padding:5px;
  border:3px solid gray;
  grid-gap:5px;
}
.btn{
  border:1px solid gray;
  height:100px;
  width:100px;
  border-radius:10px;
  font-size:2rem;
  display:flex;
  align-items:center;
  justify-content: center;
}
.btn:hover{
  background: #42b983;
  transform:scale(0.95);
}
.display{
  grid-area:1/7/1/1;
  font-size:3.5rem;
  background:rgb(14, 14, 59);
  color:white;
}
.display span{
  font-size:1rem;
  color:red;
}
</style>

