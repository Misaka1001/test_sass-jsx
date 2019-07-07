<script>
export default {
  data () {
    return {
      msg: '123'
    }
  },
  methods: {
    inputMsg (e) {
      this.msg = e.target.value
    }
  },
  render () {
    return (
      <div class='test'>
        <h1>test</h1>
        <input type='text' placeholder='input' onInput={this.inputMsg} value={this.msg}></input>
        <span>{this.msg}</span>
      </div>
    )
  }
}
</script>
<style lang="scss" scoped>
.test{
  h1{
    color: #00f;
  }
}
</style>
