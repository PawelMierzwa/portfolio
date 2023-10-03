<template>
    <div>
        <div id="projects">
            <h2>My Projects</h2>
            <ul id="project-list">
                <li class="project-object">
                    <a href="https://github.com/PawelMierzwa/MiniBattleships">
                        <div id="mb" class="project">
                            <p>Mini Battleships</p>
                        </div>
                    </a>
                </li>
                <li class="project-object">
                    <a href="https://github.com/PawelMierzwa/LoudaBot">
                        <div id="lb" class="project">
                            <p>Louda Bot</p>
                        </div>
                    </a>
                </li>
                <li class="project-object">
                    <a href="https://github.com/PawelMierzwa/RChat">
                        <div id="rc" class="project">
                            <p>Rated Chat</p>
                        </div>
                    </a>
                </li>
                <li class="project-object">
                    <a href="https://github.com/PawelMierzwa/sigma-tools">
                        <div id="st" class="project">
                            <p>Sigma Tools</p>
                        </div>
                    </a>
                </li>
            </ul>
        </div>
        <div id="contact">
            <h2>Contact</h2>
            <ul id="about-links">
                <li>
                    <a href="https://www.linkedin.com/in/paweł-mierzwa/">
                        <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 16 16" role="img"
                            aria-labelledby="LinkedinIcoTitle" fill="#362e2b" class="ico">
                            <title id="LinkedinIcoTitle">My LinkedIn</title>
                            <path stroke="none"
                                d="M14.8 0H1.2C.5 0 0 .5 0 1.2v13.7c0 .6.5 1.1 1.2 1.1h13.6c.7 0 1.2-.5 1.2-1.2V1.2c0-.7-.5-1.2-1.2-1.2zM4.7 13.6H2.4V6h2.4v7.6zM3.6 5c-.8 0-1.4-.7-1.4-1.4 0-.8.6-1.4 1.4-1.4.8 0 1.4.6 1.4 1.4-.1.7-.7 1.4-1.4 1.4zm10 8.6h-2.4V9.9c0-.9 0-2-1.2-2s-1.4 1-1.4 2v3.8H6.2V6h2.3v1c.3-.6 1.1-1.2 2.2-1.2 2.4 0 2.8 1.6 2.8 3.6v4.2z">
                            </path>
                        </svg>
                    </a>
                </li>
                <li>
                    <a href="https://github.com/pawelmierzwa/">
                        <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 16 16" role="img"
                            aria-labelledby="GithubIcoTitle" fill="#362e2b" class="ico">
                            <title id="GithubIcoTitle">My GitHub</title>
                            <path stroke="none" fill-rule="evenodd"
                                d="M8 0C3.6 0 0 3.6 0 8c0 3.5 2.3 6.5 5.5 7.6.4.1.5-.2.5-.4v-1.4c-2.2.5-2.7-1.1-2.7-1.1-.4-.9-.9-1.2-.9-1.2-.7-.5.1-.5.1-.5.8.1 1.2.8 1.2.8.7 1.2 1.9.9 2.3.7.1-.5.3-.9.5-1.1-1.8-.2-3.6-.9-3.6-4 0-.9.3-1.6.8-2.1-.1-.2-.4-1 .1-2.1 0 0 .7-.2 2.2.8.6 0 1.3-.1 2-.1s1.4.1 2 .3c1.5-1 2.2-.8 2.2-.8.4 1.1.2 1.9.1 2.1.5.6.8 1.3.8 2.1 0 3.1-1.9 3.7-3.7 3.9.3.3.6.8.6 1.5v2.2c0 .2.1.5.6.4C13.7 14.5 16 11.5 16 8c0-4.4-3.6-8-8-8z"
                                clip-rule="evenodd"></path>
                        </svg>
                    </a>
                </li>
                <li>
                    <a href="mailto:pawelmierzwa44@gmail.com">
                        <svg xmlns="http://www.w3.org/2000/svg" fill="#362e2b" viewBox="0 0 24 24" class="ico">
                            <g id="SVGRepo_bgCarrier" stroke-width="0"></g>
                            <g id="SVGRepo_tracerCarrier" stroke-linecap="round" stroke-linejoin="round"></g>
                            <g id="SVGRepo_iconCarrier">
                                <path
                                    d="M20 4H4c-1.1 0-1.99.9-1.99 2L2 18c0 1.1.9 2 2 2h16c1.1 0 2-.9 2-2V6c0-1.1-.9-2-2-2zm0 4l-8 5-8-5V6l8 5 8-5v2z">
                                </path>
                            </g>
                        </svg>
                    </a>
                </li>
            </ul>
            <a href="./assets/cv_pawel_mierzwa_en.pdf" id="download-cv">
                Download my CV
            </a>
        </div>
        <footer>
            <span id="footer-text" data-descr="Made with Vue.js 3"></span>
        </footer>
    </div>
</template>

<script>
export default {

}
</script>

<style>
#projects {
    font-size: 200%;
    padding-top: 5%;
    padding-left: 5%;
    text-align: left;
    width: 100%;
    color: #362e2b;
    mix-blend-mode: hard-light;
}

#projects #project-list {
    display: flex;
    align-items: center;
    list-style: none;
    margin: 0;
    padding-inline-start: 0;
    border: #362e2b;
    border-style: none none double;
    width: fit-content;
}

#project-list .project-object a {
    color: #362e2b;
}

#project-list .project-object a:hover {
    color: #000000;
    text-decoration: none;
}

#project-list .project-object {
    padding-right: 30px;
}

#project-list .project {
    display: flex;
    height: 200px;
    width: 300px;
    text-align: left;
}

#project-list .project p {
    align-self: flex-end;
    line-height: 40px;
}

#contact {
    text-align: left;
    padding-left: 5%;
    font-size: 200%;
    width: 100%;
    height: 40vh;
    color: #362e2b;
    mix-blend-mode: hard-light;
}

#contact a#download-cv {
    font-size: large;
    line-height: 2rem;
    border: #362e2b 5px solid;
    color: #362e2b;
    font-weight: bolder;
    border-radius: 3rem;
    height: 2rem;
    padding: 0.5rem 1rem 0.5rem 1rem;
}

#contact a#download-cv:hover {
    background-color: #362e2b;
    color: #a88f78;
}

#about-links {
    display: flex;
    align-items: center;
    list-style: none;
    padding-inline-start: 0;
    margin-top: 10px;
    margin-bottom: 10px;
}

#about-links li {
    padding: 10px 4px 10px 4px;
    flex: 0 0 auto;
    overflow: visible;
    width: 2rem;
    height: 2rem;
    stroke-width: 2px;
    transition: all .4s ease-out;
}

.ico:hover {
    fill: #000000;
}

footer {
    text-align: center;
    padding-top: 5vh;
    position: relative;
    width: 100%;
    height: 40px;
    font-weight: bold;
    font-size: large;
    mix-blend-mode: difference;
}

#footer-text::before {
    content: 'Made with 🖤 by cnsh';
}

footer:hover #footer-text::before {
    content: "";
}

footer:hover #footer-text::after {
    line-height: 25px;
    font-size: large;
    padding-top: 5px;
    content: attr(data-descr);
}

a {
    text-decoration: none;
    color: grey;
}

a:hover {
    text-decoration: underline;
    color: rgb(100, 100, 100);
}
</style>