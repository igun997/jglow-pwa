<script type="ts">
    import { fade } from 'svelte/transition';
    export let visible = true;
    export let timer = 0;
    if (timer > 0){
        setTimeout(()=>{
            visible = !visible;
        },timer)
    }
</script>
{#if visible}
    <div class="preloader" id="preloader" out:fade>
        <div class="spinner-grow text-secondary" role="status">
            <div class="sr-only">Loading...</div>
        </div>
    </div>
{/if}
