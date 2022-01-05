
  <template>
  <v-container>
    <v-row>
      <v-col
      class="text-center"

      v-for="user in users"
      :key="user.name"
      cols="4"
      >

    <ProfileBox
    :name="user.name"
    :color="user.color"
    :quote="user.quote"
    :likes="user.likes"
    :shares="user.shares"
    :avatar="user.avatar"
    
   
    >
   

      </ProfileBox>
       <v-btn
        @click="user.likes+=1" 
              icon
              x-large
              color="pink"
            >
              <v-icon>mdi-heart</v-icon>
            </v-btn>
        
         <v-btn 
          @click="user.shares+=1"
              icon
              x-large
              :color="user.color"
            >
              <v-icon>mdi-share-variant</v-icon>
            </v-btn>


      </v-col>
      <v-col
      class="text-center"

      v-for="user in users"
      :key="user.name"
      cols="4"
      >
      <ProfileStats
      :values="user.values"
      :color="user.color"
      >
      </ProfileStats>
      </v-col>

    </v-row>
    </v-container>

    
  
 
</template>

<script>
import ProfileBox from "../components/ProfileBox.vue"
import ProfileStats from "../components/ProfileStats.vue"
  export default {
    data: () => ({
      users:[
        {
          name:"Shakeeb",
          quote:"",
          color:"teal",
          likes:12,
          shares:12,
          avatar:"https://static01.nyt.com/images/2021/09/14/science/07CAT-STRIPES/07CAT-STRIPES-mediumSquareAt3X-v2.jpg",
          values:Array.from({length: 10}, () => Math.floor(Math.random() * 40)),
          
          
        },
         {
          name:"Abud",
          quote:"CDF",
          color:"blue",
          likes:12,
          shares:12,
          avatar:"https://static01.nyt.com/images/2021/09/14/science/07CAT-STRIPES/07CAT-STRIPES-mediumSquareAt3X-v2.jpg",
          values:Array.from({length: 10}, () => Math.floor(Math.random() * 40)),

        },
         {
          name:"Hamada",
          quote:"GHI",
          color:"green",
          likes:12,
          shares:12,
          avatar:"https://static01.nyt.com/images/2021/09/14/science/07CAT-STRIPES/07CAT-STRIPES-mediumSquareAt3X-v2.jpg",
          values:Array.from({length: 10}, () => Math.floor(Math.random() * 40)),

        },
      ]

    }) ,
    components:{
      ProfileBox,
      ProfileStats
    }
  }
</script>
