<script>
    let { color } = $props();
</script>

<span class="circle" style="--color: {color}"></span>

<style>
    span.circle {
        height: 2000px;
        width: 2000px;
        background: radial-gradient(var(--color) 700px, rgba(255, 255, 255, 0) 1250px);
        display: inline-block;
        filter: blur(100px);
    }
</style>