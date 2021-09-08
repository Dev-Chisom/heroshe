<template>
  <div class="max-w-sm py-4 px-8 bg-white shadow-lg rounded-lg my-4 h-52 md:w-72 w-full xl:w-72 transform transition duration-500 hover:scale-110">
  <div>
       <slot name="image">
      </slot>
    <slot name="heading">
      </slot>
    <p class="mt-2 text-gray-600">
    <slot name="text">
      </slot>
   </p>
  </div>
</div>
</template>

<script>
export default {

}
</script>

<style>

</style>