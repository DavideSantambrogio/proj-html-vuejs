<script>
export default {
    data() {
        return {            
            elements: [
            {
                title: "Android Developer",
                teacher: "David Sanders",
                cost: "Free",
                description: "Lorem ipsum dolor, sit amet consectetur adipisicing elit. Beatae, tenetur maiores! Adipisci quis tempora assumenda sequi, fugit dolorum alias asperiores ad reprehenderit laboriosam, dolores amet nulla optio, provident incidunt ratione.",
                type: "PROGRAMMING",
                tabs: "src/assets/img/course/course-1-f-img.jpg",
            },            
            {
                title: "Financial Modelling",
                teacher: "Edward Bowman",
                cost: "$20",
                description: "Lorem ipsum dolor, sit amet consectetur adipisicing elit. Beatae, tenetur maiores! Adipisci quis tempora assumenda sequi, fugit dolorum alias asperiores ad reprehenderit laboriosam, dolores amet nulla optio, provident incidunt ratione.",
                type: "BUSINESS",
                tabs: "src/assets/img/course/course-3-f-img.jpg",
            },
            {
                title: "Web Developer",
                teacher: "David Sanders",
                cost: "Free",
                description: "Lorem ipsum dolor, sit amet consectetur adipisicing elit. Beatae, tenetur maiores! Adipisci quis tempora assumenda sequi, fugit dolorum alias asperiores ad reprehenderit laboriosam, dolores amet nulla optio, provident incidunt ratione.",
                type: "PROGRAMMING",
                tabs: "src/assets/img/course/course-4-f-img.jpg",
            },
            {
                title: "Web Designing",
                teacher: "Jennifer Powell",
                cost: "Free",
                description: "Lorem ipsum dolor, sit amet consectetur adipisicing elit. Beatae, tenetur maiores! Adipisci quis tempora assumenda sequi, fugit dolorum alias asperiores ad reprehenderit laboriosam, dolores amet nulla optio, provident incidunt ratione.",
                type: "PROGRAMMING",
                tabs: "src/assets/img/course/course-2-f-img.jpg",
            },
            {
                title: "Android Designing",
                teacher: "Jennifer Powell",
                cost: "Free",
                description: "Lorem ipsum dolor, sit amet consectetur adipisicing elit. Beatae, tenetur maiores! Adipisci quis tempora assumenda sequi, fugit dolorum alias asperiores ad reprehenderit laboriosam, dolores amet nulla optio, provident incidunt ratione.",
                type: "PROGRAMMING",
                tabs: "src/assets/img/course/course-5-f-img.jpg",
            },
            {
                title: "Financial Invest",
                teacher: "Edward Bowman",
                cost: "$20",
                description: "Lorem ipsum dolor, sit amet consectetur adipisicing elit. Beatae, tenetur maiores! Adipisci quis tempora assumenda sequi, fugit dolorum alias asperiores ad reprehenderit laboriosam, dolores amet nulla optio, provident incidunt ratione.",
                type: "BUSINESS",
                tabs: "src/assets/img/course/course-6-f-img.jpg",
            },
            {
                title: "Financial Modelling",
                teacher: "Edward Bowman",
                cost: "$20",
                description: "Lorem ipsum dolor, sit amet consectetur adipisicing elit. Beatae, tenetur maiores! Adipisci quis tempora assumenda sequi, fugit dolorum alias asperiores ad reprehenderit laboriosam, dolores amet nulla optio, provident incidunt ratione.",
                type: "BUSINESS",
                tabs: "src/assets/img/course/course-9-f-img.jpg",
            },
            {
                title: "FullStack Developer",
                teacher: "David Sanders",
                cost: "Free",
                description: "Lorem ipsum dolor, sit amet consectetur adipisicing elit. Beatae, tenetur maiores! Adipisci quis tempora assumenda sequi, fugit dolorum alias asperiores ad reprehenderit laboriosam, dolores amet nulla optio, provident incidunt ratione.",
                type: "PROGRAMMING",
                tabs: "src/assets/img/course/course-7-f-img.jpg",
            },
            {
                title: "3D Designing",
                teacher: "Jennifer Powell",
                cost: "Free",
                description: "Lorem ipsum dolor, sit amet consectetur adipisicing elit. Beatae, tenetur maiores! Adipisci quis tempora assumenda sequi, fugit dolorum alias asperiores ad reprehenderit laboriosam, dolores amet nulla optio, provident incidunt ratione.",
                type: "PROGRAMMING",
                tabs: "src/assets/img/course/course-8-f-img.jpg",
            },
            
             
        ],
        selectedRadio: 1, 
    };
  },
  computed: {
    displayedCourses() {
      if (this.selectedRadio === null) {
        return [];
      }

      const startIndex = (this.selectedRadio - 1) * 3;
      const endIndex = startIndex + 3;

      return this.elements.slice(startIndex, endIndex);
    },
  },
};

