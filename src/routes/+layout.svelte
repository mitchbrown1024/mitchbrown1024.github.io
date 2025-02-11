<script>
	let { children } = $props();
    let icon_size = 48;
    let github_color = $state("black");
    let instagram_color = $state("black");
    let linkedin_color = $state("black");
	import { page } from '$app/state';
	import Github from './github.svelte';
    import Instagram from './instagram.svelte';
    import LinkedIn from './linked-in.svelte';
    import { browser } from '$app/environment';

    let vh = $state(100);

    if(browser) {
        vh = (window.innerHeight - 100) * 0.01;
    }
</script>

<div class="parent" style="--vh: {vh}px">
    <div class="line-icons">
        <div class="horizontal">
            <div class="line" style="--offset: {icon_size / 2}px"></div>
            <div class="vertical">
                <nav>
                    <ul>
                        <li><a href="/" class:active="{page.url.pathname ==='/'}">about, </a></li>
                        <li><a href="/projects" class:active="{page.url.pathname ==='/projects'}">projects, </a></li>
                        <li><a href="/experience" class:active="{page.url.pathname ==='/experience'}">experience</a></li>
                    </ul>
                </nav>
                <div class="content">
                    {@render children()} 
                </div>
            </div>
        </div>
        <div class="empty"></div>
        <div class="icon-container">
            <button class="icon" onmouseenter={() => {
                    github_color="white";
                }}
                onmouseleave={() => {
                    github_color="black";
                }}>
                <Github size={icon_size} color={github_color}></Github>
            </button>
            <button class="icon" onmouseenter={() => {
                    instagram_color="white";
                }}
                onmouseleave={() => {
                    instagram_color="black";
                }}>
                <Instagram size={icon_size} color={instagram_color}></Instagram>
            </button>
            <button class="icon" onmouseenter={() => {
                    linkedin_color="white";
                }}
                onmouseleave={() => {
                    linkedin_color="black";
                }}>
                <LinkedIn size={icon_size} color={linkedin_color}></LinkedIn>
            </button>
        </div>
    </div>
</div>

<style>
    @font-face {
        font-family: Cocogoose;
        font-style: normal;
        font-display: block;
        font-weight: bold;
        src: url(/fonts/cocogoose.ttf) format("truetype");
    }

    @font-face {
        font-family: Cocogoose;
        font-style: normal;
        font-display: block;
        font-weight: lighter;
        src: url(/fonts/cocogoose-thin.ttf) format("truetype");
    }

    nav {
        flex-grow: 1;
    }

	ul {
		display: flex;
		list-style-type: none;
		font-family: Cocogoose;
		font-weight: lighter;
        padding-left:15px;
        margin-top:0;
	}
	a {
		color: black;
		text-decoration: none;
	}
	li {
		font-size: 20px;
		margin-right: .3em;
	}

	a.active {
		text-decoration: underline;
	}

    a:hover {
        color: white;
    }

    div.line {
        background-color: black;
        flex-grow: 100;
        position: relative;
        top: 0;
        width: 4px;
        border-radius: 2.5px;
        margin-left: var(--offset);
    }

    div.parent {
        display: inline-flex;
        margin-left: 75px;
        margin-top: 50px;
        height: calc(var(--vh, 1vh) * 100);
    }

    div.content {
        flex-grow: 10;
    }

    div.line-icons {
        display: flex;
        flex-direction: column;
        justify-content: space-between;
    }

    div.horizontal {
        display: flex;
        height: 100%;
    }
    div.icon-container {
        display: flex;
    }

    div.empty {
        height: 20px;
    }

    div.vertical {
        display: flex;
        flex-direction: column;
        justify-content: flex-start;
    }
    button.icon {
        margin-right: 15px;
        background: none;
        border: none;
        width: fit-content;
        padding: 0;
    }

    :global(body) {
        margin: 0; 
        padding: 0; 
        overflow: hidden; 
        position: fixed;
    }

</style>