
<template>
<section class="text-gray-600 body-font">
<Header/>
  <div class="container px-5 py-24 mx-auto">
    <div class="flex flex-wrap -mx-4 -my-8">
      <div class="py-8 px-4 lg:w-1/3" v-for="(post, index) in posts" :key="index">
        <div class="h-full flex items-start">
          <div class="w-12 flex-shrink-0 flex flex-col text-center leading-none">
            <span class="text-gray-500 pb-2 mb-2 border-b-2 border-gray-200">{{new Date(post.created_at).getMonth()+1}}</span>
            <span class="font-medium text-lg text-gray-800 title-font leading-none">{{new Date(post.created_at).getDate()}}</span>
          </div>
          <div class="flex-grow pl-6">
            <h1 class="title-font text-xl font-medium text-gray-900 mb-3"><a v-bind:href="'/advent/post/'+post.id">{{post.title}}</a></h1>
            <p class="leading-relaxed mb-5">{{post.body.substr(0, 50)}}{{(post.body.length > 50)?"..." : ""}}<br>
            <a v-bind:href="'/advent/post/'+post.id" class="text-blue-500 inline-flex items-center">Learn More
            <svg class="w-4 h-4 ml-2" viewBox="0 0 24 24" stroke="currentColor" stroke-width="2" fill="none" stroke-linecap="round" stroke-linejoin="round">
              <path d="M5 12h14"></path>
              <path d="M12 5l7 7-7 7"></path>
            </svg>
          </a></p>
            <a class="inline-flex items-center">
              <img alt="blog" v-bind:src="post.user.avatar_url" class="w-8 h-8 rounded-full flex-shrink-0 object-cover object-center">
              <span class="flex-grow flex flex-col pl-3">
                <span class="title-font font-medium text-gray-900">{{post.user.login}}</span>
              </span>
            </a>
          </div>
        </div>
      </div>
    </div>
  </div>
</section>
</template>

<script>
import Header from '../components/Header'
export default {
  async asyncData({ $axios }) {
            // 取得先のURL
            const url = "https://api.github.com/repos/e2yamazaki/advent/issues";
            // リクエスト（Get）
            const response = await $axios.$get(url);
            // 配列で返ってくるのでJSONにして返却
            return {
                posts: response
            };
        }
}
</script>

<style>
</style>