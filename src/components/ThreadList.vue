<template>
  <div class="hello">

    <div class="thread-list">

      <h2 class="list-title">Threads</h2>
      <ThreadListItems
        v-for="thread in threads"
        :key="thread['.key']"
        :thread="thread"
      />

    </div>

    <div class="pagination">
      <button
        class="btn-circle"
        disabled
      ><i class="fa fa-angle-left"></i></button>
      1 of 3
      <button class="btn-circle"><i class="fa fa-angle-right"></i></button>
    </div>
  </div>

</template>

<script>

import ThreadListItems from './ThreadListItems'
export default {
  name: 'ThreadList',
  components: {
    ThreadListItems
  },

  props: {
    threads: {
      required: true,
      type: Array
    }
  },

  data () {
    return {

    }
  }
}
</script>
