
import type { NuxtLink } from '#build/components';
<template>
    <div>
    <div class="flex font-bold h-20 shadow-xl items-center w-full px-5 justify-between">
        <div class="border-2 border-black rounded-lg p-2 hover:bg-green-500">
            Fashion Corner
        </div>
        <div
        @click ="isSlidebarOpened  =  !isSlidebarOpened"
         class="border-black flex h-8 w-8 border rounded-lg items-center justify-center px-5 lg:hidden ">
            <i class="fa-solid fa-bars"></i>
      </div>
      <ul  class="hidden lg:flex gap-5 text-lg">
                <li v-for="(item,index) in menuItem" :key="index" class="hover:underline decoration-green-500 underline-offset-4 transition-[1s] decoration-4">
                    <NuxtLink :to="item.route">{{ item.name }}</NuxtLink>

                </li>
        
                </ul>
                
        <div class="hidden lg:block">
            <div  class="flex items-center gap-3 w-full justify-evenly">
                <NuxtLink to="/mens">
                    <div class="relative items-center justify-center hover:border border-black rounded-full p-2 bg-green-500">
                        <i class="fa-solid fa-person-digging text-sm"></i>
                    </div>

                </NuxtLink>
                <NuxtLink to="/womens">
                    <div class="relative items-center justify-center hover:border border-black rounded-full p-2 bg-green-500">
                        <i class="fa-solid fa-heart"></i>
                        
                    </div>

                </NuxtLink>
                <NuxtLink to="/contact">
                    <div class="relative items-center justify-center hover:border border-black rounded-full p-2 bg-green-500">
                        <i class="fa-solid fa-phone"></i>
                        
                    </div>
       

                </NuxtLink>
                <NuxtLink to="/login">
                <div class=" cursor-pointer hover:underline underline-offset-4 decoration-green-500 decoration-4">
                Login </div></NuxtLink>
                <NuxtLink to="register">
            <div class=" cursor-pointer hover:underline underline-offset-4 decoration-green-500 decoration-4"> Register </div></NuxtLink>
            </div>

        </div>
      </div>
      <div class="fixed top-0 h-screen bg-black/50 w-full overflow-hidden transition-[0.3] lg:hidden" 
      :class="isSlidebarOpened ? 'left-0' : '-left-full'">
        
      <div class="h-full w-[80%] max-w-[320px] bg-white p-5 shadow-md">
        <div  @click ="isSlidebarOpened  =  !isSlidebarOpened"
         class="h-10 w-10 rounded-md border border-black flex justify-center items-center">
            <i  class="fa-solid fa-xmark"> </i>
           
        </div>

      </div>
    </div>
</div>
<div
      class="fixed top-0 h-screen bg-black/50 w-full overflow-hidden transition-[0.3s] lg:hidden"
      :class="isSlidebarOpened ? 'left-0' : '-left-full'"
      ref="modal"
    >
      <div class="h-full w-[80%] max-w-[320px] bg-white p-5" ref="modalItem">
        <div class="flex justify-between items-center">
            <div class="border border-black rounded-lg p-2 hover:bg-green-500 font-bold">
            Fashion Corner
        </div>
          <div
            @click="isSlidebarOpened = !isSlidebarOpened"
            class="h-10 w-10 rounded-xl border border-black flex justify-center items-center"
          >
            <i class="fa-solid fa-xmark"></i>
          </div>
        </div>

        <div class="mt-5">
          <ul class="text-lg font-medium gap-3 hover:underline-offset-4" >
            <li v-for="(item, index) in menuItem" :key="index" class="hover:underline decoration-green-500 underline-offset-4 transition-[1s] decoration-4">
              <NuxtLink :to="item.route">{{ item.name }}</NuxtLink>
            </li>
          </ul>
        </div>

        <div class="flex items-center gap-3 mt-10 w-full justify-evenly">
          <NuxtLink to="/mens">
            <div class="relative  items-center justify-center hover:border border-black rounded-full p-2 bg-green-500">
              <i class="fa-solid fa-person-digging"></i>
            </div>
          </NuxtLink>
          <NuxtLink to="/womens">
            <div class="relative   items-center justify-center hover:border border-black rounded-full p-2 bg-green-500">
              <i class="fa-solid fa-heart"></i>
            </div>
          </NuxtLink>

          <NuxtLink to="/contact">
            <div class="relative  items-center justify-center hover:border border-black rounded-full p-2 bg-green-500">
              <i class="fa-solid fa-phone"></i>
            </div>
        </NuxtLink>
        </div>
        <NuxtLink to="/login" class="p-1 font-bold">
                <div class=" cursor-pointer hover:underline underline-offset-4 decoration-green-500 decoration-4">
                Login </div></NuxtLink>
                <NuxtLink to="register" class="font-bold">
            <div class=" cursor-pointer hover:underline underline-offset-4 decoration-green-500 decoration-4"> Register </div></NuxtLink>
      </div>
    </div>
</template>
<script> 
   export default {
     data () {
    return{
        isSlidebarOpened : false,
        menuItem:[
            {
                name : "Home",
                route:"/",
            },
            {
                name : "Mens",
                route:"/mens",
            },
            {
                name : "Womens",
                route:"/womens",
            },
            {
                name : "Contact",
                route:"/contact",
            },
            {
                name2:"login",
                route:"/login"
            },
            {
                name2:"register",
                route:"/register"
            }
        ],

    }
}
}
</script>