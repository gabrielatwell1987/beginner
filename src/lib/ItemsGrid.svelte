<script>
    import {getContext} from 'svelte';

    let items = getContext('newItemsContext');
</script>

<div class="flex items-center">
    {#each items as item}
        <div class="relative m-2 w-1/2 bg-white/20 h-40 flex items-center justify-center overflow-hidden">
            <img src={item.src} class="w-1/4" alt="">
            <div class="absolute bg-white text-black p-2 rounded-md">
                {item.name}
            </div>
        </div>
    {/each}
</div>