<template>
  <img alt="Vue logo" src="./assets/logo.png">
  <h1>App.vue</h1>

  <PostComponent :propsTest="1" />

  <h1>{{ data.name }}</h1>
  <button @click="data.name='김김김'">김김김</button><br>

  <h1>{{ data2.name}}</h1>
  <button @click="data2.name='data2'">data2</button>

  <!-- <router-link to="/">홈</router-link><br>
  <router-link to="/post">포스트</router-link>

  <router-view></router-view> -->
</template>

<script>
import PostComponent from './components/PostComponent.vue';
import { ref, reactive } from 'vue';

export default {
  name: 'App',
  setup() {
    let data = ref({
      name:'홍길동', 
      age:20
    });
    let data2 = reactive({
      name:'철수', 
      age:5
    })

    let test='bbb';
    return {test,data,data2};
  },
  components:{
    PostComponent,
  }


}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
