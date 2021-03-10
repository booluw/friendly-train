<template>
  <section>
    <div class="header header--secondary">
      <a href="tel:08035436131" class="secondary__link">
        <i class="lni lni-phone" />
        <span>08035436131</span>
      </a>
      <a href="mailto:info@laomiesglobal.com" class="secondary__link">
        <i class="lni lni-envelope" />
        <span>info@laomiesglobal.com</span>
      </a>
      <span class="secondary__link">
        <i class="lni lni-alarm-clock" />
        <b>OPEN</b>
      </span>
    </div>
    <input id="hamburger" type="checkbox">
    <header class="header">
      <nuxt-link to="/" class="header__link header__link--logo">
        <img src="~/assets/img/logo.webp" class="header__logo" alt="Laomies Global logo">
      </nuxt-link>
      <div class="header__fancy">
        <nav class="nav">
          <nuxt-link to="/" class="nav__link" exact-active-class="nav__link--active">
            home
          </nuxt-link>
          <nuxt-link to="/about" class="nav__link" exact-active-class="nav__link--active">
            about us
          </nuxt-link>
          <nuxt-link to="/fleet" class="nav__link" exact-active-class="nav__link--active">
            fleet
          </nuxt-link>
          <nuxt-link to="/career" class="nav__link" exact-active-class="nav__link--active">
            career
          </nuxt-link>
        </nav>
        <div class="header__social">
          <a href="//facebook.com/" class="header__link">
            <i class="lni lni-facebook-filled" />
          </a>
          <a href="//twitter.com/" class="header__link">
            <i class="lni lni-twitter-original" />
          </a>
          <a href="//linkedin.com/" class="header__link">
            <i class="lni lni-linkedin" />
          </a>
        </div>
        <label for="hamburger" class="hamburger" />
      </div>
    </header>
    <Nuxt />
    <footer class="footer">
      <div class="row justify-content-between align-items-end m-0">
        <div class="col-md-4 p-0 p-md-3">
          <h3 class="heading heading--sub">
            La'omies Global Marine Services Limited.
          </h3>
          <br>
          <p class="paragraph">
            KM 22, PortHarcourt Airport road,<br>
            Igwuruta, PortHarcourt, Rivers State.
          </p>
          <div class="mt-3">
            <a href="tel:08035436131" class="footer__link">08035436131</a>
            <a href="tel:08075870000" class="footer__link">08075870000</a>
            <a href="tel:08034362024" class="footer__link">08034362024</a>
          </div>
        </div>
        <div class="col-md-3 p-0 p-md-3 pt-md-5 mt-md-5">
          <div class="header__social justify-content-end">
            <a href="//facebook.com/" class="header__link">
              <i class="lni lni-facebook-filled" />
            </a>
            <a href="//twitter.com/" class="header__link">
              <i class="lni lni-twitter-original" />
            </a>
            <a href="//linkedin.com/" class="header__link">
              <i class="lni lni-linkedin" />
            </a>
          </div><br>
          <p style="text-align: right">
            &copy; La'omies Limited, 2021
          </p>
        </div>
      </div>
    </footer>
  </section>
</template>
