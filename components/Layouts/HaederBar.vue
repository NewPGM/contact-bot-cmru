<!-- components/HeaderBar.vue -->
<template>
  <header class="bg-white">
    <nav class="container mx-auto px-6 py-4">
      <div class="flex items-center justify-between">
        <!-- Logo -->
        <div class="flex items-center gap-3">
  <!-- โลโก้ -->
  <img 
    src="@/assets/img/iconcmru.png" 
    class="w-20 h-20 rounded-lg shadow-md transition-transform duration-300 hover:scale-105"
    alt="CMRU Logo"
  >
  
  <!-- ข้อความ -->
  <NuxtLink 
    to="/" 
    class="text-3xl font-extrabold text-gray-900 hover:text-transparent bg-clip-text bg-gradient-to-r from-blue-500 to-purple-600 transition-all duration-300"
  >
    BOT CMRU
  </NuxtLink>
</div>


        <!-- Desktop Menu -->
        <div class="hidden md:flex items-center space-x-12">
          <NuxtLink 
            v-for="(item, index) in menuItems" 
            :key="index"
            :to="item.path"
            class="relative text-gray-600 hover:text-blue-600 transition-colors duration-300 py-2 after:content-[''] after:absolute after:bottom-0 after:left-0 after:w-0 after:h-0.5 after:bg-blue-600 after:transition-all after:duration-300 hover:after:w-full"
          >
            {{ item.label }}
          </NuxtLink>
        </div>

        <!-- Mobile Menu Button -->
        <div class="md:hidden">
          <button
            @click="isOpen = !isOpen"
            class="p-2 rounded-lg hover:bg-gray-100 transition-colors duration-300 focus:outline-none"
            aria-label="Toggle menu"
          >
            <Icon 
              :name="isOpen ? 'heroicons:x-mark' : 'heroicons:bars-3'" 
              class="h-6 w-6 text-gray-600"
            />
          </button>
        </div>
      </div>

      <!-- Mobile Menu -->
      <transition
        enter-active-class="transition duration-200 ease-out"
        enter-from-class="transform -translate-y-2 opacity-0"
        enter-to-class="transform translate-y-0 opacity-100"
        leave-active-class="transition duration-200 ease-in"
        leave-from-class="transform translate-y-0 opacity-100"
        leave-to-class="transform -translate-y-2 opacity-0"
      >
        <div v-if="isOpen" class="md:hidden mt-4 pb-4">
          <div class="flex flex-col space-y-4">
            <NuxtLink
              v-for="(item, index) in menuItems"
              :key="index"
              :to="item.path"
              class="px-4 py-2 text-gray-600 hover:text-blue-600 hover:bg-blue-50 rounded-lg transition-colors duration-300"
              @click="isOpen = false"
            >
              {{ item.label }}
            </NuxtLink>
          </div>
        </div>
      </transition>
    </nav>
  </header>
</template>

<script setup>
const isOpen = ref(false)

const menuItems = [
  { path: '/', label: 'HOME' },
  { path: '/abstract', label: 'ABSTRACT' },
  { path: '/contact', label: 'CONTACT' }
]
</script>

<style scoped>
/* Add any component-specific styles here if needed */
</style>