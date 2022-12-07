<template>
  <div class=" flex  container  h-screen w-full">
    <aside class="flex flex-col lg:w-1/5  h-full  h-screen justify-between  px-5  border-r">
      <section class="flex flex-col   w-full mt-5">
        <div class="flex ml-2">
          <i class="w-full fab fa-twitter text-3xl mb-3 mt-5 text-blue"></i>
        </div>
        <button
          class="outline-none hover:text-blue hover:bg-lightblue w-full  mt-4 rounded font-semibold p-2 flex md:justify-start justify-center "
          v-for="tab in tabs" :key="tab.title">
          <i :class="`${tab.icon} text-2xl flex items-center `"></i>
          <span class="md:inline-block hidden ml-5">{{ tab.title }}</span>
        </button>
        <button class="outline-none  bg-blue hover:bg-darkblue  w-12 lg:w-full h-12  mt-10  rounded-full text-white">
          <i class="fas fa-plus"></i>
        </button>
      </section>

      <div class="w-full">
        <button class="flex flex-row-reverse mb-5">
          <div class="   flex-col text-start  ml-5 md:flex hidden ">
            <span class="font-semibold">Marla Singer</span>
            <span>@marla619</span>
          </div>
          <img src="./assets/hGiHpNc4_400x400-1686512996.jpg" class="h-12 w-auto bg-gray-200 rounded-full" alt="">
          
        </button>
      </div>
    </aside>
  </div>

</template>

<script>

export default {
  data() {
    return {
      tabs: [
        { icon: 'fas fa-home', title: 'Home', id: 'home' },
        { icon: 'fas fa-hashtag', title: 'Explore', id: 'explore' },
        { icon: 'far fa-bell', title: 'Notifications', id: 'notifications' },
        { icon: 'far fa-envelope', title: 'Messages', id: 'messages' },
        { icon: 'far fa-bookmark', title: 'Bookmarks', id: 'bookmarks' },
        { icon: 'fas fa-clipboard-list', title: 'Lists', id: 'lists' },
        { icon: 'far fa-user', title: 'Profile', id: 'profile' },
        { icon: 'fas fa-ellipsis-h', title: 'More', id: 'more' }
      ],
    }
  }
}

</script>
