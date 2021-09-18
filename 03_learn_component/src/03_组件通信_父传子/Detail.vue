<template>
  <div>
    <h2>{{title}}</h2>
    <p>{{content}}</p>
  </div>
</template>

<script>
  export default {
    // props: ['title', 'content'],
    props: {
      title: String,
      content: {
        type: String,
        required: true,
        default: "123",
        // 自定义验证函数
        validator(value) {
          return ["success", "warning", "danger"].includes(value)
        }
      },
      // 注意这里如果props属性是对象类型的话，default默认值返回的是函数
      // 多个组件返回的是不同的对象
      // 否则会出现多个组件引用同一个对象的问题
      info: {
        type: Object,
        // 对象或者数组必须从一个工厂函数里面获取
        default() {
          return {name: "lucas"}
        }
      }
    }
  }
</script>

<style lang="scss" scoped>

</style>