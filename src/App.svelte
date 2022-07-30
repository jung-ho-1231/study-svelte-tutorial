<script>
    let count = 0;
    $: double = count * 2;

    function handleClick() {
        count += 1;
    }
</script>

<button on:click={() => handleClick()}>
    Clicked {count} {count === 1 ? 'time' : 'times'}
</button>

<p>{count} doubles is {double}</p>