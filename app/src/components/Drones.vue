<template>
  <section class="py-12 bg-white">
    <div class="container mx-auto">
      <h1 class="text-4xl font-bold text-center mb-8">Drone Details</h1>

      <!-- Filter Drones by Type -->
      <div class="mb-8">
        <label for="drone-type" class="block mb-2 text-lg font-medium"
          >Filter by Drone Type:</label
        >
        <select
          v-model="selectedType"
          @change="filterDrones"
          class="p-2 border border-gray-300 rounded"
        >
          <option value="">All Types</option>
          <option value="Photography">Photography</option>
          <option value="Industrial">Industrial</option>
          <option value="Surveying">Surveying</option>
          <option value="Racing">Racing</option>
          <option value="Agriculture">Agriculture</option>
        </select>
      </div>

      <!-- Show filtered drone details -->
      <div
        v-if="filteredDrones.length > 0"
        class="grid grid-cols-1 md:grid-cols-2 gap-8"
      >
        <div
          v-for="drone in filteredDrones"
          :key="drone.id"
          class="bg-gray-100 p-6 rounded-lg shadow-lg"
        >
          <img
            :src="drone.image"
            alt="drone"
            class="w-full h-64 object-cover mb-4"
          />
          <h2 class="text-3xl font-bold mb-4">{{ drone.name }}</h2>
          <p class="text-lg text-gray-600 mb-6">{{ drone.description }}</p>
          <router-link to="/" class="text-blue-500 hover:underline"
            >Back to Home</router-link
          >
        </div>
      </div>

      <!-- Message if no drone found -->
      <div v-else>
        <p class="text-center text-red-500">
          No drones found for the selected type.
        </p>
        <router-link to="/" class="text-blue-500 hover:underline"
          >Back to Home</router-link
        >
      </div>
    </div>
  </section>
</template>

<script>
export default {
  name: "DronePage",
  data() {
    return {
      selectedType: "",
      drones: [
        {
          id: 1,
          name: "Phantom Pro 4",
          type: "Photography",
          description: "A top-tier drone offering 4K camera capabilities for professional-grade photography.",
          image: "https://blogs.icrc.org/law-and-policy/wp-content/uploads/sites/102/2022/03/Drone-image-1096x620.jpg",
        },
        {
          id: 2,
          name: "Matrice 600",
          type: "Industrial",
          description: "Powerful industrial drone for heavy-duty operations, equipped with a variety of payload options.",
          image: "https://cdn.thewirecutter.com/wp-content/media/2023/08/drones-2048px-0718.jpg",
        },
        {
          id: 3,
          name: "Inspire 2",
          type: "Photography",
          description: "Designed for filmmakers, the Inspire 2 offers incredible camera stabilization and 6K video.",
          image: "https://mundogeo.com/wp-content/uploads/2024/03/18143629/drone-DJI-Mavic-3-Multispectral-revolucion%C3%A1rio-para-agricultura-e-mapeamento-756x400.jpg",
        },
        {
          id: 4,
          name: "DJI Agras T30",
          type: "Agriculture",
          description: "Specialized drone for agriculture, perfect for spraying crops with precision.",
          image: "https://www.zettafarms.com/wp-content/uploads/2024/01/2952.jpg",
        },
        {
          id: 5,
          name: "Parrot Anafi USA",
          type: "Surveying",
          description: "Ideal for mapping and surveying with detailed 32x zoom and thermal imaging capabilities.",
          image: "https://pilotinstitute.com/wp-content/uploads/2021/12/Anafi-USA-Course-Cover.jpg",
        },
        {
          id: 6,
          name: "Walkera F210",
          type: "Racing",
          description: "A racing drone known for its agility, capable of reaching high speeds in competition.",
          image: "https://futurdrone.com/magaz/wp-content/uploads/2010/04/Walkera-F210-r006.jpg",
        },
        {
          id: 7,
          name: "DJI Mavic Air 2",
          type: "Photography",
          description: "Compact yet powerful drone, perfect for travelers and hobbyist photographers.",
          image: "https://patkay.com/cdn/shop/articles/dji-mavic-air-2-review-Pat-Kay-Blog-09015.jpg?v=1608345520",
        },
        {
          id: 8,
          name: "Autel Robotics EVO II",
          type: "Surveying",
          description: "Long-range surveying drone with 8K video resolution, excellent for aerial mapping.",
          image: "https://i.pcmag.com/imagery/reviews/00x599xV1C4y6W9mmaZcYNC-1.fit_scale.size_760x427.v1618610194.jpg",
        },
      ],
      filteredDrones: [],
    };
  },
  created() {
    this.filterDrones();
  },
  methods: {
    filterDrones() {
      if (this.selectedType === "") {
        this.filteredDrones = this.drones;
      } else {
        this.filteredDrones = this.drones.filter(
          (drone) => drone.type === this.selectedType
        );
      }
    },
  },
};
</script>

<style scoped>
/* Add any additional styling here */
</style>
