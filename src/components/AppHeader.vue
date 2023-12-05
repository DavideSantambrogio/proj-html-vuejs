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
    <div class="container">        
        <header>
            <div class="header-top">
                <img src="../assets/img/footer-logo-1.png" alt="">
                <ul>
                    <li v-for="(element, index) in elements" :key="index"><a href="">{{ element }}</a></li>
                </ul>
                <div class="icons">
                    <i class="fa-solid fa-magnifying-glass fa-rotate-90"></i>
                    <i class="fa-solid fa-bag-shopping"></i>
                    <i class="fa-solid fa-bars"></i></div>
            </div>
            <div class="header-body small-container">
                <h1>Contemporary Ideas</h1>
                <p>Lorem ipsum dolor, sit amet consectetur adipisicing elit. Corporis aspernatur ipsa amet, quidem accusantium repudiandae cum odio alias reprehenderit qui debitis voluptatem molestiae nostrum incidunt neque quam cumque rem magni!</p>
                <button>REGISTER NOW</button>
            </div>
        </header>        
    </div>
 
</template>

<style lang="scss" scoped> 


header{
    color: white;    
    margin: 0;
    padding: 0;
    box-sizing: border-box;
    height: var(--header-height);
    
    
}

// header top
.header-top {
    display: flex;
    justify-content: space-between;
    height: 50px;
    padding-top: 1rem;
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

a {
    text-decoration: none;
    color: white;
    &:hover {
      color: var(--azure);
    }
}


// header body
.header-body {    
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    height: calc(var(--header-height) - 50px);   
    margin: 0 auto;    
}

h1 {
    font-size: 4rem;
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
