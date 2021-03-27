<template>
  <div>
    <q-item
      clickable
      v-for="(el, i) in links"
      :key="i"
      @click="$router.push(el.link)"
    >
      <q-item-section v-if="el.icon" avatar>
        <q-icon :name="el.icon" />
      </q-item-section>

      <q-item-section>
        <q-item-label>{{ el.title }}</q-item-label>
        <q-item-label caption>
          {{ el.caption }}
        </q-item-label>
      </q-item-section>
    </q-item>
  </div>
</template>

<script>
export default {
  name: "EssentialLink",
  props: {
    links: {
      type: Array,
      default: () => [],
    },
  },
};
</script>
