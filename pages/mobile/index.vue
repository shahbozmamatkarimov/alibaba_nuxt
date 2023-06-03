<template>
  <main>
    <!------------- page path ------------->
    <section>
      <div class="flex gap-1 text-gray-500 items-center -mt-4 mb-2">
        <p>Home</p>
        <i class="bx bx-chevron-right"></i>
        <p>Clothings</p>
        <i class="bx bx-chevron-right"></i>
        <p>Men's wear</p>
        <i class="bx bx-chevron-right"></i>
        <p>Summer clothing</p>
      </div>
    </section>
  </main>

  <!------------- aside ------------->
  <div class="flex">
    <aside class="w-52 mr-5">
      <!------------- Category ------------->
      <div>
        <h1 class="flex justify-between pb-2 font-bold">
          Category<i
            class="bx bx-chevron-down text-gray-500 font-extrabold hidden"
          ></i
          ><i class="bx bx-chevron-up text-gray-500 font-extrabold"></i>
        </h1>
        <div>
          <ul class="leading-8 text-gray-500">
            <li>Mobile accessory</li>
            <li>Electronics</li>
            <li>Smartphones</li>
            <li>Modern tech</li>
            <li class="text-blue-500">See all</li>
          </ul>
        </div>
      </div>
      <hr />
      <!------------- Brands ------------->
      <div>
        <h1>
          Brands<i class="bx bx-chevron-down"></i
          ><i class="bx bx-chevron-up"></i>
        </h1>
        <div>
          <ul class="leading-8">
            <li><input type="checkbox" />Samsung</li>
            <li><input type="checkbox" />Apple</li>
            <li><input type="checkbox" />Huawei</li>
            <li><input type="checkbox" />Pocco</li>
            <li><input type="checkbox" />Lenovo</li>
            <li>See all</li>
          </ul>
        </div>
      </div>
      <hr />
      <!------------- Features ------------->
      <div>
        <h1>
          Features
          <i class="bx bx-chevron-down"></i>
          <i class="bx bx-chevron-up"></i>
        </h1>
        <div>
          <ul class="leading-8">
            <li><input type="checkbox" />Metallic</li>
            <li><input type="checkbox" />Plastic cover</li>
            <li><input type="checkbox" />8GB Ram</li>
            <li><input type="checkbox" />Super power</li>
            <li><input type="checkbox" />Large Memory</li>
            <li>See all</li>
          </ul>
        </div>
      </div>
    </aside>

    <main class="w-full">
      <!------------- navbar ------------->
      <nav
        class="flex justify-between items-center w-full pr-2 pl-5 bg-white py-2 border-2 rounded-md"
      >
        <h1>12,911 items in Mobile accessory</h1>
        <div class="flex items-center gap-4">
          <div class="flex gap-2">
            <input type="checkbox" id="verify" />
            <label for="verify">Verified only</label>
          </div>
          <select
            class="outline-none w-40 border-2 py-1 px-2 rounded-lg"
            name="filter"
            id="filter"
          >
            <option selected>Featured</option>
            <option value="1">New</option>
            <option value="2">Old</option>
          </select>
          <p>
            <i
              class="p-1 text-[20px] rounded-l-md bg-gray-300 border-2 bx bxs-dashboard"
            ></i>
            <i
              class="p-1 text-[20px] rounded-r-md border-l-0 font-bold border-2 bx bx-menu"
            ></i>
          </p>
        </div>
      </nav>

      <!------------- filter ------------->
      <section>
        <div>
          <ul class="flex gap-2 my-4 text-gray-700">
            <li class="pb-1 px-2 border-2 border-blue-400 rounded-md">
              Samsung
              <i class="bx bx-x pl-3 text-lg font-bold text-gray-500"></i>
            </li>
            <li class="pb-1 px-2 border-2 border-blue-400 rounded-md">
              Apple <i class="bx bx-x pl-3 text-lg font-bold text-gray-500"></i>
            </li>
            <li class="pb-1 px-2 border-2 border-blue-400 rounded-md">
              Poco <i class="bx bx-x pl-3 text-lg font-bold text-gray-500"></i>
            </li>
            <li class="pb-1 px-2 border-2 border-blue-400 rounded-md">
              Metallic
              <i class="bx bx-x pl-3 text-lg font-bold text-gray-500"></i>
            </li>
            <li class="pb-1 px-2 border-2 border-blue-400 rounded-md">
              4 star
              <i class="bx bx-x pl-3 text-lg font-bold text-gray-500"></i>
            </li>
            <li class="pb-1 px-2 border-2 border-blue-400 rounded-md">
              3 star
              <i class="bx bx-x pl-3 text-lg font-bold text-gray-500"></i>
            </li>
            <li class="pb-1 px-2 text-blue-500 cursor-pointer">
              Clear all filter
            </li>
          </ul>
        </div>
      </section>

      <!------------- product section ------------->
      <section>
        <div class="flex justify-between flex-wrap">
          <div
            class="text-md px-3 pb-7 w-1/4 -mx-3"
            v-for="i in store.products.data"
            :key="i"
          >
            <div class="p-5 bg-white border-2 rounded-md">
              <div class="flex justify-center">
                <img class="w-44 h-64 mb-5" :src="i.image" alt="img" />
              </div>
              <hr class="w-[117%] -mx-5" />
              <div class="leading-7 py-2">
                <div class="flex justify-between items-center">
                  <div>
                    <div class="flex justify-between items-center">
                      <h1 class="font-bold">${{ i.price }}</h1>
                      <p
                        class="line-through font-bold text-xs pt-1 text-gray-500"
                      >
                        $1128.00
                      </p>
                    </div>
                    <div class="flex">
                      <img
                        src="../../assets/header/star.svg"
                        alt="star"
                        v-for="(i, index) in Math.floor(i.rating.rate)"
                        :key="index"
                      />
                      <img
                        src="../../assets/header/star1.svg"
                        alt="star"
                        v-for="(i, index) in 5 - Math.floor(i.rating.rate)"
                        :key="index"
                      />
                      <i class="px-2 text-[#FF9017]">{{ i.rating.rate }}</i>
                    </div>
                  </div>
                  <div
                    class="flex items-center justify-center text-blue-600 border-2 h-10 w-10 text-2xl rounded-lg cursor-pointer"
                  >
                    <i class="bx bx-heart"></i>
                    <i class="bx bxs-heart hidden"></i>
                  </div>
                </div>
              </div>
              <p class="text-gray-500 w-full truncate">
                {{ i.title }}
              </p>
              <p class="text-gray-500">{{ i.category }}</p>
            </div>
          </div>
        </div>
      </section>
      <!------------- pagination section ------------->
      <section>
        <select>
          <option selected>Show 10</option>
          <option value="1">Show 25</option>
          <option value="2">Show 50</option>
          <option value="1">All</option>
        </select>

        <div>
          <ul class="inline-flex items-center -space-x-px">
            <li>
              <a
                href="#"
                class="block px-3 py-2 ml-0 leading-tight text-gray-500 bg-white border border-gray-300 rounded-l-lg hover:bg-gray-100 hover:text-gray-700 dark:bg-gray-800 dark:border-gray-700 dark:text-gray-400 dark:hover:bg-gray-700 dark:hover:text-white"
              >
                <span class="sr-only">Previous</span>
                <svg
                  aria-hidden="true"
                  class="w-5 h-5"
                  fill="currentColor"
                  viewBox="0 0 20 20"
                  xmlns="http://www.w3.org/2000/svg"
                >
                  <path
                    fill-rule="evenodd"
                    d="M12.707 5.293a1 1 0 010 1.414L9.414 10l3.293 3.293a1 1 0 01-1.414 1.414l-4-4a1 1 0 010-1.414l4-4a1 1 0 011.414 0z"
                    clip-rule="evenodd"
                  ></path>
                </svg>
              </a>
            </li>
            <li>
              <a
                href="#"
                class="px-3 py-2 leading-tight text-gray-500 bg-white border border-gray-300 hover:bg-gray-100 hover:text-gray-700 dark:bg-gray-800 dark:border-gray-700 dark:text-gray-400 dark:hover:bg-gray-700 dark:hover:text-white"
                >1</a
              >
            </li>
            <li>
              <a
                href="#"
                class="px-3 py-2 leading-tight text-gray-500 bg-white border border-gray-300 hover:bg-gray-100 hover:text-gray-700 dark:bg-gray-800 dark:border-gray-700 dark:text-gray-400 dark:hover:bg-gray-700 dark:hover:text-white"
                >2</a
              >
            </li>
            <li>
              <a
                href="#"
                aria-current="page"
                class="z-10 px-3 py-2 leading-tight text-blue-600 border border-blue-300 bg-blue-50 hover:bg-blue-100 hover:text-blue-700 dark:border-gray-700 dark:bg-gray-700 dark:text-white"
                >3</a
              >
            </li>
            <li>
              <a
                href="#"
                class="px-3 py-2 leading-tight text-gray-500 bg-white border border-gray-300 hover:bg-gray-100 hover:text-gray-700 dark:bg-gray-800 dark:border-gray-700 dark:text-gray-400 dark:hover:bg-gray-700 dark:hover:text-white"
                >4</a
              >
            </li>
            <li>
              <a
                href="#"
                class="px-3 py-2 leading-tight text-gray-500 bg-white border border-gray-300 hover:bg-gray-100 hover:text-gray-700 dark:bg-gray-800 dark:border-gray-700 dark:text-gray-400 dark:hover:bg-gray-700 dark:hover:text-white"
                >5</a
              >
            </li>
            <li>
              <a
                href="#"
                class="block px-3 py-2 leading-tight text-gray-500 bg-white border border-gray-300 rounded-r-lg hover:bg-gray-100 hover:text-gray-700 dark:bg-gray-800 dark:border-gray-700 dark:text-gray-400 dark:hover:bg-gray-700 dark:hover:text-white"
              >
                <span class="sr-only">Next</span>
                <svg
                  aria-hidden="true"
                  class="w-5 h-5"
                  fill="currentColor"
                  viewBox="0 0 20 20"
                  xmlns="http://www.w3.org/2000/svg"
                >
                  <path
                    fill-rule="evenodd"
                    d="M7.293 14.707a1 1 0 010-1.414L10.586 10 7.293 6.707a1 1 0 011.414-1.414l4 4a1 1 0 010 1.414l-4 4a1 1 0 01-1.414 0z"
                    clip-rule="evenodd"
                  ></path>
                </svg>
              </a>
            </li>
          </ul>
        </div>
      </section>

      <!------------- section ------------->
      <!------------- section ------------->
      <!------------- section ------------->
      <!------------- section ------------->
    </main>
  </div>
</template>
  
<script setup>
const store = reactive({
  products: "",
});

try {
  store.products = await useFetch("https://fakestoreapi.com/products?limit=8");
} catch (error) {
  console.log(error);
}
</script>

<style lang="scss" scoped></style>