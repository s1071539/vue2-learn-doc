<template>
  <div class="hello">
    {{ msg }}
    <hr />
  </div>
</template>

<script>
// mixin object
var mixinTwo = {
  created: function () {
    this.hi();
  },
  methods: {
    hi: function () {
      console.log("hi from mixinTwo!");
    },
  },
};
var mixinOne = {
  created: function () {
    this.hello();
  },
  methods: {
    hello: function () {
      console.log("hello from mixinOne!");
    },
  },
};

export default {
  name: "HelloWorld",
  props: {
    msg: String,
  },
  mixins: [mixinOne, mixinTwo],
};
</script>

