<template>
  <div>
    <h1>Divider</h1>

    <Demobox>
      <div class="flex justify-center w-11/12">
        <it-divider :vertical="dividerVertical" />
      </div>
      <template #props>
        <it-checkbox v-model="dividerVertical" label="Vertical" />
      </template>
    </Demobox>

    <Box :code="codeHorizontal" title="Horizontal">
      <p class="m-0 text-sm">
        Not that I wish to imply you have been sleeping on the job. No one is
        more deserving of a rest. And all the effort in the world would have
        gone to waste until...well, let's just say your hour has come again.
      </p>
      <it-divider class="ml-0" />
      <p class="m-0 text-sm">
        Not that I wish to imply you have been sleeping on the job. No one is
        more deserving of a rest. And all the effort in the world would have
        gone to waste until...well, let's just say your hour has come again.
      </p>
      <it-divider class="ml-0" />
      <p class="m-0 text-sm">
        Not that I wish to imply you have been sleeping on the job. No one is
        more deserving of a rest. And all the effort in the world would have
        gone to waste until...well, let's just say your hour has come again.
      </p>
    </Box>

    <Box :code="codeVertical" title="Vertical">
      <div class="m-0 text-sm">
        Still
        <it-divider vertical />
        Sane
        <it-divider vertical />
        Exile
      </div>
    </Box>

    <props-table :data-sheet="dataSheet" />
  </div>
</template>

<script lang="ts">
import { defineComponent } from 'vue'

export default defineComponent({
  data: () => ({
    dividerVertical: false,

    codeHorizontal: `<p>Not that I wish to imply you have been sleeping on the job. No one is more deserving of a rest. And all the effort in the world would have gone to waste until...well, let's just say your hour has come again.</p>
<it-divider />
<p>Not that I wish to imply you have been sleeping on the job. No one is more deserving of a rest. And all the effort in the world would have gone to waste until...well, let's just say your hour has come again.</p>
<it-divider />
<p>Not that I wish to imply you have been sleeping on the job. No one is more deserving of a rest. And all the effort in the world would have gone to waste until...well, let's just say your hour has come again.</p>`,

    codeVertical: `<div>
  Still
  <it-divider vertical />
  Sane
  <it-divider vertical />
  Exile
</div>`,

    dataSheet: [
      {
        property: 'vertical',
        type: ['Boolean'],
        default: false,
        values: [],
        description: 'Makes divider vertical',
      },
    ],
  }),
})
</script>
