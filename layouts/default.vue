<template>
  <v-app>
    <v-app-bar absolute height="90" dark color="#000000" elevation="0">
      <svg class="abstract-logo-footer" style="width: 138px;" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 200 51" preserveAspectRatio="xMinYMid slice">
        <g class="abstract-logo-mark-footer" fill="#fff">
          <path d="M25.41 0C5.08 0 0 5.08 0 25.41s5.08 25.41 25.41 25.41 25.41-5.08 25.41-25.41S45.74 0 25.41 0zm-4.17 39.31A9.73 9.73 0 1 1 31 29.58a9.75 9.75 0 0 1-9.76 9.73zm17.67-.4h-4.77V16.67H11.91v-4.76h27z"></path>
          <circle cx="21.24" cy="29.58" r="4.96"></circle>
        </g>
      </svg>
      <v-toolbar-title>Abstract | Help Center</v-toolbar-title>
      <v-spacer />
      <v-btn outlined class="mr-1">Submit a request</v-btn>
      <v-btn color="#4C5FD5">Sign In</v-btn>
    </v-app-bar>
    <v-main style="padding: 0 !important;">
        <nuxt />
    </v-main>
    <v-footer
    color="#000000"
    dark
    padless
    style="height:342px !important"
  >
    <v-container class="fill-height">
      <v-row class="fill-height" align="start">
        <v-col v-for="(item,i) in footer.listas" :key="i" cols="2">
          <v-list color="#000000">
            <span><h2>{{ item.title }}</h2></span>
            <v-list-item-group>
              <v-list-item v-for="(listNew, j) in item.listas" :key="j" style="min-height: 20px !important;">
                <v-list-item-content class="py-1">
                  <v-list-item-subtitle><h3>{{ listNew }}</h3></v-list-item-subtitle>
                </v-list-item-content>
              </v-list-item>
            </v-list-item-group>
          </v-list> 
        </v-col>
        <v-col
        class="py-4 fill-height text-end white--text"
        cols="4"> 
          <v-container class="fill-height">
            <v-row>
              <v-col cols="12" class="d-flex">
                <svg class="abstract-logo-footer" style="width: 138px;" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 200 51" preserveAspectRatio="xMinYMid slice">
                  <g class="abstract-logo-mark-footer" fill="#fff">
                    <path d="M25.41 0C5.08 0 0 5.08 0 25.41s5.08 25.41 25.41 25.41 25.41-5.08 25.41-25.41S45.74 0 25.41 0zm-4.17 39.31A9.73 9.73 0 1 1 31 29.58a9.75 9.75 0 0 1-9.76 9.73zm17.67-.4h-4.77V16.67H11.91v-4.76h27z"></path>
                    <circle cx="21.24" cy="29.58" r="4.96"></circle>
                  </g>
                </svg>
              </v-col>
              <v-col cols="12">
                <h3><p class="text-left"> 
                  © Copyright {{ new Date().getFullYear() }} - Abstract Studio Design, Inc. All rights reserved
                </p></h3>
              </v-col>
            </v-row>
          </v-container>
        </v-col> 
      </v-row>  
    </v-container>
  </v-footer>
  </v-app>
</template>

<script>
export default {
  data()  {return {
    footer:{
      listas:[
      {
      title: 'Abstract',
      listas: [ 'Start Trial', 'Pricing', 'Download' ],

      },
      {
        title: 'Resources',
        listas: [ 'Blog', 'Help Center', 'Release Notes', 'Status' ]
      },
      {
        title: 'Community',
        listas: [ 'Twitter', 'Linkedln', 'Facebook', 'Dribbble', 'Podcast' ]
      },
      {
        title: 'Company',
        listas: ['About Us', 'Careers', 'Legal']
      },
      // {
      //   title: 'Contact Us',
      //   listas: ['info@abstract.com']
      // }
      ]
    }
  }}
}
</script>