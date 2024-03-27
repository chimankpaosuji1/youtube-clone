<template>
  <q-page padding>
    <div class="card">
      <div v-for="(artist, x) in artists" :key="x">
        <img
          :src="artist.imageUrlProp"
          width="100%"
          height="60%"
          class="image"
        />
        <div
          class="flex flex-start items-center"
          style="gap: 15px; margin-top: 15px"
        >
          <img
             :src="artist.imageUrlProp"
            width="40px"
            height="40px"
            style="border-radius: 50px"
          />
          <div>
            <div class="title">{{ artist.title }}</div>
            <div class="subtitle">{{ artist.subtitle }}</div>
            <div class="subtitle">{{ artist.followers }}</div>
          </div>
        </div>
        </div>    
      </div>
  </q-page>
</template>

<style>
.card {
  display: grid;
  grid-template-columns: auto auto auto auto;
  gap: 20px;
}
.title {
  font-weight: bold;
}
.image {
  border-radius: 10px;
}
@media only screen and (max-width: 1400px) {
  .card {
    grid-template-columns: auto auto auto;
  }
}
@media only screen and (max-width: 1100px) {
  .card {
    grid-template-columns: auto auto;
  }
}

@media only screen and (max-width: 640px) {
  .card {
    grid-template-columns: auto;
  }
}
</style>

<script setup>
import DataLink from  'components/DataLink.vue'
defineOptions({
  name: "IndexPage",

  data() {
    return {
      
      artists: [
        {
          imageUrlProp: "https://cdn.quasar.dev/img/parallax1.jpg",
          title: "Mountain Image",
          subtitle: "A mountain image with a caption.",
          followers: "100k",
        },
         {
          imageUrlProp: "https://cdn.quasar.dev/img/parallax1.jpg",
          title: "Mountain Image",
          subtitle: "A mountain image with a caption.",
          followers: "100k",
        },
         {
          imageUrlProp: "https://cdn.quasar.dev/img/parallax1.jpg",
          title: "Mountain Image",
          subtitle: "A mountain image with a caption.",
          followers: "100k",
        },
         {
          imageUrlProp: "https://cdn.quasar.dev/img/parallax1.jpg",
          title: "Mountain Image",
          subtitle: "A mountain image with a caption.",
          followers: "100k",
        },
         {
          imageUrlProp: "https://cdn.quasar.dev/img/mountains.jpg",
          title: "Mountain Image",
          subtitle: "A mountain image with a caption.",
          followers: "100k",
        },
         {
          imageUrlProp: "https://cdn.quasar.dev/img/mountains.jpg",
          title: "Mountain Image",
          subtitle: "A mountain image with a caption.",
          followers: "100k",
        },
         {
          imageUrlProp: "https://cdn.quasar.dev/img/mountains.jpg",
          title: "Mountain Image",
          subtitle: "A mountain image with a caption.",
          followers: "100k",
        },
         {
          imageUrlProp: "https://cdn.quasar.dev/img/mountains.jpg",
          title: "Mountain Image",
          subtitle: "A mountain image with a caption.",
          followers: "100k",
        },
         {
          imageUrlProp: "https://cdn.quasar.dev/img/quasar.jpg",
          title: "Mountain Image",
          subtitle: "A mountain image with a caption.",
          followers: "100k",
        },
         {
          imageUrlProp: "https://cdn.quasar.dev/img/quasar.jpg",
          title: "Mountain Image",
          subtitle: "A mountain image with a caption.",
          followers: "100k",
        },
         {
          imageUrlProp: "https://cdn.quasar.dev/img/quasar.jpg",
          title: "Mountain Image",
          subtitle: "A mountain image with a caption.",
          followers: "100k",
        },
         {
          imageUrlProp: "https://cdn.quasar.dev/img/quasar.jpg",
          title: "Mountain Image",
          subtitle: "A mountain image with a caption.",
          followers: "100k",
        },
         {
          imageUrlProp: "https://cdn.quasar.dev/img/parallax1.jpg",
          title: "Mountain Image",
          subtitle: "A mountain image with a caption.",
          followers: "100k",
        },
         {
          imageUrlProp: "https://cdn.quasar.dev/img/parallax1.jpg",
          title: "Mountain Image",
          subtitle: "A mountain image with a caption.",
          followers: "100k",
        },
         {
          imageUrlProp: "https://cdn.quasar.dev/img/parallax1.jpg",
          title: "Mountain Image",
          subtitle: "A mountain image with a caption.",
          followers: "100k",
        },
         {
          imageUrlProp: "https://cdn.quasar.dev/img/parallax1.jpg",
          title: "Mountain Image",
          subtitle: "A mountain image with a caption.",
          followers: "100k",
        },
        
      ],
    };
  },
});
</script>
