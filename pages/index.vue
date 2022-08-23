<template>
  <v-data-table 
    :headers="headers"
    :items="restaurants"
  >
  </v-data-table>
  <!-- <v-container>
    <v-list>
      <v-list-item v-for="(restaurant, key) in restaurants" :key="key">
        {{ restaurant.shopName }} : {{ restaurant.point }}
      </v-list-item>
    </v-list>
  </v-container> -->
</template>

<script>

import restaurants from '../assets/output.json';

export default {
  name: 'IndexPage',
  data(){
    return {
        restaurants: restaurants,
        headers: [
          { text: '店名', value: 'shopName' },
          { text: '食べログ点数', value: 'point' }
        ]
    };
  }
}
</script>
