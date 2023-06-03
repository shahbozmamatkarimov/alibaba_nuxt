<template>
  <main>
    <!------------- section 1 ------------->
    <section class="flex gap-5 border-2 bg-white rounded-lg p-5">
      <div class="w-[20%]">
        <ul class="flex flex-col gap-1 text-lg">
          <li class="p-2 cursor-pointer hover:bg-[#E5F1FF] hover:font-medium rounded-md">
            Automobiles
          </li>
          <li class="p-2 cursor-pointer hover:bg-[#E5F1FF] hover:font-medium rounded-md">
            Clothes and wear
          </li>
          <li class="p-2 cursor-pointer hover:bg-[#E5F1FF] hover:font-medium rounded-md">
            Home interiors
          </li>
          <li class="p-2 cursor-pointer hover:bg-[#E5F1FF] hover:font-medium rounded-md">
            Computer and tech
          </li>
          <li class="p-2 cursor-pointer hover:bg-[#E5F1FF] hover:font-medium rounded-md">
            Tools, equipments
          </li>
          <li class="p-2 cursor-pointer hover:bg-[#E5F1FF] hover:font-medium rounded-md">
            Sports and outdoor
          </li>
          <li class="p-2 cursor-pointer hover:bg-[#E5F1FF] hover:font-medium rounded-md">
            Animal and pets
          </li>
          <li class="p-2 cursor-pointer hover:bg-[#E5F1FF] hover:font-medium rounded-md">
            Machinery tools
          </li>
          <li class="p-2 cursor-pointer hover:bg-[#E5F1FF] hover:font-medium rounded-md">
            More category
          </li>
        </ul>
      </div>
      <div class="w-[60%] relative">
        <img
          class="absolute w-full h-full"
          src="https://img.freepik.com/free-photo/music-podcast-background-with-headphones-microphone-coffee-laptop-pink-table-flat-lay-top-view-flat-lay_501050-993.jpg"
          alt="img"
        />
        <div class="relative m-10">
          <h2 class="text-3xl">Latest trending</h2>
          <h1 class="text-4xl font-bold">Electronic items</h1>
          <button class="bg-white rounded-md px-3 py-1 my-5 font-medium">
            Learn more
          </button>
        </div>
      </div>
      <div class="flex flex-col justify-between w-[20%]">
        <div class="bg-[#E3F0FF] p-3 rounded-lg">
          <div class="flex my-2">
            <img
              class="h-12 w-12"
              src="https://cdn-icons-png.flaticon.com/512/149/149071.png"
              alt="user"
            />
            <div class="px-3 font-medium">
              <h1>Hi, user</h1>
              <p>let's get stated</p>
            </div>
          </div>
          <button class="bg-blue-500 py-1 text-white w-full rounded-md my-1">
            Join now
          </button>
          <button class="bg-white py-1 text-blue-500 w-full rounded-md my-1">
            Log in
          </button>
        </div>
        <div class="bg-[#F38332] text-white p-5 rounded-lg">
          <p>
            Get US $10 off <br />
            with a new <br />
            supplier
          </p>
        </div>
        <div class="bg-[#55BDC4] text-white p-5 rounded-lg">
          Send quotes with <br />
          supplier <br />
          preferences
        </div>
      </div>
    </section>

    <!------------- section 2 ------------->
    <section class="flex my-5 bg-white rounded-lg border-2">
      <div class="w-[30%] p-5">
        <div>
          <h1 class="font-bold text-lg">Deals and offers</h1>
          <p class="text-gray-500">Hygiene equipments</p>
        </div>
        <div class="flex gap-2 py-6 text-center text-white">
          <div class="bg-[#606060] p-2 w-14 rounded-md">
            <p class="font-bold text-lg">04</p>
            <p>Days</p>
          </div>
          <div class="bg-[#606060] p-2 w-14 rounded-md">
            <p class="font-bold text-lg">13</p>
            <p>Hour</p>
          </div>
          <div class="bg-[#606060] p-2 w-14 rounded-md">
            <p class="font-bold text-lg">34</p>
            <p>Min</p>
          </div>
          <div class="bg-[#606060] p-2 w-14 rounded-md">
            <p class="font-bold text-lg">56</p>
            <p>Sec</p>
          </div>
        </div>
      </div>
      <div class="flex w-full">
        <div
          class="flex flex-col items-center p-5 w-1/4 border-l-2"
          v-for="i in store.offers.data"
          :key="i.id"
        >
          <img class="h-40 w-[70%] p-2" :src="i.image" alt="img" />
          <p class="text-center p-2 w-[80%] truncate">
            {{ i.title.split(" ").slice(2, 3).join() }}
          </p>
          <button
            class="bg-[#FFE3E3] text-[#EB001B] font-bold text-lg py-1 px-4 rounded-full"
          >
            -2{{ String(i.id).slice(0, 1) }}%
          </button>
        </div>
      </div>
    </section>

    <!------------- section 3 ------------->
    <section class="flex my-5 rounded-lg bg-white border-2 border-b-0">
      <div class="w-[31%] relative">
        <img
          class="absolute w-full h-full rounded-l-lg"
          src="https://img.freepik.com/premium-photo/home-interior-with-armchair-flower-light-living-room-orange-tones-3d-illustration_175992-230.jpg?w=2000"
          alt="img"
        />
        <div class="relative m-5">
          <h1 class="font-bold text-lg">
            Home and <br />
            outdoor
          </h1>
          <button class="bg-white py-1 px-3 rounded-md my-5">Source now</button>
        </div>
      </div>
      <div class="flex w-full">
        <div class="flex flex-wrap h-[270px]">
          <div
            class="flex justify-between text-md p-4 w-1/5 border-l-2 border-b-2"
            v-for="i in store.outdoor.data"
            :key="i"
          >
            <div>
              <h1>{{ i.title.split(" ").slice(2, 3).join() }}</h1>
              <div class="text-gray-500 text-sm">
                <p>From</p>
                <p>USD 1{{ String(i.id).slice(0, 1) }}</p>
              </div>
            </div>
            <div class="flex items-end justify-end">
              <img class="w-16 h-20" :src="i.image" alt="img" />
            </div>
          </div>
        </div>
      </div>
    </section>

    <!------------- section 4 ------------->
    <section class="flex my-5 rounded-lg bg-white border-2 border-b-0">
      <div class="w-[31%] relative">
        <img
          class="absolute w-full h-full rounded-l-lg"
          src="https://img.freepik.com/premium-photo/white-alarm-clock-headphones-blue-background-music-rest-place-text_178193-204.jpg"
          alt="img"
        />
        <div class="relative m-5">
          <h1 class="font-bold text-lg">
            Consumer <br />
            electronics and <br />
            gadgets
          </h1>
          <button class="bg-white py-1 px-3 rounded-md my-5">Source now</button>
        </div>
      </div>
      <div class="flex w-full">
        <div class="flex flex-wrap h-[300px]">
          <div
            class="flex justify-between text-md p-4 w-1/5 border-l-2 border-b-2"
            v-for="i in store.outdoor.data"
            :key="i"
          >
            <div>
              <h1>{{ i.title.split(" ").slice(2, 3).join() }}</h1>
              <div class="text-gray-500 text-sm">
                <p>From</p>
                <p>USD 1{{ String(i.id).slice(0, 1) }}</p>
              </div>
            </div>
            <div class="flex items-end justify-end">
              <img class="w-16 h-20" :src="i.image" alt="img" />
            </div>
          </div>
        </div>
      </div>
    </section>

    <!------------- section 5 ------------->
    <section class="relative bg-white section5">
      <img
        class="absolute z-0 w-full h-full"
        src="https://c8.alamy.com/comp/BNHJNB/view-of-multiple-family-residences-in-a-suburban-neighborhood-single-BNHJNB.jpg"
        alt="img"
      />
      <div class="flex justify-between p-10">
        <div class="relative text-white">
          <h1 class="text-3xl font-bold">
            An easy way to send <br />
            requests to all suppliers
          </h1>
          <p class="py-5">
            Lorem ipsum dolor sit amet, consectetur adipisicing <br />
            elit, sed do eiusmod tempor incididunt.
          </p>
        </div>
        <div class="w-[40%] p-5 bg-white rounded-md">
          <h1 class="text-xl font-bold pb-3">Send quote to suppliers</h1>
          <form class="flex flex-col gap-5 w-full">
            <input
              class="placeholder-black border-2 rounded-md w-full py-2 px-3 text-gray-700 leading-tight focus:outline-none"
              type="text"
              placeholder="What item you need?"
            />
            <textarea
              class="border-2 rounded-md w-full py-2 px-3 text-gray-700 leading-tight outline-none"
              name="details"
              id="details"
              cols="30"
              rows="3"
              placeholder="Type more details"
            ></textarea>
            <div class="flex gap-3">
              <input
                class="placeholder-black border-2 w-1/2 rounded-md py-2 px-3 text-gray-700 leading-tight focus:outline-none"
                type="text"
                placeholder="Quantity"
              />
              <select
                class="border-2 placeholder-black rounded-md max-w-fit py-2 px-3 text-gray-700 leading-tight focus:outline-none"
                name="select"
                id="select"
              >
                <option value="1">Pcs</option>
                <option value="2">Junior</option>
                <option value="3">Middle</option>
                <option value="2">Senior</option>
              </select>
            </div>
            <input
              class="bg-blue-500 py-2 px-5 rounded-md font-medium text-white max-w-fit"
              type="submit"
              value="Send inquiry"
            />
          </form>
        </div>
      </div>
    </section>
    <!------------- section 6 ------------->
    <section class="py-5 -mx-1">
      <h1 class="pb-5 mx-1 font-bold text-2xl">Recommended items</h1>
      <div class="flex justify-between flex-wrap">
        <div
          class="text-md p-5 m-1 w-[18%] bg-white my-4 border-2 rounded-md"
          v-for="i in store.outdoor.data"
          :key="i"
        >
          <div class="flex justify-center">
            <img class="w-32 h-48 mb-5" :src="i.image" alt="img" />
          </div>
          <h1 class="font-bold">${{ i.price }}</h1>
          <p class="title text-gray-500 w-full text-sm">
            {{ i.title }}
          </p>
        </div>
      </div>
    </section>

    <!------------- section 7 ------------->
    <section>
      <h1 class="pb-5 mx-1 font-bold text-2xl">Our extra services</h1>
      <div class="flex justify-between">
        <div
          class="text-md bg-white m-1 w-1/4 my-4 border-2 rounded-xl"
          v-for="i in store.electronics.data"
          :key="i"
        >
          <div class="flex justify-center">
            <img
              class="w-full h-36 rounded-t-lg"
              :src="`https://images.pexels.com/photos/201442${i.id}/pexels-photo-201442${i.id}.jpeg`"
              alt="img"
            />
          </div>
          <div class="p-5 flex relative">
            <p class="title font-bold w-[80%] text-sm">
              {{ i.title }}
            </p>
            <i
              v-if="i.id == 1"
              class="bx bx-search text-2xl bg-[#D1E7FF] py-3 px-4 rounded-full absolute right-5 -top-7"
            ></i>
            <i
              v-if="i.id == 2"
              class="bx bx-box text-2xl bg-[#D1E7FF] py-3 px-4 rounded-full absolute right-5 -top-7"
            ></i>
            <i
              v-if="i.id == 3"
              class="bx bx-send text-2xl bg-[#D1E7FF] py-3 px-4 rounded-full absolute right-5 -top-7"
            ></i>
            <i
              v-if="i.id == 4"
              class="bx bx-shield-quarter text-2xl bg-[#D1E7FF] py-3 px-4 rounded-full absolute right-5 -top-7"
            ></i>
          </div>
        </div>
      </div>
    </section>

    <!------------- section 8 ------------->
    <section>
      <h1 class="pb-5 mx-1 font-bold text-2xl">Suppliers by region</h1>
      <div class="flex flex-wrap justify-between -mx-3">
        <div class="flex items-center my-2 w-1/5" v-for="i in store.countries" :key="i[1]">
          <img class="h-5 m-3" :src="`https://flagcdn.com/16x12/${i[1]}.png`" alt="{{ i[0] }}" />
          <div>
            <h1 class="font-medium">{{ i[0] }}</h1>
            <p class="text-gray-500">shopname.{{i[1]}}</p>
          </div>
        </div>
      </div>
    </section>
  </main>