</script>


<template>
    <section class="container"> 

        <div class="small-container">
            <h1>Popular Online Courses</h1>
            <p class="text"> Lorem ipsum dolor sit amet consectetur adipisicing elit. Modi obcaecati cumque mollitia sapiente maiores, excepturi quibusdam quia fuga odit animi non est fugit molestiae placeat. Facilis omnis eos quam sunt.</p>
        </div>
        

        
        <div class="row">
            <div  v-for="(course, index) in displayedCourses" :key="index">
                
                <img :src="course.tabs" alt="Course Image">
                <div class="col">    
                    <div class="title-cost">
                        <h2>{{ course.title }}</h2>                    
                        <div v-if="course.cost === 'Free'" class="cost free-course">{{ course.cost }}</div>
                        <div v-else class="cost paid-course">{{ course.cost }}</div>
                    </div> 
                    <div class="text-color">
                        <small>{{ course.teacher }}</small>
                        <p>{{ course.description }}</p>
                        <div class="type">
                            <i class="fa-solid fa-user"></i><span>1</span>
                            <i class="fa-solid fa-tag fa-rotate-90"></i>
                            <span>{{ course.type }}</span>
                        </div>
                    </div>    
                </div>
            </div>  
        </div>
        

        <div class="imput-group">
            <input type="radio" id="radio1" v-model="selectedRadio" value="1" />      
            <input type="radio" id="radio2" v-model="selectedRadio" value="2" />
            <input type="radio" id="radio3" v-model="selectedRadio" value="3" />        
        </div>
        
    </section>
    <hr>
</template>
  

<style scoped lang="scss">
.container {
    padding: 7rem 0;    
}
.small-container {
    text-align: center;
}

h1 {
    font-size: 4rem;
    margin-bottom: 2rem;
}
.text {
    font-size: var(--primary-font-size);
    color: var(--txt-color);
    margin-bottom: 7rem;
}
.row {
    display: flex;
    gap: 2rem;
}
.col {padding: 1rem;}
.title-cost{
    display: flex;
    justify-content: space-between;
}

.free-course {
  background-color: yellow;
  color: white;
  padding: 0.3rem 1rem;
  border-radius: 1rem;
}

.paid-course {
  background-color: var(--azure);
  color: white;
  padding: 0.3rem 1rem;
  border-radius: 1rem;
}

.text-color *{
    color: var(--txt-color);
    margin-bottom: 1rem;
    margin-top: 1rem;
}

.text-color p {
    font-size: 1.2rem;
}

.type {    
    display: flex;
    align-items: center;
    gap: 0.5rem;
}

/* Stile per gli input radio */
input[type="radio"] {
    
    /* Nasconde il pulsante radio predefinito */
    appearance: none;
    -webkit-appearance: none;
    -moz-appearance: none;
    /* Imposta una dimensione personalizzata per il pulsante radio */
    width: 20px;
    height: 20px;
    /* Bordi arrotondati per un aspetto più gradevole */
    border-radius: 50%;
    /* Bordi e spaziatura interna per il layout */  
    margin: 0;
    padding: 0;
    /* Stile del cursore al passaggio del mouse */
    cursor: pointer;
}

/* Stile quando l'input radio è selezionato */
input[type="radio"]:checked {
    background-color: var(--azure); /* Sfondo bianco quando selezionato */  
}

/* Stile quando l'input radio non è selezionato */
input[type="radio"]:not(:checked) {
    background-color: #9CE0FF
  
}

.imput-group {
    justify-content: center;
    display: flex;
    gap: 1rem;
}

</style>