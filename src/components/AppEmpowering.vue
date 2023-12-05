<script>
export default {
  data() {
    return {
        
      
    };
  },
};

</script>

<template>
    <section class="container">
        <img class="full" src="../assets/img/section/h5-img-1.jpg" alt="">
        <div class="row">
            <img class="col" src="../assets/img/section/h5-img-2.jpg" alt="">
            <div class="col">
                <h1> Empowering Children to Reach Their Potential.</h1>
                <p class="text">Lorem ipsum dolor, sit amet consectetur adipisicing elit. Quia, voluptas? Repellendus ipsum minima quibusdam tempore, repudiandae ratione recusandae ducimus, obcaecati fugiat assumenda quam numquam et quaerat, aut ipsam illum odit.</p>
                <div class="row">
                    <div class="stories">
                        <h1>186</h1>
                        <p>User Stories</p>
                    </div>
                    <div class="events">
                        <h1>347</h1>
                        <p>Eventes</p>
                    </div>
                </div>
            </div>        
        </div>
    </section>

</template>

<style scoped lang="scss">

img {
    object-fit: cover;
}
.full {
    width: 100%;
    
}
.row {
    width: 100%;
    display: flex;
}
.col {
    width: 50%;
    margin-bottom: 3rem;
}

.text { 
    margin-bottom: 3rem;

}

img.col {
    margin-top: 10rem;
}
div.col {
    margin-top: 6rem;
}

p {
    font-size: var( --primary-font-size);
    color: var(--txt-color);    
}

h1{
    font-size: 4rem;
    margin-bottom: 1rem;
}

.stories , .events  {
    color: var(--azure);
    width: 50%;
}

.stories p , .events  p{
    color: var(--azure);
}

</style>