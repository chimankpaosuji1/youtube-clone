<template>
  <div class="q-pa-md">
    <q-table
      grid
       
      :rows="rows"
      :columns="columns"
    >

      <template v-slot:item="props">
        <div class="q-pa-sm col-xs-12 col-sm-6 col-md-3">
          <div style="outline: none;">
             <img src="../assets/cards/parallax1.jpg" width="100%"  height="160px">
            <q-card-section class="text-start">
              
              
              <strong>{{ props.row.name }}</strong>
            
              <div>{{ props.row.calories }}</div>
            </q-card-section>
          </div>
        </div>
        
        <div class="q-pa-sm col-xs-12 col-sm-6 col-md-3">
          <div style="outline: none;">
            <img src="../assets/cards/mountains.jpg" width="100%" height="160px">
            <q-card-section class="text-start">
              
              
              <strong>{{ props.row.name }}</strong>
            
              <div>{{ props.row.calories }}</div>
            </q-card-section>
          </div>
        </div>
        <div class="q-pa-sm col-xs-12 col-sm-6 col-md-3">
          <div style="outline: none;">
             <img src="../assets/cards/quasar.jpg" width="100%" height="160px">
            <q-card-section class="text-start">
              
              
              <strong>{{ props.row.name }}</strong>
            
              <div>{{ props.row.calories }}</div>
            </q-card-section>
          </div>
        </div>
        <div class="q-pa-sm col-xs-12 col-sm-6 col-md-3">
          <div style="outline: none;">
             <img src="../assets/cards/parallax1.jpg" width="100%" height="160px">
           <q-card-section class="text-start">
              
              
              <strong>{{ props.linksList}}</strong>
            
              <div>{{ props.rows}}</div>
            </q-card-section>
          </div>
        </div>
      </template>
    </q-table>
  </div>
  
</template>

<script>
import { useQuasar } from "quasar";
import { ref, computed, watch } from "vue";



const deserts = [
  "Frozen Yogurt",
  "Ice cream sandwich",
  "Eclair",
  "Cupcake",
  "Gingerbread",
  "Jelly bean",
  "Lollipop",
  "Honeycomb",
  "Donut",
  "KitKat",
];

const rows = [
  "label",
  "field",
   "calories", 
   "Calories (g)",
   "calories"];

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
  name: "IndexPage",
  
});
</script>
