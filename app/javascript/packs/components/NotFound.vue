<template>
  <v-card
    class="mx-auto mt-10" elevation="3"
    max-width="1200"
    outlined>
    <div class="d-flex flex-no-wrap justify-space-between">
      <v-list-item three-line>
        <v-list-item-content>
          <v-list-item-title class="black--text">Профессиональный клинический психолог, коуч, гештальт-терапевт.</v-list-item-title>

          <ul class="skills no-list-deco">
            <li> Автор и ведущая женских терапевтических групп.</li>

            <li> Большой опыт работы по специализации:
              психосоматика женской репродуктивной системы, личностные кризисы,
              вопросы самооценки, отношения с партнерами, формирования и достижения целей;
            </li>
          </ul>
          <v-list-item-title bold>Направления:</v-list-item-title>
          <ul class="skills">

            <li v-for="sk in skills" >
              {{sk}}
            </li>
          </ul>

        </v-list-item-content>
        <v-list-item-avatar
          tile
          width="360"
          height="406"
          color="pink lighten-4"
        ><img :src="require('images/da360.jpg')" alt=""></v-list-item-avatar>
      </v-list-item>
    </div>
  </v-card>

</template>
<script>
  export default {
    name: "TopMenu",
    data() {
      return {
        skills: [
          "Межличностные, семейные, в том числе детско-родительские отношения (конфликты, разводы, измены);",
          "Посттравматические и стрессовые расстройства (потери, ПТСР, тревога, страхи, фобии);",
          "Психосоматические симптомы неясной этиологии (головные боли, боли в спине, суставах, мышцах, нарушение менструального цикла, аллергии);",
          "Репродуктивное здоровье и планирование беременности;",
          "Самооценка, самоопределение и целеполагание;",
          "Женская психология (Я-образ, самооценка и самоценность, предназначение).",
          "Потеря радости в жизни, страхи, тревоги, неуверенность в себе, стыд;",
          "Раздражительность, хроническая усталость, нервозность."],
      }
    }
  }

</script>
