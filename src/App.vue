<template>
  <div class=" flex  container  h-screen w-full relative">
    <aside class="flex flex-col   lg:w-1/5  h-full  h-screen justify-between  px-5  border-r bg-white">
      <section class="flex flex-col   w-full mt-5">
        <div class="flex ml-2">
          <i class="w-full fab fa-twitter text-3xl mb-3 mt-1 text-blue"></i>
        </div>
        <button
          class="outline-none hover:text-blue hover:bg-lightblue w-full  mt-2 rounded font-semibold p-2 flex md:justify-start justify-center "
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
    <main class="lg:w-1/2 h-full border-r w-full ">
      <header class="flex items-center justify-between py-3 px-5 border-b ">
        <h2 class="font-bold  mt-1 text-xl ">Home</h2>
        <i class="far fa-star text-xl text-blue"></i>
      </header>
      <div class="">
        <div class="flex border-b p-2 ">
          <div class="p-2 flex-none">
            <img src="./assets/hGiHpNc4_400x400-1686512996.jpg" class="w-14 h-14 ml-2 rounded-full border flex-none"
              alt="">
          </div>
          <form class="w-full relative  p-5">
            <textarea class="w-full  focus:outline-none h-24 " placeholder="What's up?"></textarea>
            <div class="absolute flex justify-between w-full bottom-1 left-0">
              <div class="mt-5 flex">
                <i class="text-lg text-blue mr-4 far fa-image"></i>
                <i class="text-lg text-blue mr-4 fas fa-film"></i>
                <i class="text-lg text-blue mr-4 far fa-chart-bar"></i>
                <i class="text-lg text-blue mr-4 far fa-smile"></i>
              </div>
              <button class="bg-blue h-10 px-4 rounded-full text-white font-semibold mr-3">Tweet</button>
            </div>
          </form>
        </div>

        <!-- My Tweet -->

        <div class="border-b cursor-pointer hover:bg-gray-200">
          <div class="text p-3 ml-4 flex flex-col border-">
            <div class="flex relative">
              <img src="./assets/hGiHpNc4_400x400-1686512996.jpg" class="h-12 w-12  flex-none rounded-full absolute"
                alt="">
              <div class="flex gap-2 ml-16 mb-3 justify-between w-full items-center">
                <div class="flex gap-1">
                  <h6 class="font-semibold">Marla Singer</h6>
                  <p class="text-dark text-sm">@marla619</p>
                  <p class="text-dark text-sm">6h</p>
                </div>
                <i class="fas fa-angle-down text-dark ml-auto"></i>
              </div>
  
            </div>
            <p class="ml-16">Altarın oğlu tarkan</p>
            <section class="text-bottom flex  justify-around mt-5 text-dark">
              <i class="far fa-comment mr-3 cursor-pointer hover:text-teal-400 transition-all "></i>
              <i class="fas fa-retweet mr-3 cursor-pointer hover:text-gray-800 "></i>
              <i class="fas fa-heart mr-3 cursor-pointer hover:text-red-600 "></i>
              <i class="fas fa-share-square mr-3 cursor-pointer hover:text-indigo-600 "></i>
            </section>
          </div>
  
        </div>
       

        <!-- Following Tweet -->

        <div class="border-b cursor-pointer hover:bg-gray-200">
          <div class="text p-3 ml-4 flex flex-col border-">
            <div class="flex relative">
              <img src="./assets/hGiHpNc4_400x400-1686512996.jpg" class="h-12 w-12  flex-none rounded-full absolute"
                alt="">
              <div class="flex gap-2 ml-16 mb-3 justify-between w-full items-center">
                <div class="flex gap-1">
                  <h6 class="font-semibold">Marla Singer</h6>
                  <p class="text-dark text-sm">@marla619</p>
                  <p class="text-dark text-sm">6h</p>
                </div>
                <i class="fas fa-angle-down text-dark ml-auto"></i>
              </div>
  
            </div>
            <p class="ml-16">Altarın oğlu tarkan</p>
            <section class="text-bottom flex  justify-around mt-5 text-dark">
              <i class="far fa-comment mr-3 cursor-pointer hover:text-teal-400 transition-all "></i>
              <i class="fas fa-retweet mr-3 cursor-pointer hover:text-gray-800 "></i>
              <i class="fas fa-heart mr-3 cursor-pointer hover:text-red-600 "></i>
              <i class="fas fa-share-square mr-3 cursor-pointer hover:text-indigo-600 "></i>
            </section>
          </div>
  
        </div>


        
        
        
      </div>

    </main>
    <section class="trend w-1/3 px-6 py-2 relative hidden lg:block">
      <input class="w-full border rounded-full pl-12 p-2  text-sm bg-lighter" type="text" placeholder="Search Twitter">
      <i class="fas fa-search absolute left-0 top-0 mt-5 ml-12 text-sm text-light"></i>

      <section class="w-full bg-lightest rounded-lg mt-5 pt-3">
        <div>
          <div class="top flex justify-between  items-center border-b p-3">
            <h3 class="font-bold text-lg">
              Trends for You
            </h3>
            <i class="fas fa-cog text-lg text-blue"></i>
          </div>
          <div class="trending ">
              <div class="pt-2 relative border-b  pb-2 hover:bg-gray-200 p-3 cursor-pointer" v-for="trend in trending" :key="trend.top">
                <i class="fas fa-angle-down text-lg text-dark absolute top-3 right-5"></i>
                <span class="text-xs text-dark leading-tight">{{ trend.top }}</span>
                <h5 class="font-semibold text-sm">{{ trend.title }}</h5>
                <span class="text-sm text-dark leading-tight">{{ trend.bottom }}</span>
            </div>
            <button class="text-blue p-3 text w-full outline-none flex">Show More</button>
          </div>

        </div>

      </section>
    </section>
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
      trending: [
        { top: 'Trending in TX', title: 'Gigi', bottom: 'Trending with: Rip Gigi' },
        { top: 'Music', title: 'We Won', bottom: '135K Tweets' },
        { top: 'Pop', title: 'Blue Ivy', bottom: '40k tweets' },
        { top: 'Trending in US', title: 'Denim Day', bottom: '40k tweets' },
        { top: 'Trending', title: 'When Beyonce', bottom: '25.4k tweets' },
      ],
      following: [
        {src: 'elon.jpg', name: 'Elon Musk', handle: '@teslaBoy', time: '20 min', tweet: 'Should I just quarantine on mars??', comments: '1,000', retweets: '550', like: '1,000,003'},
        {src: 'kevin.jpg', name: 'Kevin Hart', handle: '@miniRock', time: '55 min', tweet: 'Should me and the rock do another sub-par movie together????', comments: '2,030', retweets: '50', like: '20,003'},
        {src: 'elon.jpg', name: 'Elon Musk', handle: '@teslaBoy', time: '1.4 hr', tweet: 'Haha just made a flame thrower. Shld I sell them?', comments: '100,000', retweets: '1,000,002', like: '5,000,003'},
        {src: 'elon.jpg', name: 'Elon Musk', handle: '@teslaBoy', time: '1.4 hr', tweet: 'Just did something crazyyyyyyy', comments: '100,500', retweets: '1,000,032', like: '5,000,103'}
      ],
    }
  }
}

</script>
