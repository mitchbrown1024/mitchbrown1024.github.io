<script>
	import BackgroundCircle from "$lib/components/background_circle.svelte";
	import MyExperience from "$lib/components/my_experience.svelte";



</script>

<div class="horizontal">
    <div>
        <div class="circle"><BackgroundCircle color=#12a312></BackgroundCircle></div>
        <MyExperience></MyExperience>
    </div>
</div>

<style>
    div.horizontal {
        display: flex;
        flex-direction: row;
    }
    div.circle {
        position: absolute;
        z-index: -900;
        top:0;
        left:0;
        margin-left: -1000px;
        margin-top: -500px;
    }
</style>