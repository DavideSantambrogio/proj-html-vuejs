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
        <div class="title">
            <h1>Pricing Plans</h1> 
            <p>Lorem ipsum dolor sit, amet consectetur adipisicing elit. Eligendi molestias cum quam veritatis vero ducimus soluta quae, hic ex sequi placeat, illo ipsam provident dolorem aliquam maxime neque, esse similique.</p>
        </div>
        <div class="table">
                
            <div class="data">
                <ul >
                    <li class="t-head" v-for="(value) in elementBody[0]" >
                        {{ value }}
                    </li>
                </ul>
            </div>

            <div class="plans">
                <div v-for="(element, index) in elements" :key="index">

                    <div class="t-head">
                        <img :src="element.title[0].img" alt="Course Image">
                        <p>{{ element.title[0].price }}</p>
                        <h2>{{ element.title[0].type }}</h2>
                    </div>
                    
                    <div class="txt">{{ element.number }}</div>
                    <div class="txt">{{ element.time }}</div>

                    <ul>
                        <li class="li-center" v-for="(value) in element">
                            
                        <span v-if="typeof value === 'boolean'">
                            <i class="fa-solid" :class="{ 'fa-check': value, 'fa-xmark': !value }"></i>
                        </span>
                        
                        </li>
                    </ul>
                </div>

            </div>

        </div>
          
    </section>
    <hr>
</template>
  

<style scoped lang="scss">

.title {
    text-align: center;
    margin-top: 7rem;
    margin-bottom: 7rem;
}
.title h1{
    font-size: 4rem;
    margin-bottom: 1rem;
}

.title p {
    color: var(--txt-color) ;
    font-size: var(--primary-font-size);

}
.plans {
    display: flex;    
}
.data {
    width: calc(1200px/4);
}
.plans > * {
    width: calc(1200px/4);    
}
.table {
    display: flex;
    width: 100%;
}

li {
    list-style: none;
    color: var(--txt-color) ;
    font-size: var(--primary-font-size);    
    
    
}

li.t-head , div.t-head , div.txt { 
    border: 1px solid #ababab;
    height: 6rem;
    padding: 0 2rem;
    display: flex;
    align-items: center;    
}

.txt{justify-content: center;}

i {
    color: var(--azure);
    
}
.t-head p , .t-head h2 , ul p , .txt{
    color: var(--txt-color) ;
    font-size: var(--primary-font-size); 
    text-align: center;  
    padding: 1rem;  
}

.t-head:first-child {
   height: 350px;
   color: black;
   font-size: 2.5rem;
   display: flex;
   flex-direction: column;
   align-items: center;
   justify-content: center;

}




// border li
.li-center:nth-child(4), .li-center:nth-child(5), .li-center:nth-child(6) , .li-center:nth-child(7) , .li-center:nth-child(8), .li-center:nth-child(9) {
    text-align: center;
    border: 1px solid;
    height: 6rem;
    display: flex;
    align-items: center; 
    justify-content: center;
}






</style>