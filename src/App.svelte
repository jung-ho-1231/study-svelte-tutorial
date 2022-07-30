<script>
    let scoops = 1;
    let flavours = ['Mint choc chip'];

    let menu = [
        'Cookies and cream',
        'Mint choc chip',
        'Raspberry ripple'
    ]

    function join(flavors) {
        if (flavors.length === 1) return flavors[0]
        return `${flavors.slice(0, -1).join(', ')} and ${flavors[flavors.length - 1]}`;
    }
</script>

<h2>Size</h2>


<label>
    <input type="radio" bind:group={scoops} name="scopes" value={1}>
    One scope
</label>

<lable>
    <input type="radio" bind:group={scoops} name="scopes" value={2}>
    Two scopes
</lable>

<lable>
    <input type="radio" bind:group={scoops} name="scopes" value={3}>
    Three scopes
</lable>

<h2>Flavours</h2>

{#each menu as flavour}
    <lable>
        <input type="checkbox" bind:group={flavours} name="flavors" value={flavour}>
        {flavour}
    </lable>
{/each}


{#if flavours.length === 0}
    <p>Please select at least one flavour</p>
{:else if flavours.length > scoops}
    <p>Can't order more flavours then scoops!</p>
{:else}
    <p>
        You ordered {scoops} {scoops === 1 ? 'scoop' : 'scoops'}
        of {join(flavours)}
    </p>
{/if}