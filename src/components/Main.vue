<template>
    <div>This is Main Page</div>
</template>
<script setup>
const modules = import.meta.glob("./components/*.vue");
console.log(modules["./components/HelloWorld.vue"]);
// const regex = /"\.\/([^"]+)"/;
// const match = modules["./components/HelloWorld.vue"].toString().match(regex);
// console.log(match);
// const link = document.createElement("link");
// link.href = "./assets/" + match[1];
// console.log(link.href);
// link.rel = "prefetch";
// document.head.appendChild(link);
</script>