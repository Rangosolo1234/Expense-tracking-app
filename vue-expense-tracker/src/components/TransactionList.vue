<template>
    <h3>History</h3>
    <ul id="list" class="list">
    <li v-for="transaction in transactions" v-bind:key="transaction.id" :class="transaction.amount < 0 ? 'minus' : 'plus'">
        {{ transaction.text }} <span>-${{ transaction.amount }}</span><button class="delete-btn">x</button>
    </li>
</ul>
      <!-- <ul id="list" class="list">
        <li class="minus">
          Cash <span>-$400</span><button class="delete-btn">x</button>
        </li>
        <li class="plus">
          Paycheck <span>-$800</span><button class="delete-btn">x</button>
        </li>
     -->
</template>
<script setup>
  import {defineProps} from 'vue';

  const props = defineProps({
    type: array

  })
</script>