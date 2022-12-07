<template>
  <div class="flex container w-full">
    <aside class="flex flex-col w-1/5 h-full  h-screen justify-between  border-r">
      <section class="flex flex-col  items-center w-full  mt-5">
        <div class="flex">
          <i class="w-full fab fa-twitter text-3xl mb-2 text-blue"></i>
        </div>
        <button
          class="outline-none hover:text-blue hover:bg-lightblue w-full  mt-2 rounded font-semibold p-2  md:text-center  lg:text-center"
          v-for="tab in tabs" :key="tab.title">
          <div>
            <i :class="`${tab.icon} text-2xl  md:text-center  lg:text-center`"></i>
          </div>
          <span class="md:block hidden">{{ tab.title }}</span>
        </button>
        <button class="outline-none  bg-blue hover:bg-darkblue w-12 h-12  mt-2 rounded-full text-white">
          <i class="fas fa-plus"></i>
        </button>
      </section>

      <div class="w-full text-center">
        <button>
          <img src="./assets/profile.png" class="w-12 h-12 bg-gray-200 rounded-full" alt="">
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
