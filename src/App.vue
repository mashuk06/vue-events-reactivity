<template>
  <section class="container mx-auto flex items-center flex-col">
    <h1 class="text-center text-2xl py-10">Assignment</h1>
    <p class="p-5">Make These Buttons Work</p>
    <div class="flex justify-between space-x-6">
      <div class="p-10 border w-96 flex flex-col space-y-5">
        <button @click="toggleLight(1)" :class="{'bg-blue-500 hover:bg-blue-700': lights.light1, 'bg-gray-500 hover:bg-gray-700': !lights.light1, 'text-white font-bold py-2 px-4 rounded': true}">
          Light 1 {{ lights.light1 ? 'On' : 'Off' }}
        </button>
        <button @click="toggleLight(2)" :class="{'bg-blue-500 hover:bg-blue-700': lights.light2, 'bg-gray-500 hover:bg-gray-700': !lights.light2, 'text-white font-bold py-2 px-4 rounded': true}">
          Light 2 {{ lights.light2 ? 'On' : 'Off' }}
        </button>
        <button @click="toggleLight(3)" :class="{'bg-blue-500 hover:bg-blue-700': lights.light3, 'bg-gray-500 hover:bg-gray-700': !lights.light3, 'text-white font-bold py-2 px-4 rounded': true}">
          Light 3 {{ lights.light3 ? 'On' : 'Off' }}
        </button>
      </div>
      <div class="p-10 border w-96 flex flex-col space-y-5">
        <img v-if="lights.light1" class="w-20" src="//img.icons8.com/color/512/12244/light-on--v1.png" alt="Light 1">
        <img v-else class="w-20" src="//img.icons8.com/color/512/12244/light-off.png" alt="Light 1">

        <img v-if="lights.light2" class="w-20" src="//img.icons8.com/color/512/12244/light-on--v1.png" alt="Light 2">
        <img v-else class="w-20" src="//img.icons8.com/color/512/12244/light-off.png" alt="Light 2">

        <img v-if="lights.light3" class="w-20" src="//img.icons8.com/color/512/75/light-on.png" alt="Light 3">
        <img v-else class="w-20" src="//img.icons8.com/color/512/75/light-off.png" alt="Light 3">
      </div>
    </div>
  </section>
</template>

<script>
export default {
  data() {
    return {
      lights: {
        light1: false,
        light2: false,
        light3: true,
      },
    };
  },
  methods: {
    toggleLight(lightNumber) {
      this.lights[`light${lightNumber}`] = !this.lights[`light${lightNumber}`];
    },
  },
};
</script>

<style>
/* Add any custom styles here if needed */
</style>
