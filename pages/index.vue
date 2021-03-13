<template>
  <main class="page">
    <section class="jumbotron" :style="'background-image: url('+require(`~/assets/img/${currentImg}`)+');background-position: center;background-size: cover;'">
      <div class="row align-items-center m-0">
        <div v-if="currentImg == 'jumbo.jpg'" class="col-md-5 p-0">
          <h1 class="heading heading--page mb-3">
            La'omies Global
          </h1>
          <p class="paragraph mb-5">
            Dedicated to responding promptly to our clients with daily reports to keep them abrest with current realities on the job procession.
          </p>
          <div class="d-flex justify-content-between col-md-9 p-0">
            <a href="#what-we-do" class="btn btn--secondary jumbotron__btn">
              learn more
            </a>
            <nuxt-link to="/contact" class="btn btn--cta jumbotron__btn">
              get in touch
            </nuxt-link>
          </div>
        </div>
        <div v-else-if="currentImg == 'Tokyo.jpg'" class="col-md-5 p-0">
          <h1 class="heading heading--page mb-3">
            Marine Security
          </h1>
          <p class="paragraph mb-5">
            With over two decades of experience, we have concentrated more on providing oiling,
            security and surveillance for oil and gas companies.
          </p>
          <div class="d-flex justify-content-between col-md-9 p-0">
            <nuxt-link to="/services" class="btn btn--cta jumbotron__btn">
              learn more
            </nuxt-link>
          </div>
        </div>
        <div v-else class="col-md-6 p-0">
          <h1 class="heading heading--page mb-3">
            Marine Logistics Services
          </h1>
          <p class="paragraph mb-5">
            Our experience and continous efforts over the years has made La'omies Global Marine Services Limited one
            of the most efficient and reliable companies in the maritime security and logistics segment.
          </p>
          <div class="d-flex justify-content-between col-md-9 p-0">
            <nuxt-link to="/services" class="btn btn--cta jumbotron__btn">
              learn more
            </nuxt-link>
          </div>
        </div>
        <div class="carousel-btns">
          <button class="btn btn--carousel mr-3" @click="prev()">
            <i class="lni lni-chevron-left" />
          </button>
          <button class="btn btn--carousel ml-3" @click="next()">
            <i class="lni lni-chevron-right" />
          </button>
        </div>
      </div>
    </section>
    <section class="section">
      <div class="row m-0 pb-5">
        <div class="col-md-7 px-0 py-3 p-md-3">
          <h2 class="heading heading--main">
            About us
          </h2>
          <p class="paragraph">
            La'omies Global Marine Services Limited is an indegenous company, fully registered with the
            <abbr title="CAC">CAC</abbr>. Our specialization is on the robust marine sector. We provide surveillance and
            security for multinationals. We also provide procurement, construction, installation, engineering, hiring of equipments and haulage services.
          </p>
          <nuxt-link to="/about-us" class="fancy-link mt-3">
            Read more
          </nuxt-link>
        </div>
      </div>
      <div class="row align m-0 mt-5">
        <div class="col-md-4 px-0 py-3 p-md-3">
          <div class="card">
            <div class="card__header">
              <i class="card__icon lni lni-invention" />
              <h3 class="card__heading">
                Vision
              </h3>
            </div>
            <div class="card__body">
              <p class="card__paragraph">
                To be a leading indigenous company of choice, prociding world class solution to
                a variety of problems while carrying out other programs with due diligence.
              </p>
            </div>
          </div>
        </div>
        <div class="col-md-4 px-0 py-3 p-md-3">
          <div class="card">
            <div class="card__header">
              <i class="card__icon lni lni-diamond-alt" />
              <h3 class="card__heading">
                Mission
              </h3>
            </div>
            <div class="card__body">
              <p class="card__paragraph">
                Business in Nigeria and beyond, committed to values and making impact wherever we go and to be the best in the country.
              </p>
            </div>
          </div>
        </div>
        <div class="col-md-4 px-0 py-3 p-md-3">
          <div class="card">
            <div class="card__header">
              <i class="card__icon lni lni-handshake" />
              <h3 class="card__heading">
                Belief
              </h3>
            </div>
            <div class="card__body">
              <p class="card__paragraph">
                Our company is therefore, committed to the understanding of today's hardwork and excellent results in success
                of the future. Hence, our clientele are rest assured of prompt and quality service delivery with results oriented professionals.
              </p>
            </div>
          </div>
        </div>
      </div>
    </section>
    <section class="section">
      <div class="row m-0 pb-5">
        <div class="col-md-7 px-0 py-3 p-md-3">
          <h2 class="heading heading--main">
            Marine security
          </h2>
          <p class="paragraph">
            With over two decades of experience, we have concentrated more on providing oiling, security and surveillance for oil and gas companies.
            We are also mindful of the enormity of the tasks along with the sensistive and professional nature of the business, with that we have assembled
            a highly dedicated workforce comprising of the senior and middle cadre security experts who help to design and implement maritime/industrial security concepts that
            conform to national and international standards.
          </p>
          <nuxt-link to="/services" class="fancy-link mt-3">
            Other services
          </nuxt-link>
        </div>
      </div>
      <div class="row justify-content-around m-0 mt-5">
        <div class="col-md-3 px-0 py-3 p-md-3">
          <div class="card card--bg">
            <h3 class="card__heading">
              Marine Logistics Services <br>
              <small>(Vessel chartering)</small>
            </h3>
          </div>
        </div>
        <div class="col-md-3 px-0 py-3 p-md-3">
          <div class="card card--bg">
            <h3 class="card__heading">
              Marine and Offshore security patrol
            </h3>
          </div>
        </div>
        <div class="col-md-3 px-0 py-3 p-md-3">
          <div class="card card--bg">
            <h3 class="card__heading">
              Armed and protective security <br>
              <small>for all types of vessel</small>
            </h3>
          </div>
        </div>
        <div class="col-md-3 px-0 py-3 p-md-3">
          <div class="card card--bg">
            <h3 class="card__heading">
              Port security
            </h3>
          </div>
        </div>
        <div class="col-md-3 px-0 py-3 p-md-3">
          <div class="card card--bg">
            <h3 class="card__heading">
              Meet 'N' Greet Services
            </h3>
          </div>
        </div>
        <div class="col-md-3 px-0 py-3 p-md-3">
          <div class="card card--bg">
            <h3 class="card__heading">
              Offshore catering Services
            </h3>
          </div>
        </div>
      </div>
    </section>
    <section class="section">
      <div class="row m-0">
        <div class="col-md-7 px-0 py-3 p-md-3">
          <h2 class="heading heading--main">
            Clients
          </h2>
        </div>
      </div>
      <div class="row justify-content-around m-0">
        <div class="col-md-3 px-0 py-3 p-md-3">
          <div class="card card--bg card--small card--chevron">
            <h3 class="card__heading">
              Chevron Nigeria Limited
            </h3>
          </div>
        </div>
        <div class="col-md-3 px-0 py-3 p-md-3">
          <div class="card card--bg card--small card--belema">
            <h3 class="card__heading">
              Belema Oil
            </h3>
          </div>
        </div>
        <div class="col-md-3 px-0 py-3 p-md-3">
          <div class="card card--bg card--small card--shell">
            <h3 class="card__heading">
              The Shell Petroleum Development Company of Nigeria Limited
            </h3>
          </div>
        </div>
        <div class="col-md-3 px-0 py-3 p-md-3">
          <div class="card card--bg card--small card--new-cross">
            <h3 class="card__heading card__heading--bl">
              New Cross Exploration And Production
            </h3>
          </div>
        </div>
        <div class="col-md-3 px-0 py-3 p-md-3">
          <div class="card card--bg card--small card--nnpc">
            <h3 class="card__heading">
              Nigeria National Petroleum Corporation
            </h3>
          </div>
        </div>
        <div class="col-md-3 px-0 py-3 p-md-3">
          <div class="card card--bg card--small card--delta">
            <h3 class="card__heading">
              Niger Delta Development Commission
            </h3>
          </div>
        </div>
      </div>
    </section>
  </main>
</template>
<script>
export default {
  data () {
    return {
      images: [
        'jumbo.jpg',
        'Tokyo.jpg',
        'Uni-assure.jpg'
      ],
      timer: null,
      currentIndex: 0
    }
  },
  computed: {
    currentImg () {
      return (this.images[Math.abs(this.currentIndex) % this.images.length])
    }
  },
  mounted () { this.slideStart() },
  methods: {
    slideStart () {
      this.timer = setInterval(this.next, 9000)
    },
    next () {
      this.currentIndex += 1
    },
    prev () {
      this.currentIndex -= 1
    }
  }
}
</script>
