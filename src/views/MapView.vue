<template>
  <div id="MapView">
    <div id="map"></div>

    <div class="w-full" id="VehicleSelection">
      <div class="w-full h-2 border-t"></div>
      <div class="w-full text-center border-t-2 p-1.5 text-gray-700 text-lg font-semibold">Distance - 50</div>
      <div class="scrollSection">
        
        <div class="bg-custom-gray">
          <div class="flex items-center px-4 py-5">
            <img src="img/uber/ride.png" alt="" width="75">
            <div class="w-full ml-3">
              <div class="flex items-center justify-between">
                <div class="mb-1 text-2xl">UberX</div>
                <div class="text-xl">$59.99</div>
              </div>
              <div class="text-gray-500">7 Hours</div>
            </div>
          </div>
        </div>

        <div>
          <div class="flex items-center px-4 py-5">
            <img src="img/uber/comfort.png" alt="" width="75">
            <div class="w-full ml-3">
              <div class="flex items-center justify-between">
                <div class="mb-1 text-2xl">UberX</div>
                <div class="text-xl">$89.99</div>
              </div>
              <div class="text-gray-500">9 Hours</div>
            </div>
          </div>
        </div>

        <div>
          <div class="flex items-center px-4 py-5">
            <img src="img/uber/uberxl.png" alt="" width="75">
            <div class="w-full ml-3">
              <div class="flex items-center justify-between">
                <div class="mb-1 text-2xl">UberXL</div>
                <div class="text-xl">$119.99</div>
              </div>
              <div class="text-gray-500">11 Hours</div>
            </div>
          </div>
        </div>
        
      </div>

      <div class="flex bg-white items-center justify-center py-6 px-4 w-full absolute bottom-0 shadow-inner">
        <button class="bg-black py-4 px-4 text-white text-2xl rounded-sm w-full">
          Confirm UberX
        </button>
      </div>
    </div>
  </div>
</template>

<script setup>
import { onMounted } from "vue"

onMounted(() => {
  setTimeout(() => {
    initMap()
  }, 50)
})

const initMap = () => {
  const map = new window.google.maps.Map(document.getElementById("map"), {
    center: { lat: -34.397, lng: 150.644 },
    zoom: 8,
    fullscreenControl: false,
    zoomControl: false,
    streetViewControl: false,
    mapTypeControl: false
  });
  console.log(map)
}

</script>

<style lang="scss">
#MapView {

  #map {
    width: 100%;
    height: 45vh;
    top: 0;
    left: 0;
  }

  .gm-style-cc {
    display: none;
  }
  .bg-custom-gray {
    background-color: rgb(237, 237, 237);
  }

  #VehicleSelection {
    .scrollSection {
      height: calc(50vh - 120px);
      position: absolute;
      overflow-y: auto;
      width: 100%;
    }
  }
}
</style>