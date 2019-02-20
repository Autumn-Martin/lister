<template>
  <div class="list">
    <div class="holder">
      <ul>
        <li v-for="(data, index) in list" :key='index'>
          {{index + 1}}. {{data.item}}
        </li>
      </ul>
    </div>
    <h2 v-if="list.length >= 5">You have lots to do!</h2>
    <h2 v-else>Don't you have work to do?</h2>
  </div>
</template>

<script>
export default {
  name: 'Skills',
  data() {
    return {
      list: [
          { "item": "find a puppy" },
          { "item": "ski Crested Butte" },
          { "item": "speak French" },
          { "item": "learn this Vue thing"},
          { "item": "catch a gopher"},
          { "item": "go to the art museum"},
          { "item": "see Guardians of the Galaxy, Vol 1 again"}
      ]
    }
  },
}
</script>
