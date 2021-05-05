<template>
  <div id="app">
   <!-- <Frame><img src='assests/pic.jpg'></Frame> -->
   <Frame>
     <template v-slot:default="{user = {}}">
        {{user.lastName}}
    </template>
     <!-- <h2 slot="title">{{title}}</h2>
     <p slot="text">I'm the paragrapgh text for the slot</p> -->

     <!-- <template v-slot:header>
       <h1>Here might be a page title</h1>
     </template> -->

        <!--Now everything inside the <template> elements will be passed to the 
          corresponding slots. 
          Any content not wrapped in a <template> using v-slot is assumed to be for the default slot.  -->
        <p>A paragraph for the main content.</p>
        <p>And Another one</p>

     <!-- <template v-slot:footer>
      <p>Here's some contact info</p>
     </template> -->

     <!-- To represent Scoped Slot-->
     
         
  
   </Frame>
  
  </div>
</template>

<script>
import Frame from './components/Frame'
export default {
  name: 'app', 
  components: {
    //Registering the component
    'Frame': Frame
  },
  data () {
    return {
    //   api_key: 'd726d4d33b9a988987b0e108986dbd03'
    //define all the data in the parent 
     title :"I'm the dynamic slot",
     
    }
  }
}
</script>

<style>

</style>
