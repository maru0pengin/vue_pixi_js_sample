<template>
  <div class="flex justify-center">
    <div class="mt-40 mb-24 mx-10">
      <div class="bg-white rounded-xl border-4 py-6 flex flex-col items-center">
        ボタンをクリックすると<br />Twitterのログイン画面へ遷移します。
        <button
          @click="gotoLogin"
          class="button_twitter m-4 focus:outline-none"
        >
          <img src="@/assets/icons/Twitter_white.svg" class="w-6 h-6" />
          <p class="text-white pl-2">Twitterでログイン</p>
        </button>
        <hr width="400" />
        <div class="my-2 text-sm p-4">
          本サイトは作品を投稿した方の情報を保持するためにTwitterアカウントの連携を必要としています。
          <div class="text-xs my-2 text-left">
            <li>連携許可をログイン以外の目的で使用することはありません。</li>
            <li>あなたのアカウントから勝手にツイートすることはありません。</li>
            <li>DMなどを勝手に送信することはありません。</li>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {}
  },
  computed: {
    user() {
      return this.$store.getters.user
    },
    userStatus() {
      // ログインするとtrue
      return this.$store.getters.isSignedIn
    },
  },
  methods: {
    gotoLogin() {
      this.$router.push({
        name: 'login_logout_loading',
        query: this.$route.query,
        params: {
          isLogin: true,
        },
      })
    },
  },
}
</script>

<style lang="sass" scoped>
.button_twitter
  background: #00acee
  @apply p-4 rounded-lg flex

li
  @apply py-1
</style>
