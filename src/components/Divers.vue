<template>
  <section class="content__divers">
    <article v-for="div in divers" :key="div">
      <h2>{{ div.name }}</h2>
      <ul>
        <li v-for="list in div.list" :key="list" v-html="list">{{ list }}</li>
      </ul>
    </article>
  </section>
</template>

<script>
export default {
  name: 'Divers',
  props: ['divers']
}
</script>
