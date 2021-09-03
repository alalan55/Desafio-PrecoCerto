<template>
  <nav>
    <Logo />

    <div class="links">

      <NavLink link="/" name="DASHBOARD">
        <template v-slot:after>
          <i class="fas fa-chart-line"></i>
        </template>
      </NavLink>

      <NavLink link="/" name="GERENCIAR">
        <template v-slot:before>
          <i class="fas fa-chevron-down"></i>
        </template>
      </NavLink>

      <NavLink link="/" name="OTIMIZAR">
        <template v-slot:before>
          <i class="fas fa-chevron-down"></i>
        </template>
      </NavLink>

      <NavLink link="/" name="SIMULAR">
        <template v-slot:before>
          <i class="fas fa-chevron-down"></i>
        </template>
      </NavLink>

      <NavLink link="/" name="HISTÓRICOS">
        <template v-slot:before>
          <i class="fas fa-chevron-down"></i>
        </template>
      </NavLink>

      <NavLink link="/" name="CONFIGURAR">
        <template v-slot:before>
          <i class="fas fa-chevron-down"></i>
        </template>
      </NavLink>
    </div>
  </nav>
</template>

<script>
import { Logo, NavLink } from "@/components/atoms";
export default {
  components: {
    Logo,
    NavLink,
  },
};
</script>

<style lang="scss" scoped>
nav {
  width: 100%;
  height: 100%;
  display: flex;
  align-items: center;
  color: white;

  .links {
      width: 100%;
    margin-left: 1.5rem;
    display: flex;
  }
}
</style>