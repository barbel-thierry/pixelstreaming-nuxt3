<template>
  <div>
    <h1>Welcome to the homepage</h1>
  </div>
</template>

<script>
import { Config, PixelStreaming } from '@epicgames-ps/lib-pixelstreamingfrontend-ue5.2'

export default {
  created() {
    const pixelStreaming = new PixelStreaming(
        new Config()
    )

    console.log(pixelStreaming)
  }
}
</script>
