<template>
  <q-item
    clickable
    tag="a"
    target="_blank"
    :href="props.link"
  >
    <q-item-section
      v-if="props.icon"
      avatar
      class="navbar"
    >
      <q-icon :name="props.icon" size="25px"/>
      <q-item-label class="nav-title">{{ props.title }}</q-item-label>
    </q-item-section>

    
  </q-item>
</template>

<script setup>
defineOptions({
  name: 'EssentialLink'
})

const props = defineProps({
  title: {
    type: String,
    required: true
  },


  link: {
    type: String,
    default: '#'
  },

  icon: {
    type: String,
    default: ''
  }
})
</script>

<style>
q-icon {
  color: black;
}
.navbar {
  padding: 10px 10px 10px 0;
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
}
.nav-title {
  font-size: 10px; 
  font-weight: 300;
  margin-top: 3px;
  text-align: right;
}
</style>