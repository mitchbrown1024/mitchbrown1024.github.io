<script>
	import BackgroundCircle from "$lib/components/background_circle.svelte";
    import NameTitle from "$lib/components/name_title.svelte";
</script>

<div class="horizontal">
    <div>
        <div class="circle"><BackgroundCircle color="#0496FF"></BackgroundCircle></div>
        <NameTitle></NameTitle>
    </div>
    <div class="vertical">
        <img src="/my-photo.jpeg" alt="Mitch Brown">
        <h1>about me</h1>
        <p>
            As you can probably see my name is Mitch Brown, and I am a software developer based out of Vancouver.
            I am currently a student attending Simon Fraser University with my projected graduation being in 2028.
            Though my major is Computer Science as a whole it is specifically software development that I am interested
            in pursuing.
            <br>
            <br>
            Another part of computer science that interests me is the world of AI. I know, I know, everybody is interested
            in AI now but that has been my dream since I first learned what it was.
            <br>
            <br>
            My dream is to create software that benefits everyone. Software that is accessible and useful for everybody, no matter
            how much money they have. Because of this I am very interested in Open Source Software. In my ideal world every piece
            of software would be open source allowing everybody to innovate and benefit from it.
            <br>
            <br>
            Outside the world of computer science I am also an amateur singer/songwriter. I spend a lot of my free time 
            messing around on both the piano and guitar trying to come up with my next catchy melody to put in a song. Also,
            I love to hike! That's where that image up above comes from. Now, <b>BEFORE</b> you judge how I look I would just like to
            mention that it was <b>VERY</b> cold outside and my face wouldn't let me smile. Trust me, my smile is actually quite normal
            when I'm a normal temperature.
        </p>
    </div>
</div>

<style>
    div.vertical {
        padding-left: 50px;
        padding-right: 50px;
    }
    h1 {
        font-family: Cocogoose;
        font-size: 32px;
    }
    p {
        font-family: Cocogoose;
        text-align: justify;
        text-justify: inter-word;
    }
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
    
    img {
        width: 500px;
        height: 300px;
        object-fit: cover;
        border-radius: 20px;
        display: block;
        margin-left: auto;
        margin-right: auto;
    }
</style>