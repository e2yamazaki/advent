<template>
<section class="text-gray-600 body-font">
<Header/>
  <div class="container px-5 py-24 mx-auto">
    <div class="xl:w-1/2 lg:w-3/4 w-full mx-auto text-center">
      <header class="pt-6 xl:pb-10"><div class="space-y-1 text-center"><dl class="space-y-10"><div><dt class="sr-only">Published on</dt><dd class="text-base leading-6 font-medium text-gray-500">{{new Date(created_at).toLocaleString('ja-JP')}}</dd></div></dl><div><h1 class="text-3xl font-extrabold text-gray-900 tracking-tight sm:text-4xl md:text-5xl md:leading-[3.5rem]">{{title}}</h1></div></div></header>
      <div class="leading-relaxed text-lg text-left" v-html="$md.render(body)"></div>
      <span class="inline-block h-1 w-10 rounded bg-blue-500 mt-8 mb-6"></span>
      <div>
        <a class="inline-flex items-center">
          <img alt="blog" v-bind:src="user.avatar_url" class="w-12 h-12 rounded-full flex-shrink-0 object-cover object-center">
          <span class="flex-grow flex flex-col pl-4">
            <span class="title-font font-medium text-gray-900">{{user.login}}</span>
          </span>
        </a>
        </div>
    </div>
  </div>
</section>
</template>

<script>
import Header from '../../components/Header'
    export default {
        data () {
            return {
                // テスト用データ
                title: 'test',    // タイトル
                body: '# こちらのキットを使用しました。![IMG_9572](https://user-images.githubusercontent.com/15883487/152670525-0a3da3f8-67a2-415f-80f9-2a0ab2cdc0d4.PNG)',  // コンテンツ
                created_at : '', // 作成日時
                user: {
                    avatar_url: '',
                    login: 'test'
                }
            }
        },
        async asyncData ({params, error, payload }) {
            // payloadでデータを受け取った場合
            if (payload) {
                return {
                    title: payload.title,
                    body: payload.body,
                    created_at: payload.created_at,
                    user : payload.user
                }
            }
        }
    }
</script>