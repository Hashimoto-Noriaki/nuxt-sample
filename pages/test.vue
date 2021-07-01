<template>
  <div>
    <!-- <v-ifの仲間> -->
    <div v-if="score >= 80">よくできた</div>
    <div v-else-if="score >= 30">まあまあ</div>
    <div v-else>ファイト</div>

    <!-- <a :href="googleLink">あっちゃん</a> -->
    <img v-bind:src="imageUrl()" alt="よくできたね!" width="100px" />

    <!-- <v-btn @click="showMessage('クリック')">クリック</v-btn>
    <v-btn @dblclick="showMessage('ダブルクリック')">ダブルクリック</v-btn>
    <v-btn @mouseenter="showMessage('マウスエンター')">マウスエンター</v-btn>
    <v-btn @mouseleave="showMessage('マウスリブ')">マウスリブ</v-btn> -->

    <!-- <v-show> -->
    <!-- <div v-show="isShown">見えるぞ!</div>
    <v-btn @click="toggleShown">表示/非表示の切り替え</v-btn> -->
    <input v-model="score" type="text" />
    <v-text-field v-model="score" />

    <div v-for="animal in animals" :key="animal.name">{{ animal.name }}</div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      isShown: true,
      score: 90,
      googleLink: 'https://google.com',
      animals: [
        { name: 'monkey' },
        { name: 'lion' },
        { name: 'dog' },
        { name: 'crocodile' },
      ],
    }
  },
  methods: {
    toggleShown() {
      this.isShown = !this.isShown
    },
    imageUrl() {
      if (this.score >= 90) {
        return 'https://2.bp.blogspot.com/-zDsrPiqkR_0/U0pTNj7lpoI/AAAAAAAAfGA/2Z1onz10tAw/s800/grade2_yokudekimashita.png'
      } else if (this.score >= 50) {
        return 'https://2.bp.blogspot.com/-wJDmO2MIKkg/U0pTOEZT-JI/AAAAAAAAfGc/p9uwt9Msq9A/s800/grade3_ganbarimashita.png'
      } else {
        return 'https://2.bp.blogspot.com/-Bc8NTQ2PqY8/U0pTOuIDWQI/AAAAAAAAfGY/1RU2LKdozKs/s800/grade5_ganbarimasyou.png'
      }
    },
    showMessage(message) {
      alert(message)
    },
  },
}
</script>
