
<template>
    <NavBar />
    <div class="flex items-center justify-center py-8">
    <div class=" p-2 border-2 shadow-lg h-[50%] w-[95%] max-w-[320px] rounded-xl items-center justify-center">
        <form action="login.vue">
        <div class="flex  items-center justify-center">
        <div class="p-2 items-center justify-center ">
            
            Name <br> <input  v-model="name" type="text" placeholder="Name" class="px-2 rounded-lg required: "
         :class="isColor1 ? 'border-2 border-green-500' : 'border-2 border-red-500'" > <br>
         <span class="text-sm text-red-500" 
            :class="isColor1 ? 'hidden' : 'success'" >Please Enter The Value</span>
         </div>
    </div>
    <div class="flex  items-center justify-center">
        <div class="p-2">
            
            E-Mail <br> <input v-model="email" type="e-mail" placeholder="E-Mail" class="px-2  rounded-lg border
            " :class="isColor2 ? 'border-2 border-green-500' : 'border-2 border-red-500 '" > <br>
            <span class="text-sm text-red-500" 
            :class="isColor2 ? 'hidden' : 'success'" >Please Enter The Value</span>
        </div>
    </div>
    <div class="flex  items-center justify-center">
        <div class="p-2">
            Phone  <br> <input v-model="phone" type="Number" placeholder="Phone" class="px-2  rounded-lg border"
            :class="isColor3 ? 'border-2 border-green-500' : 'border-2 border-red-500'" > <br>
            <span class="text-sm text-red-500" 
            :class="isColor3 ? 'hidden' : 'success'" >Please Enter The Value</span>
        </div>
    </div>
    <div class="flex  items-center justify-center">
        <div class="p-2">
           
            Password <br> <input v-model="password" type="password" placeholder="Password" class="px-2  rounded-lg border"
            :class="isColor4 ? 'border-2 border-green-500' : 'border-2 border-red-500'" > <br>
            <span class="text-sm text-red-500" 
            :class="isColor4 ? 'hidden' : 'success'" >Please Enter The Value</span>
        </div>
    </div>
    <div class="flex  items-center justify-center">
        <div class="p-2">
            
            Re-Password <br>   <input v-model="repassword" type="password" placeholder="Re-Password" class="px-2  rounded-lg border"
            :class="isColor5 ? 'border-2 border-green-500' : 'border-2 border-red-500' " >  <br>
            <span class="text-sm text-red-500" 
            :class="isColor5 ? 'hidden' : 'success'" >Please Enter The Value</span>
        </div>
    </div>
        <div class="p-2 flex items-center justify-center">
        <div type="button" class="flex border-2 border-black cursor-pointer bg-green-500 rounded-lg h-full w-20 items-center justify-center shadow-lg"
        @click="fshion()">
            Register
        </div>
    </div>
    <div class="text-sm flex  items-center justify-center underline cursor-pointer">
            I Allready Have a Account ?
        </div>
    </form></div>
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
                isColor1:true,
                isColor2:true,
                isColor3:true,
                isColor4:true,
                isColor5:true,
            }
        },
        methods:{
            fshion () {
                if(this.name.length >= 8){
                    this.isColor1=true
                }
                else{
                    this.isColor1=false
                }
                if (this.email.length >= 8) {
                    this.isColor2=true
                }
                else{
                    this.isColor2=false
                }
                if (this.phone.length >= 10) {
                    this.isColor3=true
                }
                else{
                    this.isColor3=false
                }
                if (this.password.length >= 8) {
                    this.isColor4=true
                }
                else{
                    this.isColor4=false
                }
                if (this.repassword.length >= 8) {
                    this.isColor5=true
                }
             else{
                    this.isColor5=false
                }
            }
        }
    }
</script>