<template>
  <div class=" mx-auto md:m-12">
    <div class="mb-4 text-center lg:text-left">
         <div class="w-14 h-14 mb-1 mx-auto lg:hidden inline-flex">
            <span
              class="m-1 mt-3 mr-2 w-10 h-10 flex justify-center items-center rounded-full bg-green-500 text-base text-white uppercase"
              >{{ displayInitials }}</span
            >
        </div>
      <p class="text-gray-800 text-2xl mt-2 font-medium">{{ user && user.name }}</p>
      <p class="mx-8 md:mx-0">
        <span class="text-gray-800 text-base lg:text-lg mt-2 font-medium"
          >{{ user && user.email }} </span
        >. Shipping since
        <span class="text-gray-800 text-base lg:text-lg font-medium">{{ user && new Date(user.date).toLocaleString('default', {month:'long'}) }} {{ user && new Date(user.date).getFullYear() }} </span>
      </p>
    </div>
    <div class="grid grid-cols-1 md:grid-cols-2 xl:grid-cols-3 gap-4 m-8 md:m-0">
      <Card>
        <template v-slot:image>
          <div class="tail-text-base tail-font-medium tail-text-left">
            <img src="~/assets/svg/Profile.svg" alt="" />
          </div>
        </template>
        <template v-slot:heading>
          <div class="text-gray-800 text-lg mt-2 font-medium">
            Personal Information
          </div>
        </template>
        <template v-slot:text>
          <div class="tail-text-base tail-font-medium tail-text-left">
            Edit your name, phone number and other personal info.
          </div>
        </template>
      </Card>
      <Card>
        <template v-slot:image>
          <div class="tail-text-base tail-font-medium tail-text-left">
            <img src="~/assets/svg/Lock.svg" alt="" />
          </div>
        </template>
        <template v-slot:heading>
          <div class="text-gray-800 text-lg mt-2 font-medium">
            Login &amp; Security
          </div>
        </template>
        <template v-slot:text>
          <div class="tail-text-base tail-font-medium tail-text-left">
            Update your password. Keep your account safe.
          </div>
        </template>
      </Card>
      <Card>
        <template v-slot:image>
          <div class="tail-text-base tail-font-medium tail-text-left">
            <img src="~/assets/svg/booklet-fill.svg" alt="" />
          </div>
        </template>
        <template v-slot:heading>
          <div class="text-gray-800 text-lg mt-2 font-medium">
            Address Book
          </div>
        </template>
        <template v-slot:text>
          <div class="tail-text-base tail-font-medium tail-text-left">
            Edit, delete and add new addresses.
          </div>
        </template>
      </Card>
      <Card>
        <template v-slot:image>
          <div class="tail-text-base tail-font-medium tail-text-left">
            <img src="~/assets/svg/help.svg" alt="" />
          </div>
        </template>
        <template v-slot:heading>
          <div class="text-gray-800 text-lg mt-2 font-medium">
            General Preferences
          </div>
        </template>
        <template v-slot:text>
          <div class="tail-text-base tail-font-medium tail-text-left">
            Set your notifications and other preferences.
          </div>
        </template>
      </Card>
      <Card>
        <template v-slot:image>
          <div class="tail-text-base tail-font-medium tail-text-left">
            <img src="~/assets/svg/booklet-fill copy.svg" alt="" />
          </div>
        </template>
        <template v-slot:heading>
          <div class="text-gray-800 text-lg mt-2 font-medium">
            Help &amp; Support
          </div>
        </template>
        <template v-slot:text>
          <div class="tail-text-base tail-font-medium tail-text-left">
            Visit our help center. We are always happy to help.
          </div>
        </template>
      </Card>
    </div>
  </div>
</template>

<script>
export default {
   props: {
    user: {
      type: Object,
      required: true,
    },
  },
    computed: {
    displayInitials() {
    if( this.user && this.user.name ){
      const fullName = this.user.name.split(' ');
      const initials = fullName.shift().charAt(0) + fullName.pop().charAt(0);
      return initials.toUpperCase();
    }
    }
  }
};
</script>

<style></style>
