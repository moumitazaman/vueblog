<script setup>
import {ref} from 'vue'
import axios from 'axios'
import { RouterLink } from 'vue-router'
const categories = ref({})
async function fetchCategories(){
    try {
        const url = `https://basic-blog.teamrabbil.com/api/post-categories`
        const res = await axios.get(url)
        Object.assign(categories.value, res.data)
    } catch (error) {
        console.error(error)
        return []
    }
}
fetchCategories()
  </script>
  <template>
    <section id="navArea">
      <nav class="navbar navbar-inverse" role="navigation">
        <div class="navbar-header">
          <button type="button" class="navbar-toggle collapsed" data-toggle="collapse" data-target="#navbar" aria-expanded="false" aria-controls="navbar"> <span class="sr-only">Toggle navigation</span> <span class="icon-bar"></span> <span class="icon-bar"></span> <span class="icon-bar"></span> </button>
        </div>
        <div id="navbar" class="navbar-collapse collapse">
          <ul class="nav navbar-nav main_nav" v-for="(category, index) in categories" :key="index">
           
            <li><RouterLink to="/">{{ category.name }}</RouterLink></li>
          </ul>
        </div>
      </nav>
    </section>
  </template>
  <style></style>