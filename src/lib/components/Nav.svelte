<script>
    let displayMenu = 'none';
    let show = false;

    function showHide(e){
        show = !show;
        displayMenu = show? 'block' : 'none';

        if(e.target.tagName == 'A'){
            document.getElementsByClassName('active')[0].classList.remove('active');
            e.target.classList.add('active');
        }
    }

</script>

<nav>
    <button on:click={showHide} ><img src="btn-menu.svg" alt="menu btn" height="25"></button>
    <ul on:click={showHide} style="--nav-ul-display: {displayMenu}">
        <li><a class="active" href="/">Hem</a></li>
        <li><a class="" href="/course">Kurs</a></li>
        <li><a class="" href="/about">Om</a></li>
    </ul>

</nav>
<div class='blur' style="--nav-ul-display: {displayMenu}" on:click={showHide}></div>

<style lang="scss">
    div.blur{
        display: none;
        position: fixed;
        width: 100%;
        height: 100%;
        top: 5.2rem;
        left: 0;
        background: rgba(255,255,255,.8);
        z-index: 2;
        backdrop-filter: grayscale(.5) blur(2px)
    }

    nav{
        display: flex;
        color: #e2e3db;
        font-size: medium;
        justify-content: end;
        margin-right: var(--margin-l);
        z-index: 10;

        button {
            border: 0;
            background: transparent;
            display: none;
            padding: 0;
        }       

        ul {
            list-style-type: none;
            margin: 0;
            padding: 0;
            overflow: hidden;
            background-color: #333;
            display: flex;
            z-index: 100;

            li {
                background-color: #333;
                color:#e2e3db;

                &:hover:not(.active) {
                    background-color: #111;
                    color: #fff;
                }
                
                a {
                    display: block;
                    text-align: center;
                    padding: 0.8rem 1.6rem;
                    text-decoration: none;
                    font-weight: 600;
                    margin: 0;
                    color: inherit;

                    &.active {
                        background-color: #ff3e00;
                    }
                }
            }

    
        }
    }    

    @media only screen and (max-width: 768px) {
        
        nav{
            --nav-ul-display: none;
            margin-right: var(--margin-m);

            button {
                display: inline;
                cursor: pointer;
            }

            ul{
                display: var(--nav-ul-display, none);
                position: absolute;
                top: 4rem;
                width: 50%;

                li {
                    display: block;
                }       
            }
        }

        div.blur{
            display: var(--nav-ul-display, none);
        }
    }

    @media only screen and (max-width: 420px) {
        nav{
            margin-right: var(--margin-s);
        }
    }

</style>