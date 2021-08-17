<template>
  <q-page>
    <div class="row q-mb-xl">
      <div class="col bg-primary">1</div>
      <div class="col bg-secondary">2</div>
      <div class="col bg-accent">3</div>
    </div>
    <div class="row q-mb-xl">
      <div class="col bg-primary">1</div>
      <div class="col-5 bg-secondary">2</div>
      <div class="col-6 bg-accent">3</div>
    </div>
    <div class="row q-mb-xl justify-center">
      <div class="col-4 bg-secondary">2</div>
      <div class="col-4 bg-accent">3</div>
    </div>
    <div class="row q-mb-xl justify-end">
      <div class="col-4 bg-secondary">2</div>
      <div class="col-4 bg-accent">3</div>
    </div>
    <div class="row q-mb-xl justify-between">
      <div class="col-4 bg-secondary">2</div>
      <div class="col-4 bg-accent">3</div>
    </div>

    <q-separator spaced />

    <div class="row q-mb-xl justify-between">
      <div class="col-12 col-sm-5 col-md-4 bg-secondary">2</div>
      <div class="col-12 col-sm-5 col-md-4 bg-accent">3</div>
    </div>

    <q-separator spaced />

    <div class="row q-mb-md">
      <div class="square-box bg-primary"></div>
      <div class="square-box bg-secondary"></div>
      <div class="square-box bg-accent"></div>
    </div>

    <div class="row justify-between q-mb-md">
      <div class="square-box bg-primary"></div>
      <div class="square-box bg-secondary"></div>
      <div class="square-box bg-accent"></div>
    </div>

    <div class="row justify-end q-mb-md">
      <div class="square-box bg-primary"></div>
      <div class="square-box bg-secondary"></div>
      <div class="square-box bg-accent"></div>
    </div>

    <div class="row justify-around q-mb-md">
      <div class="square-box bg-primary"></div>
      <div class="square-box bg-secondary"></div>
      <div class="square-box bg-accent"></div>
    </div>

    <div class="column items-center q-mb-md bg-dark">
      <div class="square-box bg-primary"></div>
      <div class="square-box bg-secondary"></div>
      <div class="square-box bg-accent"></div>
    </div>

    <div class="column items-end q-mb-md bg-dark">
      <div class="square-box bg-primary"></div>
      <div class="square-box bg-secondary"></div>
      <div class="square-box bg-accent"></div>
    </div>

    <div class="column custom-height items-center justify-center q-mb-md bg-dark">
      <div class="square-box bg-primary"></div>
      <div class="square-box bg-secondary"></div>
      <div class="square-box bg-accent"></div>
    </div>

    <div class="column custom-height items-center justify-between q-mb-md bg-dark">
      <div class="square-box bg-primary"></div>
      <div class="square-box bg-secondary"></div>
      <div class="square-box bg-accent"></div>
    </div>

    <div class="column custom-height items-center justify-between q-mb-md bg-dark">
      <div class="square-box bg-primary self-start"></div>
      <div class="square-box bg-secondary self-end"></div>
      <div class="square-box bg-accent"></div>
    </div>

  </q-page>
</template>

<script>
import { defineComponent } from "vue";

export default defineComponent({
  name: "Flex",
});
</script>

<style scoped>
.col, .col-4, .col-6, .col-12{
  height: 50px;
}

.square-box{
  width: 50px;
  height: 50px;
}

.custom-height{
  height: 300px;
}
</style>