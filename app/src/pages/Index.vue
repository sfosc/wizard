<template>
  <q-page class="q-pa-md">
    <q-stepper
      v-model="step"
      vertical
      color="primary"
      animated
      style="opacity:0.9"
    >
      <q-step
        :name="1"
        title="Select license"
        icon="settings"
        :done="step > 1"
      >
        <q-markdown>
# Licenses
You can have one or more licenses.
        </q-markdown>
        <q-stepper-navigation>
          <q-btn @click="step = 2" color="primary" label="Continue" />
        </q-stepper-navigation>
      </q-step>

      <q-step
        :name="2"
        title="Choose Voting"
        caption="Optional"
        icon="create_new_folder"
        :done="step > 2"
      >
        <q-markdown>
# Voting is important for stuff.
- Glory
- Fame
- Fun
        </q-markdown>

        <q-stepper-navigation>
          <q-btn @click="step = 4" color="primary" label="Continue" />
          <q-btn flat @click="step = 1" color="primary" label="Back" class="q-ml-sm" />
        </q-stepper-navigation>
      </q-step>

      <q-step
        :name="3"
        title="Disabled Choice"
        icon="assignment"
        disable
      >
        This step won't show up because it is disabled.
      </q-step>

      <q-step
        :name="4"
        title="Download your charter"
        icon="add_comment"
      >
        <q-markdown>
# Download the charter documents.
        </q-markdown>
        <q-btn color="teal" label="here" icon="fa-download"></q-btn>
        <q-stepper-navigation>
          <q-btn color="primary" label="Finish"/>
          <q-btn flat @click="step = 2" color="primary" label="Back" class="q-ml-sm" />
        </q-stepper-navigation>
      </q-step>
    </q-stepper>
  </q-page>
</template>

<style>
</style>

<script>
export default {
  name: 'PageIndex',
  data () {
    return {
      step: 1
    }
  }
}
</script>
