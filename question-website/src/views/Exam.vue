<template>
  <div class="exam">
    <div class="exam-topText">自动出题或者自己定制!</div>
    <div class="exam-card">
      <AutoExam />
      <CustomExam />
    </div>
  </div>
</template>
<script lang="ts">
import { Vue, Component } from 'vue-property-decorator'
import AutoExam from '@/components/AutoExam.vue'
import CustomExam from '@/components/CustomExam.vue'
@Component({
  name: 'Exam',
  components: { AutoExam, CustomExam }
})
export default class Exam extends Vue {
}
</script>
<style scoped lang="less">
.exam {
  &-topText {
    text-align: center;
    margin-top: 5rem;
    font-size: 2rem;
    letter-spacing: 1rem;
    font-weight: 600;
  }
  &-card {
    display: flex;
    margin-top : 2rem;
    justify-content: center;
  }
}
</style>
