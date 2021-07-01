<template>
  <div>
    <div>よも</div>
    <v-text-field ref="number" v-model="number" />
    <div>数値: {{ number }}</div>
    <div :class="$style.container" v-for="user in users" :key="user.id">
      <div>名前:{{ user.name }}</div>
      <div>メールアドレス:{{ user.email }}</div>
      <div>電話:{{ user.phone }}</div>
      <div>住所:{{ user.address }}</div>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      number: 0,
      users: [],
    }
  },

  created() {
    console.log('created')

    this.$axios
      .get('http://jsonplaceholder.typicode.com/users')
      .then((response) => {
        this.users = response.data
      })
  },

  mounted() {
    console.log('mounted')
    this.$refs.number.focus()
  },

  updated() {
    console.log('updated')
    console.log(this.number)
  },

  destroyed() {
    console.log('destroyed')
  },
}
</script>

<style lang="scss" module>
.container {
  margin: 10px 0;
  padding: 10px;
  border-radius: 6px;
  border: 2px solid white;
}
</style>
