<script>
	import BackgroundCircle from "$lib/components/background_circle.svelte";
	import MyExperience from "$lib/components/my_experience.svelte";



</script>

<div class="horizontal">
    <div>
        <div class="circle"><BackgroundCircle color=#12a312></BackgroundCircle></div>
        <MyExperience></MyExperience>
    </div>
    <div class="vertical">
        <div class="horizontal">
            <h1>IT Intern</h1>
            <h1 class="light">&nbsp;<a href="https://www.glcsolutions.ca" target="_blank">GLC Solutions</a></h1>
        </div>
        <p>
            May 2024 - Present
            <br>
            <br>
            Working as an IT Intern at GLC Solutions has really given me an insight into the world of technology. 
            During this internship I get the opportunity to work with many different clients to provide or develop
            solutions that work for them. This has given me the opportunity to see many different team aspects
            played out in real life.
        </p>
        <div class="horizontal">
            <h1>Student</h1>
            <h1 class="light">&nbsp;<a href="https://www.sfu.ca" target="_blank">Simon Fraser University</a></h1>
        </div>
        <p>
            September 2023 - Present
            <br>
            <br>
            As I mentioned in my bio I am currently a student at Simon Fraser University. I am pursuing my
            bachelor of science, majoring in computer science and plan on graduating in 2028.
        </p>
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
    h1 {
        font-family: Cocogoose;
        font-size: 32px;

    }
    h1.light {
        font-weight: lighter;
    }
    p {
        font-family: Cocogoose;
        text-align: justify;
        text-justify: inter-word;
        font-size: 18px;
        margin-top: -15px;
    }
    div.vertical {
        padding-left: 50px;
        padding-right: 50px;
        flex-grow: 1;
    }
    a {
        text-decoration: none;
        color:black;
    }
    a:hover {
        text-decoration: underline;
    }
</style>