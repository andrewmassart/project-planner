<template>
  <nav class="filter-nav">
      <button
        @click="updateFilter('all')"
        :class="{ active: current === 'all' }"
      >View All</button>
      <button
        @click="updateFilter('completed')"
        :class="{ active: current === 'completed' }"
      >Completed</button>
      <button
        @click="updateFilter('ongoing')"
        :class="{ active: current === 'ongoing' }"
      >Ongoing</button>
  </nav>
</template>

<script>
export default {
    props: ['current'],
    methods: {
        updateFilter(by) {
            this.$emit('filterChange', by)
        }
    }
}
</script>

<style>
.filter-nav button {
    background: transparent;
    border: none;
    color: #bbb;
    outline: none;
    font-size: 12px;
    text-transform: uppercase;
    margin-right: 10px;
    letter-spacing: 1px;
    font-weight: bold;
    cursor: pointer;
}
.filter-nav button.active {
    color: #555;
    border-bottom: 2px solid #555;
}
.filter-nav button:hover {
    color: #555;
    transition: .2s ease-in-out;
}

</style>