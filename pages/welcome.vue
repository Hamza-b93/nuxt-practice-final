<template>
    <div id="" class="">
        <span id="" class=""> Hello {{ name }} </span>
        <br />
        <span id="" class="">
            The Date For You Right Now Is: {{ date }}/{{ month }}/{{
                year
            }}</span
        >
        <br />
        The Time For You Right Now Is <span id="" class="" v-text="time"></span>
        <br />
        Anything That Is Bold In This Sentence is So Because We Have Used The
        v-html Directive To Inject HTML Directly Into The Template.
        <span id="" class="" v-html="bold"></span>
        <br />
        <span v-bind:id="blueText">
            The Reason This Text Is Pink Is Because We Have Used The
            v-bind:class Directive To Bind An ID Of 'pinkText To This Span.
        </span>
        <br />
        <span v-bind:class="pinkText">
            The Reason This Text Is Blue Is Because We Have Used The v-bind:id
            Directive To Bind A Class Of 'blueText To This Span.
        </span>
        <br />
        <span
            v-bind:style="{
                color: highlightColor,
            }"
        >
            The Reason This Text Is Orange Is Because We Have Used The
            v-bind:style Directive To Bind A Style Of 'highLightColor To This
            Span That Gives ITs Text An Orange Color.
        </span>
    </div>
</template>

<style scoped></style>

<script>
export default {
    name: "Welcome",
    data() {
        return {
            name: "Hamza",
            date: new Date().getDate(),
            month: new Date().getMonth(),
            time: new Date().toTimeString(),
            day: new Date().getDay(),
            year: new Date().getFullYear(),
            bold: "<b> Bold Text </b>",
            blueText: "blueText",
            pinkText: "pinkText",
            highlightColor: "orange",
        };
    },
};
</script>

<style scoped>
#blueText {
    color: blue;
}
.pinkText {
    color: pink;
}
</style>
