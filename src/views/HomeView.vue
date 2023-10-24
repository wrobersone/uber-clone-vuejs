<template>
  <div id="Home" class="flex flex-col h-screen">
    <div class="m-3 mb-auto">
      <div class="my-20"><img width="150" src="img/uber/uber2.svg" alt=""></div>
      <div class="grid grid-cols-2 gap-3 my-3">
        <ServiceSelectLarge 
          text="Ride"
          image="ride"
          imageWidth="74"
          :promo="true"
        />
        <ServiceSelectLarge 
          text="Food"
          image="food"
          imageWidth="72"
        />
      </div>

      <div class="grid grid-cols-4 gap-3 my-3">
        <ServiceSelectSmall 
          text="2 Wheels"
          image="2wheels"
        />
        <ServiceSelectSmall 
          text="Transit"
          image="transit"
        />
        <ServiceSelectSmall 
          text="Reserve"
          image="reserve"
        />
        <ServiceSelectSmall 
          text="Travel"
          image="travel"
        />
      </div>

      <div class="flex w-full bg-custom-color h-14 items-center p-3 rounded-full">
        <MagnifyIcon size="40" />
        <div class="ml-3 text-xs font-semibold text-gray-700">Enter Pick-Up</div>
      </div>
    </div>

    <footer class="flex justify-around w-full z-50 p-1 mb-2 border-t-2 border-t-gray-200">
      <div class="grid place-items-center">
        <HomeIcon :size="30" fillColor="#1F1E1E" />
        <div class="w-full -mt-1 text-xs text-center text-gray-800 font-semibold">
          Home
        </div>
      </div>
      <div class="grid place-items-center">
        <MapMarkerIcon :size="30" fillColor="#B3B1B1" />
        <div class="w-full -mt-1 text-xs text-center text-gray-400 font-semibold">
          Destination
        </div>
      </div>
    </footer>

  </div>
</template>

<script setup>
import ServiceSelectLarge from "../components/ServiceSelectLarge.vue"
import ServiceSelectSmall from "@/components/ServiceSelectSmall.vue";
import MagnifyIcon from "vue-material-design-icons/Magnify.vue"
import HomeIcon from "vue-material-design-icons/Home.vue"
import MapMarkerIcon from "vue-material-design-icons/MapMarker.vue"
</script>

<style lang="scss" scoped>
#Home {
  .bg-custom-color {
    background-color: rgb(237, 237, 237);
  }

}
</style>