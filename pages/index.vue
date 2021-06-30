<template>
  <div class="container">
    <div class="number">{{ count }}</div>
    <!-- <button class="button" @click="plus">+</button>
    <button class="button" @click="minus">-</button> -->

    <!-- <v-btn class="mx-1" fab dark color="yellow" @click="plus">
      <v-icon dark>mdi-plus</v-icon>
    </v-btn>

    <v-btn class="mx-1" fab dark color="blue" @click="minus">
      <v-icon dark>mdi-minus</v-icon>
    </v-btn>

    <v-btn class="mx-2" fab dark large color="cyan">
      <v-icon dark> mdi-pencil </v-icon>
    </v-btn> -->

    <counter-button kind="plus" color="yellow" @push="plus" />
    <counter-button kind="minus" color="blue" @push="minus" />
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
      this.count += 10
    },
    minus() {
      this.count -= 10
    },
  },
}
</script>

<style lang="scss">
.number {
  font-size: 80px;
}

// .button {
//   font-size: 40px;
//   font-weight: 30px;
//   border: 2px solid gray;
//   width: 60px;
//   height: 60px;
//   border-radius: 6px;
// }
</style>

<!-- <div class="container"> -->

<!-- <div class="number">{{ count }}</div> -->

<!-- <v-btn class="mx-1" fab dark color="green" @click="plus">
//       <v-icon dark> mdi-plus</v-icon>
//     </v-btn>

//     <v-btn class="mx-1" fab dark color="red" @click="minus">
//       <v-icon dark> mdi-minus</v-icon>
//     </v-btn> -->

<!-- <counter-button kind="plus" color="blue" @click="plus" />
//     <counter-button kind="minus" color="orange" @click="minus" />
//   </div>
// </template> -->

<!-- <script>
// import CounterButton from '@/components/CounterButton.vue'

// export default {
//   components: {
//     CounterButton,
//   },

//   data() {
//     return {
//       count: 100,
//     }
//   },
//   methods: {
//     plus() {
//       this.count += 1
//     },
//     minus() {
//       this.count -= 1
//     },
//   },
// }
// </script>

// <style lang="scss" module>
// .container {
//   .number {
//     font-size: 70px;
//   }
// }
//
// </style> -->
