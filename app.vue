<template>
  <div :class="{ dark: darkMode }">
    <div class="bg-white dark:bg-dim-900">
      <div class="min-h-full">
        <div
          class="grid grid-cols-12 mx-auto sm:px-6 lg:max-w-7xl lg:px-8 lg:gap-5"
        >
          <!-- Left sidebar -->
          <div
            class="hidden md:block lg:block xs:col-span-1 lg:col-span-2"
          >
            <div class="sticky top-0">
              <SideBarLeft />
            </div>
          </div>

          <!-- main content -->
          <!-- <main class="col-span-12 md:col-span-8 xl:col-span-6 bg-red-400">
            <h1>ass</h1>
          </main> -->

          <!-- right sidebar -->
          <div
            class="hidden col-span-12 bg-blue-400 md:block md:col-span-3 xl:col-span-4"
          >
            <div class="sticky top-0">
              <SideBarRight/>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script setup>
const darkMode = ref(false);
</script>
