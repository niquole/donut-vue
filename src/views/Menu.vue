<template>
    <div>
  <v-expansion-panel>
    <v-expansion-panel-content
      v-for="(item,i) in menu"
      :key="i"
    >
      <template v-slot:header>
        <div>{{ item.name }}</div>
      </template>
      <v-card>
        <v-card-text>{{ item.info }}</v-card-text>
      </v-card>
    </v-expansion-panel-content>
  </v-expansion-panel>
    </div>
</template>



<script>
export default {
    data() {
        return {
            menu: [
                {
                    name: "Basic Donut",
                    info: "Lorem ipsum, dolor sit amet consectetur adipisicing elit. Doloremque modi voluptates cupiditate ducimus suscipit porro ipsam exercitationem. At, quae id."
                },
                {
                    name: "Chocolate Donut",
                    info: "Lorem ipsum, dolor sit amet consectetur adipisicing elit. Doloremque modi voluptates cupiditate ducimus suscipit porro ipsam exercitationem. At, quae id."

                },
                {
                    name: "Vanilla Donut",
                    info: "Lorem ipsum, dolor sit amet consectetur adipisicing elit. Doloremque modi voluptates cupiditate ducimus suscipit porro ipsam exercitationem. At, quae id."
                },
                {
                    name: "Caramel Donut",
                    info: "Lorem ipsum, dolor sit amet consectetur adipisicing elit. Doloremque modi voluptates cupiditate ducimus suscipit porro ipsam exercitationem. At, quae id."
                },
                {
                    name: "Coconut Donut",
                    info: "Lorem ipsum, dolor sit amet consectetur adipisicing elit. Doloremque modi voluptates cupiditate ducimus suscipit porro ipsam exercitationem. At, quae id."
                },
                {
                    name: "Strawberry Donut",
                    info: "Lorem ipsum, dolor sit amet consectetur adipisicing elit. Doloremque modi voluptates cupiditate ducimus suscipit porro ipsam exercitationem. At, quae id."
                },
                {
                    name: "Pinapple Donut",
                    info: "Lorem ipsum, dolor sit amet consectetur adipisicing elit. Doloremque modi voluptates cupiditate ducimus suscipit porro ipsam exercitationem. At, quae id."
                }

            ]
        }
    }
}
</script>


<style lang="scss">
.v-expansion-panel__header {
    background-color: #FD8682;
}
.v-card__text {
    background-color: #fff;
}
</style>
