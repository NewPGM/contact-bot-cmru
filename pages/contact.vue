<script setup>
import { Mail, Facebook, User } from 'lucide-vue-next' // ใช้ Lucide Icons
</script>

<template>
  <div class="flex justify-center items-center min-h-[620px] bg-gray-100 p-6">
    <div class="bg-white shadow-lg rounded-lg p-8 max-w-md w-full text-center">
      <!-- หัวข้อ -->
      <h1 class="text-4xl font-bold text-gray-800 mb-6">CONTACT</h1>

      <!-- ข้อมูลนักศึกษา -->
      <div class="flex flex-col items-center gap-2">
        <User class="w-12 h-12 text-gray-700" />
        <p class="text-2xl font-semibold text-gray-700">นายจีระศักดิ์ ต๋าใจ</p>
        <p class="text-gray-600">รหัสนักศึกษา 64143109</p>
      </div>

      <!-- Facebook -->
      <div class="mt-6">
        <a 
          href="https://www.facebook.com/profile.php?id=100063983498112" 
          target="_blank" 
          class="flex items-center justify-center gap-2 text-blue-600 font-medium hover:scale-105 transition-transform"
        >
          <Facebook class="w-8 h-8" />
          <p class="text-2xl">Facebook</p>
        </a>
      </div>

      <!-- Email -->
      <div class="mt-4">
        <a 
          href="mailto:64143109@g.cmru.ac.th" 
          class="flex items-center justify-center gap-2 text-red-700 font-medium hover:scale-105 transition-transform"
        >
          <Mail class="w-8 h-8" />
          <p class="text-2xl">Email: 64143109@g.cmru.ac.th</p>
        </a>
      </div>

      <!-- สาขาวิชา -->
      <p class="mt-6 text-gray-700 font-semibold">สาขาวิทยาการคอมพิวเตอร์</p>
      
    </div>
  </div>
</template>
