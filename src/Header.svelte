<script>
    export let name = "I'm Priyanshu Pathak";
</script>

<div class="hii">
    <header>
        <h1>{name}</h1>
        <div class="intro">Hi👋, Welcome to my tech side</div>
    </header>
</div>

<style>
    .hii {
        display: flex;
        justify-content: center;
    }
    header {
        text-align: center;
        padding-top: 40px;
    }

    h1 {
        font-size: 4.5rem;
        color: tomato;
        margin-bottom: 0;
    }

    .intro {
        font-size: 2.5rem;
        color: var(--highlight-color);
    }
</style>
