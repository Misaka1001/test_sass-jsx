<script>
export default {
  name: 'App',
  components: {
  },
  render () {
    let liClass = ['title', 'error', 'serious_error']
    return (
      <div id='app'>
        <p>
          p
          <span></span>
        </p>
        <ul class='test'>
          {liClass.map(item => {
            return (
              <li class={item}>{item}</li>
            )
          })}
        </ul>
      </div>
    )
  }
}
</script>
<style lang="scss" scoped>
*{
  padding: 0;
  margin: 0;
  list-style: none;
}
#app{
  p{
    $font-color:#f40;
    color:$font-color;
    span{
      color: $font-color;
    }
  }
  .test{
    .title{
      color: #0f0;
      font: {
        family: arial;
        size: 15px + 15px;
        weight: bolder;
      }
    }
    .error{
      color: #f00;
      font-size: 14px;
      $test-global: #00f !global;
    }
    .serious_error{
      @extend .error ;
      @if 1+1!=2 {
        font-weight: bolder;
      }@else if 1+2==3 {
        font-weight: bolder;
      }
    }
  }
}
</style>
