<template>
  <div class="team">
    <h1 class="subtitle-1 grey--text mt-6">Team</h1>
    <v-container class="my-5">
      <v-row>
        <v-col
          v-for="person in team"
          :key="person.name"
          xs="12"
          sm="6"
          md="4"
          lg="3"
        >
          <v-card class="ma-3">
            <v-avatar size="100">
              <img :src="person.avatar" />
            </v-avatar>
            <v-card-text>
              <div class="subtitle-1">{{ person.name }}</div>
              <div class="grey--text">{{ person.role }}</div>
            </v-card-text>
            <v-card-actions>
              <v-btn depressed color="light--grey">
                <v-icon small left>mdi-message</v-icon>
                <span>Message</span>
              </v-btn>
            </v-card-actions>
          </v-card>
        </v-col>
      </v-row>
    </v-container>
  </div>
</template>

<script>
export default {
  data() {
    return {
      team: [
        {
          name: 'Braden Wong',
          role: 'Web developer',
          avatar: '@/assets/avatar-1.png',
        },
        {
          name: 'Ruobin',
          role: 'Graphic designer',
          avatar: '@/assets/avatar-2.png',
        },
        {
          name: 'Jason',
          role: 'Web developer',
          avatar: '@/assets/avatar-3.png',
        },
        {
          name: 'Sam',
          role: 'Social media maverick',
          avatar: '@/assets/avatar-4.png',
        },
        { name: 'Yoshi', role: 'Sales guru', avatar: '@/assets/avatar-5.png' },
      ],
    }
  },
}
</script>

<style></style>
