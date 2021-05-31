<template>
  <section class="comp--skills">
    <b-container fluid>
      <h1>Skills</h1>
      <b-row>
        <b-col
          cols="6"
          v-for="(skill, index) in skills"
          :key="index">
            <h4>{{ skill.title }}</h4>
            <div class="percent">
              <div
                class="percent__value"
                :style="'width: ' + skill.percent*100 + '%;'"></div>
            </div>
        </b-col>
      </b-row>
    </b-container>
  </section>
</template>

<script>
export default {
  props: {
    skills: Array,
  }
}
</script>

<style scoped>
.percent {
  width: 100%;
  height: 4px;
  background: #10262B;
  position: relative;
}
.percent__value {
  position: absolute;
  top: 0;
  left: 0;
  height: 4px;
  background: #E6855A;
}
</style>
