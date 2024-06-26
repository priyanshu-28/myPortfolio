<script>
    let projects = [
        {
            name: "Descrownomics",
            designation: "Solidity, Next.js",
            date: "December 2023",
            description:
                "Devised game theory concept to minimize the risk of fraud by leveraging the power of smart contracts with utmost transparency and accountability",
        },
        {
            name: "Canteen Management System",
            designation: "HTML, CSS, Javascript, NodeJS, PostgreSQL, Express",
            date: "April 2023",
            description:
                "Built caching layer on top of the app that helped reduce latency by 500ms, using Redis stream, improvising overall 70% performance, after building the app from scratch",
        },
    ];
</script>

<section>
    <h2>Projects</h2>
    {#each projects as project}
        <div class="project">
            <h3>
                {project.name}
            </h3>
            <h4>
                <i>{project.designation}</i>
            </h4>
            <h5>
                {project.date}
            </h5>
            {#if project.name === "Descrownomics"}
                <li>{project.description}</li>
                <li>
                    Architected a blockchain-powered system, fortifying product
                    functionality against unauthorized access and data
                    tampering; bolstered user confidence and trust, resulting in
                    a 30% increase in user retention and engagement
                </li>
            {:else if project.name === "Canteen Management System"}
                <li>{project.description}</li>
            {/if}
        </div>
    {/each}
</section>

<style>
    section {
        padding: 20px;
        margin-top: -40px;
    }

    h2 {
        font-size: 2.5rem;
        display: flex;

        color: tomato;
        margin-bottom: -10px;
        border-bottom: 5px solid var(--border-color);
    }

    .project {
        border-bottom: 1px solid var(--border-color);
        padding: 20px 0;
    }

    .project h3 {
        font-size: 2.1rem;
        color: var(--highlight-color);
        margin-bottom: 10px;
        margin-top: 12px;
    }

    .project h4 {
        margin-top: 10px;
        font-size: 1.2rem;
    }

    .project h5 {
        margin-top: -10px;
        font-size: 1.1rem;
        color: gray;
    }

    .project li {
        word-spacing: 0.1cm;
        letter-spacing: 0.01cm;
        margin: 10px 0px;
        color: var(--experience-description) white;
        font-size: 1.2rem;
    }
</style>
