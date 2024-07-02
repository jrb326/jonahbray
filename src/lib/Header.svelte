<script>
    import {onMount} from "svelte";

    let isResume = false;


    onMount(() => {
        let stickyOffset = document.body.scrollHeight;


        if (window.location.pathname === '/') {
            if (window.scrollY < 300) {
                isResume = true;
            }

            stickyOffset = document.querySelector("#sticky").offsetTop + 5;
            console.log(stickyOffset)
        }

        window.addEventListener('scroll', () => {
            let scroll = window.scrollY;
            if (window.location.pathname === '/') {

                if (scroll < 300) {
                    isResume = true;
                }

                let elem = document.querySelector('.links');
                if( elem == null ) return;
                /** @type {HTMLElement} */
                let links = elem;
                if (scroll >= stickyOffset) {
                    // sticky the nav buttons
                    // links.style.animation = 'dropin 2s';
                    links.style.position = 'fixed';
                    links.style.backgroundColor = 'rgba(27,25,20,0.41)';
                    links.style.backdropFilter = 'blur(8px)';
                    links.style.width = "100%";
                    links.style.margin = "0";
                    links.style.top = "0";
                    links.style.zIndex = "1000";
                    links.style.left = "50%";
                    links.style.transform = "translateX(calc(-50%))";


                } else {
                    // un-sticky the nav buttons
                    links.style.position = 'absolute';
                    links.style.backgroundColor = 'inherit';
                    links.style.backdropFilter = 'none';
                    links.style.width = "auto";
                    links.style.top = "inherit";
                    links.style.zIndex = "inherit";
                    links.style.left = "50%";
                    links.style.transform = "translateX(calc(-50% + 1.5em)";
                    links.style.animation = "none";
                    links.style.margin = "1em 0 1em 0";
                }
            }
        });

    });

</script>


<header class="header">
    <nav class="navbar">
        <div class="logo">
            <a href="/">
                <img src="logo.png" alt="logo"/>
            </a>
        </div>
        <div class="wrap">
            <ul class="links">
                <li>
                    <div class="link">
                        <sup>01</sup>
                        <a href="/#hero-section">//: home</a>
                    </div>
                </li>
                <li>
                    <div class="link">
                        <sup>02</sup>
                        <a href="/#expertise">//: expertise</a>
                    </div>
                </li>
                <li>
                    <div class="link">
                        <sup>03</sup>
                        <a href="/#work">//: work</a>
                    </div>

                </li>
                <li>
                    <div class="link">
                        <sup>04</sup>
                        <a href="/#experience">//: experience</a>
                    </div>

                </li>
                <li>
                    <div class="link">
                        <sup>05</sup>
                        <a href="/#contact">//: contact</a>
                    </div>

                </li>
            </ul>
        </div>
    </nav>
</header>


<style>

    .header {
        position: relative;
    }

    .wrap {
        width: 100%;
        height: 100%;
    }

    .resume {
        width: 40px;
        height: 40px;
        display: flex;
        justify-content: center;
        align-items: center;
        margin: 1em;

    }

    .links {
        display: flex;
        position: absolute;
        justify-content: center;
        align-items: center;
        list-style: none;
        padding: 0;
        left: 50%;
        transform: translateX(calc(-50% + 1.5em));
    }

    .logo {
        max-height: 40px;
        max-width: 182px;
        width: 100%;
        height: 100%;
        flex-basis: 182px;
        align-self: center;
        justify-content: center;
        margin-left: 1em;
    }

    .navbar {
        display: flex;
        flex-direction: row;
        justify-content: space-between;
    }

    .link {
        display: flex;
        justify-content: center;
        align-items: center;
        flex-direction: column;
        margin: 0 1.5rem 0 0;
    }

    .link > a, .link > sup {
        color: #1cff6b;
        font-family: "Poppins", sans-serif;
    }

    .link a {
        text-decoration: none;
    }

    .link:hover a, .link:hover sup {
        color: #1cff6b;
    }

    .links .link:hover a, .links .link:hover sup {
        color: #1cff6b;
        transition: none;
    }

    .links:hover a, .links:hover sup {
        color: rgba(28, 255, 107, 0.51);
        transition: color 0.3s ease-in-out;
    }

    .link > sup {
        align-self: flex-end;
    }
</style>