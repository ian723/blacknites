<template>
  <div class="container mx-auto p-8">
    <div class="grid grid-cols-1 md:grid-cols-2 gap-8">
      <!-- Drones Section -->
      <div class="relative h-[500px]"> <!-- Set a fixed height -->
        <img
          src="https://images.unsplash.com/photo-1507582020474-9a35b7d455d9?w=600&auto=format&fit=crop&q=60&ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxzZWFyY2h8M3x8ZHJvbmVzfGVufDB8fDB8fHww"
          alt="Drone"
          class="w-full h-full object-cover"
        />
        <div class="absolute inset-0 bg-black bg-opacity-50 flex flex-col justify-center items-center">
          <h2 class="text-white text-3xl font-bold">Drones</h2>
          <p class="text-white text-lg mt-2">
            YUNEEC drones for commercial use
          </p>
          <a href="#" class="mt-4 inline-block px-4 py-2 bg-white text-black rounded hover:bg-gray-300">
            Learn More
          </a>
        </div>
      </div>

      <!-- Payloads Section -->
      <div class="relative h-[500px]"> <!-- Set a fixed height -->
        <img
          src="https://images.unsplash.com/photo-1514861292806-adb0227f827f?w=600&auto=format&fit=crop&q=60&ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxzZWFyY2h8MTh8fGRyb25lc3xlbnwwfHwwfHx8MA%3D%3D"
          alt="Payload"
          class="w-full h-full object-cover"
        />
        <div class="absolute inset-0 bg-black bg-opacity-50 flex flex-col justify-center items-center">
          <h2 class="text-white text-3xl font-bold">Payloads</h2>
          <p class="text-white text-lg mt-2">
            Payload options for commercial use
          </p>
          <a href="#" class="mt-4 inline-block px-4 py-2 bg-white text-black rounded hover:bg-gray-300">
            Learn More
          </a>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "DroneSection",
};
</script>

<style scoped>
/* Add any component-specific styles here */
</style>
