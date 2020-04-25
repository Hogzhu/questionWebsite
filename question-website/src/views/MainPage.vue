<template>
  <div class="mainPage">
    <QuestionList />
    <RankList />
  </div>
</template>

<script>
// @ is an alias to /src
import QuestionList from '@/components/QuestionList.vue'
import RankList from '@/components/RankList.vue'

export default {
  name: 'MainPage',
  components: {
    QuestionList,
    RankList
  }
}
</script>
<style lang="less">
  .mainPage {
    padding: 2rem 10rem;
  }
</style>
