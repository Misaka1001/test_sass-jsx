<script>
export default {
  props: ['msg', 'handle'],
  data () {
    return {
      number: [1, 2, 3],
      styleObject: {
        backgroundColor: 'red',
        fontColor: 'blue'
      }
    }
  },
  render () {
    return (
      <div>
        <input {...{
          style: {
            // color: this.styleObject.fontColor
          }
        }} type='text' value={this.msg} onInput={this.handle}/>
        <div {...{
          style: {
            backgroundColor: 'red',
            width: '100px',
            height: '100px',
            color: this.styleObject.fontColor,
            border: '1px solid black',
            borderRadius: '50%'
          },
          class: {
            blue: true
          }
        }}>12122</div>
        {
          this.number.map(item => {
            return <div>{ item }</div>
          })
        }
      </div>
    )
  }
}
</script>
<style lang="scss" scoped>
@mixin test{
  border: 1px solid black;
  background: red;
}
input{
  $test: #f40 !default;
  $test: #fff;
  @include test;
  color: $test;
}
</style>
