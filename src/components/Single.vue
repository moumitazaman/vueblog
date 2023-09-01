<script setup>
import {ref} from 'vue'
import { useRoute } from 'vue-router';
import axios from 'axios'

const route = useRoute()
const postId = route.query.id

const post = ref({})

async function postDetails(){
    const url = `https://basic-blog.teamrabbil.com/api/post-details/${postId}`
    const res = await axios.get(url)
   return Object.assign(post.value, res.data)
}

console.log(postDetails())
</script>
<template>

  <section id="contentSection">
    <div class="row">
      <div class="col-lg-8 col-md-8 col-sm-8">
        <div class="left_content">
          <div class="single_page">
           
            <h1>{{post.title}}</h1>
            <div class="post_commentbox"> <a href="#"><i class="fa fa-user"></i>Admin</a> </div>
            <div class="single_page_content"> <img class="img-center" :src="post.img" alt="">
         <p>{{ post.content }}</p>
              
            </div>
            <div class="social_link">
              <ul class="sociallink_nav">
                <li><a href="#"><i class="fa fa-facebook"></i></a></li>
                <li><a href="#"><i class="fa fa-twitter"></i></a></li>
                <li><a href="#"><i class="fa fa-google-plus"></i></a></li>
                <li><a href="#"><i class="fa fa-linkedin"></i></a></li>
                <li><a href="#"><i class="fa fa-pinterest"></i></a></li>
              </ul>
            </div>
            
          </div>
        </div>
      </div>
      
      <div class="col-lg-4 col-md-4 col-sm-4">
     
      </div>
    </div>
  </section>
  


</template>
<style></style>