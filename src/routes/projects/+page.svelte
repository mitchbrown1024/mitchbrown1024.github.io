<script>
	import BackgroundCircle from "$lib/components/background_circle.svelte";
	import MyProjects from "$lib/components/my_projects.svelte";
	import Github from "../github.svelte";

</script>

<div class="horizontal">
    <div>
        <div class="circle"><BackgroundCircle color=#b335fc></BackgroundCircle></div>
        <MyProjects></MyProjects>
    </div>
    <div class="vertical">
        <div class = "horizontal-centered">
            <img src="/grocery_1.png" alt="grocery app's pantry view" class="iphone">
            <img src="/grocery_2.png" alt="grocery app's list view" class="iphone">
        </div>
        <div class="horizontal">
            <h1>my grocery app</h1>
            <a href="https://github.com/mitchbrown1024/GroceryApp" target="_blank"><Github size=32 color=black></Github></a> 
        </div>
        <p>
            This is a grocery app that I am developing because every other grocery app is either
            paid or looks like it's from 100 years ago.
            <br>
            <br>
            It's nothing crazy and definitely still a work in progress but I am using
            both swift and swiftUI to make the app and honestly, it's quite nice to work with.
        </p>
    </div>
</div>

<style>
    h1 {
        font-family: Cocogoose;
        font-size: 32px;
    }
    a {
        margin-top: 25px;
        margin-left: 25px;
    }
    p {
        font-family: Cocogoose;
        text-align: justify;
        text-justify: inter-word;
        font-size: 18px;
    }
    div.vertical {
        padding-left: 50px;
        padding-right: 50px;
        flex-grow: 1;
    }
    div.horizontal {
        display: flex;
        flex-direction: row;
    }
    div.horizontal-centered {
        display: flex;
        flex-direction: row;
        width: 100%;
        justify-content: center;
        gap: 50px;
    }
    div.circle {
        position: absolute;
        z-index: -900;
        top:0;
        left:0;
        margin-left: -1000px;
        margin-top: -500px;
    }

    img.iphone {
        border: 5px solid black;
        width: 300px;
        height: 650px;
        border-radius: 30px;
        display: block;
        margin-left: 0;
        margin-right: 0;
        margin-bottom: 0px;
        padding: 0;
    }
</style>