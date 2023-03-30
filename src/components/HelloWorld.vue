<template>
  <div class="hello">
    <h1>Embedded datastudio</h1>
    <div id="report-container"></div>
  </div>
</template>

<script>
export default {
  name: 'HelloWorld',
  props: {
    msg: String
  },
  mounted() {
    const embedUrl = 'https://lookerstudio.google.com/embed/reporting/8b3a9813-fe7d-4d3d-9c74-58ebe4caab3c/page/zkuKD'; // Substitua pela URL de incorporação do seu relatório

    const container = document.getElementById('report-container');

    const iframe = document.createElement('iframe');
    iframe.setAttribute('src', embedUrl);
    iframe.setAttribute('width', '100%');
    iframe.setAttribute('height', '300px');
    iframe.setAttribute('frameborder', '0');
    container.appendChild(iframe);
  }

}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h3 {
  margin: 40px 0 0;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
</style>
