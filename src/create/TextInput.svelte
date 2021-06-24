<script>
    export let label;
    export let value;
    export let multiline = false;
</script>

<style>
    label {
    font-weight: var(--typeWeightBold);
    text-transform: uppercase;
  }
  span {
    padding: 0 0 var(--spacingSmall) var(--spacingSmall);
  }
  input,
  textarea {
    display: block;
    background: white;
    border-radius: 25px;
    border: 2px solid var(--colorFg);
    width: 80%;
  }
  textarea {
    height: 8rem;
  }
</style>

<!-- svelte-ignore a11y-label-has-associated-control -->
<label>
    <span>{label}:</span>
    {#if multiline}
        <textarea bind:value maxlength="500"/>
    {:else}
        <input type="text" bind:value maxlength="25"/>
    {/if}
</label>