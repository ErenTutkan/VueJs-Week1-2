<template >
  <div>
      <div class="class--list--app">
      <div class="card">
        <ul class="class-list">
          <li>
            <label>
              <input class="mr-5" v-model="backgroundColor" type="checkbox" />
              <span>Background Color</span>
            </label>
          </li>
          <li>
            <label>
              <input class="mr-5" v-model="border" type="checkbox" />
              <span>Border</span>
            </label>
          </li>
          <li>
            <label>
              <input class="mr-5" v-model="borderRadius" type="checkbox" />
              <span>Border Radius</span>
            </label>
          </li>
          <li>
            <label>
              <input class="mr-5" v-model="fontColor" type="checkbox" />
              <span>Color</span>
            </label>
          </li>
          <li>
            <label>
              <input class="mr-5"  v-model="fontBold" type="checkbox" />
              <span>Font Bold</span>
            </label>
          </li>
          <li>
            <label>
              <input class="mr-5" v-model="fontItalic" type="checkbox" />
              <span>Font Italic</span>
            </label>
          </li>
        </ul>

        <textarea rows="5" :class="[{'red':backgroundColor},{'border':border},{'border-radius':borderRadius}
        ,{'font-color':fontColor},{'font-bold':fontBold},{'font-italic':fontItalic}]"></textarea>
      </div>
    </div> 
  </div>
  
</template>
<script>
export default {
    data(){
        return{
              backgroundColor:false,
            border:false,
            borderRadius:false,
            fontColor:false,
            fontBold:false,
            fontItalic:false
        }
      

    }
}
</script>
<style >
    .red{
        background-color: rgba(30, 0, 163, 0.842);
    }
    .border{
        border:10px solid yellow;
    }
    .border-radius{
        border-radius: 10px;
    }
    .font-color{
        color: yellow;
    }
    .font-bold{
        font-weight: bold;
    }
    .font-italic{
        font-style:italic;
    }
</style>