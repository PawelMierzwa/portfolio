<template>
    <div>
        {{ formattedDate }}
    </div>
</template>
  
<script>
export default {
    data() {
        return {
            currentDate: '',
        }
    },
    computed: {
    formattedDate() {
      const options = {
        weekday: 'long',
        year: 'numeric',
        month: 'long',
        day: 'numeric'
      };
      return new Date(this.currentDate).toLocaleDateString('en-US', options);
    }
  },
    mounted() {
        const today = new Date();
        this.currentDate = today.toDateString();
    },
}
</script>