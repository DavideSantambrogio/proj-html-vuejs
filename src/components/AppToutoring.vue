<script>

export default {
  data() {
    return {
        elements: [
            {
                title: "Languages",
                image: "src/assets/img/icon/h5-custom-icon-1.png"
            },
            {
                title: "Software",
                image: "src/assets/img/icon/h5-custom-icon-2.png"
            },
            {
                title: "Business",
                image: "src/assets/img/icon/h5-custom-icon-3.png"
            },
            {
                title: "Chemistry",
                image: "src/assets/img/icon/h5-custom-icon-4.png"
            },
            {
                title: "Science",
                image: "src/assets/img/icon/h5-custom-icon-5.png"
            },
            {
                title: "DIY&Craft",
                image: "src/assets/img/icon/h5-custom-icon-6.png"
            },                        
        ]
    };
  }
};
</script>

<template>
    <section class="container">
        <div class="row">
            <div v-for="(element, index) in elements" :key="index" class="col" >
                <div >
                    <img :src="element.image" alt="Icon">
                    <h2>{{ element.title }}</h2>                    
                </div>
            </div>
        </div>
        <div>
            <h1>
                The Trusted Name for In-Home Tutoring.
            </h1>
            <p>Lorem, ipsum dolor sit amet consectetur adipisicing elit. Iure officiis, vero, ipsa praesentium possimus placeat repellendus odit pariatur labore consequuntur soluta accusamus cumque nemo iste corrupti consequatur eum beatae perspiciatis.</p>
            <a href="">LEARN MORE</a>
        </div>

    </section>
</template>
  

<style lang="scss" scoped> 
.row {
    margin: 3rem 0;    
    display:flex;
    gap: 1.5rem;

}

h2 {margin-top: 3rem;}
.col {
    background-color: var(--card-background);
    width: calc(100%/6);
    text-align: center;
    padding: 3rem 0;
    
    &:hover {
      background-color: white;
    }
}

h1 {
    max-width: 50%;
    font-size: 3.5rem;
    margin-top: 7rem
}

p {
    margin: 2rem 0;
    font-size:var(--primary-font-size);
    color: var(--txt-color);
}

a {
    text-decoration: none;
    color: var(--azure);
    font-weight: bold;
    
}

</style>
