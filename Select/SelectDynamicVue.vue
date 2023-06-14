<template>
  <div>
    <select name="" id="">
      <option value="" v-for="(index, county) in counties" @click="Change(index)">
        {{ county }}
      </option>
    </select>
    <h1>const</h1>
    <select name="" id="">
      <option value="" v-for="(constist, index) in dispConst">
        {{ constist }}
      </option>
    </select>
    <h1>Ward</h1>
    <select name="" id="">
      <option value="" v-for="(ward, index) in dispWarp">
        {{ ward }}
      </option>
    </select>
  </div>
</template>

<script>
export default {
  data() {
    return {
      dispWarp: [],
      dispConst: [],

      counties: {
        Nyeri: "19",
        Nakuru: "32",
        Mombasa: "01",
        Bungoma: "21",
      },

      consc: {
        19: ["Othaya", "Mukurweini", "Karatina", "Kigumoini"],
        32: ["Bahati", "Lanet", "Njoro", "Moro"],
        1: ["Pangani", "pwani", "Msambweni", "coast"],
      },

      conwardsc: {
        19: ["Othaya1", "Mukurweini2", "Karatina3", "Kigumoini4"],
        1: ["Othaya1M", "Mukurweini2M", "Karatina3M", "Kigumoini4M"],
      },
    };
  },
  methods: {
    Change(code) {
      let consitutututt = this.consc[parseInt(code)];
      this.dispConst = consitutututt;
    },
  },
};
</script>

<style lang="scss" scoped></style>
