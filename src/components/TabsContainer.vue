<template>
  <div class="tabs">
    <ul class="tabs__header">
      <li
        class="tabs_header-item"
        v-for="tab in tabs"
        :key="tab"
        :class="{ 'is-active': tab.isActive }"
      >
        <a
          :class="{ 'active-tab': tab.isActive }"
          class="tabs__header-link"
          @click="selectTab(tab)"
          >{{ tab.name }}</a
        >
      </li>
    </ul>
  </div>

  <div class="tabs__details">
    <!-- Tab details will be inside the slot -->
    <slot></slot>
  </div>
</template>

<script>
export default {
  data() {
    return { tabs: [] }
  },
  created() {},
  methods: {
    selectTab(selectedTab) {
      this.tabs.forEach((tab) => {
        tab.isActive = tab.name == selectedTab.name
      })
    }
  }
}
</script>

<style scoped>
.tabs__header {
  list-style: none;
  display: flex;
  gap: 8rem;
  padding: 0;
  margin: 4rem 0 5rem 0;
}

.tabs__header-link {
  cursor: pointer;
  font-weight: 600;
  font-size: 2.4rem;
  line-height: 5.4rem;
  text-decoration: none;
  color: #828282;
  border-bottom: 4px solid transparent;
  transition: 0.5s all;
}

.tabs__header-link.active-tab,
.tabs__header-link:hover {
  color: #eebf63;
  border-bottom: 4px solid #eebf63;
}

@media (max-width: 600px) {
  .tabs__header {
    gap: 2rem;
    flex-direction: column;
    justify-content: space-around;
    align-items: center;
  }

  .tabs__header-link.active-tab,
  .tabs__header-link:hover {
    border-bottom: 2px solid #eebf63;
  }
}
</style>
