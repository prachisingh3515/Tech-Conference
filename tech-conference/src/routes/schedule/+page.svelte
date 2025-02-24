<script>
    import "../../lib/styles.css";
    import "./schedule.css"
    import { writable } from 'svelte/store';

    const selectedDay = writable("Monday");

    const schedule = {
        "Monday": [
            { time: "10:00 AM", topic: "AI in 2025", speaker: "Alice Johnson", date: "March 10, 2025" },
            { time: "11:30 AM", topic: "Cloud Security", speaker: "Bob Williams", date: "March 10, 2025" },
            
        ],
        "Tuesday": [
            { time: "10:00 AM", topic: "Quantum Computing", speaker: "Jane Doe", date: "March 11, 2025" },
            { time: "11:30 AM", topic: "Cybersecurity Trends", speaker: "John Smith", date: "March 11, 2025" },
            { time: "2:00 PM", topic: "Blockchain & NFTs", speaker: "Evelyn Carter", date: "March 11, 2025" },
        ],
        "Wednesday": [
            { time: "10:00 AM", topic: "UI/UX Design Principles", speaker: "Grace Thompson", date: "March 12, 2025" },
            { time: "3:30 PM", topic: "DevOps in 2025", speaker: "James Wilson", date: "March 12, 2025" }
        ],
        "Thursday": [
            { time: "10:00 AM", topic: "Edge Computing", speaker: "Alice Johnson", date: "March 13, 2025" },
            { time: "11:30 AM", topic: "5G and IoT", speaker: "Bob Williams", date: "March 13, 2025" },
            { time: "2:00 PM", topic: "Cyber Resilience", speaker: "Carla Brown", date: "March 13, 2025" },
            { time: "3:30 PM", topic: "Smart Cities and AI", speaker: "David Smith", date: "March 13, 2025" }
        ],
        "Friday": [
            { time: "10:00 AM", topic: "The Rise of AR/VR", speaker: "Jane Doe", date: "March 14, 2025" },
            { time: "11:30 AM", topic: "Ethical AI", speaker: "John Smith", date: "March 14, 2025" },
            { time: "3:30 PM", topic: "AI-Generated Content", speaker: "Frank Lee", date: "March 14, 2025" }
        ],
        "Saturday": [
            { time: "10:00 AM", topic: "E-commerce Innovations", speaker: "Grace Thompson", date: "March 15, 2025" },
            { time: "11:30 AM", topic: "Serverless Computing", speaker: "Henry White", date: "March 15, 2025" },
            { time: "2:00 PM", topic: "Sustainable Tech", speaker: "Isabella Moore", date: "March 15, 2025" },
            { time: "3:30 PM", topic: "Cybersecurity in AI", speaker: "James Wilson", date: "March 15, 2025" },
            { time: "11:30 AM", topic: "Mobile App Development", speaker: "Henry White", date: "March 12, 2025" },
            { time: "2:00 PM", topic: "AI in Healthcare", speaker: "Isabella Moore", date: "March 12, 2025" },
        ],
        "Sunday": [
            { time: "10:00 AM", topic: "AI-Powered Chatbots", speaker: "Alice Johnson", date: "March 16, 2025" },
            { time: "11:30 AM", topic: "Cloud-Native Development", speaker: "Bob Williams", date: "March 16, 2025" },
            { time: "2:00 PM", topic: "Big Data Analytics", speaker: "Carla Brown", date: "March 16, 2025" },
            { time: "3:30 PM", topic: "Tech Leadership", speaker: "David Smith", date: "March 16, 2025" },
            { time: "2:00 PM", topic: "Ethical Hacking", speaker: "Carla Brown", date: "March 10, 2025" },
            { time: "3:30 PM", topic: "The Future of Web 3.0", speaker: "David Smith", date: "March 10, 2025" },
            { time: "2:00 PM", topic: "Quantum Cryptography", speaker: "Evelyn Carter", date: "March 14, 2025" }
        ]
    };
</script>

<section class="schedule">
    <h1>Conference Schedule</h1>
    <p class="description">Explore the agenda and plan your sessions.</p>

    <div class="tabs">
        {#each Object.keys(schedule) as day}
            <button class:active={$selectedDay === day} on:click={() => selectedDay.set(day)}>
                {day}
            </button>
        {/each}
    </div>

    <table>
        <thead>
            <tr>
                <th>Time</th>
                <th>Topic</th>
                <th>Speaker</th>
                <th>Date</th>
            </tr>
        </thead>
        <tbody>
            {#each schedule[$selectedDay] as session}
                <tr>
                    <td>{session.time}</td>
                    <td>{session.topic}</td>
                    <td>{session.speaker}</td>
                    <td>{session.date}</td>
                </tr>
            {/each}
        </tbody>
    </table>
</section>

