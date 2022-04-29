<footer>
    <div>
        <a rel="license" href="http://creativecommons.org/licenses/by-nc/4.0/">
        <img alt="Creative Commons-licens" src="https://i.creativecommons.org/l/by-nc/4.0/88x31.png" /></a>
        <p>
            Detta verk är licensierat under en <br><a rel="license" href="http://creativecommons.org/licenses/by-nc/4.0/">Creative Commons Erkännande-IckeKommersiell 4.0 Internationell Licens</a>.
        </p>
    </div>
    <p>
        Kontakt: Henrik Bygren<br>&lt;henrik.bygren@engelholm.se&gt;
    </p>
</footer>

<style lang="scss">
    footer {
        box-sizing: border-box;
        display: flex;
        justify-content: space-between;
        background-color: #333333;
        border-top: 2px solid #ff3e00;  
        color: #e2e3db;  
        position: fixed;
        bottom: 0;
        width: 100vw;
        font-size: 1.2rem;
        padding: 0.6rem 4rem;

        div {
            display: flex;
            p {
                margin-left: 3rem;
            }

            a {
                color: #fff;
                text-decoration: none;
            }

            img{
                border-width:0;
            }
        }
    }  

    @media only screen and (max-width: 768px) {
        footer{
            padding: 0.4rem var(--margin-m);   

            p{
                margin-left: 1rem;
                font-size: 1rem;
            }

            div {
                p{
                    display: none;
                }

                img{
                    height: 25px;
                }
            }
        }

    }

    @media only screen and (max-width: 768px) {
        footer{
            padding: 0.4rem var(--margin-s);   
        }
    }
    
</style>