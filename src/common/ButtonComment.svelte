<script>
    import { links } from "svelte-routing";

    export let book = {};
    export let interactive = false;
</script>

{#if interactive}
    <a href={"/comment/" + book.id} on:click use:links class="button">
        <slot />
    </a>
{:else}
    <button on:click class="button">
        <slot />
        <i class="fas fa-comments"></i>
    </button>
{/if}

<style>
    .button {
        width: 10%;
        height: 13%;
        border-radius: 35px;
        cursor: pointer;
    }
</style>