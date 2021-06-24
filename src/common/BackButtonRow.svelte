<!-- ///////////////////////// 
///////// script ////////////
///////////////////////////// -->
<script>
    import Button from "../common/Button.svelte";
</script>

<!-- ///////////////////////// 
///////// display ///////////
///////////////////////////// -->
<nav>
    <Button to="/">&lt; Back</Button>

    <div class="text">
        To the
        <span>Library</span>
    </div>
</nav>

<!-- ///////////////////////// 
////////// style ////////////
///////////////////////////// -->
<style>
    nav {
        display: flex;
        align-items: center;
        text-transform: uppercase;
        margin-bottom: var(--spacingXLarge);
    }
    .text {
        margin-left: var(--spacingSmall);
    }
    span {
        font-weight: var(--typeWeightBold);
    }
</style>
