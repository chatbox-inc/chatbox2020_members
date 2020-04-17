<template>
  <section v-if="getMember" class="p-member">
    <c-hero />
    <c-profile :profile="getMember.profile" />
    <c-timeline :timeline="getMember.timeline" />
    <c-interview :interview="getMember.interview" />
    <c-other :member-list="memberList" />
  </section>
</template>

<script>
import cHero from "@/pages/member/-cHero"
import cProfile from "@/pages/member/-cProfile"
import cTimeline from "@/pages/member/-cTimeline"
import cInterview from "@/pages/member/-cInterview"
import cOther from "@/pages/member/-cOther"
import { member } from "@/static/api/member.json"
export default {
  components: {
    cHero,
    cProfile,
    cOther,
    cInterview,
    cTimeline,
  },
  data() {
    return {
      memberList: member,
    }
  },
  computed: {
    getMember() {
      return this.memberList.find(({ id }) => String(id) === this.getParam)
    },
    getParam() {
      return this.$route.params.id
    },
  },
  mounted() {
    console.log(this.getMember)
  },
}
</script>

<style scoped lang="scss">
.p-member {
  width: 100%;
}
</style>
