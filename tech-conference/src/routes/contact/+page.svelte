<script>
    import "../../lib/styles.css"; 
    import "./contact.css"
</script>

<section class="contact">
    <div class="container">
        <h1 class="title">Get in Touch</h1>
        <p class="subtitle">We’d love to hear from you! Fill out the form below and we'll get back to you as soon as possible.</p>

        <form class="form">
            <div class="input">
                <label for="name">Name</label>
                <input type="text" id="name" placeholder="Your Name" required>
            </div>

            <div class="input">
                <label for="email">Email</label>
                <input type="email" id="email" placeholder="Your Email" required>
            </div>

            <div class="input">
                <label for="message">Message</label>
                <textarea id="message" rows="5" placeholder="Your Message" required></textarea>
            </div>

            <button type="submit" class="submit-btn">Send Message</button>
        </form>
    </div>
</section>
