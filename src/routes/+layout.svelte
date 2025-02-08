<script>
	let { children } = $props();
	import { page } from '$app/state';
</script>

<nav>
	<ul>
		<li><a href="/" class:active="{page.url.pathname ==='/'}">about, </a></li>
		<li><a href="/projects" class:active="{page.url.pathname ==='/projects'}">projects, </a></li>
		<li><a href="/experience" class:active="{page.url.pathname ==='/experience'}">experience</a></li>
	</ul>
</nav>

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
		list-style: none;
		font-family: Cocogoose;
		font-weight: lighter;
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

</style>

{@render children()}