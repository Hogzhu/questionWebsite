<template>
  <div class="exam">
    <div class="exam-topText">自动出题或者自己定制!</div>
    <AutoExam />
    <CustomExam />
  </div>
</template>
<script>
import AutoExam from '@/components/AutoExam.vue'
import CustomExam from '@/components/CustomExam.vue'
export default {
  name: 'Exam',
  components: {
    AutoExam,
    CustomExam
  }
}
</script>
<style scoped lang="less">
.exam {
  &-topText {
    text-align: center;
    margin-top: 3rem;
    font-size: 2rem;
    letter-spacing: 1rem;
    font-weight: 600;
  }
}
</style>
