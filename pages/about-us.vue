<template>
  <main class="page">
    <section class="section section--y-small">
      <h2 class="heading heading--main">
        About Us
      </h2>
    </section>
    <section class="section py-0">
      <div class="row m-0">
        <div class="col-md-7 pb-5 p-0">
          <p class="paragraph">
            La'omies Global Marine Services Limited is an indigenous company, fully registered with the <abbr title="Coperate Affairs Commission">CAC</abbr>.
            Our specialization is on the robust marine sector. We provide surveillance and security for multinationals. We also provide procurement, construction, installation, engineering, hiring of equipments and haulage services.
          </p>
          <p class="paragraph">
            We are dedicated to responding promptly to our clients with daily reports to keep them abreast with cureent realities on the job in procession. We strive to provide them with the best services and ensure proper security for their vessels
            and with that we have entered into a Joint Operational Agreement (JOA) with the military/security agency and this is done within the legal and fiscal framework of a Memorandum of Understanding (MoU) agreed on by our clients. A reconnaissance survey is also done to ascertain the number of communities enroute our destination.
          </p>
        </div>
      </div>
    </section>
    <section class="section pt-0">
      <div class="row m-0">
        <div class="col-md-7 p-0">
          <h2 class="heading heading--sub">
            Our Story
          </h2>
          <p class="paragraph">
            In the wake of the early 2000s, when the Niger Delta region was largely characterized by violence, rode in <abbr title="Mister">Mr.</abbr> Amachree Ibinabo Sonny (aka Alabo), defied all odds and did some very critical escort moves for major drilling, maintenance and construction companies.
            He had a team of escort experts who were armed with requisite expertise to deliver these jobs without any hitch.
          </p>
          <p class="paragraph">
            <abbr title="Mister">Mr.</abbr> Amachree was the Community Liaison Officer for Dredging International. It was a time when working in a terrain as volatile as Kula, Ekulama I & II, Belema, Opukula, Boro and other Niger Delta communities. Despite the very many impossibilities of that period, he was able to handle the youths at the time
            and the project was executed and completed on the record time. That singular project ushered in companies such as <b>SDV Nig. Ltd</b>, <b>Dellatore Bezons Nig. Ltd (DBN)</b>, <b>Daewood Nig. Ltd</b>, <b>Jacon Nigeria Limited</b>, <b>Ikonibo Nigeria Limited</b>, <b>Beweic Engineering</b> and others.
          </p>
        </div>
        <div class="col-md-5 p-0 p-md-5">
          <img src="~/assets/img/amachree-ibinabo.jpeg" class="responsive-img" alt>
        </div>
      </div>
    </section>
    <section class="section py-0">
      <h2 class="heading heading--sub">
        Board of Directors
      </h2>
      <div class="row m-0 my-5">
        <div v-for="director in directors" :key="director.name" class="col-md-3">
          <div class="card card--about" @click="modal = director">
            <img :src="require(`~/assets/img/${director.img}`)" class="card__img" alt>
            <h3 class="card__heading">
              {{ director.name }}
            </h3>
            <h4 class="card__heading card__heading--sub mt-0">
              {{ director.portfolio }}
            </h4>
          </div>
        </div>
      </div>
    </section>
    <modal v-if="modal" :data="modal" @close="modal = null" />
  </main>
</template>

<script>
import { gsap } from 'gsap'
import { ScrollTrigger } from 'gsap/dist/ScrollTrigger'

import modal from '~/components/modal.vue'

if (process.client) {
  gsap.registerPlugin(ScrollTrigger)
}

export default {
  components: { modal },
  data () {
    return {
      directors: [
        {
          name: 'Amachree Ibinabo Sonny',
          text: `
            Amachree holds a Bachelor Degree in Public Administration from the University of PortHarcourt. He has worked with several marine related companies.<br /> He was onetime chairman, Kula Community Development Community (KCDC) and chairman, Kula Regional Development Council (KRDC); a trust board set up by Chevron Nig. Ltd. and Rivers State Government for the benefit of Kula Kingdom, a trust board saddled with the responsibility to interface between Chevron Nig. Ltd and Kula Kingdom vis CNL/Kula GMoU, also to manage the local contracts due Kula Kingdom and
            the management of the hundreds of million naira from the coffers of Chevron Nig. Ltd. for the development of Kula kingdom's communities.<br /> <br />He has wealth of experience in the marine and construction industries.
          `,
          portfolio: 'MD / CEO',
          img: 'amachree-ibinabo.jpeg'
        },
        {
          name: 'Ibiene Minabelari Hamilton',
          text: `
            Madam Ibiene holds stage two (2) in Pitmans. She has worked with the Nigeria Prisons Department and left the services voluntarily after 7 years.<br /> She held the post of treasurer in Kula Community Development Committee.
            Lastly she recently retired from the Rivers State Judiciary after many years of services.
          `,
          portfolio: 'Director',
          img: 'ibinene-minabelari.png'
        },
        {
          name: 'Brig. Gen. Ukagu Enang Mbang (Rtd)',
          text: `
            Ukang holds a bachelor degree in Public Administration and Masters degree in Development Studies from the University of PortHarcourt.<br /> He has worked with Bastam Services Ltd as a ICT Network Administrator and also with a marine related company. He has good experience in both Information and Communication Technology and Maritime Services.
          `,
          portfolio: 'Director',
          img: 'mma-dan.jpeg'
        },
        {
          name: 'Babra Philemon George',
          text: `
            Babra holds a Bachelor Degree in Mass Communication from Rivers State University of Science and Technology, PortHarcourt.<br />She is an HSE and IT consultant and has worked with Finale Concept Ltd.
          `,
          portfolio: 'Director',
          img: 'babra-philemon.jpeg'
        }
      ],
      modal: null
    }
  },
  head: {
    title: "About Us | La'omies Global",
    meta: [
      { hid: 'description', name: 'description', content: "At La'omies, We are dedicated to responding promptly to our clients with daily reports to keep them abreast with current realities on the job in procession. We strive to provide customers like you, with the best services and ensure proper security for your vessels." },
      { hid: 'keyword', name: 'keyword', content: "La'omies, safety first, vessel safety, maritime safety" }
    ]
  },
  mounted () {
    gsap.utils.toArray('.card').forEach((el, i) => {
      gsap.from(el, {
        scrollTrigger: {
          trigger: el,
          scrub: i
        },
        opacity: 0.6,
        y: '40px'
      })
    })
  }
}
</script>

<style>

</style>
