<template>
  <div class="home">
    <h1 class="mb-5">
      Experts
    </h1>
    <div class="expert-table bg-white">
      <b-table
          :sticky-header="stickyHeader"
          :no-border-collapse="noCollapse"
          responsive
          :items="items"
          :fields="fields"
          @row-clicked="Hamed($event)"
      >
        <!-- We are using utility class `text-nowrap` to help illustrate horizontal scrolling -->
        <template #head(id)="scope">
          <div class="text-nowrap">Row ID</div>
        </template>
        <template #head()="scope">
          <div class="text-nowrap">
            {{ scope.label }}
          </div>
        </template>
        <template #cell(image)="image">
          <img src="../assets/images/client.jpg" alt="">
        </template>
      </b-table>
    </div>
  </div>
</template>

<script>
export default {
  name: 'Home',
  data() {
    return {
      stickyHeader: true,
      noCollapse: false,
      fields: [
        'id',
        'image',
        'name',
        { key: 'return', stickyColumn: true, isRowHeader: true, variant: 'warning' },
        { key: 'risk', stickyColumn: true, variant: 'success' },
      ],
      items: [
        { id: 1 , name: 'Hamed Karampour', image: 1, return: '-50.25', risk: 2},
        { id: 2 , name: "Mohamad Ali", image: 1, return: '32', risk: 1},
      ]
    }
  },
  methods:{
    Hamed(e){
      this.$router.push({path : '/single-expert' , query:{
        name : e.name
      }})
    }
  }
}
</script>
