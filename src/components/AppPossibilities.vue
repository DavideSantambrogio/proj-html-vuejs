<script>
export default {
    data() {
        return {
            currentVisibleIndex: 0,
            elements: [
            {
                title: "What we do",
                description: "Lorem ipsum dolor, sit amet consectetur adipisicing elit. Beatae, tenetur maiores! Adipisci quis tempora assumenda sequi, fugit dolorum alias asperiores ad reprehenderit laboriosam, dolores amet nulla optio, provident incidunt ratione.",
                possibilities: [
                    "We enrich lives throught learning",
                    "Maximizing potential trought individual attention",
                    "The Trusted name for specialized training",
                    "People teach. People learn. This is where they connect"
                ],
                tabs: "src/assets/img/tabs/h12-tabs-icon-1.png",
                visible: false,
            },
            {
                title: "Degree Programme",
                description: "Lorem ipsum dolor, sit amet consectetur adipisicing elit. Beatae, tenetur maiores! Adipisci quis tempora assumenda sequi, fugit dolorum alias asperiores ad reprehenderit laboriosam, dolores amet nulla optio, provident incidunt ratione.",
                possibilities: [
                    "We enrich lives throught learning",
                    "Maximizing potential trought individual attention",
                    "The Trusted name for specialized training",
                    "People teach. People learn. This is where they connect"
                ],
                tabs: "src/assets/img/tabs/h12-tabs-icon-2.png",
                visible: false,
            },
            {
                title: "Carrer Archivements",
                description: "Lorem ipsum dolor, sit amet consectetur adipisicing elit. Beatae, tenetur maiores! Adipisci quis tempora assumenda sequi, fugit dolorum alias asperiores ad reprehenderit laboriosam, dolores amet nulla optio, provident incidunt ratione.",
                possibilities: [
                    "We enrich lives throught learning",
                    "Maximizing potential trought individual attention",
                    "The Trusted name for specialized training",
                    "People teach. People learn. This is where they connect"
                ],
                tabs: "src/assets/img/tabs/h12-tabs-icon-3.png",
                visible: false,
            },
            {
                title: "Personal Menagemant",
                description: "Lorem ipsum dolor, sit amet consectetur adipisicing elit. Beatae, tenetur maiores! Adipisci quis tempora assumenda sequi, fugit dolorum alias asperiores ad reprehenderit laboriosam, dolores amet nulla optio, provident incidunt ratione.",
                possibilities: [
                    "We enrich lives throught learning",
                    "Maximizing potential trought individual attention",
                    "The Trusted name for specialized training",
                    "People teach. People learn. This is where they connect"
                ],
                tabs: "src/assets/img/tabs/h12-tabs-icon-4.png",
                visible: false,
            },
            {
                title: "Step To Success",
                description: "Lorem ipsum dolor, sit amet consectetur adipisicing elit. Beatae, tenetur maiores! Adipisci quis tempora assumenda sequi, fugit dolorum alias asperiores ad reprehenderit laboriosam, dolores amet nulla optio, provident incidunt ratione.",
                possibilities: [
                    "We enrich lives throught learning",
                    "Maximizing potential trought individual attention",
                    "The Trusted name for specialized training",
                    "People teach. People learn. This is where they connect"
                ],
                tabs: "src/assets/img/tabs/h12-tabs-icon-5.png",
                visible: false,
            },      
            {
                title: "Knowlwdge Transfer",
                description: "Lorem ipsum dolor, sit amet consectetur adipisicing elit. Beatae, tenetur maiores! Adipisci quis tempora assumenda sequi, fugit dolorum alias asperiores ad reprehenderit laboriosam, dolores amet nulla optio, provident incidunt ratione.",
                possibilities: [
                    "We enrich lives throught learning",
                    "Maximizing potential trought individual attention",
                    "The Trusted name for specialized training",
                    "People teach. People learn. This is where they connect"
                ],
                tabs: "src/assets/img/tabs/h12-tabs-icon-6.png",
                visible: false,
            }, 
        ],
        }
    },
    methods: {
        toggleVisibility(index) {
            // Questo metodo cambierà il valore di 'visible' per l'elemento indicato dall'indice.
            this.currentVisibleIndex = (this.currentVisibleIndex === index) ? this.currentVisibleIndex : index;
        }
    }
    
}
</script>


<template>
    <section class="container">        
        <div v-for="(element, index) in elements" :key="element.title">
            <div class="possibility">
                <div class="title" :class="{ 'active': currentVisibleIndex === index }" @click="toggleVisibility(index)">
                    <h2 >{{ element.title }}</h2>
                </div>
                
                <div class="description" v-show="currentVisibleIndex === index"> 
                    <div>                    
                        <h3>{{ element.title }}</h3>               
                        <p>{{ element.description }}</p>
                    </div>    
                    <div class="list">    
                        <ul>
                            <li v-for="(possibility, possibilityIndex) in element.possibilities" :key="possibilityIndex">
                                <i class="fa-solid fa-check"></i>{{ possibility }}
                            </li>
                        </ul>
                        <img :src="element.tabs" alt="Icon"> 
                    </div>
                                      
                </div>
            </div>
        </div>        
    </section>
    <hr>
</template>
  

<style scoped lang="scss">

section {
    position: relative;
    padding: 7rem 0;
}


.possibility {
    display: flex;
}    
.title {
    width: 330px;    
    border: 1px solid var(--txt-color);
    padding: 2rem;
    color: var(--txt-color);
    
}
.active {
    color: var(--azure);
    border-left:7px solid var(--azure);
    background-color: var(--card-background);
}

    // description
.description {
    position: absolute;
    left: 400px;
    top: 7rem;
    
}
h3 {
    font-size: 3rem;
    padding: 1rem 0;
}

p, ul {
    color: var(--txt-color);
    font-size: var(--primary-font-size);
}

p {
    padding-bottom: 2rem;
}

li {
    padding: 1rem 0;
    list-style: none;
}
.list {
    display: flex;
}
img {
    
    width: 150px;    
    
    align-self: self-end;
    margin-left: 2rem;
    
}

i {
    color: var(--azure);
    padding-right: 1rem;
}
</style>