<template>
  <div class="questionList">
    <div class="questionList-top">
      <ul class="questionList-top-ul" v-for="(item,index) in questionNum" :key="index">
        <li :style="[{backgroundColor:item.color}]">{{item.text}}</li>
      </ul>
      <div class="questionList-top-search">
        <input type="text" placeholder="请输入搜索关键字" />
      </div>
    </div>
    <div class="questionList-list">
      <div class="questionList-list-nav">
        <ul>
          <li class="questionList-list-nav-id">题号#</li>
          <li class="questionList-list-nav-title">题名</li>
          <li class="questionList-list-nav-edit">解题率</li>
          <li class="questionList-list-nav-accept">通过率</li>
          <li class="questionList-list-nav-difficult">难度</li>
          <li class="questionList-list-nav-type">题型</li>
        </ul>
      </div>
      <div class="questionList-list-item" v-for="item in question" :key="item">
        <span>{{item.id}}</span>
        <span>{{item.title}}</span>
        <span>{{item.edit}}</span>
        <span>{{item.accept}}</span>
        <span>{{item.difficult}}</span>
        <span>{{item.type}}</span>
      </div>
    </div>
  </div>
</template>

<script lang="ts">
import { Vue, Component, Prop } from 'vue-property-decorator'
export default class QuestionList extends Vue {
  private question: Array<any> = []
  private questionNum: Array<any> = []

  private mounted () {
    this.getQuestionNum()
    this.getQuestion()
  }

  private getQuestionNum () {
    const allQuestion = {
      text: '已解决 ' + 300 + '/' + 789,
      color: '#337ab7'
    }
    const easyQuestion = {
      text: '简单 ' + 452,
      color: '#5cb85c'
    }
    const midQuestion = {
      text: '中等 ' + 216,
      color: '#f0ad4e'
    }
    const diffQuestion = {
      text: '困难 ' + 121,
      color: '#d9534f'
    }
    this.questionNum.push(allQuestion, easyQuestion, midQuestion, diffQuestion)
  }

  private getQuestion () {
    const question1 = {
      id: 1,
      title: '这是第一道困难选择题哦',
      edit: '40.7%',
      accept: '30.2%',
      difficult: '困难',
      type: '选择题'
    }
    const question2 = {
      id: 2,
      title: '这是第二道简单简答题哦',
      edit: '87.5%',
      accept: '90.2%',
      difficult: '简单',
      type: '简答题'
    }
    const question3 = {
      id: 3,
      title: '这是第三道简单选择题哦',
      edit: '95.7%',
      accept: '98.9%',
      difficult: '简单',
      type: '选择题'
    }
    const question4 = {
      id: 4,
      title: '这是第四道中等简答题哦',
      edit: '84.5%',
      accept: '62.1%',
      difficult: '中等',
      type: '简答题'
    }
    const question5 = {
      id: 5,
      title: '这是第五道简单简答题哦',
      edit: '52.5%',
      accept: '62.1%',
      difficult: '简单',
      type: '简答题'
    }
    const question6 = {
      id: 6,
      title: '这是第六道困难简答题哦',
      edit: '23.5%',
      accept: '34.1%',
      difficult: '困难',
      type: '简答题'
    }
    const question7 = {
      id: 7,
      title: '这是第七道简单选择题哦',
      edit: '84.5%',
      accept: '85.9%',
      difficult: '简单',
      type: '选择题'
    }
    const question8 = {
      id: 8,
      title: '这是第八道中等选择题哦',
      edit: '84.5%',
      accept: '52.1%',
      difficult: '中等',
      type: '选择题'
    }
    const question9 = {
      id: 9,
      title: '这是第九道中等简答题哦',
      edit: '57.5%',
      accept: '79.1%',
      difficult: '中等',
      type: '简答题'
    }
    const question10 = {
      id: 10,
      title: '这是第十道简单简答题哦',
      edit: '97.5%',
      accept: '86.7%',
      difficult: '简单',
      type: '简答题'
    }
    this.question.push(question1, question2, question3, question4, question5, question6, question7, question8, question9, question10)
  }
}
</script>
<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="less">
ul {
  list-style-type: none;
  margin: 0;
  padding: 0;
}
a {
  color: #42b983;
}
.questionList {
  display: inline-block;
  &-top {
    display: flex;
    align-items: center;
    border-top: 1px solid #ddd;
    padding-top: 1rem;
    li {
      display: inline-block;
      margin-right: 2rem;
      padding: 0.1rem 0.8rem;
      font-size: 0.8rem;
      color: #fff;
      background-color: #5cb85c;
      border-radius: 1rem;
    }
    &-search {
      input {
        padding: 0.2rem 0.8rem;
        margin: 0;
        width: 20rem;
        height: 1.5rem;
        border: 1px solid #aaa;
        border-radius: 1.2rem;
        font-size: 1rem;
        &:hover {
          border-color: #42b983;
        }
      }
    }
  }
  &-list {
    margin-top: 1rem;
    &-nav {
      ul {
        border-width: 1px 0 1px 0;
        display: flex;
        border-style: solid;
        border-color: #eee #eee #ddd #eee;
        li {
          padding: 0.4rem 0;
          font-weight: 600;
          flex: 1;
          cursor: pointer;
          &:first-child {
            padding-left: 1rem;
          }
          &:nth-child(2) {
            flex: 5;
          }
          &:hover {
            color: #42b983;
          }
        }
      }
    }
    &-item {
      display: flex;
      &:nth-child(even) {
        background-color: rgb(245,245,245);
      }
      &:hover {
        cursor: pointer;
        background-color: #ddd;
      }
      span {
        padding: 0.4rem 0;
        flex: 1;
        &:first-child {
          padding-left: 1rem;
        }
        &:nth-child(2) {
          flex: 5;
        }
      }
    }
  }
}
</style>
