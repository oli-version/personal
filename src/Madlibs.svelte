<script>
    let surname = '';
    let weekday = '';
    let temp = '';
    let emotion = '';
    let submitted = false;

    function submit() {
        submitted = true
    }

    function unsubmit() {
        submitted = false
    }
</script>

<main>
    <h1>Madlibs</h1>
    <p>Madlibs :)</p>
    <br>
    <input type="text" bind:value={surname} placeholder="surname"> <br>
    <input type="text" bind:value={weekday} placeholder="day"> <br>
    <input type="text" bind:value={temp} placeholder="temp"> <br>
    <input type="text" bind:value={emotion} placeholder="adjective"> <br>
    {#if submitted === false}
    <button on:click={submit}><i class="fa fa-eye"></i> Show</button>
    {:else}
    <button on:click={unsubmit}><i class="fa fa-eye-slash"></i> Hide</button>
    {/if}
    <br>
    <br>
    <br>
    {#if submitted === true}
    <p>I went to Mr. {surname}'s office and he told me that last {weekday} he went to the beach and the water was {temp.toLowerCase()}, and then he went back home to his {emotion.toLowerCase()} life.</p>
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