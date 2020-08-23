<template>
  <div id="app">
    <!--文本框 -->
    <label>
      <input v-model="message" placeholder="edit me">
    </label>
    <p>Message is: {{ message }}</p>
    <p>
      <button @click="message = 'suixin'"> set message to suixin</button>
    </p>

    <!--单复选框 -->
    <input type="checkbox" id="checkbox" v-model="checked">
    <label for="checkbox">{{ checked }}</label>
    <br>
    <p></p>

    <!--多复选框 -->
  爱好：{{ habit }}
    <label>
      <input type="checkbox" v-model="habit" :value="1">
      <span>踢球</span>
    </label>
    <label>
      <input type="checkbox" v-model="habit" :value="2">
      <span>画画</span>
    </label>
    <label>
      <input type="checkbox" v-model="habit" :value="3">
      <span>看书</span>
    </label>
    <br>
    <p></p>

    <!--单选-->
    habit：{{ x }}
    <label>
      <input type="radio" v-model="x" :value="1">
      <span>踢球</span>
    </label>
    <label>
      <input type="radio" v-model="x" :value="2">
      <span>画画</span>
    </label>
    <label>
      <input type="radio" v-model="x" :value="3">
      <span>看书</span>
    </label>
    <br>
    <p></p>

    <!--下拉列表-->
    <span>我想要：{{ wanted }}</span>
    <label>
      <select v-model="wanted">
        <option disabled value="">请选择</option>
        <option>金钱</option>
        <option>权力</option>
        <option>开心</option>
      </select>
    </label>
    <br>
    <p></p>

    <!--form-->
登录表单
    {{user}}
    <hr/>
    <br>
    <form @submit.prevent="onSubmit">
      <label>
        <span>用户名：</span>
        <input type="text" v-model.number="user.username">
      </label>
      <label>
        <span>密码：</span>
        <input type="password" v-model.lazy="user.password">
      </label>
      <button type="submit">登录</button>
    </form>

  </div>
</template>

<script>
export default {
  name: "App",
  data() {
    return {
      message: 'hi',
      checked: true,
      habit: [],
      x:' ',
      wanted: '',
      user:{
        username:'0',
        password: ''
      }

    }
  },
  methods:{
    onSubmit(){
      console.log(this.user)
    }
  }
}
</script>

