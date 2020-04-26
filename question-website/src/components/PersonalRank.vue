<template>
  <div class="personalRank">
    <div class="personalRank-pie"></div>
    <div class="personalRank-bar"></div>
  </div>
</template>
<script>
export default {
  name: 'PersonalRank',
  data () {
    return {
      barCharts: {
        title: {
          text: '当前排行数据'
        },
        tooltip: {
          trigger: 'axis'
        },
        legend: {
          x: 'right',
          itemWidth: 40,
          itemHeight: 15,
          data: ['已完成', '未完成']
        },
        grid: {
          left: '20%'
        },
        xAxis: {
          data: ['张三', '李四', '王五', '赵六', 'hog', 'zhu']
        },
        yAxis: {},
        series: [{
          name: '已完成',
          type: 'bar',
          stack: '完成情况',
          barWidth: '20',
          data: [567, 456, 346, 332, 300, 289]
        }, {
          name: '未完成',
          type: 'bar',
          stack: '完成情况',
          barWidth: '20',
          data: [222, 333, 443, 437, 489, 500]
        }]
      },
      pieCharts: {
        title: {
          text: '我的个人数据'
        },
        radius: ['40%', '60%'],
        center: ['10%', '5%'],
        legend: {
          x: 'right'
        },
        color: ['#7EC0EE', '#be002f'],
        series: [
          {
            name: '题目',
            type: 'pie',
            radius: '60%',
            center: ['60%', '50%'],
            data: [
              { value: 233, name: '已完成' },
              { value: 556, name: '未完成' }
            ],
            labelLine: {
              normal: {
                show: true
              }
            },
            label: {
              normal: {
                position: 'inner',
                formatter: '{a}{b}{d}%',
                textStyle: {
                  fontSize: '12',
                  color: '#fff'
                }
              }
            }
          }
        ]
      },
      myBarCharts: '',
      myPieCharts: ''
    }
  },
  mounted: function () {
    this.myBarCharts = window.echarts.init(document.getElementsByClassName('personalRank-bar')[0])
    this.myPieCharts = window.echarts.init(document.getElementsByClassName('personalRank-pie')[0])
    this.createBarCharts()
    this.createPieCharts()
  },
  methods: {
    createBarCharts: function () {
      this.myBarCharts.setOption(this.barCharts)
    },
    createPieCharts: function () {
      console.log(this.pieCharts)
      this.myPieCharts.setOption(this.pieCharts)
    }
  }
}
</script>
<style scoped lang="less">
  .personalRank {
    &-pie {
      width: 25rem;
      height: 25rem;
    }
    &-bar {
      width: 30rem;
      height: 30rem;
    }
  }
</style>
