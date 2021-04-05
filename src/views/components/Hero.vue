<template>
  <section id="hero" class="section-hero section-shaped my-0">
    <div class="shape shape-style-1 shape-primary">
      <span class="span-150"></span>
      <span class="span-50"></span>
      <span class="span-50"></span>
      <span class="span-75"></span>
      <span class="span-100"></span>
      <span class="span-75"></span>
      <span class="span-50"></span>
      <span class="span-100"></span>
      <span class="span-50"></span>
      <span class="span-100"></span>
    </div>
    <div class="container shape-container d-flex align-items-center">
      <div class="col px-0">
        <div class="row justify-content-center align-items-center">
          <div class="col-lg-7 text-center pt-lg">
            <img
              src="img/brand/white.png"
              style="width: 300px"
              class="img-fluid"
            />
            <p class="lead text-white mt-4 mb-5">
              Open Block 提供基于 PoS 共识币种的 Staking
              服务，专注于公有链节点和社区生态建设。为用户资产增值，为区块链贡献力量。
            </p>
            <div class="btn-wrapper">
              <!-- <base-button tag="a"
                                         href="https://demos.creative-tim.com/vue-argon-design-system/documentation"
                                         class="mb-3 mb-sm-0"
                                         type="info"
                                         icon="fa fa-code">
                                Components
                            </base-button> -->
              <base-button
                tag="a"
                href="https://www.creative-tim.com/product/vue-argon-design-system"
                class="mb-3 mb-sm-0"
                type="white"
                icon="ni ni-cloud-download-95"
              >
                开始委托
              </base-button>
            </div>
          </div>
        </div>
        <div
          class="row align-items-center justify-content-around stars-and-coded"
          style="display: none"
        >
          <div class="col-sm-4">
            <span class="text-white alpha-7 ml-3">Star us on</span>
            <a
              href="https://github.com/creativetimofficial/argon-design-system"
              target="_blank"
              title="Support us on Github"
            >
              <img
                src="img/brand/github-white-slim.png"
                style="height: 22px; margin-top: -3px"
              />
            </a>
          </div>
          <div class="col-sm-4 mt-4 mt-sm-0 text-right">
            <span class="text-white alpha-7">Coded by</span>
            <a
              href="https://www.creative-tim.com"
              target="_blank"
              title="Creative Tim - Premium Bootstrap Themes and Templates"
            >
              <img
                src="img/brand/creativetim-white-slim.png"
                class="ml-3"
                style="height: 30px"
              />
            </a>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>
<script>
export default {
  mounted: function () {
    window.particlesJS("particles-js", {
      particles: {
        number: { value: 6, density: { enable: true, value_area: 800 } },
        color: { value: "#1b1e34" },
        shape: {
          type: "polygon",
          stroke: { width: 0, color: "#000" },
          polygon: { nb_sides: 6 },
          image: { src: "img/github.svg", width: 100, height: 100 },
        },
        opacity: {
          value: 0.3,
          random: true,
          anim: { enable: false, speed: 1, opacity_min: 0.1, sync: false },
        },
        size: {
          value: 39.45738208161363,
          random: false,
          anim: { enable: true, speed: 10, size_min: 40, sync: false },
        },
        line_linked: {
          enable: false,
          distance: 200,
          color: "#ffffff",
          opacity: 1,
          width: 2,
        },
        move: {
          enable: true,
          speed: 8,
          direction: "none",
          random: false,
          straight: false,
          out_mode: "out",
          bounce: false,
          attract: { enable: false, rotateX: 600, rotateY: 1200 },
        },
      },
      interactivity: {
        detect_on: "canvas",
        events: {
          onhover: { enable: false, mode: "grab" },
          onclick: { enable: false, mode: "push" },
          resize: true,
        },
        modes: {
          grab: { distance: 400, line_linked: { opacity: 1 } },
          bubble: {
            distance: 400,
            size: 40,
            duration: 2,
            opacity: 8,
            speed: 3,
          },
          repulse: { distance: 200, duration: 0.4 },
          push: { particles_nb: 4 },
          remove: { particles_nb: 2 },
        },
      },
      retina_detect: true,
    });
    var count_particles, stats, update;
    stats = new Stats();
    stats.setMode(0);
    stats.domElement.style.position = "absolute";
    stats.domElement.style.left = "0px";
    stats.domElement.style.top = "0px";
    document.body.appendChild(stats.domElement);
    count_particles = document.querySelector(".js-count-particles");
    update = function () {
      stats.begin();
      stats.end();
      if (
        window.pJSDom[0].pJS.particles &&
        window.pJSDom[0].pJS.particles.array
      ) {
        count_particles.innerText = window.pJSDom[0].pJS.particles.array.length;
      }
      requestAnimationFrame(update);
    };
    requestAnimationFrame(update);
  },
};
</script>
<style>
</style>
