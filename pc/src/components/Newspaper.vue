<template>
    <div id="newspaper">
        <div id="header">
            <div class="header-rect" id="ai-credits">
                Articles created by Artificial Intelligence.
            </div>
            <div id="headertext">
                THE CNSH NEWS
            </div>
            <div class="header-rect" id="gobackbutton" @click="callVisibilityChange()">
                Go back to the main page
            </div>
        </div>
        <div id="info-bar">
            <div id="left-item" class="info-item">
                <ViewCounter />
            </div>
            <div id="center-item" class="info-item">
                <CurrentDate />
            </div>
            <div id="right-item" class="info-item">Free Copy, Made by cnsh</div>
        </div>
        <div id="section1-content">
            <div id="content-block-1" class="content-block">
                <div class="block-title">
                    <h1>FEATURED PROJECTS</h1>
                </div>
                <div id="cb1-subblocks" class="subblocks">
                    <div id="csb1-1" class="subblock">
                        <div class="focusable subsubblock">
                            <h2>Mini Battleships</h2>
                            Get ready to embark on an epic maritime adventure like never before with the upcoming video
                            game
                            sensation,
                            Mini Battleships. Developed by a team of gaming enthusiasts and naval history aficionados,
                            this game
                            is
                            poised to redefine the world of multiplayer strategy games. Prepare to engage in intense
                            naval warfare
                            as
                            you command your fleet of warships to outwit, outmaneuver, and ultimately sink your
                            opponents'
                            vessels.
                            <p>A New Dimension of Strategy Gaming</p>
                            "Mini Battleships" takes the classic game of Battleship to a whole new level. Gone are the
                            days of
                            pencil
                            and paper – now you'll be able to navigate the high seas, strategize, and engage in
                            explosive battles
                            right
                            from the comfort of your gaming setup. Each player is armed with a diverse array of
                            warships, each
                            with
                            its
                            unique strengths and weaknesses. From nimble destroyers to formidable battleships, you'll
                            have to
                            carefully
                            consider your fleet composition and tactics to ensure victory. <a href="" class="readmore">Read
                                More</a>
                        </div>
                    </div>
                    <div id="csb1-2" class="subblock">
                        <div class="focusable subsubblock">
                            <h2>Louda Bot</h2>
                            Multipurpose Discord bot that brings a range of features to your server. Whether you're a
                            gaming enthusiast, a community manager, or just looking to add some extra flair to your
                            server, Louda
                            has
                            got you covered. <br>
                            Louda is a Discord bot designed to make your server experience richer and more engaging.
                            Louda is
                            packed
                            with features that cater to a wide range of interests and needs.
                            From moderation and utility functions to entertainment,
                            <br>Louda can do it all.. <a href="" class="readmore">Read More.</a>
                        </div>
                        <hr class="linebreak">
                        <div class="focusable subsubblock">
                            <h2>Websites</h2>
                            Explore this intriguing assortment of recently developed open-source websites I've put
                            together for
                            you! Although the hosting for some of them may not be currently active, these digital
                            creations offer
                            a glimpse into the cutting-edge world of web design. Despite their relative freshness, these
                            websites
                            already contribute to the evolving landscape of online innovation. Feel free to <a href=""
                                class="readmore">dive in</a> and uncover
                            their contemporary charm!
                        </div>
                    </div>
                </div>
            </div>
            <div id="content-block-2" class="content-block">
                <div id="cb2-subblocks" class="subblocks">
                    <div id="csb2-1" class="subblock subsubblock " style="padding-top: 10px;">
                        <h2 style="text-align: left;">cnsh: <br>Bridging Modern Design and Classic Elegance</h2>
                        <div class="focusable">
                            In the heart of a bustling city, a talented web designer named Paweł embarked on a creative
                            journey.
                            Inspired by his love for both modern design and classic elegance, he set out to craft a
                            portfolio
                            website that would captivate visitors.
                            <p></p>

                            Paweł's homepage welcomed users with a sleek and contemporary design, showcasing his
                            proficiency in
                            the latest web trends. Clean lines and vibrant colors greeted visitors, setting the stage
                            for an
                            immersive experience.
                            <p></p>

                            The portfolio section was where Paweł's artistic genius truly shone. Each project was
                            presented as a
                            visual masterpiece, with interactive elements that engaged users on a deeper level. A simple
                            click
                            on
                            any project led to a world of creativity, making it feel like a journey through Paweł's
                            design
                            process.
                            <p></p>

                            Paweł's "About Me" page was a testament to his minimalist yet captivating style. A
                            professional
                            photograph and a concise bio gave visitors a glimpse into the person behind the pixels,
                            creating a
                            sense of connection.
                        </div>
                    </div>
                    <div id="csb2-2" class="subblock subsubblock focusable" style="padding-top: 10px;">

                        The contact page, designed with user-friendliness in mind, allowed visitors to easily reach out
                        to
                        Paweł. It was a seamless fusion of modern technology and timeless accessibility.
                        <p></p>

                        Upon the website's launch, Paweł received accolades for his ability to seamlessly blend modern
                        design
                        with classic elegance. His portfolio was a testament to his creative prowess, showcasing the
                        power of
                        innovation and artistic vision in the digital age. Paweł's website left an indelible mark,
                        proving
                        that timeless elegance and contemporary design could coexist harmoniously.
                        <p></p>

                        Paweł's work serves as an inspiration to aspiring designers and creatives worldwide. It reminds
                        us
                        that,
                        in the ever-changing landscape of design, there's room for both progress and reverence for
                        tradition.
                        As
                        we navigate the digital era, Paweł's portfolio stands as a shining example of how to bridge the
                        gap
                        between modernity and timelessness, leaving an indelible mark on the world of web design. His
                        ability
                        to
                        create visually stunning, user-friendly interfaces that evoke a sense of nostalgia while
                        embracing the
                        future is a testament to the enduring power of creativity and innovation.
                    </div>
                </div>
            </div>
            <div id="content-block-3" class="content-block">
                <div class="block-title">
                    <h1>ABOUT ME</h1>
                </div>
                <div id="cb3-subblocks" class="subblocks">
                    <div id="csb3-1" class="subblock subsubblock">
                        <div id="photo-upnote">Someday I will find a better picture</div>
                        <img src="../assets/photo.png" class="photo" alt="photo" id="photo-pic">
                        <p class="photo-title">
                            Literally Me
                        </p>
                    </div>
                    <div id="csb3-2" class="subblock focusable subsubblock">
                        In the fast-paced realm of technology, where innovation is a constant and change is the norm, a
                        new
                        star
                        has emerged on the IT scene, captivating the industry with their exceptional skills and
                        boundless
                        potential. Meet <u>Paweł Mierzwa</u>, a highly skilled software engineer whose journey into the
                        world of
                        technology has been nothing short of awe-inspiring.
                        <p></p>
                        Paweł's story is one that resonates with many aspiring tech enthusiasts. Studying
                        Computer Science in a prestigious university, Paweł's passion for coding ignited at a young age
                        and
                        evolved into an unquenchable thirst for creating transformative digital solutions.
                        <p></p>
                        In an industry where innovation is driven by fresh perspectives and groundbreaking ideas, Paweł
                        Mierzwa's rise as a highly skilled software engineer is a testament to the limitless
                        possibilities
                        that
                        await those who dare to dream, learn, and code. As the tech world watches in anticipation, one
                        thing
                        is
                        certain – this is only the beginning of a remarkable journey that will leave an indelible mark
                        on the
                        IT landscape.
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
import ViewCounter from "./ViewCounter";
import CurrentDate from "./CurrentDate";

