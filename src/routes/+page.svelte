<script>

    import Header from "$lib/Header.svelte";
    import SkillCarousel from "$lib/SkillCarousel.svelte";
    import ExperienceTimeline from "$lib/ExperienceTimeline.svelte";
    import ContactForm from "$lib/ContactForm.svelte";
    import WorkGallery from "$lib/WorkGallery.svelte";
    import Socials from "$lib/Socials.svelte";
</script>

<div class="page">
    <div class="hero-background">
        <Header/>
        <section id="hero-section" class="landing">
            <h1>Jonah Bray</h1>
            <p id="sticky">Software Engineer, Backend Developer.</p>
        </section>
    </div>

    <section id="expertise" class="landing">
        <h1>Work In Progress</h1>
        <p>I appreciate your interest in my portfolio.</p>

        <p style="margin-top: 50px; font-family: 'Roboto', sans-serif; text-transform: none; font-weight: 100">
            I am currently still working on making this website, but please feel free to reach out to me at my
        </p>

        <p style="margin-top: 0px; font-family: 'Roboto', sans-serif; text-transform: none; font-weight: 100">
            <a style="color: #1cff6b" href="https://www.linkedin.com/in/jonah-bray-587b83244">LinkedIn</a>, <a style="color: #1cff6b" href="https://github.com/jrb326">Github</a>, Email, or Phone Number that is listed on my resume.
        </p>
<!--        <SkillCarousel />-->
    </section>
<!--    <section id="work">-->
<!--        <WorkGallery />-->
<!--    </section>-->
<!--    <section id="experience">-->
<!--        <ExperienceTimeline />-->
<!--    </section>-->
<!--    <section id="contact">-->
<!--        <ContactForm />-->
<!--        <Socials />-->
<!--    </section>-->

</div>


<style>

    :global(body) {
        margin: 0;
        padding: 0;
    }

    .page {
        background-color: rgb(27, 25, 20);
    }

    .hero-background {
        background-image: url("/bkg.jpg");
        background-size: cover;
        background-position: center;
        height: 100dvh;
        width: 100%;
        position: relative;
        z-index: 2;
    }

    .landing {
        display: flex;
        justify-content: center;
        align-items: center;
        height: 100dvh;
        flex-direction: column;
        text-transform: uppercase;

    }

    .landing h1 {
        font-size: 6rem;
        font-weight: 700;
        font-family: "Poppins", sans-serif;
        margin: 0 auto;
        color: white;
    }

    .landing p {
        font-size: 1.5rem;
        font-weight: 400;
        font-family: "Roboto Thin", sans-serif;
        color: white;
        margin: 0 auto;
    }

    #expertise {
        background-color: rgb(27, 25, 20);
        width: 100%;
        height: 100vh;
        z-index: 0;
    }

    #work {
        background-color: rgb(27, 25, 20);
        width: 100%;
        height: 100vh;
        z-index: 0;
    }

    #experience {
        background-color: rgb(27, 25, 20);
        width: 100%;
        height: 100vh;
        z-index: 0;
    }

    #contact {
        background-color: rgb(27, 25, 20);
        width: 100%;
        height: 100vh;
        z-index: 0;
    }
</style>