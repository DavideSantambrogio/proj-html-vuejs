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
    <div>
        <div v-for="(element, index) in elements" :key="index">
            <h2 @click="toggleVisibility(index)">{{ element.title }}</h2>
            <div v-show="currentVisibleIndex === index">                
                <p>{{ element.description }}</p>
                <ul>
                    <li v-for="(possibility, possibilityIndex) in element.possibilities" :key="possibilityIndex">
                    {{ possibility }}
                    </li>
                </ul>
                <img :src="element.tabs" alt="Icon">
                
            </div>
        </div>
    </div>
  </template>
  

<style scoped lang="scss">
</style>