export default {
    name: 'NewspaperComponent',
    components: {
        ViewCounter,
        CurrentDate,
    },
    methods: {
        callVisibilityChange() {
            this.$emit("callVisibilityChange");
        },
    },
};
</script>

<style>
#header {
    width: 100%;
    justify-content: center;
    display: flex;
    align-items: center;
    text-align: center;
    font-size: 6vw;
    font-style: oblique;
    font-weight: bolder;
    top: 0;
    left: 0;
    right: 0;
    flex: content;
}

.header-rect {
    position: absolute;
    font-size: 1vw;
    font-weight: lighter;
    border: #362e2b 1px solid;
    padding: 30px;
}

#ai-credits {
    left: 0;
    margin-left: 20px;
}

#gobackbutton {
    margin-right: 20px;
    right: 0;
    cursor: pointer;
}

#gobackbutton:hover {
    border-width: 3px;
    font-weight: 700;
    margin-right: 18px;
}

#info-bar {
    display: flex;
    justify-content: space-between;
    align-items: center;
    height: 5vh;
    color: #362e2b;
    border-style: double none double none;
    border-color: #362e2b;
}

.info-item {
    font-weight: bold;
    flex: 1;
}

#left-item {
    text-align: left;
    padding-left: 30px;
}

#center-item {
    text-align: center;
}

#right-item {
    text-align: right;
    padding-right: 30px;
}

.content-block {
    height: 80vh;
    font-weight: bold;
    flex: 1;
}

#content-block-1 {
    border-right-style: solid;
    border-right-width: 1px;
    border-right-color: #362e2b;
}

#content-block-3 {
    border-left-style: solid;
    border-left-width: 1px;
    border-left-color: #362e2b;
}

.block-title {
    text-align: center;
}

.subblocks {
    display: inline-flex;
    justify-content: space-between;
    width: 100%;
}

.subblock {
    height: 80%;
    width: 100%;
    text-align: justify;
}

.subsubblock {
    padding: 0 12px 0 12px;
}

#newspaper {
    font-size: 0.85vw;
    text-overflow: ellipsis;
    overflow: hidden;
}

#newspaper h1 {
    font-size: 2.5vw;
    line-height: 2vh;
}

#newspaper h2 {
    font-size: 1.5vw;
    text-transform: uppercase;
}

#newspaper p {
    font-family: 'Franklin Gothic Medium', 'Arial Narrow', Arial, sans-serif;
    font-weight: bolder;
    font-size: 1vw;
}

.linebreak {
    border-top: 1px solid #362e2b;
    border-bottom: none;
    text-shadow: none;
}

.focusable:hover {
    transform: scale(1.04);
}

#photo-upnote {
    padding-top: 25px;
    border-top: solid 1px #362e2b;
    padding-bottom: 25px;
    font-weight: lighter;
}

#csb1-1,
#csb2-1,
#csb3-1 {
    border-right-style: solid;
    border-right-width: 1px;
    border-right-color: #362e2b;
}

#csb1-2 {
    border-top: solid 1px #362e2b;
}

#csb2-2 {
    margin-top: 40px;
}

#csb3-1 {
    text-align: center;
}

#csb3-2 {
    padding: 0 30px 0 10px;
}

#photo-pic {
    height: 45vh;
}

.photo {
    width: 100%;
    filter: sepia(100%);
}

.photo:hover {
    filter: none;
    transform: scale(103%);
}

.photo-title {
    padding-bottom: 20px;
    border-bottom-style: solid;
    border-bottom-width: 1px;
    border-bottom-color: #362e2b;
}

#moresign {
    padding-top: 20px;
    text-align: center;
    font-weight: bolder;
}


#section1-content {
    display: inline-flex;
    justify-content: space-between;
    align-items: center;
    width: 100%;
}
</style>