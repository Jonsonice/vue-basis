<template>
  <div>
    <PersonalInfo v-model="phoneInfo" :zip-code.sync="zipCode" />

    <PersonalInfo
      :phone-info="phoneInfo"
      :zip-code="zipCode"
      @change="val => (phoneInfo = val)"
      @update:zipCode="val => (zipCode = val)"
    />

    phoneInfo： {{ phoneInfo }}
    <br />
    zipCode： {{ zipCode }}

    <hr>
    <Directives></Directives>
    <hr>
    <CustomerDirectives></CustomerDirectives>
  </div>
</template>
<script>
import PersonalInfo from "./components/PersonalInfo"
import Directives from "./components/Directives"
import CustomerDirectives from "./components/CustomerDirectives"

export default {
  components: {
    PersonalInfo,
    Directives,
    CustomerDirectives
  },
  data() {
    return {
      phoneInfo: {
        areaCode: "+86",
        phone: ""
      },
      zipCode: ""
    };
  }
};
</script>
<style>
  * {
    text-align: center;
  }
</style>
