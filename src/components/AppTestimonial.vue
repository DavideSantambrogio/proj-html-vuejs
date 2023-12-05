<script>
export default {
    data() {
    return {
        elements: [            
            {
                image: "src/assets/img/testimonial/testimonials-standard-2.png",
                text: '"Lorem ipsum dolor, sit amet consectetur adipisicing elit. Beatae, tenetur maiores! Adipisci quis tempora assumenda sequi, fugit dolorum alias asperiores ad reprehenderit laboriosam, dolores amet nulla optio, provident incidunt ratione."',
                name: "Joan Collins",
                profession: "STUDENT",
            },
            {
                image: "src/assets/img/testimonial/testimonials-standard-3.png",
                text: '"Lorem ipsum dolor, sit amet consectetur adipisicing elit. Beatae, tenetur maiores! Adipisci quis tempora assumenda sequi, fugit dolorum alias asperiores ad reprehenderit laboriosam, dolores amet nulla optio, provident incidunt ratione."',
                name: "Paul Fox",
                profession: "TEACHER",
            },
            {
                image: "src/assets/img/testimonial/testimonials-standard-4.png",
                text: '"Lorem ipsum dolor, sit amet consectetur adipisicing elit. Beatae, tenetur maiores! Adipisci quis tempora assumenda sequi, fugit dolorum alias asperiores ad reprehenderit laboriosam, dolores amet nulla optio, provident incidunt ratione."',
                name: "Emily Bis",
                profession: "STUDENT",
            },
            {
                image: "src/assets/img/testimonial/testimonials-standard-5.png",
                text: '"Lorem ipsum dolor, sit amet consectetur adipisicing elit. Beatae, tenetur maiores! Adipisci quis tempora assumenda sequi, fugit dolorum alias asperiores ad reprehenderit laboriosam, dolores amet nulla optio, provident incidunt ratione."',
                name: "Mary Cross",
                profession: "TEACHER",
            },
            {
                image: "src/assets/img/testimonial/testimonials-standard-6.png",
                text: '"Lorem ipsum dolor, sit amet consectetur adipisicing elit. Beatae, tenetur maiores! Adipisci quis tempora assumenda sequi, fugit dolorum alias asperiores ad reprehenderit laboriosam, dolores amet nulla optio, provident incidunt ratione."',
                name: "Susan Ford",
                profession: "STUDENT",
            },                       
        ],   
        selectedTestimonial: 0       
    };
  }
};

</script>

<template>
    <section >
        <div class="container">
            <div class="testimonial small-container">
                <div>
                    <img :src="elements[selectedTestimonial].image" alt="Testimonial Image">
                    <p>{{ elements[selectedTestimonial].text }}</p>
                    <h2>{{ elements[selectedTestimonial].name }}</h2>
                    <h3>{{ elements[selectedTestimonial].profession }}</h3>
                </div>

                <div class="radio-group">
                    <div v-for="(testimonial, index) in elements" :key="index">
                        <input
                            type="radio"
                            :id="'testimonial' + index"
                            v-model="selectedTestimonial"
                            :value="index"                
                            />               
                        <label :for="'testimonial' + index"></label>
                    </div>
                </div>
            </div>
        </div>

    </section>
</template>

<style scoped lang="scss">

section {
    background-image: url(../assets/img/background/h5-parallax-img-1.png);    
    background-repeat: no-repeat;     
    background-position-x: center;
    
}
.testimonial {
    text-align: center;
    padding: 8rem 0;
    color: white;
}

img {    
    width: 150px;
}

p {
    font-size: var(--primary-font-size);
    padding: 3rem 0;
}

h2 {
    font-size: 2rem;
    margin-bottom: 1rem;
}

h3 {    
    margin-bottom: 3rem;
}

.radio-group {
    display: flex;
    justify-content: center;
    gap: 1rem;
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
    background-color: #ffffff; /* Sfondo bianco quando selezionato */  
}

/* Stile quando l'input radio non è selezionato */
input[type="radio"]:not(:checked) {
    background-color: rgba($color: #ffffff, $alpha: 0.5); /* Sfondo verde quando non selezionato */
  
}

</style>