<template>
    <div class="post-list-page">
        <h1>포스트 게시글</h1>
        <post-list :posts="posts" />
    </div>
</template>

<script>
import PostList from '@/components/PostList'
//import api from '@/api'
import { mapActions, mapState } from 'vuex'

export default {
    name : 'PostListPage',
    components : { PostList },
    // data() {
    //    return {
    //        posts : []
    //    }
    // },
    computed : {
        ...mapState([ 'posts' ])
    },
    created() {
        this.fetchPostList()

      //  api.get('/posts')
      //  .then(res => {
      //      this.posts = res.data
      //  })
    },
    methods : {
        ...mapActions(['fetchPostList'])
    }
}
</script>