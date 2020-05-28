<template>
  <div>
    <v-row>
      <v-col>
        <VideoPlayer :hero="hero" @currentTime="updateCurrentTime" />
        <TopicDetail :topic-id="topicId" :current-time="currentTime" />
        <div>Title: {{ data.title }}</div>
        <!-- <div :v-for="authors in data" :key="authors">Authors: {{ authors }}</div> -->
      </v-col>
      <v-col>
        <v-navigation-drawer width="full" permanent>
          <h1>Title of Course</h1>
          <h3>Author of Course</h3>
          <v-expansion-panels accordion>
            <v-expansion-panel v-for="datum in data" :key="datum">
              <!-- TODO Set up dynamic numbering system for sections -->
              <v-expansion-panel-header>{{
                datum.title
              }}</v-expansion-panel-header>
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

<script lang="ts">
import Vue from 'vue'
import { v4 } from 'uuid'
import data from '../../components/topicDetailData'
import TopicDetail from '@/components/TopicDetail.vue'
import VideoPlayer from '@/components/VideoPlayer.vue'
export default Vue.extend({
  components: {
    TopicDetail,
    VideoPlayer
  },
  data() {
    return { topicId: v4(), currentTime: 0, data }
  },
  methods: {
    updateCurrentTime(currentTime: number) {
      this.currentTime = currentTime
    }
  }
})
</script>
