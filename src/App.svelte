<script>
    import Inner from "./Inner.svelte";

    let handleMessage = (event) => {
        alert(event.detail.text)
    };
</script>

<Inner on:message={handleMessage} />
