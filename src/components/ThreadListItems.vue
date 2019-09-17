<template>
  <div class="threadListItems">

    <div class="thread">
      <div>
        <p>
          <a :href="`/thread/${thread['.key']}`">{{thread.title}}</a>
        </p>
        <p class="text-faded text-xsmall">
          By <a href="#">{{user.name}}</a>, {{thread.publishedAt}}.
        </p>
      </div>

      <div class="activity">
        <p class="replies-count">
          {{repliesCout}} replies
        </p>

        <img
          class="avatar-medium"
          src="http://i0.kym-cdn.com/photos/images/facebook/000/010/934/46623-batman_pikachu_super.png"
          alt=""
        >

        <div>
          <p class="text-xsmall">
            <a href="profile.html">Bruce Wayne</a>
          </p>
          <p class="text-xsmall text-faded">2 hours ago</p>
        </div>
      </div>
    </div>

  </div>
</template>

<script>
import sourseData from '@/data'

export default {

  props: {
    thread: {
      requrired: true,
      type: Object
    }
  },
  computed: {
    repliesCout () {
      return Object.keys(this.thread.posts).length - 1
    },
    user () {
      return sourseData.users[this.thread.userId]
    }
  }

}
</script>
