<template>
  <div class="q-pa-md">
    <q-table grid :rows="rows" :columns="columns">
      <template v-slot:item="props">
        <div class="q-pa-sm col-xs-12 col-sm-6 col-md-3">
          <div style="outline: none">
            <img
              :src="props.row.imageUrlProp"
              width="100%"
              height="160px"
            />
            <div
              class="flex flex-start items-center"
              style="gap: 15px; margin-top: 15px"
            >
              <img
                :src="props.row.imageUrlProp"
                width="40px"
                height="40px"
                style="border-radius: 50px"
              />
              <div>
                <strong>{{ props.row.title }}</strong>
                <div>{{ props.row.subtitle }}</div>
                <div class="subtitle">{{ props.row.followers }}</div>
              </div>
            </div>
          </div>
        </div>

        <div class="q-pa-sm col-xs-12 col-sm-6 col-md-3">
          <div style="outline: none">
            <img
              :src="props.row.imageUrlProp"
              width="100%"
              height="160px"
            />
            <div
              class="flex flex-start items-center"
              style="gap: 15px; margin-top: 15px"
            >
              <img
                :src="props.row.imageUrlProp"
                width="40px"
                height="40px"
                style="border-radius: 50px"
              />
              <div>
                <strong>{{ props.row.title }}</strong>
                <div>{{ props.row.subtitle }}</div>
                <div class="subtitle">{{ props.row.followers }}</div>
              </div>
            </div>
          </div>
        </div>
        <div class="q-pa-sm col-xs-12 col-sm-6 col-md-3">
          <div style="outline: none">
            <img :src="props.row.imageUrlProp" width="100%" height="160px" />
            <div
              class="flex flex-start items-center"
              style="gap: 15px; margin-top: 15px"
            >
              <img
                :src="props.row.imageUrlProp"
                width="40px"
                height="40px"
                style="border-radius: 50px"
              />
              <div>
                <strong>{{ props.row.title }}</strong>
                <div>{{ props.row.subtitle }}</div>
                <div class="subtitle">{{ props.row.followers }}</div>
              </div>
            </div>
          </div>
        </div>
        <div class="q-pa-sm col-xs-12 col-sm-6 col-md-3">
          <div style="outline: none">
            <img
             :src="props.row.imageUrlProp"
              width="100%"
              height="160px"
            />
            <div
              class="flex flex-start items-center"
              style="gap: 15px; margin-top: 15px"
            >
              <img
                :src="props.row.imageUrlProp"
                width="40px"
                height="40px"
                style="border-radius: 50px"
              />
              <div>
                <strong>{{ props.row.title }}</strong>
                <div>{{ props.row.subtitle }}</div>
                <div class="subtitle">{{ props.row.followers }}</div>
              </div>
            </div>
          </div>
        </div>
      </template>
    </q-table>
  </div>
</template>

<script>

const rows = [
   {
    imageUrlProp: "https://cdn.quasar.dev/img/mountains.jpg",
    title: "Mountain Image",
    subtitle: "A mountain image with a caption.",
    followers: "100k",
  },
  {
    imageUrlProp: "https://cdn.quasar.dev/img/parallax2.jpg",
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
    imageUrlProp: "https://cdn.quasar.dev/img/quasar.jpg",
    title: "Mountain Image",
    subtitle: "A mountain image with a caption.",
    followers: "100k",
  },
  
 
];
</script>

<style lang="sass">
.example-masonry-table-grid
  flex-direction: column
  height: 700px

  &--2
    > div
      &:nth-child(2n + 1)
        order: 1
      &:nth-child(2n)
        order: 2

    &:before
      content: ''
      flex: 1 0 100% !important
      width: 0 !important
      order: 1
  &--3
    > div
      &:nth-child(3n + 1)
        order: 1
      &:nth-child(3n + 2)
        order: 2
      &:nth-child(3n)
        order: 3

    &:before,
    &:after
      content: ''
      flex: 1 0 100% !important
      width: 0 !important
      order: 2
</style>

<script setup>
defineOptions({
  name: "testPage",
});
</script>
