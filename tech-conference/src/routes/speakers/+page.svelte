<script>
    import "../../lib/styles.css";
    import "./speakers.css"

    const speakers = [
        { name: "Alice Johnson", title: "AI Researcher, OpenAI", image: "https://thumbs.dreamstime.com/b/young-confident-smiling-businesswoman-standing-office-ar-portrait-modern-interior-arms-crossed-looking-camera-great-91929117.jpg", bio: "Alice is a leading AI researcher at OpenAI, specializing in machine learning and neural networks." },
        { name: "Bob Williams", title: "Cloud Architect, AWS", image: "https://media.gettyimages.com/id/1354898581/photo/shot-of-a-young-businessman-using-a-laptop-in-a-modern-office.jpg?s=612x612&w=gi&k=20&c=v7Lt9TKgpUX24eVZOSJcZ2Xlpn4U0u_4pjae_vDe4Xc=", bio: "Bob is an expert in cloud computing, working with AWS to design scalable and secure cloud solutions." },
        { name: "Carla Brown", title: "Cybersecurity Expert, CyberSafe", image: "https://media.istockphoto.com/id/1386217759/photo/portrait-of-a-confident-young-businesswoman-standing-against-an-urban-background.jpg?s=612x612&w=0&k=20&c=fAzBj4UAksz3wwAjXxKxByZMqDSuqQZSTij7jBiPtJc=", bio: "Carla has over 15 years of experience in cybersecurity, focusing on ethical hacking and data protection." },
        { name: "David Smith", title: "CTO, FutureTech", image: "https://media.istockphoto.com/id/1366857153/photo/portrait-of-dreamy-young-black-man-looking-at-infinity-in-a-park.jpg?s=612x612&w=0&k=20&c=HL3lvJBWtgmBFgpYySbYdlTcprPvufSvxKrlHGMi7HE=", bio: "David is a visionary in emerging tech trends, leading FutureTech’s innovations in software development." },
        { name: "Evelyn Carter", title: "Blockchain Developer, CryptoNet", image: "https://imgv3.fotor.com/images/blog-richtext-image/female-professional-corporate-headshots.png", bio: "Evelyn has contributed to several blockchain projects and is a strong advocate for decentralization." },
        { name: "Frank Lee", title: "Data Scientist, DataX", image: "https://www.shutterstock.com/image-photo/confident-young-professional-working-on-260nw-2492527961.jpg", bio: "Frank is a data analytics expert, using AI-driven insights to shape business strategies." },
        { name: "Grace Thompson", title: "Product Manager, Google", image: "https://headshots-inc.com/wp-content/uploads/2020/11/Professional-Headshot-Poses-Blog-Post.jpg", bio: "Grace has led multiple product launches at Google, blending innovation with user experience." },
        { name: "Henry White", title: "Full Stack Developer, Meta", image: "https://sb.kaleidousercontent.com/67418/1672x1018/6463a5af0d/screenshot-2022-05-24-at-15-22-28.png", bio: "Henry specializes in building scalable web applications and optimizing front-end performance." },
        { name: "Isabella Moore", title: "Robotics Engineer, Tesla", image: "https://media.istockphoto.com/id/1371934584/photo/portrait-of-a-confident-mature-businesswoman-working-in-a-modern-office.jpg?s=612x612&w=0&k=20&c=NF_IO6IEXY3HifRIhRqP0KDFJFdlFwaMwo3zfOOvKnQ=", bio: "Isabella works on AI-powered robotics for Tesla’s automation systems." },
        { name: "James Wilson", title: "DevOps Engineer, Microsoft", image: "https://media.istockphoto.com/id/1360063450/photo/headshot-profile-picture-young-businessman-sit-in-kitchen-webcam-view.jpg?s=612x612&w=0&k=20&c=6DoR9bff-RQ5N31LV_tQPsj_hT1HPxGAIn07mLkLxgc=", bio: "James integrates automation and infrastructure management to enhance software delivery pipelines." }
    ];
</script>

<section class="speakers">
    <h1>Meet Our Expert Speakers</h1>
    <p class="description">
        Learn from industry leaders, innovators, and tech pioneers as they share their insights on the future of technology.
    </p>

    <div class="grid">
        {#each speakers as speaker}
            <div class="card">
                <div class="img-container">
                    <img src={speaker.image} alt={speaker.name} />
                </div>
                <div class="card-content">
                    <h3>{speaker.name}</h3>
                    <p>{speaker.title}</p>
                    <p class="bio">{speaker.bio}</p>
                </div>
            </div>
        {/each}
    </div>
</section>
