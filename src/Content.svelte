<script>
    let screenshots = [
        "images/screen1.png",
        "images/screen2.png",
        "images/screen3.png",
        "images/screen4.png",
        "images/screen5.png",
    ];

    let staff = [
        {
            name: "Dan Salvato",
            work: "Writing,coding, music",
            links: [
                { website: "Twitter", href: "https://twitter.com/dansalvato" },
                { website: "Twitch", href: "https://twitch.tv/dansalvato" },
                { website: "YouTube", href: "https://youtube.com/dansalvato" },
            ],
        },
        {
            name: "Satchely",
            work: "Character art",
            links: [
                { website: "Twitter", href: "https://twitter.com/_satchely" },
                {
                    website: "DeviantArt",
                    href: "https://satchely.deviantart.com",
                },
            ],
        },
        {
            name: "Velinquent",
            work: "Background art",
            links: [
                { website: "Twitter", href: "https://twitter.com/VelinquenT" },
                {
                    website: "Pixiv",
                    href: "https://www.pixiv.net/users/17385446",
                },
            ],
        },
    ];
</script>

<div class="content">
    <div class="upper-content">
        <h1 id="tagline">Will you write the way into her heart?</h1>
        <div class="plus-banner">
            <div class="banner-divider" />
            <a href="https://ddlc.plus"
                ><img src="/images/plus-banner.png" alt="" /></a
            >
            <div class="banner-divider" />
            <h2>Or, check out the original game below...</h2>
        </div>
        <iframe
            id="trailer"
            src="https://www.youtube.com/embed/kB1663FTpzU?rel=0&amp;showinfo=0"
            frameborder="0"
            allowfullscreen=""
            title="Download Doki Doki Literature Club! Trailer"
        />
        <div class="download-widget">
            <iframe
                frameborder="0"
                src="https://itch.io/embed/106599?border_width=5&amp;fg_color=000&amp;link_color=bb5599&amp;border_color=ffbde1"
                width="560"
                height="175"
                title="Download Doki Doki Literature Club!"
            />
        </div>
    </div>
    <div class="lower-content">
        <div class="banner-divider" />
        <div class="promo-container">
            <span class="promo" style="top: -53.912px;" />
        </div>
        <div class="banner-divider" />
        <div class="description-container">
            <div class="description-container-left">
                <h2>Hi, Monika here!</h2>
                <p>
                    Welcome to the Literature Club! It's always been a dream of
                    mine to make something special out of the things I love. Now
                    that you're a club member, you can help me make that dream
                    come true in this cute game!
                </p>
                <p>
                    Every day is full of chit-chat and fun activities with all
                    of my adorable and unique club members:
                </p>
                <p>
                    <strong>Sayori</strong>, the youthful bundle of sunshine who
                    values happiness the most;<br />
                    <strong>Natsuki</strong>, the deceivingly cute girl who
                    packs an assertive punch;<br />
                    <strong>Yuri</strong>, the timid and mysterious one who
                    finds comfort in the world of books;<br />
                    ...And, of course, <strong>Monika</strong>, the leader of
                    the club! That's me!
                </p>
                <p>
                    I'm super excited for you to make friends with everyone and
                    help the Literature Club become a more intimate place for
                    all my members. But I can tell already that you're a
                    sweetheart—will you promise to spend the most time with me?
                    ♥
                </p>
                <hr />
                <a href="https://ddlcstore.com" target="_blank"
                    ><img src="/images/store_banner.png" alt="" /></a
                >
                <h2>DDLC Fan Pack</h2>
                <p>
                    <strong>Doki Doki Literature Club</strong> is 100% free to
                    play, but you are welcome to contribute any amount you'd
                    like. Contributing $10 or more will reward you with the
                    <strong>DDLC Fan Pack</strong>!
                </p>
                <p>
                    Just click the <strong>Download</strong> button and contribute
                    a payment of $10 or more to unlock the Fan Pack.
                </p>
                <h3>What You Get</h3>
                <ul>
                    <li>
                        The complete <strong>DDLC Official Soundtrack</strong> with
                        24 tracks, including remixes, bonus tracks, sketches, and
                        song variants not included in the game
                    </li>
                    <li>
                        <strong>High-resolution wallpapers</strong> of in-game art
                        for desktop and mobile
                    </li>
                    <li>
                        <strong>DDLC Concept Art Booklet</strong> which includes
                        concept art and developer notes, providing insight into early
                        stages of development
                    </li>
                    <li>Our gratitude for helping us make more great games!</li>
                </ul>
                <hr />
                <h2>The Team</h2>
                <p>
                    <strong>Doki Doki Literature Club</strong> was developed by
                    <a href="https://twitter.com/TeamSalvato" target="_blank"
                        >Team Salvato</a
                    >. Our team is constantly working on bigger and better
                    projects—any generous contributions or merchandise sales
                    will go right towards making our future games more awesome!
                </p>
                <h3>DDLC Staff</h3>
                {#each staff as member, i}
                    <p>
                        <strong>{member.name}</strong
                        >&nbsp;-&nbsp;{member.work}<br />
                        {#each staff[i].links as link, j}
                            {#if j < staff[i].links.length - 1}
                                <a href={link.href} target="_blank"
                                    >{link.website}</a
                                >&nbsp;-&nbsp;
                            {:else}
                                <a href={link.href} target="_blank"
                                    >{link.website}</a
                                >
                            {/if}
                        {/each}
                    </p>
                {/each}
                <hr />

                <h3 class="text-center">
                    This game is not suitable for children<br />or those who are
                    easily disturbed.
                </h3>
            </div>
            <div class="description-container-right">
                {#each screenshots as screenshot}
                    <a href={screenshot} data-lightbox="screenshots"
                        ><img src={screenshot} alt="" /></a
                    >
                {/each}
            </div>
        </div>
    </div>
</div>

<style>
    .content {
        width: 960px;
        height: inherit;
        margin: 0px auto;
        background: #fff;
        text-align: center;
        border-style: solid;
        border-color: #fff;
        border-width: 40px 0px 0px 0px;
        box-shadow: 0px 0px 15px rgba(0, 0, 0, 0.3);
    }

    .upper-content {
        display: block;
        min-height: 100vh;
        padding-bottom: 200px;
    }

    #tagline {
        display: block;
        font-family: "Annie Use Your Telescope", cursive;
        margin: auto;
        text-align: center;
        font-size: 2em;
        margin-block-start: 1em;
        margin-block-end: 2em;
        margin-inline-start: 0px;
        margin-inline-end: 0px;
        font-weight: bold;
    }

    #trailer {
        width: 960px;
        height: 540px;
    }

    .download-widget {
        margin-top: 30px;
    }

    .plus-banner {
        display: block;
        min-height: 100vh;
    }

    .plus-banner h2 {
        margin-top: 120px;
    }

    .plus-banner img {
        display: block;
    }

    .banner-divider {
        position: relative;
        background: #ffbde1;
        height: 40px;
    }

    @font-face {
        font-family: "Annie Use Your Telescope";
        src: url("/fonts/AnnieUseYourTelescope-Regular/AnnieUseYourTelescope-Regular.ttf");
    }

    .promo-container {
        height: 428px;
        margin-top: -40px;
    }

    .promo {
        position: relative;
        display: block;
        height: 640px;
        background: url("/images/promo.png") top no-repeat;
    }

    .text-center {
        text-align: center;
    }

    .description-container {
        position: relative;
        padding: 20px 0px 200px 20px;
        min-height: 800px;
        background: #fff;
        text-align: left;
    }

    .description-container a {
        color: #bb5599;
    }

    .description-container-left {
        display: inline-block;
        vertical-align: top;
        width: 552px;
        margin-right: 20px;
    }

    .description-container-left h2 {
        margin: 0.5em 0;
        font-family: "Lato", sans-serif;
    }

    .description-container-left h3 {
        margin: 0.5em 0;
        font-family: "Lato", sans-serif;
        font-size: 1.17em;
    }

    .description-container-right {
        float: right;
        width: 347px;
    }

    .description-container-right img {
        display: block;
        margin-bottom: 10px;
        max-width: 100%;
    }

    .description-container p {
        line-height: 1.4;
        display: block;
        -webkit-margin-before: 1em;
        -webkit-margin-after: 1em;
        -webkit-margin-start: 0px;
        -webkit-margin-end: 0px;
    }

    .description-container hr {
        margin: 1em 0;
        border: 0;
        height: 1px;
        background: #dadada;
    }

    .description-container ul {
        line-height: 1.4;
        padding-left: 2em;
    }
</style>
