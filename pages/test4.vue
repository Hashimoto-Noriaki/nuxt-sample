<template>
  <div>
    <v-text-field ref="number" v-model="number" />
    <div>数値: {{ number }}</div>
    <div :class="$style.container" v-for="user in users" :key="user.id">
      <div>名前: {{ user.name }}</div>
      <div>メールアドレス: {{ user.email }}</div>
      <div>電話番号: {{ user.phone }}</div>
    </div>
  </div>
</template>

<script>
export default {
  computed: {
    users() {
      return this.$store.state.user.users
    },
  },

  async created() {
    await this.$store.dispatch('user/fetchUsers')
  },
}
</script>

<style lang="scss" module>
.container {
  margin: 10px 0;
  padding: 8px;
  border: 2px solid #ccc;
  border-radius: 4px;
}
</style>
