<template>
  <q-layout view="hHh Lpr lff">
    <q-header class="bg-white" style="padding: 5px 0;">
      <q-toolbar style="align-items: center; justify-content: space-between">
        <div
          style="
            display: flex;
            align-items: center;
            justify-content: flex-start;
          "
        >
          <q-btn
            flat
            dense
            round
            icon="menu"
            aria-label="Menu"
            @click="toggleLeftDrawer"
          />

          <q-toolbar-title>
            <img
              src="../assets/img.svg"
              width="100px"
              style="margin-top: 7px"
            />
          </q-toolbar-title>
        </div>

        <div
          style="
            display: flex;
            align-items: center;
            justify-content: flex-start;
            width: 40%;
          "
        >
          <q-input
            dense
            borderless="borderless"
            debounce="300"
            placeholder="Search"
            style="
              width: 100%;
              border-radius: 20px;
              border: 1px solid rgba(0, 0, 0, 0.25);
              padding: 0 0 0 15px;
            "
          >
            <template v-slot:append>
              <q-icon
                name="search"
                size="20px"
                style="
                  padding: 10px;
                  width: 40px;
                  padding-left: 10px;
                  border-radius: 20px;
                  background: rgba(0, 0, 0, 0.1);
                "
              />
            </template>
          </q-input>

          <q-icon name="mic" size="20px" style="padding: 8px" />
        </div>
        <div
          style="display: flex; align-items: center; justify-content: flex-end"
        >
          <q-icon :name="akarMoreVertical" size="20px" />

          <div
            style="
              align-items: center;
              justify-content: center;
              padding: 5px 10px;
              border: 1px solid #2B74BA;
              border-radius: 25px;
              margin-left: 10px;
            "
          >
            <q-icon
              name="person"
              size="15px"
              color="white"
              style="padding: 1px; background: #2B74BA; border-radius: 50%"
            />
            <span class="profile">Chimankpa</span>
          </div>

          <q-icon name="invert_colors" size="20px" style="margin-left: 10px" />
        </div>
      </q-toolbar>
    </q-header>

    <q-drawer v-model="leftDrawerOpen" show-if-above width="80">
      <q-list>
        <EssentialLink
          v-for="link in linksList"
          :key="link.title"
          v-bind="link"
        />
      </q-list>
    </q-drawer>

    <q-page-container>
      <router-view />
    </q-page-container>
  </q-layout>
</template>

<script setup>
import { ref } from "vue";
import EssentialLink from "components/EssentialLink.vue";
import { akarMoreVertical } from "quasar-extras-svg-icons/akar-icons";

defineOptions({
  name: "MainLayout",
});

const linksList = [
  {
    title: "Home",
    icon: "home",
  },
  {
    title: "Shorts",
    icon: "music_video",
  },
  {
    title: "Subscriptions",
    icon: "subscriptions",
  },
  {
    title: "You",
    icon: "video_library",
  },
];

const leftDrawerOpen = ref(false);

function toggleLeftDrawer() {
  leftDrawerOpen.value = !leftDrawerOpen.value;
}
</script>

<style>
.q-icon {
  color: black;
}
.profile {
  color: #2B74BA;
  margin-left: 15px;
}
@media only screen and (max-width: 640px) {
  .profile {
    display: none;
  }
}
</style>
