<template>
  <html>

  <body>
    <nav class="navbar navbar-expand-lg navbar-default fixed-top raja-nav">
      <a class="navbar-brand" href="https://rajabrawijaya.ub.ac.id">Fr-Store</a>
      <button class="navbar-toggler custom-toggler float-xs-right" type="button" data-toggle="collapse"
        data-target="#menu-raja" aria-controls="menu-raja" aria-expanded="false" aria-label="Toggle navigation">
        <span class="navbar-toggler-icon"></span>
      </button>

      <div class="collapse navbar-collapse" id="menu-raja">
        <ul class="navbar-nav mr-auto mt-2 mt-lg-0">
          <li class="nav-item active">
            <a class="nav-link" href="#">Home</a>
          </li>
          <li class="nav-item">
            <a class="nav-link" href="#">Shop</a>
          </li>
          <li class="nav-item">
            <a class="nav-link" href="#">Features</a>
          </li>
          <li class="nav-item">
            <a class="nav-link" href="#">Pages</a>
          </li>
          <li class="nav-item">
            <a class="nav-link" href="#">Blog</a>
          </li>
        </ul>
        <ul class="navbar-nav my-2 my-lg-0">
          <li class="nav-item">
            <a class="nav-link" href="#"><i class="fas fa-search"></i></a>
          </li>
          <li class="nav-item">
            <a class="nav-link" href="#"><i class="fas fa-user"></i></a>
          </li>
          <li class="nav-item">
            <a class="nav-link" href="#"><i class="fa fa-shopping-cart"></i></a>
          </li>
        </ul>
      </div>
    </nav>
    <!-- slider -->

    <div>
      <b-carousel id="carousel-1" v-model="slide" :interval="5000"  fade indicators background="#ababab"
        style="text-shadow: 1px 1px 2px #333;;" @sliding-start="onSlideStart" @sliding-end="onSlideEnd">
        <!-- Text slides with image -->
        <b-carousel-slide caption="First slide" text="Nulla vitae elit libero, a pharetra augue mollis interdum."
          img-src="/image/compass.jpg"></b-carousel-slide>

        <!-- Slides with custom text -->
        <b-carousel-slide img-src="/image/ellesse.jpg">
          <h1>Hello world!</h1>
        </b-carousel-slide>

        <!-- Slides with custom text -->
        <b-carousel-slide img-src="/image/lacoste2.jpg">
          <h1>Hello world!</h1>
        </b-carousel-slide>

       
      </b-carousel>
    </div>
    <!-- end slider -->

  <div id="category-sect">
    <h4 class="font-weight-bold pt-5 text-center"> Shop By Category </h4>
      <section id="tabs" class="project-tab">
        <div class="container-fluid">
            <div class="row justify-content-center">
                <div class="col-md-12">
                    <b-tabs content-class="mt-3" fill>
                    <b-tab title="Sneakers" active>
                    <ul class="container mt-4">
                          <div class="row justify-content-center">
                        <div v-for="(sneaker, index) in sneakers" :key="index" class="my-3 mr-2 text-center">
                          <div class="product-image">
                            <img :src="/image/ + fs + index + filetype" class="img-responsive h-100 w-100 "/>
                            </div>
                          <div class="product-details">
                            <h6 class="display-6 mt-3">{{ sneaker.name }}</h6>
                            <h6 class="display-6 text-muted">Rp.{{ sneaker.price }}</h6>
                          </div>
                        </div>
                    </div>
                    </ul>
                    </b-tab>
                    <b-tab title="Jacket">
                      <ul class="container mt-4">
                          <div class="row justify-content-center">
                        <div v-for="(jacket, index) in jacket" :key="index" class="my-3 mr-2 text-center">
                          <div class="product-image">
                            <img :src="/image/ + fs + index + filetype" class="img-responsive h-100 w-100"/>
                            </div>
                          <div class="product-details">
                            <h6 class="display-6 mt-3">{{ jacket.name }}</h6>
                            <h6 class="display-6 text-muted">Rp.{{ jacket.price }}</h6>
                          </div>
                        </div>
                    </div>
                    </ul>
                      </b-tab>
                    <b-tab title="Polo shirt">
                      <ul class="container mt-4">
                          <div class="row justify-content-center">
                        <div v-for="(polo, index) in polo" :key="index" class="my-3 mr-2 text-center">
                          <div class="product-image">
                            <img :src="/image/ + fs + index + filetype" class="img-responsive h-100 w-100 "/>
                            </div>
                          <div class="product-details">
                            <h6 class="display-6 mt-3">{{ polo.name }}</h6>
                            <h6 class="display-6 text-muted">Rp.{{ polo.price }}</h6>
                          </div>
                        </div>
                    </div>
                    </ul>
                    </b-tab>
                  </b-tabs>

                    </div>
                </div>
            </div>
            </section>
        </div>
 

  <!-- footer -->
  <footer>
        <div class="container">         
            <div class="row">
                <div class="col-md-3 col-sm-6">
                    <h3>Quick Links</h3>
                    <ul>
                        <li><a href="#">Link First</a></li>
                        <li><a href="#">Link Second</a></li>
                        <li><a href="#">Link Third</a></li>
                        <li><a href="#">Link Fourth</a></li>
                        <li><a href="#">Link Fifth</a></li>
                    </ul>
                </div>
                <div class="col-md-3 col-sm-6">
                    <h3>Our Services</h3>
                    <ul>
                        <li><a href="#">Link First</a></li>
                        <li><a href="#">Link Second</a></li>
                        <li><a href="#">Link Third</a></li>
                        <li><a href="#">Link Fourth</a></li>
                        <li><a href="#">Link Fifth</a></li>
                    </ul>
                </div>
                <div class="col-md-3 col-sm-6">
                    <h3>Our Programs</h3>
                    <ul>
                        <li><a href="#">Link First</a></li>
                        <li><a href="#">Link Second</a></li>
                        <li><a href="#">Link Third</a></li>
                        <li><a href="#">Link Fourth</a></li>
                        <li><a href="#">Link Fifth</a></li>
                    </ul>
                </div>
                <div class="col-md-3 col-sm-6">
                    <h3 class="mb-4">Fr-store</h3>
                    <form action="">
                        <div class="input-group">
                            <input type="text" class="form-control" placeholder="Enter Your Email Id*">
                            <div class="input-group-append">
                                <button class="btn btn-dark" type="button">Submit</button>
                            </div>
                        </div>
                    </form>
                    <p>Subscribe Now and stay updated</p>
                </div>

                <!-- Copyright section -->
                <div class="col-12">
                    <hr>
                    <div class="row">
                        <div class="col-md-7">
                            <!-- Social Links -->
                            <div class="follow-us">
                                <a href="#"><i class="fab fa-facebook-f"></i> Facebook</a>
                                <a href="#"><i class="fab fa-twitter"></i> Twitter</a>
                                <a href="#"><i class="fab fa-instagram"></i> Instagram</a>
                                
                            </div>
                        </div>
                        <div class="col-md-5">
                            <p class="text-right">© 2019 Fr-store <a href="" target="_blank" rel="noopener noreferrer"></a></p>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </footer>
