<template>
  <header class="shadow w-screen">
    <nav>
      <nav
        class="flex items-center justify-between flex-wrap bg-purple-700 p-6"
      >
        <div class="flex items-center flex-shrink-0 text-white mr-6">
          <px-icon class="mr-4" />
          <router-link
            :to="{ name: 'home' }"
            class="font-semibold text-3xl tracking-tight"
            >Bitcoin Exchange</router-link
          >
        </div>
        <div
          class="hidden sm:block w-full block flex-grow lg:flex lg:items-center lg:w-auto"
        >
          <div class="w-full text-sm md:text-center lg:text-right lg:flex-grow">
            <router-link
              v-for="l in links"
              :key="l.title"
              :to="l.to"
              class="block mt-4 lg:inline-block lg:mt-0 text-gray-100 font-bold hover:text-white md:py-4 mx-10"
              >{{ l.title }}</router-link
            >
            <router-link
              class="block mt-4 lg:inline-block lg:mt-0 text-gray-100 font-bold hover:text-white md:py-4 mx-10"
              :to="{ name: 'about' }"
              >About</router-link
            >
          </div>
        </div>
      </nav>
    </nav>
  </header>
</template>

<script>
import PxIcon from "@/components/PxIcon";

export default {
  name: "PxHeader",
  components: { PxIcon },

  props: {
    links: {
      type: Array,
      default: () => []
    }
  }
};
</script>
