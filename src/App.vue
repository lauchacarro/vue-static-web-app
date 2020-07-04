<template>
  <div>Hello {{ value }}</div>
</template>

<script>
export default {
  name: "App",
  data() {
    return {
      value: "World"
    };
  },
  created() {
    fetch("api/api-pre-demo?name=Lautaro")
        .then(json => json.json())
        .then(obj => (this.value = obj.text));
  },
};
</script>
