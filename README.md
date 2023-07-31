# Develop Client Side, Create Sample Dashboard

## Create dashboardComponent.ts File
```bash
export const posts = [
  {
    img : 'src/image/mountains.jpg',
    title : 'Best View',
    username: 'Hossein Pourghadiri',
    description : 'Lorem ipsum dolor sit amet, nam ne liber propriae, vel no vidit nullam volutpat. Ut harum inciderint usu, vivendum invenire est ut. In vix nobis legendos deterruisset. Quas dignissim cum ad. Sea quaestio assentior ut, ad eum idque regione salutatus. Inani splendide scripserit et nec. Et has aperiam civibus.',
    upVoteCount : 5,
  },
  {
    img : 'src/image/mountains.jpg',
    title : 'Best View',
    username: 'Hossein Pourghadiri',
    description : 'Lorem ipsum dolor sit amet, nam ne liber propriae, vel no vidit nullam volutpat. Ut harum inciderint usu, vivendum invenire est ut. In vix nobis legendos deterruisset. Quas dignissim cum ad. Sea quaestio assentior ut, ad eum idque regione salutatus. Inani splendide scripserit et nec. Et has aperiam civibus.',
    upVoteCount : 4,
  },
  {
    img : 'src/image/mountains.jpg',
    title : 'Best View',
    username: 'Hossein Pourghadiri',
    description : 'Lorem ipsum dolor sit amet, nam ne liber propriae, vel no vidit nullam volutpat. Ut harum inciderint usu, vivendum invenire est ut. In vix nobis legendos deterruisset. Quas dignissim cum ad. Sea quaestio assentior ut, ad eum idque regione salutatus. Inani splendide scripserit et nec. Et has aperiam civibus.',
    upVoteCount : 3,
  },
  {
    img : 'src/image/mountains.jpg',
    title : 'Best View',
    username: 'Hossein Pourghadiri',
    description : 'Lorem ipsum dolor sit amet, nam ne liber propriae, vel no vidit nullam volutpat. Ut harum inciderint usu, vivendum invenire est ut. In vix nobis legendos deterruisset. Quas dignissim cum ad. Sea quaestio assentior ut, ad eum idque regione salutatus. Inani splendide scripserit et nec. Et has aperiam civibus.',
    upVoteCount : 2,
  },
];
```
## Update DashboardPage.vue File
```bash
<template>
  <div class="q-pa-md row items-start q-gutter-md justify-center">
    <q-card class="my-card" v-for="post in posts" :key="post">
      <q-img :src="post.img" />
      <q-card-section>
        <q-btn
          fab
          color="light-blue-8"
          icon="place"
          class="absolute"
          style="top: 0; right: 12px; transform: translateY(-50%);"
        />
        <div class="row no-wrap items-center">
          <div class="col text-h6 ellipsis">
            {{ post.title }}
          </div>
          <div class="col-auto text-grey text-caption q-pt-md row no-wrap items-center">
          </div>
        </div>
      </q-card-section>
      <q-card-section class="q-pt-none">
        <div class="text-subtitle1">
          {{ post.username }}
        </div>
        <div class="text-caption text-grey">
          {{ post.description }}
        </div>
      </q-card-section>
      <q-separator />
      <q-card-actions>
        <q-btn color="light-blue-8" icon-right="favorite" :label="`Like (${post.upVoteCount})`" />
      </q-card-actions>
    </q-card>
  </div>
</template>
<script lang="ts" setup>
import {posts} from 'src/components/dashboard/ts/dashboardComponent'
</script>


<style lang="sass" scoped>
.my-card
  width: 100%
  max-width: 300px
</style>
```
