<template>
    <div class="problem-box">
        <h2>{{this.$root.$data.detail.name}}</h2>
        <h1 class="problem">Current state: {{this.$root.$data.detail.problem}}</h1>
        <p>Issue status: {{this.$root.$data.detail.status}}</p>
        <p>Severity: {{this.$root.$data.detail.severity}}</p>
    </div>
</template>

<style>
.problem-box {
    border: .25em solid red;
    border-radius: 1em;
}
.problem {
    color: red;
}
</style>