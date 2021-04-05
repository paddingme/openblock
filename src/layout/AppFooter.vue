<template>
    <footer class="footer">
        <div class="container container-lg" style="display:none">
            <div class="row">
                <div class="col-md-6 mb-5 mb-md-0">
                    <div class="card card-lift--hover shadow border-0">
                        <router-link to="/landing" title="Landing Page">
                            <img v-lazy="'img/theme/landing.jpg'" class="card-img">
                        </router-link>
                    </div>
                </div>
                <div class="col-md-6 mb-5 mb-lg-0">
                    <div class="card card-lift--hover shadow border-0">
                        <router-link to="/profile" title="Profile Page">
                            <img v-lazy="'img/theme/profile.jpg'" class="card-img">
                        </router-link>
                    </div>
                </div>
            </div>
        </div>
        <div class="container">
            <div class="row row-grid align-items-center my-md">
                <div class="col-lg-6">
                    <h3 class="text-primary font-weight-light mb-2">Trust in OpenBlock</h3>
                    <h4 class="mb-0 font-weight-light">Open Block Produce Consensus!</h4>
                </div>
                <div class="col-lg-6 text-lg-center btn-wrapper">
                    <a target="_blank" href="https://twitter.com/openblock"
                       class="btn btn-neutral btn-icon-only btn-twitter btn-round btn-lg" data-toggle="tooltip"
                       data-original-title="Follow us">
                        <i class="fa fa-twitter"></i>
                    </a>
                    <a target="_blank" href="https://weibo.com/openblock"
                       class="btn btn-neutral btn-icon-only  btn-round btn-lg btn-facebook btn-round btn-lg" data-toggle="tooltip"
                       data-original-title="Like us">
                        <i class="fa fa-weixin"></i>
                    </a>
                    <a target="_blank" href="https://weibo.com/openblock"
                       class="btn btn-neutral btn-icon-only  btn-round btn-lg btn-dribbble btn-lg btn-round" data-toggle="tooltip"
                       data-original-title="Like us">
                        <i class="fa fa-weibo"></i>
                    </a>
                    <a target="_blank" href="https://github.com/openblock"
                       class="btn btn-neutral btn-icon-only btn-github btn-round btn-lg" data-toggle="tooltip"
                       data-original-title="Star on Github">
                        <i class="fa fa-github"></i>
                    </a>
                </div>
            </div>
            <hr>
            <div class="row align-items-center justify-content-md-between">
                <div class="col-md-12">
                    <div class="copyright text-center">
                        &copy; {{year}}
                        <a href="https://openblock.pro" target="_blank" rel="noopener">Open Block</a>
                    </div>
                </div>
            </div>
        </div>
    </footer>
</template>
<script>
export default {
  name: 'app-footer',
  data() {
    return {
      year: new Date().getFullYear()
    }
  }
};
</script>
<style>
</style>
