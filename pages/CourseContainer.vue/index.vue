<template>
  <div>
    <v-row>
      <v-col>
        <v-img src="https://picsum.photos/410/300?random" width="50rem"></v-img>
      </v-col>
      <v-col>
        <v-navigation-drawer width="full" permanent>
          <h1>Title of Course</h1>
          <h3>Author of Course</h3>
          <!-- Potentially unnecessary, saw the tabs idea on pluralsight -->
          <v-tabs grow>
            <v-tab>Table of Contents</v-tab>
            <v-tab>Notes</v-tab>
          </v-tabs>
          <!-- Accordion removes extra space around panels, preference choice -->
          <v-expansion-panels accordion>
            <v-expansion-panel v-for="(section, i) in 5" :key="i">
              <!-- TODO Set up dynamic numbering system for sections -->
              <v-expansion-panel-header>Section</v-expansion-panel-header>
              <v-expansion-panel-content>
                Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do
                eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut
                enim ad minim veniam, quis nostrud exercitation ullamco laboris
                nisi ut aliquip ex ea commodo consequat.
              </v-expansion-panel-content>
            </v-expansion-panel>
          </v-expansion-panels>
          <h1>
            Do we want this to inherit the size of the parent container or
            adjust based on the amount of content inside?
          </h1>
        </v-navigation-drawer>
      </v-col>
    </v-row>
  </div>
</template>

<script>
import Vue from 'vue'
export default Vue.extend({
  //   props: []
})
</script>
