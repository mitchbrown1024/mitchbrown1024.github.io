<script>
	let { children } = $props();
	import { page } from '$app/state';
</script>

<div class="parent">
        <div class="line"></div>
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
		font-size: 16px;
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
        height: 70vh;
        position: relative;
        top: 0;
        width: 4px;
        border-radius: 2.5px;
    }

    div.parent {
        display: inline-flex;
    }
    div.content {
        padding-left: 20px;
    }

</style>