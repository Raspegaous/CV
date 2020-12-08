<template>
  <main class="main" id="app">
    <header class="header">
      <Navbar name="Jérémy Bonnet" title="Développeur Web Junior"></Navbar>
      <Presentation></Presentation>
    </header>



    <section class="content">
      <Skill title="Compétences" :skills="skills"></Skill>
      <Pro v-for="pro in pros" :key="pro" :pro="pro"></Pro>
      <Divers :divers="divers"></Divers>
    </section>
    <footer class="footer">
      <h3>Disponible rapidement</h3>
    </footer>



  </main>
</template>

<script>
import './assets/styles/app.css'
import Skill from '@/components/Skill'
import Pro from '@/components/Pro'
import Navbar from "@/components/Navbar"
import Presentation from "@/components/Presentation"
import Divers from "@/components/Divers"

export default {
  name: 'App',
  components: {Skill, Pro, Navbar, Presentation, Divers},
  data() {
    return {
      skills: [{
        title: "Développement",
        list: [
          {name: "HTML", stars: 4},
          {name: "CSS", stars: 4},
          {name: "Javascript", stars: 4},
          {name: "PHP", stars: 3}
        ]
      }, {
        title: "Frameworks",
        list: [
          {name: "SASS", stars: 4},
          {name: "NodeJS", stars: 3},
          {name: "Laravel", stars: 3},
          {name: "Bootstrap", stars: 4}
        ]
      }, {
        title: "Logiciel",
        list: [
          {name: "Linux", stars: 4},
          {name: "Windows", stars: 4},
          {name: "IntelliJ", stars: 4},
          {name: "Git", stars: 3}
        ]
      }, {
        title: "Base de donnée",
        list: [
          {name: "MongoDB", stars: 3},
          {name: "MySQL", stars: 3},
          {name: "MariaDB", stars: 3},
        ]
      }],
      pros: [
        {name: "Expériences professionnelles", list: [
            {date: "2012 à maintenant", content: "Agent de sécurité Incendie - Société des Bains de Mer - Monaco - Sécurité incendie dans le domaine du Luxe à Monaco"},
            {date: "2008 à 2012", content: "Vendeur - Alphabet Monaco - Vente de produit scolaire, parascolaire. Gestion des stock, gestion informatique"},
            {date: "2007 à 2008", content: "Intérimaire - Monaco - Diverses missions intérim à Monaco"},
            {date: "2006 à 20015", content: "Sapeur Pompier Volontaire - Breil sur Roya"},
          ]},
        {name: "Formations & diplômes", list: [
            {date: "2020", content: "Dévelopeur Web Junior - OpenclassRoom (Ecole en ligne) - Niveau 4"},
            {date: "2007", content: "BAC Sciences et Techniques Industrielle, Génie Electrotechnique - Les Eukalyptus (Nice) - Niveau 2"},
            {date: "2004", content: "Brevet des collèges - L'eau Vive (Breil sur Roya)"},
          ]}
      ],
      divers: [
        {name: "Centre d'interêts", list: ["<i class=\"fa fa-code fa-2x\" aria-hidden=\"true\"></i>",  "<i class=\"fa fa-bicycle fa-2x\" aria-hidden=\"true\"></i>", "<i class=\"fa fa-video-camera fa-2x\" aria-hidden=\"true\"></i>"]},
        {name: "Qualités", list: ["Capacité à travaille en équipe", "Organisé", "Rigoureux", "Curieux", "Passioné"]}
      ]
    }
  }
}
</script>
