<script>
    let yes = false;
</script>

<lable>
    <input type="checkbox" bind:checked={yes}>
    Yes! Send me regular email spam
</lable>


{#if yes}
    <p>Thank you. We will bombard your inbox and sell your personal details</p>
{:else}
    <p>You must opt in continue. if you're not paying, you're the product</p>
{/if}
