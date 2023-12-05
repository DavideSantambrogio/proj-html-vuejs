<script>
export default {
  data() {
    return {
        footerItems: [
        {
            isImageInTitle: true,
            title: 'src/assets/img/footer-logo-1.png',
            txt: ["Providing Life Changing Experience Through Education, Class that Fit Your Busy Life. Closer to Home"]
        },
        {
            title: "Popular Courses",
            section:[
                {
                subtitle: "Business English",
                teacher: "Preston Marshall",
                },
                {
                subtitle: "Social Computing",
                teacher: "David Sanders",
                },
                {
                subtitle: "Learn Spanish",
                teacher: "Jennie King",
                },
            ]
            
        },
        {
            title: "Support",
            list: ["User Dashboard", "Contact Us", "FAQ", "Course Offer", "Events"]
        },
        {
            title: "Flexible learning",
            isImageInList: true,
            list: ["src/assets/img/footer-img-1.png"]
        },
      ], 
      
    };
  },
};

</script>

<template>
    <footer>
        <div class="container">
            <div class="list">
                <div v-for="(item, index) in footerItems" :key="index" class="col">
                    <h3 class="title" v-if="!item.isImageInTitle">{{ item.title }}</h3>
                    <img class="title" v-else :src="item.title" alt="Footer Image" />
                    
                    <div v-if="item.txt"  class="content">
                        <p>{{ item.txt[0] }}</p>
                        <div class="contacts">
                            <i class="fa-solid fa-phone"></i><span> 1-677-124-44-22-7</span><br>
                            <br><i class="fa-regular fa-clock"></i><span> Mon-Sat 8.00-18.00</span>
                        </div>
                    </div>

                    <ul v-if="item.list" class="content">
                        <li v-for="(listItem, listIndex) in item.list" :key="listIndex">
                            <a v-if="!item.isImageInList" href="">{{ listItem }}</a>
                            <img v-else :src="listItem" alt="Footer Image" />
                        </li>
                    </ul>

                    <ul v-if="item.section" class="content">
                        <li v-for="(course, courseIndex) in item.section" :key="courseIndex">
                            <h4>{{ course.subtitle }}</h4> 
                            <a href="">{{ course.teacher }}</a>
                        </li>
                    </ul>
                </div>
            </div>
            <hr>
            <div class="footer-bottom">
                Copyrights 2017 ©Mikado Themes
                <div class="social">
                    <span>CALL +44 300 303 0266</SPAN>
                    <span>FOLLOW US</span>
                    <span><i class="fa-brands fa-twitter"></i></span>
                    <span><i class="fa-brands fa-instagram"></i></span>
                    <span><i class="fa-brands fa-facebook-f"></i></span>
                </div>
            </div>

            
        </div>
    </footer>
</template>

<style scoped lang="scss">

footer {
    background-color: var(--background-footer);  
    color: white;  
}

.title {
    font-size: 1.2rem;
    height: 1.5rem;
    margin-bottom: 1rem;
}
.list {  
    padding: 3rem 0;  
    display: flex;
    justify-content: space-between;      
}



.col {
    height: fit-content;
    width: calc(100%/4);
    padding-right: 1rem;
}

a {
    color: white;
    text-decoration: none;
    
    &:hover {
      color: var(--azure);
    }
}


li {
    list-style-type: none;
}

.content{
    display: flex;
    flex-direction: column;
    justify-content: space-between; /* o altre opzioni come space-around, space-evenly, center, etc. */
    height: 200px;
}

.footer-bottom {
    display: flex;
    justify-content: space-between;
    padding: 1.5rem 0;
}
.social{ 
    gap: 1rem;
    display: flex;

}

</style>