<template>
  <div>
    <p>{{daily.date}}</p>
    <div>
      <p>今天完成任务</p>
      <table border="1" cellspacing="0">
        <tr>
          <th>名称</th><th>进度</th><th>已完成</th><th>未完成</th><th>增加进度</th>
        </tr>
        <tr>
          <td>{{daily.task.name}}</td><td>{{daily.task.speed}}</td><td>{{daily.task.hadDone}}</td><td>{{daily.task.notDone}}</td><td>{{daily.task.raise}}</td>
        </tr>
      </table>
    </div>
    <div>
      <p>今天学习的内容</p>
      <table border="1" cellspacing="0">
        <tr>
          <th>名称</th><th>进度</th><th>已完成</th><th>未完成</th><th>增加进度</th>
        </tr>
        <tr>
          <td>{{daily.homework.name}}</td><td>{{daily.homework.speed}}</td><td>{{daily.homework.hadDone}}</td><td>{{daily.homework.notDone}}</td><td>{{daily.homework.raise}}</td>
        </tr>
      </table>
    </div>
    <div>
      <p>不懂的问题：</p>
      <textarea  rows="6" v-model="daily.problem"></textarea>
    </div>
    <div>
      <p>明天计划：</p>
      <textarea  rows="6" v-model="daily.plan"></textarea>
    </div>
    <hr style="border:1px dotted black" />
  </div>
</template>

<script>
export default {
  name: 'dailyList',
  props: {
    daily: {
      type: Object,
      required: true
    }
  }
}
</script>

<style scoped>
p{
  margin-left:3%;
  text-align: left;
  font-size:20px;
  font-weight: bold;
}
textarea{
  position: relative;
  left:-25%;
  width:40%;
  /*margin-left:-55%;*/
}
table{
  border-color: darkgray;
  width:60%;
  margin-left:4%;
}
</style>
