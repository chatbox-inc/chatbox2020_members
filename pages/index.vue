<template>
  <section class="p-members">
    <c-hero />
    <c-intro />
    <c-vision />
    <c-skill />
    <c-members :member-list="memberList" />
  </section>
</template>

<script>
import CHero from "@/pages/-cHero.vue"
import CIntro from "@/pages/-cIntro.vue"
import CVision from "@/pages/-cVision.vue"
import CSkill from "@/pages/-cSkill.vue"
import CMembers from "@/pages/-cMembers.vue"
import { member } from "@/static/api/member.json"
export default {
  components: {
    CHero,
    CIntro,
    CVision,
    CSkill,
    CMembers,
  },
  data() {
    return {
      memberList: member,
    }
  },
}
</script>

<style lang="scss" scoped>
.p-members {
  width: 100%;
}
</style>
