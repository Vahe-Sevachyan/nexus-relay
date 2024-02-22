<template>
  <v-app>
    <v-navigation-drawer
      v-model="drawer"
      :rail="rail"
      permanent
      @click="rail = false"
    >
      <v-list-item
        prepend-avatar="https://randomuser.me/api/portraits/men/85.jpg"
        title="John Leider"
        nav
      >
        <template v-slot:append>
          <v-btn
            variant="text"
            icon="mdi-chevron-left"
            @click.stop="rail = !rail"
          ></v-btn>
        </template>
      </v-list-item>
      <v-divider></v-divider>
      <div>
        <v-col cols="auto">
          <span class="crt-category-title" v-if="!sidebarCollapsed">{{
            AddCategory
          }}</span>
          <v-btn icon="mdi-plus" size="x-small"></v-btn>
        </v-col>
      </div>

      <!-- <div class="filter-container">
        <button>By Date</button>
        <button>A-Z</button>
      </div> 
      <input type="text" placeholder="Search..." /> -->
      <v-list density="compact" nav>
        <v-list-item
          prepend-icon="mdi-folder"
          title="Home"
          value="home"
        ></v-list-item>
        <v-list-item
          prepend-icon="mdi-folder"
          title="My Account"
          value="account"
        >
        </v-list-item>
        <v-list-item
          prepend-icon="mdi-folder"
          title="Users"
          value="users"
        ></v-list-item>
      </v-list>
    </v-navigation-drawer>
  </v-app>
</template>
<script>
export default {
  data() {
    return {
      drawer: true,
      rail: true,
      AddCategory: "Add Category",
      sidebarCollapsed: false,
    };
  },
  methods: {
    // removeTitle() {
    //   if (this.drawer === true) {
    //     this.AddCategory.style.display = "none";
    //   }
    // },
  },
};
</script>
<style scope>
.crt-category-title {
  margin-right: 6.4rem;
}
</style>
