<template>
    <div id="app">
        <Card>
            <template #title>{{title}}</template>
            <template #content>
                <p class="m-0">
                    Lorem ipsum dolor sit amet, consectetur adipisicing elit. Inventore sed consequuntur error repudiandae numquam deserunt quisquam repellat libero asperiores earum nam nobis, culpa ratione quam perferendis esse, cupiditate neque
                    quas!
                </p>
            </template>
        </Card>
    </div>
</template>

<script>
import Card from 'primevue/card';

export default {
    props : ['title'],
    el: '#app', // Mount point selector

    components: {
        Card
    },

    data() {
        return {
            // Your data here if needed
        };
    },
}
</script>
