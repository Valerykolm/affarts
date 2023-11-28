<template>
  <button
    class="add-employee"
    @click="$emit('add-employee-button')"
    :disabled="disabled"
    :class="{ 'opacity-25': disabled }"
  >
    <div class="add-plus">
      <svg
        xmlns="http://www.w3.org/2000/svg"
        width="20"
        height="20"
        viewBox="0 0 20 20"
        fill="none"
      >
        <path
          d="M10 6V14"
          stroke="white"
          stroke-linecap="round"
          stroke-linejoin="round"
        />
        <path
          d="M14 10H6"
          stroke="white"
          stroke-linecap="round"
          stroke-linejoin="round"
        />
      </svg>
    </div>
    Add new Employee
  </button>
</template>
<script>
export default {
  data() {
    return {
      showForm: false,
    };
  },

  props: {
    disabled: {
      type: Boolean,
      required: false,
      default: false,
    },
  },
};
</script>