<template>
  <article class="content__pro">
    <h2>{{ pro.name }}</h2>
    <aside v-for="list in pro.list" :key="list">
      <p>{{ list.date }}</p>
      <p>{{ list.content }}</p>
    </aside>
  </article>
</template>

<script>
export default {
  name: 'Pro',
  props: ['pro']
}
</script>
