<template>
  <div class="hello">
    <span v-once>执行一次性地插值:{{msg}}</span>
      {{msg}}
      <button @click="edit">更改</button>
      <p>Using mustaches: {{ rawHtml }}</p>
<p>Using v-html directive: <span v-html="rawHtml"></span></p>
  </div>
</template>

<script>
export default {
  name: 'HelloWorld',
  data () {
    return {
      msg: 'hhhh',
      rawHtml:'<div style="color:red">777</div>'
    }
  },
  created(){
    this.msg = "kkkk"
    console.log(this.msg)
  },
  methods:{
    edit(){
      this.msg = "ggg"
    }
  }
  
}
</script>

<style scoped>

</style>
