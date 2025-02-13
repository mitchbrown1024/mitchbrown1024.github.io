<script>
	import Line from "../../routes/line.svelte";

</script>

<div class="vertical-flex">
    <div class="empty"></div>
    <div class="container">
        <h1>hi, I'm</h1>
        <h1 class = "less-space">mitch brown</h1>
        <div class="line"><Line width=875 height=35></Line></div>
        <h2>software developer, not website designer</h2>
    </div>
    <div class="empty"></div>
</div>

<style>
    h1 {
        font-family: Cocogoose;
        font-weight: bold;
        font-size: 100px;
        padding-bottom: 70px;
        line-height: 0;
        margin-bottom: -20px;
    }
    h1.less-space {
        padding-bottom: 50px;
        z-index: 9;
    }
    h2 {
        font-family: Cocogoose;
        font-weight: lighter;
        font-size: 25px;
        line-height: 0;
    }
    div.line {
        position: relative;
        padding: 0;
        margin-top: -26px;
        margin-left: -75px;
        margin-bottom: -24px;
        z-index: -9;
    }
    div.vertical-flex {
        display: flex;
        flex-direction: column;
        justify-content: center;
        padding-left: 40px;
    }
    div.container {
        position:relative;
    }
</style>
