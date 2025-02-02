<template>
  <div class="flex flex-col items-center justify-start min-500-screen bg-gray-100 p-6">
    <!-- ข้อความ Welcome -->
    <div class="text-center flex flex-row">
      <p class="text-6xl sm:text-7xl font-bold text-gray-900">Welcome to -</p>
      <p class="text-6xl sm:text-7xl font-bold bg-clip-text text-transparent bg-gradient-to-r from-yellow-500 to-orange-500">
        BOT CMRU
      </p>
    </div>

    <!-- คำอธิบาย -->
    <p class="text-2xl sm:text-4xl text-gray-700 mt-4">
      Scan the QR code to start using the chatbot.
    </p>

    <!-- ส่วนของ QR Code -->
    <div class="flex flex-wrap justify-center items-center gap-6 mt-6">
      <div class="flex flex-col items-center gap-10">
      <img 
        src="@/assets/img/qr1.jpg" 
        alt="QR Code 1"
        class="w-40 sm:w-52 rounded-lg shadow-lg transition-transform duration-300 hover:scale-105"
      >
      <p class="text-6xl sm:text-4xl font-bold bg-clip-text text-transparent bg-gradient-to-r from-green-500 to-yellow-500">Scan </p>
      <p class="text-6xl sm:text-4xl font-bold bg-clip-text text-transparent bg-gradient-to-r from-green-500 to-yellow-500">QR Code</p>
    </div>
      <img 
        src="@/assets/img/F1.jpg" 
        alt="QR Code 2"
        class="w-[180px] sm:w-52 rounded-lg shadow-lg transition-transform duration-300 hover:scale-105"
      >
    </div>
  </div>
</template>


        
<script setup>

        definePageMeta({
          layout: 'default'
        })
 </script>
        