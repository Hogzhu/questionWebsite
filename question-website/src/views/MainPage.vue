<template>
  <div class="mainPage">
    <QuestionList />
    <PersonalRank />
  </div>
</template>

<script>
// @ is an alias to /src
import QuestionList from '@/components/QuestionList.vue'
import PersonalRank from '@/components/PersonalRank.vue'

export default {
  name: 'MainPage',
  components: {
    QuestionList,
    PersonalRank
  }
}
</script>
<style lang="less">
  .mainPage {
    padding: 2rem 5rem 0 5rem;
    display: flex;
    justify-content: space-between;
  }
</style>
