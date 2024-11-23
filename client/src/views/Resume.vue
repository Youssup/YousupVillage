<script setup lang="ts">

</script>

<template>
    <div class="container">
        <div class="header">
            <h1>Yoosup Song</h1>
            <p>845-376-3639 | <a href="mailto:youssupsong@gmail.com">youssupsong@gmail.com</a> | <a
                    href="https://www.linkedin.com/in/yousupsong/">linkedin.com/in/yousupsong</a> | <a
                    href="https://github.com/Youssup">github.com/Youssup</a></p>
        </div>

        <section>
            <h2>Education</h2>
            <div class="subheading">
                <h3>State University of New York at New Paltz</h3>
                <p>August 2022 -- May 2026</p>
            </div>
            <p>Bachelor of Science in Computer Science, Minor in Music | New Paltz, NY</p>
            <ul>
                <li>Cumulative GPA: 3.8, Dean's List</li>
                <li>Relevant Coursework: Computer Science I / II / III , Assembly Language & Computer Architecture,
                    Language Processing, Object Oriented Programming, Machine Learning, Software Engineering, Web Server
                    Programming, Web & Database Programming</li>
            </ul>
        </section>

        <section>
            <h2>Experience</h2>
            <div class="subheading">
                <h3>Sales Associate</h3>
                <p>September 2023 -- Present</p>
            </div>
            <p>Club Monaco | Monroe, NY</p>
            <ul>
                <li>Recognized as "Stylist of the Week" 5 consecutive times since joining the company in recognition of
                    top sales</li>
                <li>Adapted to change, resolved customer concerns efficiently while under pressure by prioritizing tasks
                </li>
                <li>Exceeded sale goals by collaborating on display setups and sharing sales strategies, increasing
                    customer satisfaction</li>
            </ul>
        </section>

        <section>
            <h2>Projects</h2>
            <div class="subheading">
                <h3><a href="https://github.com/Youssup/BetterCalendar">Better Calendar Chrome Extension</a></h3>
                <p>Flask, Python, JavaScript, HTML, CSS</p>
            </div>
            <ul>
                <li>Developed a Chrome Extension, automating event reminders and emails based on user and event
                    locations</li>
                <li>Engineered a REST API using Flask integrating Google Calendar, Google Maps, and Geolocation APIs for
                    real-time event tracking and optimized routes, accounting for real-time traffic conditions</li>
                <li>Administered flexible event location settings allowing users to set defaults and override
                    auto-detected locations</li>
            </ul>

            <div class="subheading">
                <h3><a href="https://github.com/Youssup/SoftwareEngineering">Computation Optimizer</a></h3>
                <p>Java, JUnit, Mockito, GRPC, Bootstrap, HTML, CSS, Gradle</p>
            </div>
            <ul>
                <li>Led a team of 3 to develop a full-stack creating 3 APIs for job communication, transfer and
                    processing, and efficient computation using the Ackermann function</li>
                <li>Enhanced application performance by integrating multi-threading capabilities for concurrent
                    computations, utilized GRPC and Protocol Buffers for efficient data transfer, optimizing system
                    scalability and responsiveness</li>
                <li>Implemented Test-Driven Development (TDD) approach using JUnit and Mockito for debugging</li>
            </ul>

            <div class="subheading">
                <h3><a href="https://github.com/Youssup/WebServerProgrammingPersonal">Fitness Website</a></h3>
                <p>Vue.js, JavaScript, TypeScript, Bulma, HTML, CSS, Node.js, Vite</p>
            </div>
            <ul>
                <li>Designed a fitness site with personalized experiences, incorporating login and data management via
                    sessions</li>
                <li>Arranged role-based access control for admins, ensuring proper user access</li>
                <li>Selected Bulma framework for responsive UI (User Interface), improving application aesthetics</li>
            </ul>

            <div class="subheading">
                <h3>Data Visualization System</h3>
                <p>Python, pandas, NumPy, scikit-learn, Matplotlib</p>
            </div>
            <ul>
                <li>Created a Python Machine Learning app using pandas and NumPy for data manipulation and categorical
                    encoding</li>
                <li>Implemented data preprocessing with scikit-learn to split datasets for model accuracy evaluation
                </li>
                <li>Incorporated Matplotlib for graphical data representation, improving data presentation</li>
            </ul>
        </section>

        <section>
            <h2>Leadership</h2>
            <div class="subheading">
                <h3><a href="https://eleetcoders.com/">Computer Science Career Readiness Club</a></h3>
                <p>Vice President | August 2022 -- Present</p>
            </div>
            <ul>
                <li>Presented in-depth explanations on data structures and algorithms</li>
                <li>Organized events by communicating with various departments and collaborating with other clubs</li>
                <li>Managed executive members, increasing member engagement to cultivate a supportive and learning
                    community</li>
            </ul>
        </section>

        <section>
            <h2>Technical Skills</h2>
            <ul>
                <li><strong>Languages:</strong> Java, Python, C, C++, Assembly, HTML, CSS, JavaScript, TypeScript, SQL
                </li>
                <li><strong>Frameworks:</strong> JUnit, Mockito, Flask, Express.js, Vue.js, GRPC, Bulma, BootStrap</li>
                <li><strong>Libraries:</strong> pandas, NumPy, scikit-learn, Matplotlib</li>
                <li><strong>Developer Tools:</strong> Git, Github, Node.js, Vite, Gradle, Postman, MySQL, Azure, Google
                    Cloud</li>
            </ul>
        </section>
    </div>
</template>

<style scoped>
body {
    font-family: Arial, sans-serif;
    margin: 0;
    padding: 0;
    line-height: 1.6;
    color: #333;
}

.container {
    width: 80%;
    margin: 0 auto;
    padding: 20px;
}

.header {
    text-align: center;
    margin-bottom: 20px;
}

.header h1 {
    margin: 0;
    font-size: 2.5em;
}

.header p {
    margin: 5px 0;
}

section {
    margin-bottom: 20px;
}

section h2 {
    border-bottom: 2px solid #000;
    padding-bottom: 5px;
    margin-bottom: 10px;
}

.subheading {
    display: flex;
    justify-content: space-between;
    align-items: baseline;
}

.subheading h3 {
    margin: 0;
    font-size: 1.2em;
}

.subheading p {
    margin: 0;
    font-size: 0.9em;
}

ul {
    list-style-type: none;
    padding: 0;
}

ul li {
    margin-bottom: 10px;
}
</style>