<!--end footer -->
 </body>
  </html>
</template>

<script>
  import axios from 'axios'
  import 'bootstrap/dist/css/bootstrap.css'
  import 'bootstrap-vue/dist/bootstrap-vue.css'
  import '@fortawesome/fontawesome-free/css/all.css'
  import '@fortawesome/fontawesome-free/js/all.js'

  export default {
    name: 'App',
    data() {
      return {
        slide: 0,
        sliding: null,
        fs: 'sneakers',
        fj: 'jacket',
        fp: 'polo',
        filetype: '.jpg',
        sneakers: [],
        jacket: [],
        polo: []
      }
    },
    async created() {
      const baseURI = 'db.json'
      axios.get(baseURI).then((result) => {
        this.sneakers = result.data.sneakers
        this.jacket = result.data.jacket
        this.polo = result.data.polo
      })
    }

  }
</script>

<style>
  @import 'assets/navbar.css';

  #app {
    font-family: Avenir, Helvetica, Arial, sans-serif;
    -webkit-font-smoothing: antialiased;
    -moz-osx-font-smoothing: grayscale;
    text-align: center;
    color: #2c3e50;
    margin-top: 60px;
  }

  * {
    padding: 0;
    margin: 0;
  }

  html,
  body {
    height: 100%;
  }

 

  #my-jumbotron {
    background-size: cover;
    overflow: hidden;
  }

  #jumbo-text-contain {
    color: black;
    min-height: 400px;
  }

  #jumbotron-btn {
    font-size: 20px;
    border: 3px solid;
    border-radius: 0;
    transition: 0.3s;
  }

  #jumbotron-btn:hover {
    color: white;
    border: 1px solid white;
  }

  #products-container li {
    list-style-type: none;
    height: 250px;
  }
 

  .product-image {
    background: #f4f4ef;
    width: 250px;
    height: 275px;
  }

  .project-tab {
    padding: 10%;
    margin-top: -8%;
  }

  .project-tab #tabs {
    background: #007b5e;
    color: #eee;
  }

  .project-tab #tabs h6.section-title {
    color: #eee;
  }

  .project-tab #tabs .nav-tabs .nav-item.show .nav-link,
  .nav-tabs .nav-link.active {
    color: #20232a;
    background-color: transparent;
    border-color: transparent transparent #f3f3f3;
    border-bottom: 3px solid !important;
    font-size: 16px;
    font-weight: bold;
  }

  .project-tab .nav-link {
    border: 1px solid transparent;
    border-top-left-radius: .25rem;
    border-top-right-radius: .25rem;
    color: #acbebe;
    font-size: 16px;
    font-weight: 600;
  }

  .project-tab .nav-link:hover {
    border: none;
  }

  .project-tab thead {
    background: #f3f3f3;
    color: #333;
  }

  .project-tab a {
    text-decoration: none;
    color: #333;
    font-weight: 600;
  }

  .page-footer {
    color: rgb(0, 0, 0);
    background: #20232a;
  }
footer {
    padding: 50px 0px 20px;
    background-color: powderblue;
    
}
footer ul {
    padding: 0px;
}
footer ul li {
    list-style: none;
}
footer ul li a {
    padding: 3px 0px;
    display: block;
}
footer a {
    font-size: 16px;
    color: rgb(0, 0, 0);
    text-decoration: none;
}
footer a:hover {
    color: green;
    text-decoration: none;
}
footer p {
    color: black;
    margin: 0;
    font-size: 16px;
    padding: 8px 6px;
}
footer h3 {
    font-size: 20px;
    color: green;
}
.follow-us a {
    padding: 8px 6px;
    display: inline-block;
}
  
  @media only screen and (min-width: 1100px) {
   .carousel-item {
    height: 100vh;
    background-size: cover;
  }
}
</style>