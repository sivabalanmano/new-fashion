<template>
    <NavBar />
    <div class="flex items-center justify-center py-10">
    <div class=" p-2 border-2 shadow-lg h-[50%] w-[95%] max-w-[320px] rounded-xl items-center justify-center">
        <div class="flex  items-center justify-center">
        <div class="p-2 items-center justify-center">
            Name <br> <input type="text" placeholder="Name" class="px-2  rounded-lg border ">
        </div>
    </div>
    <div class="flex  items-center justify-center">
        <div class="p-2">
            
            E-Mail <br> <input type="e-mail" placeholder="E-Mail" class="px-2  rounded-lg border">
        </div>
    </div>
    <div class="flex  items-center justify-center">
    </div>
    <div class="flex  items-center justify-center">
        <div class="p-2">
           
            Password <br> <input type="password" placeholder="Password" class="px-2  rounded-lg border"><br>
            <div class="text-sm text-green-500 flex items-center justify-end text-shadow-lg">
            <div >
                Forget Password</div>
            </div>
        </div> 
    </div>
    <div class="flex  items-center justify-center">
    </div>
        <div class="p-2 flex items-center justify-center">
        <div class="flex border-2 border-black cursor-pointer bg-green-500 rounded-lg h-full w-20 items-center justify-center shadow-lg">
            Login
        </div> 
        
    </div>
        <div class="text-sm flex  items-center justify-center">
            I don't Have a Account
        </div>
    </div>
</div>
</template>