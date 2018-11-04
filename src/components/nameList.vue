<!--suppress ALL -->
<template>
<div class="onePerson">
  <div class="person">
    <button :class="[flag1?'person12':'person11']" @click="zhang()">{{person1}}</button>
    <button :class="[flag2?'person22':'person21']" @click="xu()">{{person2}}</button>
    <button :class="[flag3?'person32':'person31']" @click="Tan()">{{person3}}</button>
  </div>
  <div class="personal">
    <div class="chooseRange">
      <p class="range">范围</p>
      <select>
        <option value="一周" selected="selected">一周</option>
        <option value="五天">五天</option>
        <option value="三天">三天</option>
      </select>
    </div>
    <dailyList
      v-if="which==1"
      v-for="daily in dateList1"
      :daily="daily"
      :key="daily.id"
    />
    <dailyList
      v-else-if="which==2"
      v-for="daily in dateList2"
      :daily="daily"
      :key="daily.id2"
    />
    <dailyList
      v-else-if="which==3"
      v-for="daily in dateList3"
      :daily="daily"
      :key="daily.id3"
    />
  </div>
</div>
</template>

<script>
import dailyList from './dailyList.vue'
let dailyId1 = 1
let dailyId2 = 1
let dailyId3 = 1
let flag11 = true
let flag22 = false
let flag33 = false
let which = 1
export default {
  name: 'nameList',
  components: {
    dailyList
  },
  data () {
    return {
      person1: '张梦瑶',
      person2: '许嘉涵',
      person3: '谭宁静',
      flag1: flag11,
      flag2: flag22,
      flag3: flag33,
      which: which,
      dateList1: [
        {
          id: dailyId1++,
          problem: '暂无',
          plan: '作业+任务',
          date: '2018-11-04',
          homework: {
            name: '计组实验报告',
            speed: '100%',
            hadDone: '全部',
            notDone: '无',
            raise: '50%'
          },
          task: {
            name: '红宝书十一章',
            speed: '10%',
            hadDone: '一点',
            notDone: '很多',
            raise: '0%'
          }
        },
        {
          id: dailyId1++,
          problem: '暂无',
          plan: '作业+任务',
          date: '2018-11-03',
          homework: {
            name: '计组实验报告',
            speed: '100%',
            hadDone: '全部',
            notDone: '无',
            raise: '50%'
          },
          task: {
            name: '红宝书十一章',
            speed: '10%',
            hadDone: '一点',
            notDone: '很多',
            raise: '0%'
          }
        },
        {
          id: dailyId1++,
          problem: '暂无',
          plan: '作业+任务',
          date: '2018-11-02',
          homework: {
            name: '计组实验报告',
            speed: '100%',
            hadDone: '全部',
            notDone: '无',
            raise: '50%'
          },
          task: {
            name: '红宝书十一章',
            speed: '10%',
            hadDone: '一点',
            notDone: '很多',
            raise: '0%'
          }
        },
        {
          id: dailyId1++,
          problem: '暂无',
          plan: '作业+任务',
          date: '2018-11-01',
          homework: {
            name: '计组实验报告',
            speed: '100%',
            hadDone: '全部',
            notDone: '无',
            raise: '50%'
          },
          task: {
            name: '红宝书十一章',
            speed: '10%',
            hadDone: '一点',
            notDone: '很多',
            raise: '0%'
          }
        },
        {
          id: dailyId1++,
          problem: '暂无',
          plan: '作业+任务',
          date: '2018-10-31',
          homework: {
            name: '计组实验报告',
            speed: '100%',
            hadDone: '全部',
            notDone: '无',
            raise: '50%'
          },
          task: {
            name: '红宝书十一章',
            speed: '10%',
            hadDone: '一点',
            notDone: '很多',
            raise: '0%'
          }
        },
        {
          id: dailyId1++,
          problem: '暂无',
          plan: '作业+任务',
          date: '2018-10-30',
          homework: {
            name: '计组实验报告',
            speed: '100%',
            hadDone: '全部',
            notDone: '无',
            raise: '50%'
          },
          task: {
            name: '红宝书十一章',
            speed: '10%',
            hadDone: '一点',
            notDone: '很多',
            raise: '0%'
          }
        },
        {
          id: dailyId1++,
          problem: '暂无',
          plan: '作业+任务',
          date: '2018-10-29',
          homework: {
            name: '计组实验报告',
            speed: '100%',
            hadDone: '全部',
            notDone: '无',
            raise: '50%'
          },
          task: {
            name: '红宝书十一章',
            speed: '10%',
            hadDone: '一点',
            notDone: '很多',
            raise: '0%'
          }
        }
      ],
      dateList2: [
        {
          id2: 'x' + 1,
          problem: '暂无',
          plan: '红宝书啊啊啊啊啊',
          date: '2018-11-04',
          homework: {
            name: '微积分作业',
            speed: '100%',
            hadDone: '全部',
            notDone: '无',
            raise: '0%'
          },
          task: {
            name: '日报网页',
            speed: '90%',
            hadDone: '写页面',
            notDone: '很多',
            raise: '80%'
          }
        },
        {
          id2: 'x' + 2,
          problem: '暂无',
          plan: '作业+任务',
          date: '2018-11-03',
          homework: {
            name: '计组实验报告',
            speed: '100%',
            hadDone: '全部',
            notDone: '无',
            raise: '50%'
          },
          task: {
            name: '红宝书十一章',
            speed: '10%',
            hadDone: '一点',
            notDone: '很多',
            raise: '0%'
          }
        },
        {
          id2: 'x' + 3,
          problem: '暂无',
          plan: '作业+任务',
          date: '2018-11-02',
          homework: {
            name: '计组实验报告',
            speed: '100%',
            hadDone: '全部',
            notDone: '无',
            raise: '50%'
          },
          task: {
            name: '红宝书十一章',
            speed: '10%',
            hadDone: '一点',
            notDone: '很多',
            raise: '0%'
          }
        },
        {
          id2: 'x' + 4,
          problem: '暂无',
          plan: '作业+任务',
          date: '2018-11-01',
          homework: {
            name: '计组实验报告',
            speed: '100%',
            hadDone: '全部',
            notDone: '无',
            raise: '50%'
          },
          task: {
            name: '红宝书十一章',
            speed: '10%',
            hadDone: '一点',
            notDone: '很多',
            raise: '0%'
          }
        },
        {
          id2: 'x' + 5,
          problem: '暂无',
          plan: '作业+任务',
          date: '2018-10-31',
          homework: {
            name: '计组实验报告',
            speed: '100%',
            hadDone: '全部',
            notDone: '无',
            raise: '50%'
          },
          task: {
            name: '红宝书十一章',
            speed: '10%',
            hadDone: '一点',
            notDone: '很多',
            raise: '0%'
          }
        },
        {
          id2: 'x' + 6,
          problem: '暂无',
          plan: '作业+任务',
          date: '2018-10-30',
          homework: {
            name: '计组实验报告',
            speed: '100%',
            hadDone: '全部',
            notDone: '无',
            raise: '50%'
          },
          task: {
            name: '红宝书十一章',
            speed: '10%',
            hadDone: '一点',
            notDone: '很多',
            raise: '0%'
          }
        },
        {
          id2: 'x' + 7,
          problem: '暂无',
          plan: '作业+任务',
          date: '2018-10-29',
          homework: {
            name: '计组实验报告',
            speed: '100%',
            hadDone: '全部',
            notDone: '无',
            raise: '50%'
          },
          task: {
            name: '红宝书十一章',
            speed: '10%',
            hadDone: '一点',
            notDone: '很多',
            raise: '0%'
          }
        }
      ],
      dateList3: [
        {
          id3: dailyId3++,
          problem: '暂无',
          plan: '上课上课上课啊啊啊',
          date: '2018-11-04',
          homework: {
            name: '物理实验',
            speed: '100%',
            hadDone: '做了光学实验',
            notDone: '剩报告',
            raise: '60%'
          },
          task: {
            name: '网页日报',
            speed: '70%',
            hadDone: '一点',
            notDone: '1-（一点）',
            raise: '50%'
          }
        },
        {
          id3: dailyId3++,
          problem: '暂无',
          plan: '作业+任务',
          date: '2018-11-03',
          homework: {
            name: '计组实验报告',
            speed: '100%',
            hadDone: '全部',
            notDone: '无',
            raise: '50%'
          },
          task: {
            name: '红宝书十一章',
            speed: '10%',
            hadDone: '一点',
            notDone: '很多',
            raise: '0%'
          }
        },
        {
          id3: dailyId3++,
          problem: '暂无',
          plan: '作业+任务',
          date: '2018-11-02',
          homework: {
            name: '计组实验报告',
            speed: '100%',
            hadDone: '全部',
            notDone: '无',
            raise: '50%'
          },
          task: {
            name: '红宝书十一章',
            speed: '10%',
            hadDone: '一点',
            notDone: '很多',
            raise: '0%'
          }
        },
        {
          id3: dailyId3++,
          problem: '暂无',
          plan: '作业+任务',
          date: '2018-11-01',
          homework: {
            name: '计组实验报告',
            speed: '100%',
            hadDone: '全部',
            notDone: '无',
            raise: '50%'
          },
          task: {
            name: '红宝书十一章',
            speed: '10%',
            hadDone: '一点',
            notDone: '很多',
            raise: '0%'
          }
        },
        {
          id3: dailyId3++,
          problem: '暂无',
          plan: '作业+任务',
          date: '2018-10-31',
          homework: {
            name: '计组实验报告',
            speed: '100%',
            hadDone: '全部',
            notDone: '无',
            raise: '50%'
          },
          task: {
            name: '红宝书十一章',
            speed: '10%',
            hadDone: '一点',
            notDone: '很多',
            raise: '0%'
          }
        },
        {
          id3: dailyId3++,
          problem: '暂无',
          plan: '作业+任务',
          date: '2018-10-30',
          homework: {
            name: '计组实验报告',
            speed: '100%',
            hadDone: '全部',
            notDone: '无',
            raise: '50%'
          },
          task: {
            name: '红宝书十一章',
            speed: '10%',
            hadDone: '一点',
            notDone: '很多',
            raise: '0%'
          }
        },
        {
          id3: dailyId3++,
          problem: '暂无',
          plan: '作业+任务',
          date: '2018-10-29',
          homework: {
            name: '计组实验报告',
            speed: '100%',
            hadDone: '全部',
            notDone: '无',
            raise: '50%'
          },
          task: {
            name: '红宝书十一章',
            speed: '10%',
            hadDone: '一点',
            notDone: '很多',
            raise: '0%'
          }
        }
      ]

    }
  },
  methods: {
    zhang: function () {
      this.flag1 = true
      this.flag2 = false
      this.flag3 = false
      this.which = 1
    },
    xu: function () {
      this.flag1 = false
      this.flag2 = true
      this.flag3 = false
      this.which = 2
    },
    Tan: function () {
      this.flag1 = false
      this.flag2 = false
      this.flag3 = true
      this.which = 3
    }
  }
}
</script>

<style scoped>
.person{
  width:25%;
  margin-left: 15%;
}
.person12{
  background-color: #a2c7cf;
  display: inline-block;
  height:30px;
  width:70px;
  line-height: 30px;
}
.person11{
  background-color: #d8f2f7;
  display: inline-block;
  height:30px;
  width:70px;
  line-height: 30px;
}
.person22{
  background-color: #a2c7cf;
  display: inline-block;
  height:30px;
  width:70px;
  line-height: 30px;
}
.person21{
  background-color: #d8f2f7;
  display: inline-block;
  height:30px;
  width:70px;
  line-height: 30px;
}
.person32{
  background-color: #a2c7cf;
  display: inline-block;
  height:30px;
  width:70px;
  line-height: 30px;
}
.person31{
  background-color: #d8f2f7;
  display: inline-block;
  height:30px;
  width:70px;
  line-height: 30px;
}
.personal{
  border-radius: 20px;
  border-style: solid;
  border-color: #a8a8a8;
  border-width: medium;
  margin: 0 150px 50px 150px;
}
.range{
  display: inline;
}
.chooseRange{
  float:right;
  margin-right:20px
}
</style>
