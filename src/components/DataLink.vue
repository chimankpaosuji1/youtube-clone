<template>
  <div>
    <img :src="imageUrl" alt="Image">
  </div>
</template>

<script>
export default {
  name: 'DataLink',
  props: {
    imageUrl: {
      type: String,
      required: true
    },
   
  }
}
</script>

