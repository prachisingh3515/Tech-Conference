<script>
    import "../../lib/styles.css";
    import "./sponsors.css"

    const sponsors = {
        Gold: [
            { name: "Tech Corp", logo: "https://thumbs.dreamstime.com/b/trust-icon-handshake-business-partnership-agreement-successful-achievement-meeting-concept-vector-trust-icon-handshake-217966238.jpg", link: "https://techcorp.com" },
            { name: "InnovateX", logo: "https://thumbs.dreamstime.com/b/trust-icon-handshake-business-partnership-agreement-successful-achievement-meeting-concept-vector-trust-icon-handshake-217966238.jpg", link: "https://innovatex.com" },
            { name: "Future Labs", logo: "https://thumbs.dreamstime.com/b/trust-icon-handshake-business-partnership-agreement-successful-achievement-meeting-concept-vector-trust-icon-handshake-217966238.jpg", link: "https://futurelabs.com" },
           
        ],
        Silver: [
            { name: "Cloudify", logo: "https://thumbs.dreamstime.com/b/trust-icon-handshake-business-partnership-agreement-successful-achievement-meeting-concept-vector-trust-icon-handshake-217966238.jpg", link: "https://cloudify.com" },
            { name: "NextGen AI", logo: "https://thumbs.dreamstime.com/b/trust-icon-handshake-business-partnership-agreement-successful-achievement-meeting-concept-vector-trust-icon-handshake-217966238.jpg", link: "https://nextgenai.com" },
            { name: "SecureNet", logo: "https://thumbs.dreamstime.com/b/trust-icon-handshake-business-partnership-agreement-successful-achievement-meeting-concept-vector-trust-icon-handshake-217966238.jpg", link: "https://securenet.com" },
            { name: "CodeWorks", logo: "https://thumbs.dreamstime.com/b/trust-icon-handshake-business-partnership-agreement-successful-achievement-meeting-concept-vector-trust-icon-handshake-217966238.jpg", link: "https://codeworks.com" }
        ],
        Bronze: [
            { name: "DevTech", logo: "https://thumbs.dreamstime.com/b/trust-icon-handshake-business-partnership-agreement-successful-achievement-meeting-concept-vector-trust-icon-handshake-217966238.jpg", link: "https://devtech.com" },
            { name: "ByteForge", logo: "https://thumbs.dreamstime.com/b/trust-icon-handshake-business-partnership-agreement-successful-achievement-meeting-concept-vector-trust-icon-handshake-217966238.jpg", link: "https://byteforge.com" },
            { name: "SmartSys", logo: "https://thumbs.dreamstime.com/b/trust-icon-handshake-business-partnership-agreement-successful-achievement-meeting-concept-vector-trust-icon-handshake-217966238.jpg", link: "https://smartsys.com" }
        ]
    };
</script>

<section class="sponsors">
    <h1>Our Sponsors</h1>
    <p class="description">We extend our gratitude to the companies supporting TechConf 2025.</p>

    {#each Object.keys(sponsors) as tier}
        <div class="tier">
            <div class="tier-heading {tier.toLowerCase()}">
                 {tier} Sponsors
            </div>
            <div class="grid">
                {#each sponsors[tier] as sponsor}
                    <a href={sponsor.link} target="_blank" class="sponsor-card">
                        <img src={sponsor.logo} alt={sponsor.name} />
                        <p>{sponsor.name}</p>
                    </a>
                {/each}
            </div>
        </div>
    {/each}
</section>
