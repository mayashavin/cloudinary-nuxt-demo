<template>
  <section>
    <div class="flex">
      <cld-image public-id="jigglypuff" width="100" height="100" cloudName="mayashavin">
        <cld-transformation effect="grayscale" angle="45" crop="scale"/>
      </cld-image>
      <div>
        <cld-context cloud-name="demo" secure=true>
          <cld-image publicId="face_top" quality="80" />
        </cld-context>
      </div>
      <cld-context cloud-name="demo" secure=true>
        <div>
          <cld-image public-id="face_top" crop="thumb" height="100" width="100" radius="max" gravity="auto"/>
        </div>
      </cld-context>
      <cld-image publicId="vue-sdk-demo/1891680-040wigglytuff" cloudName="demo" :transformation="transformation"/>
    </div>
  </section>
</template>

<script>

export default {
  data() {
    return {
      transformation: [{
        width: 200,
        height: 200,
        crop: 'scale'
      }, {
        angle: '45'
      }]
    }
  }
}
</script>

<style scoped>
.flex {
  display: flex;
  flex-wrap: nowrap;
}
.title {
  font-family: 'Quicksand', 'Source Sans Pro', -apple-system, BlinkMacSystemFont,
    'Segoe UI', Roboto, 'Helvetica Neue', Arial, sans-serif;
  display: block;
  font-weight: 400;
  font-size: 100px;
  color: #2E495E;
  letter-spacing: 1px;
  font-size: 6em;
}
.green {
  color: #00C48D;
}

.subtitle {
  font-weight: 300;
  font-size: 3em;
  color: #2E495E;
  word-spacing: 5px;
  padding-bottom: 15px;
}

.links {
  padding-top: 15px;
}
</style>
