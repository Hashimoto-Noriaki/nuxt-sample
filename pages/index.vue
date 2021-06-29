<template>
  <div class="container">
    <div class="number">{{ count }}</div>
    <!-- <v-btn class="mx-1" fab dark @click="plus" color="pink">
      <v-icon dark> mdi-plus </v-icon>
    </v-btn>

    <v-btn class="mx-1" fab dark @click="minus" color="yellow">
      <v-icon dark> mdi-minus </v-icon>
    </v-btn> -->

    <counter-button kind="plus" ,color="pink" @click="plus" />
    <counter-button kind="minus" ,color="yellow" @click="minus" />
  </div>
</template>

<script>
import CounterButton from '@/components/CounterButton.vue'

export default {
  components: {
    CounterButton,
  },
  data() {
    return {
      count: 100,
    }
  },
  methods: {
    plus() {
      this.count += 1
    },
    minus() {
      this.count -= 1
    },
  },
}
</script>

<style lang="scss">
.container {
  .number {
    font-size: 100px;
    color: white;
  }
}
</style>
<!-- <div class="container"> -->
<!-- <div class="number">{{ count }}</div> -->

<!-- <v-btn class="mx-1" fab dark color="green" @click="plus">
      <v-icon dark> mdi-plus</v-icon>
    </v-btn>

    <v-btn class="mx-1" fab dark color="red" @click="minus">
      <v-icon dark> mdi-minus</v-icon>
    </v-btn> -->

<!-- <counter-button kind="plus" color="blue" @click="plus" />
    <counter-button kind="minus" color="orange" @click="minus" />
  </div>
</template> -->

<!-- <script>
import CounterButton from '@/components/CounterButton.vue'

export default {
  components: {
    CounterButton,
  },

  data() {
    return {
      count: 100,
    }
  },
  methods: {
    plus() {
      this.count += 1
    },
    minus() {
      this.count -= 1
    },
  },
}
</script>

<style lang="scss" module>
// .container {
//   .number {
//     font-size: 70px;
//   }
// }
//
// </style> -->
