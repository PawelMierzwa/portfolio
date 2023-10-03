<template>
    <section class="scrollsection" id="s1">
        <div id="date-strip"><CurrentDate/></div>
        <div id="title">
            <h1>CNSH</h1>
            <h2>Paweł Mierzwa</h2>
            <h3>Software Engineer/<br>/Web developer</h3>
        </div>
        <div id="viewcount-strip"><ViewCounter/></div>
    </section>
</template>

<script>
import CurrentDate from './CurrentDate.vue';
import ViewCounter from './ViewCounter.vue';

export default {
    name: 'IntroductionSection',
    components: {
        CurrentDate,
        ViewCounter,
    }
}
</script>

<style>
#s1 {
    height: 100vh;
    width: 100%;
    background: linear-gradient(-45deg, black, #debd9e);
    background-size: 200% 200%;
    animation: animate 12s ease infinite;
    font-size: 7.5vw;
}

#s1 h1 {
    font-weight: bolder;
    font-size: 300%;
}

#title {
    padding-top: 30%;
    width: 100%;
    height: 40%;
    font-weight: bold;
    line-height: 9vw;
    mix-blend-mode: difference;
}

#date-strip {
    padding-top: 10px;
    font-size: 6vw;
    border-bottom: 1px double #362e2b;
    line-height: 45px;
}

#viewcount-strip {
    position: absolute;
    align-items: center;
    justify-content: center;
    bottom: 0;
    mix-blend-mode: difference;
    font-size: 5.5vw;
    width: 100%;
}
</style>