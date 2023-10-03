<template>
    <div id="actual-section" ref="section">
        <div id="button-line">
            <button id="unblur-button" @click="callVisibilityChange()">
                <span class="button-text">
                    Unblur
                </span>
            </button>
        </div>
        <div id="title">
            <h1>CNSH</h1>
            <h2>Paweł Mierzwa</h2>
            <h3>Software Engineer/<br>/Web developer</h3>
        </div>
    </div>
</template>

<script>
export default {
    name: 'ActualSectionComponent',
    methods: {
        callVisibilityChange() {
            this.$emit("callVisibilityChange");
        },
    },
};

</script>

<style>
#actual-section {
    position: absolute;
    width: 100%;
    height: 100%;
    top: 0;
    left: 0;
    z-index: 1;
}

#title {
    padding-top: 4%;
    width: 100%;
    height: 40%;
    text-align: center;
    font-size: 300%;
}

#actual-section h1 {
    font-size: 200%;
}

#button-line {
    top: 0;
    height: 30px;
    width: 100%;
    padding: 1% 0 0 0;
    display: inline-flex;
}

#unblur-button {
    background-color: #362e2b;
    color: #debd9e;
    font-size: 13px;
    position: absolute;
    right: 0;
    padding: 10px 10px;
    margin: 10px 30px;
    border: none;
    border-radius: 3rem;
    outline: none;
    cursor: pointer;
}
</style>