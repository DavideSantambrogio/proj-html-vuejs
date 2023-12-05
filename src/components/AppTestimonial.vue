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
    <div>
        <div v-for="(testimonial, index) in elements" :key="index">
            <input
                type="radio"
                :id="'testimonial' + index"
                v-model="selectedTestimonial"
                :value="index"/>
                
            <label :for="'testimonial' + index"></label>
        </div>

        <div >
            <img :src="elements[selectedTestimonial].image" alt="Testimonial Image">
            <p>{{ elements[selectedTestimonial].text }}</p>
            <p>{{ elements[selectedTestimonial].name }}</p>
            <p>{{ elements[selectedTestimonial].profession }}</p>
        </div>
    </div>
</template>

<style scoped lang="scss">


</style>