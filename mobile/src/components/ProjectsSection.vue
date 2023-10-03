<template>
    <section class="scrollsection" id="s2">
        <div id="projects">
            <h1>Projects</h1>
            <div id="project-list">
                <div class="list-item"><a href="https://github.com/PawelMierzwa/MiniBattleships">Mini Battleships</a></div>
                <div class="list-item"><a href="https://github.com/PawelMierzwa/LoudaBot">Louda Bot</a></div>
                <div class="list-item"><a href="https://github.com/PawelMierzwa/RChat">Rated Chat</a></div>
                <div class="list-item"><a href="https://github.com/PawelMierzwa/sigma-tools">Sigma Tools</a></div>
            </div>
        </div>
    </section>
</template>

<script>
export default {
    name: 'ProjectSection',
}
</script>

<style>
#s2 {
    height: 100vh;
    width: 100%;
    background: linear-gradient(45deg, #debd9e, black);
    background-size: 200% 200%;
    animation: animate2 12s ease infinite;
    font-size: 7.5vw;
}

#s2 h1 {
    font-weight: bolder;
    font-size: 300%;
}

#projects {
    padding-top: 10%;
    mix-blend-mode: difference;
    text-align: center;
}

#project-list {
    display: inline-block;
    list-style: none;
    padding-inline-start: 0;
    height: fit-content;
    margin-top: 5%;
}

#project-list .list-item {
    mix-blend-mode: darken;
    padding: 22px 40px 22px 40px;
    background-color: #ffffff02;
    border: 1px solid #362e2b;
    cursor: pointer;
}

#project-list :first-child {
    border-radius: 3rem 3rem 0 0;
}

#project-list :last-child {
    border-radius: 0 0 3rem 3rem;
    mix-blend-mode: difference;
}

.list-item a {
    text-decoration: none;
    color: #362e2b;
}
</style>