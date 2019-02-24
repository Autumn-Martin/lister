<template>
  <div id="list">
    <div class="holder">
      <ul>
        <li v-for="(data, index) in list" :key='index'>
          {{index + 1}}. {{data.item}}
        </li>
      </ul>
    </div>
    <h2 v-if="list.length >= 5">I have lots to do!</h2>
    <h2 v-else>Don't I have work to do?</h2>
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
<style scoped>
  ul {
    margin: 0;
    padding: 0;
    list-style-type: none;
  }

  ul li {
    padding: 20px;
    font-size: 1.3em;
    background-color: #E0EDF4;
    border-left: 5px solid #3EB3F6;
    margin-bottom: 2px;
    color: turquoise;
  }

  p {
    text-align: center;
    padding: 30px 0;
    color: gray;
  }

  .container {
    box-shadow: 0px 0px 40px lightgray;
  }

  .holder {
    background: #fff;
  }

  #list {
    text-align: left;
    margin: 0% 25% 0% 25%;
  }
</style>
