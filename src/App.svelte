<script>
    import { fade, fly, slide } from 'svelte/transition';
    import wjuton from './assets/untitled.png'
</script>

<style>
    
</style>

<div class="flex w-[100vw] h-[100vh] select-none">
    <div class="flex flex-col justify-center w-[40%] pl-10 bg-zinc-900 gap-3">
        <p class="text-gray-50">wjuton.dev</p>
        <p class="text-white font-semibold md:text-3xl xl:text-5xl text-left" transition:fade={{duration: 150}}>
            Hi! 👋 I'm <span class="transition-all text-pink-500 shadow-pink-300 hover:text-pink-300 cursor-pointer">@wjuton</span>
        </p>
        <p class="text-gray-300 font-semibold md:text-xl xl:text-3xl text-left w-[75%]">
            Silly kitty lover and sometimes coder...
        </p>
        <div class="bg-pink-500 w-fit p-2 rounded-xl text-gray-50 drop-shadow-xl transition-all cursor-pointer hover:bg-pink-400 hover:animate-pulse">
            See more..
        </div>
    </div>
    <div class="w-[60%] flex justify-center items-center h-full overflow-hidden bg-zinc-900 ">
        <img src={wjuton} class="rounded-full  shadow-pink-500 drop-shadow-2xl transition-all " alt="" />
    </div>
</div>

