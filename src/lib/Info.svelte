<script>
    import { fade, slide } from 'svelte/transition';

    let projects = [
        {title: "💫 kosmici.net", url: "https://kosmici.net"}
    ]

    let links = [
        {title: "Github", url: "https://github.com/fjuton"},
        {title: "Twitter", url: "https://twitter.com/wjuton"},
        {title: "Wakatime", url: "https://wakatime.com/@wjuton"},
        {title: "Discord", url: "https://discord.gg/xKHEdYn3cq"},
    ]

</script>

<style>
    .data:not(:last-child)::after {
        content: "";
        display: block;
        width: 100%;
        background: theme('textColor.pink.400');
        opacity: 0.2;
        height: 1.5px;
        margin-top: 1.25rem;
    }
</style>

<div class="bg-zinc-800 info p-10 flex flex-col gap-5 info">
    <div class="data">
        <p transition:slide={{duration: 200}} class="text-gray-50 text-3xl">🌸 Projects</p>
        <div class="grid md:grid-cols-2 xl:grid-cols-4 gap-3 mt-3 ">
            {#each projects as project}
                <a transition:fade={{duration:200}} class="transition-all bg-zinc-600 hover:bg-pink-500 p-3 rounded-sm" href="{project.url}" target="_blank">
                    <p class="text-gray-50 md:text-xl 2xl:text-2xl">{project.title}</p>
                </a>
            {/each}
          
        </div>

        
    </div>

    <div class="data">
        <p transition:slide={{duration: 200}} class="text-gray-50 text-3xl">🔗 Find me</p>
        <div class="grid md:grid-cols-2 xl:grid-cols-4 gap-3 mt-3 ">
            {#each links as link}
                <a transition:fade={{duration:200}} class="transition-all bg-zinc-600 hover:bg-pink-500 p-3 rounded-sm" href="{link.url}" target="_blank">
                    <p class="text-gray-50 md:text-xl 2xl:text-2xl">{link.title}</p>
                </a>
            {/each}
          
        </div>
    </div>
    
</div>

