
<template>
    <NavBar />
    <div class="flex items-center justify-center py-8">
    <div class=" p-2 border-2 shadow-lg h-[50%] w-[95%] max-w-[320px] rounded-xl items-center justify-center">
        <div class="flex  items-center justify-center">
        <div class="p-2 items-center justify-center ">
            Name <br> <input  v-model="name" type="text" placeholder="Name" class="px-2 rounded-lg border"  >
             </div>
    </div>
    <div class="flex  items-center justify-center">
        <div class="p-2">
            
            E-Mail <br> <input v-model="email" type="e-mail" placeholder="E-Mail" class="px-2  rounded-lg border">
        </div>
    </div>
    <div class="flex  items-center justify-center">
        <div class="p-2">
            Phone  <br> <input v-model="phone" type="Number" placeholder="Phone" class="px-2  rounded-lg border">
        </div>
    </div>
    <div class="flex  items-center justify-center">
        <div class="p-2">
           
            Password <br> <input v-model="password" type="password" placeholder="Password" class="px-2  rounded-lg border">
        </div>
    </div>
    <div class="flex  items-center justify-center">
        <div class="p-2">
            
            Re-Password <br>   <input v-model="repassword" type="password" placeholder="Re-Password" class="px-2  rounded-lg border">
        </div>
    </div>
        <div class="p-2 flex items-center justify-center">
        <div class="flex border-2 border-black cursor-pointer bg-green-500 rounded-lg h-full w-20 items-center justify-center shadow-lg">
            Register
        </div>
    </div>
    <div class="text-sm flex  items-center justify-center underline cursor-pointer">
            I Allready Have a Account ?
        </div>
    </div>
</div>
</template>
<script>
    export default {
        data (){
            return {
                name :"",
                email:"",
                phone:"",
                password:"",
                repassword:"", 
            }
        },
        methods:{
            
        }
    }
</script>