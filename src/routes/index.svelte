<svelte:head>
    <title>SvelteKit Tutorial</title>
</svelte:head>
<main>
    <h1>SvelteKit Tutorial</h1>
    <picture>
        <source type="image/webp" srcset="evolution-js.webp">  
        <img src="evolution-js.png" alt="Evolution of frontend">
    </picture>
    
    <article>
        <h2>Om denna sida</h2>
        <p>Sidan används och utvecklas i samband med en utbildning i SvelteKit</p>
        <p>Förhoppningsvis blir sidan så småningom en permanent utbildningssida.</p>
    </article>
</main>

<style>
    picture {
        display: inline-block;
        background-color:aliceblue;
        padding: 2rem;
    }

    img {
        width: 100%;
        max-width: 800px;
    }
</style>

