<template>
  <div class="threadShow">
    <div class="col-large push-top">

      <h2>{{thread.title}}</h2>

      <div
        class="post-list"
        v-for="postId in thread.posts"
        :key="postId.id"
      >

        <div class="post">

          <div class="user-info">
            <a
              href="#"
              class="user-name"
            >{{users[posts[postId].userId].name}}</a>

            <a href="#">
              <img
                v-if="!users[posts[postId].userId].avatar"
                class="avatar-large"
                src="http://i.imgur.com/s0AzOkO.png"
                alt=""
              >

              <img
                v-if="users[posts[postId].userId].avatar"
                class="avatar-large"
                :src="users[posts[postId].userId].avatar"
                alt=""
              >
            </a>

            <p class="desktop-only text-small">107 posts</p>

          </div>

          <div class="post-content">
            <div>
              <p>
                {{ posts[postId].text }}
              </p>
            </div>
            <a
              href="#"
              style="margin-left: auto;"
              class="link-unstyled"
              title="Make a change"
            ><i class="fa fa-pencil"></i></a>
          </div>

          <div class="post-date text-faded">
            {{ posts[postId].publishedAt }}
          </div>

          <div class="reactions">
            <ul>
              <li>💡</li>
              <li>❤️</li>
              <li>👎</li>
              <li>👍</li>
              <li>👌</li>
            </ul>
            <button class="btn-xsmall"><span class="emoji">❤️</span>️ 3</button>
            <button class="btn-xsmall active-reaction"><span class="emoji">👌️</span>️ 1</button>
            <button class="btn-xsmall">+ <i class="fa fa-smile-o emoji"></i></button>
          </div>

        </div>

      </div>
    </div>
  </div>
</template>

<script>
import sourseData from '@/data'
export default {
  props: {
    id: {
      required: true,
      type: String
    }
  },
  data () {
    return {
      thread: sourseData.threads[this.id],
      posts: sourseData.posts,
      users: sourseData.users
    }
  }
}
</script>
