<template>
  <article class="content__skill">
    <h2>{{ title }}</h2>
    <section>
      <aside v-for="skill in skills" :key="skill">
        <h3>{{ skill.title }}</h3>
        <ul class="stars">
          <li v-for="list in skill.list" :key="list.name">
            <p>{{ list.name }}</p>
            <i class="fa fa-star" aria-hidden="true" v-for="star in list.stars" :key="star"></i>
            <i class="fa fa-star grey" aria-hidden="true" v-for="star in (5 - list.stars)" :key="star">
            </i>
          </li>
        </ul>
      </aside>
    </section>
  </article>
</template>

<script>
export default {
  name: 'Skill',
  props: ['skills', 'title']
}
</script>
