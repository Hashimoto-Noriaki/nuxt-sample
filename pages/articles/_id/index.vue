<template>
  <div>
    <div>詳細ページ</div>
    <div>
      <nuxt-link to="/articles/10/edit">Nuxt Link</nuxt-link>
    </div>
    <div>
      <a href="/articles/10/edit">リンク</a>
    </div>
  </div>
</template>

<script>
export default {
  mounted() {
    const piko = 'piko'
    console.log(piko)
  },
}
</script>
