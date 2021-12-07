<template>
<div>
<h1>{{animal}} 안녕 ???</h1>
<h2>{{animal}}는 {{food1}}를 먹습니다</h2>
<h2>{{animal}}는 {{food2}}를 좋아합니다. </h2>
<input type="text" v-model="animal" /><hr/>

<h2> {{alertMessage}} </h2>
<div v-html="alertMessage"> </div>
<a :href="naverUrl">naver</a>
<hr/>

<input type="text" v-model="food3" /><hr/>
<h2 v-bind:class ="{red : food3 ==='apple', blue : food3 ==='banana'}">
                   {{animal}}는 {{food3}}를 좋아합니다. 
</h2>
</div>
</template>

<script>
export default {
  name: 'App',
  data(){
    return{
      animal : "원숭이",
      food1 : "apple",
      food2 : "banana",
      food3 : "banana",           
      alertMessage : "<h2>경고!!!</h2>",
      naverUrl : "https://www.naver.com",
    };
  }
}
</script>

<style scoped>
input {
  font-size : 20px;
}
orange {
    color : orange ;
}
.red {
    color : red ;
}
.blue {
    color : blue ;
}
</style>