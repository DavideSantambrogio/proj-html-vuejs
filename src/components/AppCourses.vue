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
                title: "Web Designing",
                teacher: "Jennifer Powell",
                cost: "Free",
                description: "Lorem ipsum dolor, sit amet consectetur adipisicing elit. Beatae, tenetur maiores! Adipisci quis tempora assumenda sequi, fugit dolorum alias asperiores ad reprehenderit laboriosam, dolores amet nulla optio, provident incidunt ratione.",
                type: "PROGRAMMING",
                tabs: "src/assets/img/course/course-2-f-img.jpg",
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
            {
                title: "Financial Modelling",
                teacher: "Edward Bowman",
                cost: "$20",
                description: "Lorem ipsum dolor, sit amet consectetur adipisicing elit. Beatae, tenetur maiores! Adipisci quis tempora assumenda sequi, fugit dolorum alias asperiores ad reprehenderit laboriosam, dolores amet nulla optio, provident incidunt ratione.",
                type: "BUSINESS",
                tabs: "src/assets/img/course/course-9-f-img.jpg",
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
        

        <div v-for="(course, index) in displayedCourses" :key="index">
            <div>
                <h2>{{ course.title }}</h2>
                <p>{{ course.teacher }}</p>
                <p>{{ course.cost }}</p>
                <p>{{ course.type }}</p>
                <p>{{ course.description }}</p>
                <img :src="course.tabs" alt="Course Image">
            </div>
        </div>  

        <input type="radio" id="radio1" v-model="selectedRadio" value="1" />
        

        <input type="radio" id="radio2" v-model="selectedRadio" value="2" />
        

        <input type="radio" id="radio3" v-model="selectedRadio" value="3" />
        
    </section>
    <hr>
</template>
  

<style scoped lang="scss">



</style>