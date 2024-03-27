<template>
  <q-page padding>
    <div class="card">
      <div v-for="(datalink, x) in datalinks" :key="x">
        <img
          :src="datalink.imageUrlProp"
          width="100%"
          height="60%"
          class="image"
        />
        <div
          class="flex flex-start items-center"
          style="gap: 15px; margin-top: 15px"
        >
          <img
             :src="datalink.imageUrlProp"
            width="40px"
            height="40px"
            style="border-radius: 50px"
          />
          <div>
            <div class="title">{{ datalink.title }}</div>
            <div class="subtitle">{{ datalink.subtitle }}</div>
            <div class="subtitle">{{ datalink.followers }}</div>
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
defineOptions({
  name: "IndexPage",

  data() {
    return {
      
      datalinks: [
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
