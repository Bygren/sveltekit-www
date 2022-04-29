<script>
    import Nav from "./Nav.svelte";
</script>
    
<header>
    <img src="svelteEGY.svg" alt="loggo" height="50">
    <h1><span class="spacing"><span class="dark">SVELTE</span>KIT</span>.egyweb.se</h1>
    <Nav />
</header>
    
<style>
    header{
        display: flex;
        background-color: #333;
        border-bottom: 1px solid #ff3e00;
        padding: 4px 0;
        margin: 0;
        align-items: center;
        justify-content: space-between;
        z-index: 10;
    }   

    span.dark{
        color: #888;
    }
    span.spacing{
        letter-spacing: 0.6rem;
    }

    h1{
        color: #e2e3db;
        font-size: 2.6rem;
    }

    header img{
        margin-left: var(--margin-l);
        padding: 2px 0;
    }

        


    @media only screen and (max-width: 768px) {
        header {
            padding: 2px 0;
        }
        
        h1{
            font-size: 2.4rem;
        }

        span.spacing{
            letter-spacing: 0.5rem;
        }

        header img{
            height: 40px;
            margin-left: var(--margin-m);
        }
    }

    @media only screen and (max-width: 420px) {
        h1{
            font-size: 2rem;
        }
        span.spacing{
            letter-spacing: 0.3rem;
        }

        header img{
            margin-left: var(--margin-s);
        }

    }
</style>