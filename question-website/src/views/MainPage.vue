<template>
  <div class="mainPage">
    <QuestionList />
    <PersonalRank />
    <div class="mainPage-login-bg">
      <Login />
    </div>
  </div>
</template>

<script>
// @ is an alias to /src
import QuestionList from '@/components/QuestionList.vue'
import PersonalRank from '@/components/PersonalRank.vue'
import Login from '@/components/Login.vue'

export default {
  name: 'MainPage',
  components: {
    QuestionList,
    PersonalRank,
    Login
  }
}
</script>
<style lang="less">
  .mainPage {
    padding: 2rem 3rem 0 3rem;
    display: flex;
    justify-content: space-between;
    &-login-bg {
      display: none;
      position: fixed;
      width: 100%;
      height: 100%;
      top: 0;
      left: 0;
      z-index: 999;
      background-color: rgba(0, 0, 0, 0.4);
    }
    Login {
      display: none;
    }
  }
</style>
