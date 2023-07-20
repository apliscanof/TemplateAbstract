<template>
  <v-continer fluid >
    <v-row>
      <v-col cols="12" class="pa-0">
        <v-card height="500" color="#dadbf1" flat rounded="0">
          <v-container fluid class="fill-height">
            <v-row justify="center" align="center">
              <v-col cols="5">
                <v-card-title class="text-h1" style="font-size: 60px !important; line-height: 90px; font-weight: 500;">How can we help?</v-card-title>
              </v-col>
              <v-col cols="12" sm="8">
                <v-text-field
                  placeholder="Search"
                  outlined
                  single-line
                  color="#4C5FD5"
                  append-icon="mdi-arrow-right"
                ></v-text-field>
              </v-col>
            </v-row>
          </v-container>
        </v-card>
      </v-col>
    </v-row>
    <v-row style="margin: 175px 130px 175px 130px;">
      <v-container>
        <v-row>
          <v-col v-for="(item,i) in cards" :key="i" cols="12" md="6" class="pa-0">
            <v-card min-height="238px" flat>
              <v-container fluid>
                <v-row>
                  <v-col cols="3">
                    <v-img contain max-width="85" :src="item.src"></v-img>
                  </v-col>
                  <v-col cols="9">
                    <v-container style="font-family: 'Vesterbro', sans-serif;" >
                      <v-row align="start" justify="start">
                        <h2><strong>{{ item.title }}</strong></h2>
                        <p>{{ item.description }}</p>
                      </v-row>
                      <v-row>
                        <v-btn plain color="#4C5FD5">Learn More<v-icon light> mdi-arrow-right-thin</v-icon></v-btn> 
                      </v-row>
                    </v-container>
                  </v-col>
                </v-row>
              </v-container>
            </v-card>
          </v-col> 
        </v-row>  
      </v-container>
    </v-row>
  </v-continer>
</template>

<script>
export default {
  data()  {return {
    cards:[
      {
      src: 'https://theme.zdassets.com/theme_assets/2197739/aed6500f4da41c641f3de5d96247eb6654e9c386.png',
      title: 'Using Abstract',
      description: 'Abstract lets you manage, version, and document your designs in one place.',
      to: ''
    },
    {
      src: 'https://theme.zdassets.com/theme_assets/2197739/91588b3d042df901d9b941ccbb57af4f151401c7.png',
      title: 'Manage your account',
      description: 'Configure your account settings, such as your email, profile details, and password.',
      to: ''
    },
    {
      src: 'https://theme.zdassets.com/theme_assets/2197739/50d0db451c0e1e66e1caddd142986fcf6792ca05.png',
      title: 'Manage organizations, teams, and projects',
      description: 'Use Abstract organizations, teams, and projects to organize your people and your work.',
      to: ''
    },
    {
      src: 'https://theme.zdassets.com/theme_assets/2197739/3e82d0126e97d7b7c60a611d4e11b3c278d33743.png',
      title: 'Manage billing',
      description: 'Change subscriptions and payment details.',
      to: ''
    },
    {
      src: 'https://theme.zdassets.com/theme_assets/2197739/7712592465ef5c7bf18f1c7cb16e19ab44eb81e3.png',
      title: 'Authenticate to Abstract',
      description: 'Set up and configure SSO, SCIM, and Just-in-Time provisioning.',
      to: ''
    },
    {
      src: 'https://theme.zdassets.com/theme_assets/2197739/dcc25d18e224d12621d74e545cc8bdd1b5685ca8.png',
      title: 'Abstract support',
      description: 'Get in touch with a human.',
      to: ''
    }
  ]
  }},
}
</script>