</template>


<script setup>
const store = reactive({
  offers: "",
  outdoor: "",
  electronics: "",
  services: "",
  countries: [
    ["Arabic Emirates", "ae"],
    ["Australia", "au"],
    ["United States", "vi"],
    ["Russia", "ru"],
    ["Italy", "it"],
    ["Denmark", "dk"],
    ["France", "fr"],
    ["Arabic Emirates", "ae"],
    ["China", "cn"],
    ["Great Britain", "br"],
  ],
});

try {
  store.offers = await useFetch("https://fakestoreapi.com/products?limit=5");
} catch (error) {
  console.log(error);
}

try {
  store.outdoor = await useFetch(
    "https://fakestoreapi.com/products?limit=10&sort=desc"
  );
} catch (error) {
  console.log(error);
}

try {
  store.electronics = await useFetch(
    "https://fakestoreapi.com/products?limit=20&sort=desc"
  );
} catch (error) {
  console.log(error);
}

try {
  store.electronics = await useFetch(
    "https://fakestoreapi.com/products?limit=4"
  );
} catch (error) {
  console.log(error);
}
</script>

<style lang="scss" scoped>
.section5 {
  background: rgba(0, 0, 255, 0.679);
  background-size: cover;
  background-repeat: no-repeat;
  img {
    z-index: -1;
  }
}

.title {
  display: -webkit-box;
  overflow: hidden;
  height: 45px;
  -webkit-box-orient: vertical;
  -webkit-line-clamp: 2;
  line-clamp: 2;
  -webkit-line-clamp: 2;
}
</style>