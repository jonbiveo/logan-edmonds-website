<template>
  <v-card max-width="900px" class="mx-auto mb-12 transparent" flat>
    <div class="text-center">
      <v-btn class="ma-4" rounded outlined href="Edmonds_Logan.pdf" download>
        Download PDF
      </v-btn>
    </div>
    <v-card-title primary-title class="justify-center text-h2">
      Logan Edmonds
    </v-card-title>
    <v-row justify="center">
      <v-btn icon href="https://github.com/jonbiveo" target="_blank">
        <v-icon class="pa-2">mdi-github</v-icon>
      </v-btn>
      <v-btn icon href="https://www.linkedin.com/in/logantedmonds/" target="_blank">
        <v-icon class="pa-2">mdi-linkedin</v-icon>
      </v-btn>
      <v-btn icon href="mailto:logantedmonds@gmail.com">
        <v-icon class="pa-2">mdi-email</v-icon>
      </v-btn>
    </v-row>

    <v-card-text class="mb-n3 text-h4 font-weight-bold">
      Technical Skills
    </v-card-text>
    <v-divider></v-divider>

    <v-card-text class="mb-n7 text-subtitle-1 font-weight-bold">
      Languages & Software
    </v-card-text>
    <v-card-text class="px-8">
      JavaScript, Java, Vue.js, React, Nuxt.js, Node.js, HTML, CSS, Spring Boot, Bootstrap, Vuetify, PostgreSQL, MongoDB, Reach
    </v-card-text>
    <v-card-text class="mb-n7 text-subtitle-1 font-weight-bold">
      Tools, Techniques & OS
    </v-card-text>
    <v-card-text class="px-8">
      VS Code, IntelliJ IDEA, Windows, Linux, JUnit, Integration Testing, TDD, Git, Jira, Agile, Kanban, Scrum
    </v-card-text>

    <v-card-text class="mb-n3 text-h4 font-weight-bold">
      Education
    </v-card-text>
    <v-divider></v-divider>

    <v-card-text class="mb-n7 d-flex justify-space-between">
    <span class="text-subtitle-1 font-weight-bold">Tech Elevator &#8212; National Live Remote</span><span>June 2021 &#8212; October 2021</span>
    </v-card-text>
    <v-card-text class="px-8">
      Graduated from a 14-week coding bootcamp learning how to develop dynamic web-based software systems using Java, JavaScript, and Vue.js
    </v-card-text>
    <v-card-text class="mb-n7 d-flex justify-space-between">
      <span class="text-subtitle-1 font-weight-bold">Houston Community College &#8212; Houston, TX</span><span>August 2017 &#8212; May 2019</span>
    </v-card-text>
    <v-card-text class="px-8">
      Earned credits towards an Associate of Arts in Business. Looking to obtain a Bachelor's of Computer Science.
    </v-card-text>

    <v-card-text class="mb-n3 text-h4 font-weight-bold">
      <v-icon x-large>mdi-unfold-more-vertical</v-icon>
      Projects
    </v-card-text>
    <v-divider></v-divider>

    <v-card-text class="mb-n7 text-subtitle-1 font-weight-bold">
      <v-icon medium>mdi-ethereum</v-icon>
      <a href="http://nucarbit.cc/" target="_blank">NuCarbit.cc (ETHDenver Hackathon 2022)</a>
    </v-card-text>
    <v-card-text class="px-8">
      A hackathon project built around the idea of providing carbon credit security via blockchain tokenization. Built the front-end for this project, with MetaMask and Coinbase wallet functionality.
    </v-card-text>

    <v-card-text class="mb-n7 text-subtitle-1 font-weight-bold">
      <v-icon medium>mdi-ethereum</v-icon>
      <a href="https://github.com/jonbiveo/logan-edmonds-morra" target="_blank">Morra</a>
    </v-card-text>
    <v-card-text class="px-8">
      A blockchain smart contract game built with Reach and React. Attended a 6 week training on Reach and built this morra game as my final project. Reach is compatible with Ethereum, Algorand and Conflux.
    </v-card-text>

    <v-card-text class="mb-n7 text-subtitle-1 font-weight-bold">
      <v-icon medium>mdi-ethereum</v-icon>
      <a href="https://github.com/Tuxman/crypto-goals" target="_blank">Crypto Goals Tracker</a>
    </v-card-text>
    <v-card-text class="px-8">
      Application to track and calculate cryptocurrencies projected and historical data using Vue.js. Planning to employ GraphQL, MongoDB, and Nuxt.js. Goal is to authenticate users, track types of coins, graph and project value of coins. Use historical data for predictive analytics of future values.
    </v-card-text>

    <v-card-text class="mb-n7 text-subtitle-1 font-weight-bold">
      <v-icon medium>mdi-home</v-icon>
      <a href="https://github.com/jonbiveo/house-planner" target="_blank">House Planner</a>
    </v-card-text>
    <v-card-text class="px-8">
      Vue.js frontend application with a Java backend. House planner that allows you to select the most common options when building a house and displays approximate cost according to an external API’s information. Coded login, registration, and requirements for passwords on a 4-person virtual team. Contributed to front-end design and back-end logic.
    </v-card-text>

    <v-card-text class="mb-n7 text-subtitle-1 font-weight-bold">
      <v-icon medium>mdi-currency-usd</v-icon>
      <a href="https://github.com/jonbiveo/tenmo" target="_blank">TEnmo (Tech Elevator Venmo Clone)</a>
    </v-card-text>
    <v-card-text class="px-8">
      Designed and co-developed a peer-to-peer pseudo-currency transfer command line application utilizing RESTful API, PostgreSQL database, and Java. Users are able to send, request, and approve transfers.
    </v-card-text>


    <v-card-text class="mb-n3 text-h4 font-weight-bold">
      Professional Experience
    </v-card-text>
    <v-divider></v-divider>


    <v-card-text class="mb-n7 mt-3 d-flex justify-space-between">
      <span class="text-subtitle-1 font-weight-bold">Topl &#8212; Software Engineer Intern</span><span>June 2022 &#8212; May 2022</span>
    </v-card-text>
    <v-card-text class="px-8 my-n7">
      <v-icon x-small class="pa-n9">mdi-rhombus-medium</v-icon>
      Participated in code reviews with senior engineers and gained experience in writing custom, scalable code
    </v-card-text>
    <v-card-text class="px-8 my-n7">
      <v-icon x-small class="pa-n9">mdi-rhombus-medium</v-icon>
      Developed code following common security practices and development design patterns
    </v-card-text>
    <v-card-text class="mb-n7 d-flex justify-space-between">
      <span class="text-subtitle-1 font-weight-bold">Target &#8212; Stocker</span><span>February 2019 &#8212; May 2021</span>
    </v-card-text>
    <v-card-text class="px-8 my-n7">
      <v-icon x-small class="pa-n9">mdi-rhombus-medium</v-icon>
      Reliable team member who greeted guests with a smile and the expertise to assist with any questions
    </v-card-text>
    <v-card-text class="px-8 my-n7">
      <v-icon x-small class="pa-n9">mdi-rhombus-medium</v-icon>
      Used communication and attention to detail skills to guarantee proper receiving and stocking of products
    </v-card-text>
    <v-card-text class="mb-n7 mt-3 d-flex justify-space-between">
      <span class="text-subtitle-1 font-weight-bold">Torchy's Tacos &#8212; Cashier</span><span>June 2018 &#8212; February 2019</span>
    </v-card-text>
    <v-card-text class="px-8 my-n7">
      <v-icon x-small class="pa-n9">mdi-rhombus-medium</v-icon>
      Maintained customer facing area while attending to needs of customers
    </v-card-text>
    <v-card-text class="px-8 my-n7">
      <v-icon x-small class="pa-n9">mdi-rhombus-medium</v-icon>
      Performed all order taking operations while promoting monthly products quickly and accurately
    </v-card-text>
    <v-card-text class="px-8 my-n7">
      <v-icon x-small class="pa-n9">mdi-rhombus-medium</v-icon>
      Worked as a team with bartenders and servers in order to ensure prompt service
    </v-card-text>
  </v-card>
</template>

<script>
export default {
  name: 'ResumeComp',
}
</script>

<style>

</style>