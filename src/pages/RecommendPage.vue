<template>
  <q-page padding>
    <div class="flex flex-center q-pt-xl">
      <div class="full-width" style="max-width: 500px">
        <q-form @submit.prevent="onSubmit">
          <q-input
            dense
            color="warning"
            v-model="id"
            label="User ID"
            lazy-rules
            outlined
            :rules="[(val) => val.length > 0 || 'Please type user ID']"
          />

          <q-input
            dense
            color="warning"
            outlined
            v-model="number"
            label="Number of Products to Recommend"
            lazy-rules
            :rules="[
              (val) =>
                val.length > 0 || 'Please type number of products to recommend',
            ]"
          />

          <q-btn
            class="full-width"
            label="recommend"
            color="warning"
            type="submit"
          />
        </q-form>
      </div>
    </div>
  </q-page>
</template>

<script>
export default {
  // name: 'PageName',
  data() {
    return {
      id: "",
      number: "",
    };
  },

  methods: {
    onSubmit() {
      alert("submit");
    },
  },
};
</script>
