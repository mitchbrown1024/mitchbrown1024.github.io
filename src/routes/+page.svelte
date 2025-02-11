<script>
	import BackgroundCircle from "./background_circle.svelte";
    import NameTitle from "./name_title.svelte";
</script>

<div class="circle"><BackgroundCircle></BackgroundCircle></div>
<NameTitle></NameTitle>

<style>
    div.circle {
        position: absolute;
        z-index: -900;
        top:0;
        left:0;
        margin-left: -1000px;
        margin-top: -500px;
    }
</style>