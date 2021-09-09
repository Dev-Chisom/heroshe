<template>
  <header
    class="bg-black sticky top-0 text-white px-8 flex items-center capitalize"
  >
    <div class="mr-auto flex items-center space-x-5 py-3.5">
       <button
        type="button"
        class="group lg:hidden inline-flex items-center justify-center text-sm font-medium hover:text-gray-900"
        aria-expanded="false"
        aria-label="toggle sidebar"
         @click="$emit('showMobile')"
      >
         <img src="~/assets/svg/burger.svg" alt="">
      </button>
      <svg
      class="hidden lg:block"
        width="25"
        height="24"
        viewBox="0 0 25 24"
        fill="none"
        xmlns="http://www.w3.org/2000/svg"
      >
        <path
          d="M15.6746 23.0033C12.8847 23.0033 10.9991 19.9633 12.3652 17.4812C13.3657 15.6341 14.5587 13.9025 15.7131 12.1516C16.021 11.6706 16.0017 11.3435 15.6939 10.8817C14.6549 9.3232 13.6543 7.72622 12.6538 6.14849C11.2108 3.87809 11.9804 1.22288 14.4432 0.260848C16.0209 -0.354853 17.8103 0.126164 18.7916 1.62693C20.4463 4.14746 22.0625 6.72571 23.6787 9.26547C24.0635 9.88118 24.4484 10.4969 24.8524 11.1126C25.0256 11.3819 25.0641 11.6128 24.8716 11.9014C22.8514 15.0569 20.8504 18.2316 18.8108 21.3871C18.0605 22.503 16.983 23.0418 15.6746 23.0033Z"
          fill="#F1C34E"
        />
        <path
          d="M3.76451 23.253C0.974618 23.253 -0.910957 20.213 0.455129 17.7309C1.45564 15.8838 2.64856 14.1522 3.803 12.4013C4.11085 11.9203 4.09161 11.5932 3.78376 11.1314C2.74476 9.57289 1.74425 7.97592 0.743739 6.39818C-0.69931 4.12779 0.070314 1.47258 2.53312 0.510543C4.11085 -0.105158 5.90023 0.375858 6.8815 1.87663C8.5362 4.39716 10.1524 6.9754 11.7686 9.51517C12.1534 10.1309 12.5383 10.7466 12.9423 11.3623C13.1155 11.6316 13.154 11.8625 12.9616 12.1511C10.9413 15.3066 8.94025 18.4813 6.8815 21.6368C6.1696 22.7335 5.09212 23.2722 3.76451 23.253Z"
          fill="#F1C34E"
        />
      </svg>
      <span>settings</span>
      <div class="mt-1 relative rounded">
        <input
          type="text"
          name="search"
          class="focus:ring-indigo-500 focus:border-indigo-500  hidden lg:block pr-10 sm:text-sm border-gray-300 rounded h-9 w-44 px-3 capitalize placeholder-gray-400 font-extrabold"
          placeholder="search"
        />
        <div
          class="absolute inset-y-0 right-0 pr-3 hidden lg:flex items-center pointer-events-none"
        >
          <svg
            width="20"
            height="20"
            viewBox="0 0 20 20"
            fill="none"
            xmlns="http://www.w3.org/2000/svg"
          >
            <circle cx="9.56322" cy="9.56322" r="9.56322" fill="#F1C34E" />
            <path
              fill-rule="evenodd"
              clip-rule="evenodd"
              d="M7.96514 14.3924C7.70522 14.1325 7.70522 13.7111 7.96514 13.4512L11.1343 10.2821L7.96514 7.11292C7.70522 6.853 7.70522 6.43159 7.96514 6.17168C8.22506 5.91176 8.64646 5.91176 8.90638 6.17168L12.5461 9.81144C12.8061 10.0714 12.8061 10.4928 12.5461 10.7527L8.90638 14.3924C8.64646 14.6524 8.22506 14.6524 7.96514 14.3924Z"
              fill="black"
            />
          </svg>
        </div>
      </div>
    </div>
    <div class="flex space-x-5">
      <button
        type="button"
        class="group lg:inline-flex items-center justify-center text-sm font-medium hover:text-gray-900 hidden"
        aria-expanded="false"
        aria-label="what's new"
      >
        <span class="mr-2">What's new?</span>
        <span
          class="ml-1.5 rounded-full py-0.5 px-1.5 bg-red-500 text-xs font-semibold tabular-nums"
          >2</span
        >
      </button>
      <button
        type="button"
        class="group lg:inline-flex items-center justify-center text-sm font-medium hover:text-gray-900 hidden "
        aria-expanded="false"
        aria-label="resources"
      >
        <span class="mr-2">Resources</span>
        <span
          class="ml-1.5 rounded-full py-0.5 bg-white px-2 text-black text-xs font-semibold tabular-nums"
          >i</span
        >
      </button>

      <button
        type="button"
        class="group lg:inline-flex items-center justify-center text-sm font-medium hover:text-gray-900 hidden"
        aria-expanded="false"
        aria-label="currency"
      >
        <span class="truncate text-sm font-normal mr-1.5">Currency</span>
        <div
          class="flex items-center py-0.5 px-1.5 bg-white text-xs text-black ml-0.5 h-8 w-20"
        >
          <img src="~/assets/svg/flag.svg" alt="" />
          <span>USD</span>
          <img src="~/assets/svg/logo.svg" alt="" class="ml-2" />
        </div>
      </button>
      <button
        type="button"
        class="group inline-flex items-center justify-center text-sm font-medium hover:text-gray-900"
        aria-expanded="false"
        aria-label="cart"
      >
        <span class="mr-2 hidden lg:inline-flex">Cart</span>
        <span class="relative">
          <svg
            width="24"
            height="24"
            viewBox="0 0 24 24"
            fill="none"
            xmlns="http://www.w3.org/2000/svg"
          >
            <path
              d="M10.4935 20.5C11.4584 20.5 12.2406 19.7165 12.2406 18.75C12.2406 17.7835 11.4584 17 10.4935 17C9.52856 17 8.74634 17.7835 8.74634 18.75C8.74634 19.7165 9.52856 20.5 10.4935 20.5Z"
              fill="white"
            />
            <path
              d="M17.4818 20.5C18.4467 20.5 19.2289 19.7165 19.2289 18.75C19.2289 17.7835 18.4467 17 17.4818 17C16.5168 17 15.7346 17.7835 15.7346 18.75C15.7346 19.7165 16.5168 20.5 17.4818 20.5Z"
              fill="white"
            />
            <path
              d="M21.4232 5.54334C21.3126 5.41034 21.1483 5.33334 20.976 5.33334H7.28765L6.78098 3.43284C6.71342 3.17733 6.4828 3 6.2184 3H3.5045C3.18303 3 2.92212 3.26133 2.92212 3.58334C2.92212 3.90534 3.18303 4.16667 3.5045 4.16667H5.77113L8.76574 15.4006C8.83329 15.6561 9.06392 15.8334 9.32832 15.8334H18.6464C18.9679 15.8334 19.2288 15.5721 19.2288 15.2501C19.2288 14.9281 18.9679 14.6667 18.6464 14.6667H9.77559L9.44829 13.4394L19.8403 12.9155C20.1094 12.9015 20.3353 12.7044 20.3843 12.4384L21.549 6.02168C21.5805 5.85018 21.5339 5.67518 21.4232 5.54334ZM16.3169 10H12.8226C12.5011 10 12.2402 9.73869 12.2402 9.41669C12.2402 9.09469 12.5011 8.83336 12.8226 8.83336H16.3169C16.6384 8.83336 16.8993 9.09469 16.8993 9.41669C16.8993 9.73869 16.6384 10 16.3169 10Z"
              fill="white"
            />
          </svg>
          <span
            class="absolute -top-1.5 -right-2 rounded-full py-0 bg-red-400 px-1 text-black text-xs font-semibold tabular-nums"
            >3</span
          >
        </span>
      </button>
      <button
        type="button"
        class="flex items-center justify-center text-sm font-medium rounded-md focus:outline-none focus:ring-2 focus:ring-offset-2 focus:ring-blue-600"
        id="menu-0-button"
        aria-expanded="false"
        aria-haspopup="true"
        aria-label="initials"
      >
        <div class="w-12 h-12 relative mb-4">
            <span
              class="m-1 mt-3 mr-2 w-8 h-8 relative flex justify-center items-center rounded-full bg-green-500 text-base text-white uppercase"
              >{{ displayInitials }}</span
            >
        </div>
        <span class="mx-2 hidden lg:block">{{ user && user.name }}</span>
        <svg
          width="18"
          height="18"
          viewBox="0 0 18 18"
          fill="none"
          xmlns="http://www.w3.org/2000/svg"
        >
          <path
            d="M5.75189 7.22122L9.35424 10.8321L12.9566 7.22122H5.75189Z"
            fill="white"
          />
        </svg>
      </button>
    </div>
  </header>
</template>

<script>
export default {
  props: {
    user: {
      type: Object,
      required: true
    }
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
