<script>
export default {
    data() {
        return {    
            elementBody: [
            {
                title: "Save up 40% by paying weekly",
                number: "Number of courses",                
                time: "Time",
                webDesigning: "Web Designing",
                humanCentredDesign: "Human-Centred design",
                basicMarketing: "Basic Marketing",
                pytonForEverybody: "Pyton for Everybody",
                androidDeveloper: "Android developer",
                businessEnglish: "Business English"
            },
            ],        
            elements: [
            
            {
                title: 
                [{
                    img:"src/assets/img/icon/h5-custom-icon-7.png",
                    type:"Standard",
                    price:"$12",
                }],
                number: "2",                
                time: "15 Days",
                webDesigning: true,
                humanCentredDesign: true,
                basicMarketing: false,
                pytonForEverybody: false,
                androidDeveloper: false,
                businessEnglish: false
            },
            {
                title: 
                [{
                    img:"src/assets/img/icon/h5-custom-icon-8.png",
                    type:"Professional",
                    price:"$59",
                }],
                number: "4",                
                time: "30 Days",
                webDesigning: true,
                humanCentredDesign: true,
                basicMarketing: true,
                pytonForEverybody: true,
                androidDeveloper: false,
                businessEnglish: false
            },
            {
                title: 
                [{
                    img:"src/assets/img/icon/h5-custom-icon-9.png",
                    type:"Advanced",
                    price:"$88",
                }],
                number: "6",                
                time: "30 Days",
                webDesigning: true,
                humanCentredDesign: true,
                basicMarketing: true,
                pytonForEverybody: true,
                androidDeveloper: true,
                businessEnglish: true
            },
            
        ],
        }
    },
        
}
</script>


<template>
    <section class="container">  
    <div>
        <ul>
            <li v-for="(value) in elementBody[0]" >
                {{ value }}
            </li>
        </ul>
    </div>

    <div>
        <div v-for="(element, index) in elements" :key="index">
            <h2>{{ element.title[0].type }}</h2>
            <p>{{ element.number }}</p>
            <p>{{ element.time }}</p>

            <ul>
                <li v-for="(value) in element" >                 
                <i class="fa-solid" :class="{ 'fa-check': value, 'fa-xmark': !value }"></i>
                </li>
            </ul>

            <img :src="element.title[0].img" alt="Course Image">
            <p>{{ element.title[0].price }}</p>
        </div>
    </div>

        
          
    </section>
    <hr>
</template>
  

<style scoped lang="scss">


</style>