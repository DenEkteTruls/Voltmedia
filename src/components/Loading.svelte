<script>
    window.onload = (event) => {
        document.getElementById("yes").style.backgroundPosition = "left";
        document.getElementById("sir").style.marginBottom = "0";
        document.getElementById("sir").style.opacity = "1"; 
        sessionStorage.setItem("loaded", true);
        setTimeout(() => {
            document.getElementById("sir").style.transform = "translateY(30%)";
            document.getElementById("sir").style.opacity = "0";
            setTimeout(() => {
                window.location.href = "/";
            }, 100);
        }, 1400);
    };
</script>



<div id="yes" class="container">
    <img id="sir" class="show" src="./design/load_title.png" alt=""/>
</div>



<style>
    .container {
        width: 100vw;
        height: 100vh;
        display: flex;
        justify-content: center;
        align-items: center;
        background-color: black;
        background: linear-gradient(to left, black 50%, var(--background-color) 50%) right;
        background-size: 200%;
        transition: 1.5s ease-in-out;
        overflow: hidden;
    }

    img {
        width: 60%;
        opacity: 0;
        transition: all 0.3s ease-out;
        margin-bottom: 30%;
    }
</style>