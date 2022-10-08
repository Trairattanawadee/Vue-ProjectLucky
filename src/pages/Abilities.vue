<template>
    <div>
      <Navbar />

      <h1 class="heading"> About <span>Me</span> </h1>
      <div class="content2">
          <p> <span>name : </span> Trairattanawadee Foythong </p>
          <p> <span>age : </span> 19 </p>
          <p> <span>email : </span> trairattanawade.foy@bumail.net </p>
          <p> <span>address : </span> Sisaket, Thailand 33110 </p>
          <p> <span>freelance : </span> available </p>
          <p> <span>Commission Avatar : </span> Close (Full) </p>
          <p> <span>skill : </span> All Photoshop &amp; Voice actor </p>
          <p> <span>language : </span> thai </p>
      </div>

      <h1 class="heading"> MY <span>Skills</span> </h1>
      <!---article-->
      <main class="content margin-auto">
        <article class="artical">
          <section class="text-center title">
            <h1>{{artical}} </h1>
          </section>
  
          <section class="row-50 bg-white center">
            <table class="table-cute">
              <tr>
            <h1><td>{{ sub_article }}</td></h1>
                <!--Emoji Windows: WIN+. or WIN+; | MAC: ^+Command+space-->
                <td>⭐⭐⭐⭐⭐</td>
              </tr>
              <tr>
            <h1><td>{{ sub_article1 }}</td></h1>
                <td>⭐⭐⭐⭐⭐</td>
              </tr>
              <tr>
            <h1><td>{{ sub_article2 }}</td></h1>
                <td>⭐⭐⭐⭐⭐</td>
              </tr>
              <tr>
            <h1><td>{{ sub_article3 }}</td></h1>
                <td>⭐⭐⭐⭐⭐</td>
              </tr>
              <tr>
                <h1><td>{{ sub_article4 }}</td></h1>
                <td>⭐⭐⭐⭐⭐</td>
              </tr>
              <tr>
            <h1><td>{{ sub_article5 }}</td></h1>
                <td>⭐⭐⭐⭐⭐</td>
              </tr>
            </table>
          </section>
        </article>
      </main>
    </div>
  </template>
  
  <script>
  import Navbar from "../components/Navbar.vue";
  export default {
    components: { Navbar },
    methods: {
      async fetchAbilities() {
        try {
          let res = await axios.get(
            "https://63416d1d20f1f9d79972d06d.mockapi.io/project/v1/luckyEX"
          );
          this.fetchAbilities = res.data;
        } catch (error) {}
      },
    },
    data() {
      return {
        
        sub_article: "Cooking",
        sub_article1: "Gaming",
        sub_article2: "Singing",
        sub_article3: "Photography",
        sub_article4: "Drawing",
        sub_article5: "Swiming",
      };
    },
    beforeMount() {
      this.fetchAbilities();
    },
  };
  </script>
  
  <style>
  </style>