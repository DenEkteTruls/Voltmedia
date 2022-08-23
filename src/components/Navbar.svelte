<script>
import { element } from "svelte/internal";

    let menu = [
        {'title': 'Services', 'href': '#'},
        {'title': 'Work', 'href': '#'},
        {'title': 'Products', 'href': '#'},
        {'title': 'People', 'href': '#'},
        {'title': 'Blog', 'href': '#'},
        {'title': 'Contact', 'href': '#'}
    ];
</script>



<div class="container">
    <div class="title">
        <img src="./design/white.png" alt="" onclick="{() => { window.location.href="/"}}"/>
    </div>
    <div class="menu">
    {#each menu as element}
        <a id="menu-a" href="{element.href}"><p id="menu-p">{element.title}</p></a>
    {/each}
    </div>
</div>



<style>
    .container {
        display: flex;
        flex-direction: row;
        justify-content: space-between;
        align-items: center;
        height: 100px;
        width: 100%;
        background-color: var(--background-color);
        padding: 10px;
    }

    .title {
        display: flex;
        width: fit-content;
        justify-content: center;
        align-items: center;
    }

    .title > img {
        max-width: 200px;
        padding: 50px;
    }

    .menu {
        display: flex;
        flex-direction: row;
        justify-content: space-evenly;
        align-items: center;
        float: right;
        width: 720px;
        padding-right: 50px;
    }

    #menu-a {
        text-decoration: none;
        color: white;
    }

    #menu-p {
        font-weight: 700;
        font-size: 19px;
        letter-spacing: .2px;
        padding: 5px 0;
    }

    #menu-p:hover {
        border-bottom: 2px solid var(--default-red);
        padding-top: 7px;
    }
</style>