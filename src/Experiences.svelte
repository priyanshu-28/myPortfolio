<script>
    let projects = [
        {
            name: "Zeta(Directi)",
            designation: "Software Development Engineer",
            date: "July 2024 - Present",
            description:
                "Built Hugo sites for internal teams, created an AI chat bot, and migrated the workflow to Azure from Suite",
            link: "https://zeta.in/",
        },
        {
            name: "Juspay",
            designation: "Software Development Engineer",
            date: "February 2024 - July 2024",
            description:
                "Built, improved, and added features utilized by more than 200 companies and over 100k people using Svelte for Breeze checkout page, ensuring end to end testing and flow of data-pipelines",
            link: "https://juspay.in/",
        },
        {
            name: "Oblivious.ai",
            designation: "Software Development Engineer",
            date: "June 2023 - Decemeber 2023",
            description:
                "Collaborated with the Chief Technology Officer to orchestrate a 30% cost reduction in product development, leveraging Large Language Models for enhanced efficiency",
            link: "https://www.oblivious.com/",
        },
        {
            name: "StepWell Radio",
            designation: "Software Development Engineer",
            date: "July 2021 - February 2022",
            description:
                "Engineered and launched innovative features, overhauled UI/UX with user-centric designs, and seamlessly integrated APIs to enhance platform functionality; accelerated user engagement by 40% and slashed bounce rate by 25%",
            link: "#",
        },
    ];
</script>

<section>
    <h2>Experiences</h2>
    {#each projects as project}
        <div class="project">
            <h3>
                <a href={project.link} target="_blank" rel="noopener noreferrer"
                    >{project.name}</a
                >
            </h3>
            <h4>
                <i>{project.designation}</i>
            </h4>
            <h5>
                {project.date}
            </h5>
            {#if project.name === "Zeta(Directi)"}
                <li>{project.description}</li>
            {:else if project.name === "Juspay"}
                <li>{project.description}</li>
                <li>
                    Automated functionalities and enhanced the product
                    experience by 67% using Haskell and engineering principles
                </li>
                <li>
                    Collaborated with team peers, documented code-bases and
                    fulfilled customer requirements with 98% retention rate
                </li>
            {:else if project.name === "Oblivious.ai"}
                <li>{project.description}</li>
                <li>
                    Pioneered product build, executing data extraction of over 1
                    million web privacy policies using Beautiful Soup
                </li>
                <li>
                    Evaluated model precision employing Pinecone VectorDB in
                    tandem with OpenAI, ensuring superior accuracy metrics
                </li>
                <li>
                    Developed and implemented advanced Python algorithms that
                    optimized data analysis process, resulting in a 40%
                    reduction in processing time and improved decision-making
                    capabilities through enhanced insights and reporting
                    accuracy for Antigranular
                </li>
            {:else if project.name === "StepWell Radio"}
                <li>{project.description}</li>
                <li>
                    Simplified Libretime audio streaming platform to integrate
                    streaming facility using ReactJS and NodeJS
                </li>
            {/if}
        </div>
    {/each}
</section>

<style>
    section {
        padding: 20px;
        margin: 0 300px;
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

    .project a {
        color: var(--highlight-color);
        text-decoration: none;
    }

    .project a:hover {
        text-decoration: underline;
    }

    .project li {
        word-spacing: 0.1cm;
        letter-spacing: 0.01cm;
        margin: 10px 0px;
        color: var(--experience-description) white;
        font-size: 1.2rem;
    }
</style>
