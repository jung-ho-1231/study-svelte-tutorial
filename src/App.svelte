<script>
    let x = 7;
</script>

{#if x > 10}
    <p>{x} is grater then 10</p>
{:else if x > 5}
    <p>{x} is less then 5</p>
{:else}
    <p>{x} is between 5 and 10</p>
{/if}