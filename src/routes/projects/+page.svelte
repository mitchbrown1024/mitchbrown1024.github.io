<script>
	import BackgroundCircle from "$lib/components/background_circle.svelte";
	import MyProjects from "$lib/components/my_projects.svelte";
	import NameTitle from "$lib/components/name_title.svelte";


</script>

<div class="horizontal">
    <div>
        <div class="circle"><BackgroundCircle color=#b335fc></BackgroundCircle></div>
        <MyProjects></MyProjects>
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