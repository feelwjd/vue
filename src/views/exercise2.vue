<template>
<div>
<div>
  <h2 v-if="age >=18"> 성인입니다</h2>
  <h2 v-else-if="age < 18 && age >= 15"> 청소년 입니다</h2>
  <h2 v-else> 어른 입니다.</h2>
</div> <hr/>  
<div>
  <h2> {{animals}} </h2><hr/>
  <h2 v-for="animal in animals" :key="animal"> {{animal}} </h2><hr/>
  <h2 v-for="(index, animal) in animals" :key="index">{{index}} : {{animal}} </h2><hr/>
  <ul>
    <li v-for="(user, index) in users" :key="index"> <h2>{{user}} </h2></li>
  </ul>
</div> <hr/>  
<div>
  <ul>
    <li v-for="(user, index) in users" :key="index">
      이름 : {{user.name}} / 부서 : {{user.job}} / 성별 : {{user.gender}}<br/>
    </li>
  </ul>  <hr/>
</div> 
 <div>
  <ul>  
    <li v-for="(user, index) in users1" :key="index">
      이름 : {{user.name}} / 부서 : {{user.job}} / 성별 : {{user.gender}}<br/>
      취미 : {{user.hobby}}
    </li>
  </ul>
</div> <hr/>  
<div>
  <ul>
    <li v-for="(user, index) in users1" :key="index">
      이름 : {{user.name}} / 부서 : {{user.job}} / 성별 : {{user.gender}}<br/>
      <p v-for="hobby in user.hobby" :key="hobby">
      취미 : {{hobby}}
      </p>
    </li>
  </ul>  
</div> <hr/>  
</div>
</template>
<script>
export default {
  name: 'App',
  data() {
    return {
      age: 20,
      animals: ["monkey", "rat", "dog", "lion"], 
      users: [
      { name: '김창복', job: 'developer', gender: 'male' },
      { name: '홍길동', job: 'designer', gender: 'male' },
      { name: '갑순이', job: 'pm', gender: 'female' },
      ],
      users1: [
      { name: '김창복', job: 'developer', gender: 'male', hobby: ["운동", "영화감상", "코딩"] },
      { name: '홍길동', job: 'designer', gender: 'male', hobby: ["운동", "영화감상", "코딩"] },
      { name: '갑순이', job: 'pm', gender: 'female', hobby:  ["운동", "영화감상", "코딩"] },
      ]
    };
  }
}
</script>