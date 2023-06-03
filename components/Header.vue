<template>
  <header>
    <nav class="bg-white">
      <div class="flex justify-between py-4 border-b-2 px-20">
        <h1>
          <router-link to="/" class="flex cursor-pointer">
            <img
              class="bg-[#0D6EFD] p-2 h-10 rounded-md"
              src="../assets/header/bag.svg"
              alt="img"
            />
            <img src="../assets/header/brand.svg" class="px-3" alt="img" />
          </router-link>
        </h1>
        <form
          @submit.prevent="Search"
          class="flex w-[45%] h-[35px] mx-20 border-2 border-[#0D6EFD] rounded-lg"
        >
          <input
            type="text"
            placeholder="Search"
            class="w-[60%] h-full rounded-l-lg outline-none pl-3 focus:ring-2 ring-[#166ff4]"
          />
          <div class="w-[23%] pr-5 border-x-2 min-w-fit border-[#0D6EFD]">
            <select
              class="h-full mx-1 text-md min-w-fit w-full text-center outline-none"
            >
              <option selected>All category</option>
              <option value="0">Mobile accessory</option>
              <option value="1">Electronics</option>
              <option value="2">Smartphones</option>
              <option value="3">Modern tech</option>
            </select>
          </div>
          <button
            type="submit"
            class="h-full w-[17%] bg-[#0D6EFD] text-white rounded-r-lg focus:ring-2 ring-[#166ff4] hover:bg-[#1464db]"
          >
            Search
          </button>
        </form>
        <ul class="flex gap-10">
          <li>
            <img class="mx-auto" src="../assets/header/user.svg" alt="img" />
            <h1 class="text-xs text-gray-400 font-medium">Profile</h1>
          </li>
          <li>
            <img class="mx-auto" src="../assets/header/message.svg" alt="img" />
            <h1 class="text-xs text-gray-400 font-medium">Message</h1>
          </li>
          <li>
            <img
              class="mx-auto font-"
              src="../assets/header/orders.svg"
              alt="img"
            />
            <h1 class="text-xs text-gray-400 font-medium">Orders</h1>
          </li>
          <li class="min-w-fit">
            <img class="mx-auto" src="../assets/header/cart.svg" alt="img" />
            <h1 class="text-xs text-gray-400 min-w-fit font-medium">My cart</h1>
          </li>
        </ul>
      </div>
      <div class="flex items-center text-md justify-between py-2 px-20 border-b-2">
        <ul class="flex gap-5 items-center">
          <li><i class="bx bx-menu px-1 text-lg"></i>All category</li>
          <li>Hot offers</li>
          <li>Gift boxes</li>
          <li>Projects</li>
          <li>Menu item</li>
          <li>
            <select class="text-md min-w-fit text-center outline-none">
              <option selected>Help</option>
              <option value="0">Call</option>
              <option value="1">Chat</option>
            </select>
          </li>
        </ul>
        <ul class="flex items-center gap-5">
          <li>
            <select class="text-md min-w-fit text-center outline-none">
              <option selected>English, USD</option>
              <option value="0">Uzbek, UZS</option>
              <option value="1">Russian, Rubl</option>
            </select>
          </li>
          <li>
            <select class="text-md min-w-fit text-center outline-none">
              <option selected>
                Ship to <img src="../assets/header/flag.png" alt="img" />
              </option>
              <option value="0">Ship to</option>
              <option value="1">Chat</option>
            </select>
          </li>
        </ul>
      </div>
    </nav>
  </header>
</template>

<script setup></script>

<style lang="scss" scoped>
ul li {
  cursor: pointer;
}
</style>