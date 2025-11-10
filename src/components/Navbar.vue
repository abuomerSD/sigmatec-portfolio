<template>
  <nav class="bg-white shadow-md">
    <div class="flex justify-center mb-2">
      <div class="w-11/12 mx-auto px-4 sm:px-6 lg:px-8">
        <div class="flex justify-between h-16">
          <!-- Logo -->
          <div class="flex-shrink-0 flex items-center">
            <!-- <a href="#" class="text-xl font-bold text-gray-800">MyLogo</a> -->
            <img
              class="w-[80px] cursor-pointerx"
              src="/src/assets/images/sigmatec-logo.png"
              alt="logo"
            />
          </div>

          <!-- Desktop Menu -->
          <div class="hidden md:flex gap-2 md:items-center space-x-6">
            <a href="#about" class="text-gray-700 hover:text-blue-600"
              >حول الشركة</a
            >
            <a href="#" class="text-gray-700 hover:text-blue-600">المنتجات</a>
            <a href="#" class="text-gray-700 hover:text-blue-600"
              >تصنيع اللوحات الكهربائية</a
            >
            <a href="#" class="text-gray-700 hover:text-blue-600"
              >الصيانة الالكترونية</a
            >
            <a href="#" class="text-gray-700 hover:text-blue-600">تواصل معنا</a>
          </div>

          <!-- Mobile Hamburger -->
          <div class="flex items-center md:hidden">
            <button
              @click="isOpen = !isOpen"
              type="button"
              class="text-gray-700 hover:text-blue-600 focus:outline-none"
            >
              <svg
                v-if="!isOpen"
                class="h-6 w-6"
                fill="none"
                stroke="currentColor"
                viewBox="0 0 24 24"
              >
                <path
                  stroke-linecap="round"
                  stroke-linejoin="round"
                  stroke-width="2"
                  d="M4 8h16M4 16h16"
                />
              </svg>
              <svg
                v-else
                class="h-6 w-6"
                fill="none"
                stroke="currentColor"
                viewBox="0 0 24 24"
              >
                <path
                  stroke-linecap="round"
                  stroke-linejoin="round"
                  stroke-width="2"
                  d="M6 18L18 6M6 6l12 12"
                />
              </svg>
            </button>
          </div>
        </div>
      </div>
    </div>

    <!-- Mobile Menu -->
    <div
      v-if="isOpen"
      class="md:hidden bg-white px-2 pt-2 pb-3 space-y-1 shadow-md"
    >
      <a href="#" class="block text-gray-700 hover:text-blue-600">Home</a>
      <a href="#" class="block text-gray-700 hover:text-blue-600">About</a>
      <a href="#" class="block text-gray-700 hover:text-blue-600">Services</a>
      <a href="#" class="block text-gray-700 hover:text-blue-600">Contact</a>
    </div>
  </nav>
</template>

<script>
export default {
  data() {
    return {
      isOpen: false,
    };
  },
};
</script>

<style></style>
