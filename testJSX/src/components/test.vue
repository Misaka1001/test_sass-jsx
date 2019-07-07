<script>
import test2 from './test2'
export default {
  data () {
    return {
      class: 'test',
      msg: 'test'
    }
  },
  components: {
    test2
  },
  methods: {
    handle (e) {
      this.msg = e.target.value
    }
  },
  render () {
    return (
      <div class={this.class}>
        <test2 msg={this.msg} handle={this.handle}>
        </test2>
        <span>{this.msg}</span>
      </div>
    )
  }
}
</script>
