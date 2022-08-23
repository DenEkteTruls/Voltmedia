<script>
    import Navbar from "./components/Navbar.svelte";
    import Loading from "./components/Loading.svelte";

    $: loaded = sessionStorage.getItem("loaded");
</script>



{#if !loaded}
    <Loading/>
{/if}


<Navbar/>
<div class="container">
    <div class="launch">
        <div class="left">
            <h1 id="title"><b>You challenge<br>is our</b> priority.</h1>
            <p id="details">Global leadership teams trust Modern to deliver marketing-led business solutions that define and realise bold ambitions. From singular campaigns to wide-reaching transformation programmes; we help the world’s most innovative businesses to grow wiser, stronger and faster.</p>
            <button id="button">View our work</button>
        </div>
        {#if loaded}
            <div class="show" id="red-box"/>
            <div class="show" id="yellow-box"/>
        {:else}
            <div id="red-box"/>
            <div id="yellow-box"/>
        {/if}
    </div>
</div>



<style>
    .container {
        height: 100%;
        max-width: 1280px;
        display: flex;
        justify-content: left;
        margin: 0 auto;
    }

    .launch {
        display: flex;
        justify-content: left;
        align-items: center;
        margin: 40px 7%;
    }

    .left {
        display: flex;
        flex-direction: column;
        max-width: 700px;
    }

    #title {
        font-size: 75px;
        font-weight: 700;
        color: white;
        margin-bottom: 20px;
        line-height: 80px;
    }

    #title > b {
        color: var(--default-red);
        font-weight: 700;
    }

    #details {
        color: white;
        font-size: 20px;
        font-weight: 300;
        margin-top: 0px;
        letter-spacing: .5px;
    }

    #red-box {
        position: fixed;
        top: 550px;
        left: 42%;
        background-color: var(--default-red); 
        width: 80vw;
        height: 80vw;
        transform: rotate(50deg);
        visibility: hidden;
    }

    #yellow-box {
        background-color: var(--default-yellow);
        position: fixed;
        top: calc(800px + 18%);
        left: 55%;
        width: 80vw;
        height: 80vw;
        transform: rotate(30deg);
        visibility: hidden;
    }

    #button {
        margin-top: 20px;
        width: 190px;
        height: 60px;
        border: 2px solid var(--default-red);
        background-color: var(--background-color);
        color: white;
        font-size: 18px;
        border-radius: 8px 25px;
        transition: background-color .2s ease-in-out;
        font-weight: 600;
    }

    #button:hover {
        background-color: var(--default-red);
        cursor: pointer;
    }

    .show {
        visibility: visible !important;
    }
</style>