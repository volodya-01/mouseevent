<template>
    <div>
       <!--  <div>{{messege}}</div> -->
      <span v-bind:title="message">
    鼠标悬停几秒钟查看此处动态绑定的提示信息！
  </span>
  <div v-if="Math.random() > 0.5">
  此时大于0.5
</div>
<div v-else-if="Math.random() < 0.1">
 此时小于0.1
</div>
<div v-else>
  Now you don't
</div>
<template v-if="loginType === 'username'">
  <label>Username</label>
  <input placeholder="Enter your username" key="username-input">
</template>
<template v-else>
  <label>Email</label>
  <input placeholder="Enter your email address" key="email-input">
</template>
    </div>
</template>
<script>
export default {
    name:"son",
      data(){
    return{
       message: '页面加载于 ' + new Date().toLocaleString()
    }
  },
}
</script>

