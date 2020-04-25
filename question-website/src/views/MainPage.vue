<template>
  <div class="mainPage">
    <QuestionList />
    <RankList />
  </div>
</template>

<script>
// @ is an alias to /src
import QuestionList from '@/components/QuestionList.vue'

export default {
  name: 'MainPage',
  components: {
    QuestionList
  }
}
</script>
<style lang="less">
  .mainPage {
    padding: 2rem 10rem;
  }
</style>
