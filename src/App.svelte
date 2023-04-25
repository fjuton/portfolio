<script>
    import { fade } from 'svelte/transition';
    import wjuton from './assets/untitled.png'

    import Info from './lib/Info.svelte';
    import Footer from './lib/Footer.svelte';

    const scrollDown = () => {
        document.querySelector(".info").scrollIntoView({
            behavior: 'smooth',
        })
    }

</script>

<style>

</style>

<div class="flex md:flex-row w-[100vw] h-[100vh] select-none">
    <div class="flex flex-col justify-center w-[100%] md:w-[40%] pl-10 bg-zinc-900 gap-3">
        <p class="text-gray-50">wjuton.dev</p>
        <p class="text-white font-semibold md:text-3xl xl:text-5xl text-left" transition:fade={{duration: 150}}>
            <a href="https://github.com/fjuton" target="_blank">Hi! 👋 I'm <span class="transition-all text-pink-500 shadow-pink-300 hover:text-pink-300 cursor-pointer">@wjuton</span></a>
        </p>
        <p class="text-gray-300 font-semibold md:text-xl xl:text-3xl text-left w-[75%]">
            Silly kitty lover and sometimes coder...
        </p>
        <!-- svelte-ignore a11y-click-events-have-key-events -->
        <div class="bg-pink-500 w-fit p-2 rounded-xl  text-gray-50 drop-shadow-xl transition-all cursor-pointer hover:bg-pink-400 hover:animate-pulse" on:click|preventDefault={scrollDown}>
            See more..
        </div>
    </div>
    <div class="w-[100%]  md:w-[60%] flex justify-center items-center h-full overflow-hidden bg-zinc-900 ">
        <img src={wjuton} class="rounded-full shadow-pink-500 drop-shadow-2xl transition-all " alt="" draggable="false" />
    </div>


</div>

<Info></Info>
<Footer></Footer>