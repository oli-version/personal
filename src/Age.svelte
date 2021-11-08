<script>
    let year = 2021;
    let n = '';
    let min = 1930
    let buttons = true

    function hideButtons() {
        buttons = false
    }

    function buttonClickNo() {
        buttons = 'no'
    }
</script>

<main>
    <h1>Age calculator</h1>
    <p>Enter in your birth year and let the magic happen</p>
    <p>This is a rippoff of <a href="https://age.vercel.app">age.versel.app</a> by <a href="https://twitter.com/onsclom">@onsclom</a></p>
    <br>
    <input type="number" {min} max={year - 1} bind:value={n} placeholder="birth year">
    {#if n === ''}
    <p>Please enter a year</p>
    {:else if n < min}
    <p>Please enter a year above {min}</p>
    {:else if n > year}
    <p>Please enter a year below {year}</p>
    {:else if n >= min}
    <p>Are you <b>{year - n}</b> years old?</p>
        {#if buttons === true}
        <button on:click={hideButtons}><i class="fa fa-check"></i> Yes</button> <button on:click={buttonClickNo}><i class="fa fa-times"></i> No</button>
        {:else if buttons === false}
        <p></p>
        {:else if buttons === 'no'}
        <p>Please message me on <a href="https://discord.gg/SZ4pW3g5GD">Discord</a></p>
        {/if}
    {/if}
</main>

<style>
    main{
        border-color: white;
        border-style: solid;
        border-width: 1px;
        padding: 50px;
        width: 700px;
        border-radius: 5px;
    }
</style>