<template>
  <div>This is Main Page</div>
</template>
<script setup>
const globModules = import.meta.glob("/src/components/HelloWorld.vue");


Object.entries(globModules).forEach(([path, globModule]) => {
  console.log(path, globModule);
  globModule().then((mod) => {
    console.log(path + "模块内容", mod.default);
  });
});

// const regex = /"\.\/([^"]+)"/;
// const match = modules["./HelloWorld.vue"].toString().match(regex);
// console.log(match);
// const link = document.createElement("link");
// link.href = "./assets/" + match[1];
// console.log(link.href);
// link.rel = "prefetch";
// document.head.appendChild(link);
</script>
