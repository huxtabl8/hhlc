<script>
    let links = [
        { website: "TWITTER", href: "https://twitter.com/teamsalvato" },
        { website: "YOUTUBE", href: "https://youtube.com/teamsalvato" },
        { website: "ITCH.IO", href: "https://teamsalvato.itch.io" },
    ];
</script>

<div class="footer">
    <div class="footer-content">
        <a href="http://teamsalvato.com" target="_blank"
            ><img src="/images/tsfooter.png" alt="" /></a
        >
        <p>
            {#each links as link, i}
                {#if i < links.length - 1}
                    <a href={link.href}>{link.website}</a>&nbsp;-&nbsp;
                {:else}
                    <a href={link.href}>{link.website}</a>
                {/if}
            {/each}
        </p>
    </div>
</div>

<style>
    .footer {
        background: #222;
        height: 40px;
    }

    .footer-content {
        line-height: 40px;
        width: 960px;
        height: inherit;
        margin: auto;
        color: #fff;
    }

    .footer-content a {
        color: inherit;
        text-decoration: inherit;
    }

    .footer-content img {
        vertical-align: top;
        margin-top: 4px;
    }

    .footer-content p {
        display: block;
        float: right;
        height: 40px;
        margin: 0px;
        padding: 0px;
        font-weight: 300;
        letter-spacing: 2px;
    }
</style>
