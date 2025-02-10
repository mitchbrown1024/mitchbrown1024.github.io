<script>
	let { children } = $props();
    let icon_size = 48;
	import { page } from '$app/state';
	import { onMount } from 'svelte';
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
        <div class="icons">
            <Github size={icon_size}></Github>
            <Instagram size={icon_size}></Instagram>
            <LinkedIn size={icon_size}></LinkedIn>
        </div>
    </div>
</div>

<style>
    @font-face {
        font-family: Cocogoose;
        font-style: normal;
        font-display: swap;
        font-weight: bold;
        src: url(/fonts/cocogoose.ttf) format("truetype");
    }

    @font-face {
        font-family: Cocogoose;
        font-style: normal;
        font-display: swap;
        font-weight: lighter;
        src: url(/fonts/cocogoose-thin.ttf) format("truetype");
    }

	ul {
		display: flex;
		list-style-type: none;
		font-family: Cocogoose;
		font-weight: lighter;
        padding-left:15px;
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
        color: grey;
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
        padding-top:0;
        padding-left: 30px;
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

    div.empty {
        height: 20px;
    }

    :global(body) { /* this will apply to <body> */ margin: 0; padding: 0; }

</style>