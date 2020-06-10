<template>
<div class="w-full shadow-md border-b-2 border-blue-200">
    <nav class=" mx-32 py-12 rounded-lg">
    <div class="container flex justify-between">
        <h1 class="font-semibold text-3xl text-blue-400">
          Twitter Clone
        </h1>
        <ul class="flex font-medium items-center text-gray-600">
          <li><a href="#" class="pr-12 text-blue-300">Home</a> </li>
          <li><a href="#" class="pr-12 hover:text-blue-300">Moment</a></li>
          <li><a href="#" class="pr-12 hover:text-blue-300">Notification</a></li>
          <li><a href="#" class="pr-12 hover:text-blue-300">Message</a></li>
        </ul>
    </div>
    </nav>
</div>
   
</template>

<script>
export default {
    name:'Nav',
    data() {
      return {
        isActive:false,
      }
    },
}
</script>

<style>

</style>