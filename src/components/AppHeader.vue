<script>

export default {
  data() {
    return {
        elements: ['HOME', 'COURSES', 'INSTRUCTORS', 'EVENTS', 'PAGES', 'ELEMENTS']
    };
  }
};

</script>

<template>
    <header>        
        <div class="container">
            <div class="header-top">
                <img src="../assets/img/footer-logo-1.png" alt="">
                <ul>
                    <li v-for="(element, index) in elements" :key="index">{{ element }}</li>
                </ul>
                <div class="icons">
                    <i class="fa-solid fa-magnifying-glass fa-rotate-90"></i>
                    <i class="fa-solid fa-bag-shopping"></i>
                    <i class="fa-solid fa-bars"></i></div>
            </div>
            <div class="header-body">
                <h1>Contemporary Ideas</h1>
                <p>Lorem ipsum dolor, sit amet consectetur adipisicing elit. Corporis aspernatur ipsa amet, quidem accusantium repudiandae cum odio alias reprehenderit qui debitis voluptatem molestiae nostrum incidunt neque quam cumque rem magni!</p>
                <button>REGISTER NOW</button>
            </div>
        </div>
        
    </header>
 
</template>

<style lang="scss" scoped> 


header{
    color: white;
    background-color: aquamarine;
    margin: 0;
    padding: 0;
    box-sizing: border-box;
    
}

// header top
.header-top {
    display: flex;
    justify-content: space-between;
}

ul {
    display: flex;
    list-style-type: none;
    gap: 2rem;  
    align-items: center;  
}
.icons {
    display: flex;
    gap: 1rem;
    align-items: center; 
}

// header body
.header-body {
    padding: 10rem;
    text-align: center;
}

p {
    padding: 2rem;
} 

button {
    padding: 1rem 1.5rem;
    color: white;
    background-color: var(--azure);
    border: none;
    font-weight: bold;
}


</style>
