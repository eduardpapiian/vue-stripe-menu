<template>
  <div>
    <base-title title="Demo" />
    <pre><code class="javascript">{{ DemoHeaderRaw }}</code></pre>
  </div>
</template>

<script>
// eslint-disable-next-line
import DemoHeaderRaw from '!!raw-loader!../BaseHeader'
import BaseTitle from '../BaseTitle'
import highlight from 'highlight.js'

export default {
  components: {
    BaseTitle
  },
  data () {
    return {
      DemoHeaderRaw
    }
  },
  mounted () {
    highlight.initHighlightingOnLoad()
  }
}
</script>
