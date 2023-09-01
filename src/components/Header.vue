  <script setup>
import { RouterLink} from 'vue-router'

  </script>
  <template>
       <header id="header">
    <div class="row">
      <div class="col-lg-12 col-md-12 col-sm-12">
        <div class="header_top">
          <div class="header_top_left">
            <ul class="top_nav">
             <li> <RouterLink to="/">হোম </RouterLink></li>
              <li><RouterLink to="/about">আমাদের সম্পর্কে </RouterLink></li>
              <li><RouterLink to="/contact">যোগাযোগ </RouterLink></li>
            </ul>
          </div>
          <div class="header_top_right">
            <ul class="social_nav">
              <li class="facebook"><a href="#"></a></li>
              <li class="twitter"><a href="#"></a></li>
              <li class="flickr"><a href="#"></a></li>
              <li class="pinterest"><a href="#"></a></li>
              <li class="googleplus"><a href="#"></a></li>
              <li class="vimeo"><a href="#"></a></li>
              <li class="youtube"><a href="#"></a></li>
              <li class="mail"><a href="#"></a></li>
            </ul>
         
          </div>
        </div>
      </div>
      <div class="col-lg-12 col-md-12 col-sm-12">
        <div class="header_bottom">
          <div class="logo_area"><a href="/" class="logo"><img src="images/logo.jpg" alt=""></a></div>
        </div>
        
      </div>
    </div>
  </header>
  </template>
  <style scoped></style>