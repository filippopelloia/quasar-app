<template>
  <q-page class="row">
    <!--   -->
    <q-card class="col-xs-9">
      <q-toolbar >
        <q-input class="full-width" :model-value="search" placeholder="Search an item..." borderless dense >
          <template #append>
            <q-icon name="mdi-magnify" />
          </template>
        </q-input>
      </q-toolbar>
      <q-list bordered>
        <q-item>
          <q-item-section>
            <q-checkbox :model-value="true" >Check this</q-checkbox>
          </q-item-section>
          <q-item-section side>
            <q-btn icon="mdi-delete" size="sm" round flat />
          </q-item-section>
        </q-item>
      </q-list>
    </q-card>
    <div class="col-xs-3">
      <q-toolbar class="bg-primary ">
        <CreateToDoButton fab icon="mdi-plus" color="secondary" style="margin-bottom: -42px;" class="q-ml-md"/>
      </q-toolbar>
    </div>
  </q-page>
</template>

<script>
import CreateToDoButton from 'components/CreateToDoButton.vue'
import { defineComponent } from 'vue'

export default defineComponent({
  name: 'IndexPage',

  data () {
    return {
      selected: null,
      search: ''
    }
  },
  components: {
    CreateToDoButton
  }
})
</script>
