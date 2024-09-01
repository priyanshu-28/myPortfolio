<script>
    let socials = [
        {
            name: "LinkedIn",
            link: "https://linkedin.com/in/priyanshu-p",
        },
        {
            name: "Twitter",
            link: "https://x.com/Priyanshuu_28",
        },
        {
            name: "GitHub",
            link: "https://github.com/priyanshu-28",
        },
    ];
</script>

<footer>
    <h2>Connect with me</h2>
    <div class="socials">
        {#each socials as social}
            <a href={social.link} target="_blank" rel="noopener noreferrer"
                >{social.name}</a
            >
        {/each}
    </div>
</footer>

<style>
    footer {
        padding: 20px;
        text-align: center;
    }

    h2 {
        font-size: 2.5rem;
        color: tomato;
        margin-bottom: 20px;
    }

    .socials {
        display: flex;
        justify-content: center;
        gap: 20px;
        margin-top: 20px;
    }

    .socials a {
        color: var(--highlight-color);
        text-decoration: none;
        font-size: 1.5rem;
    }

    .socials a:hover {
        text-decoration: underline;
    }
</style>
