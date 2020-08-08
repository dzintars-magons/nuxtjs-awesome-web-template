<template>
     <div class="website-wrapper">

        
            <div class="intro-container__background">
                <div class="intro-container">
                    <h4 class="heading-four"><nuxt-link to="/">BACK TO MAIN PAGE</nuxt-link></h4>
                    <h1 class="intro-container__heading">Here's the Title</h1>
                    <div class="intro-container__text">
                        <h4 class="intro-container__text__heading">Little Heading</h4>
                        <p class="intro-container__text__desc">Lorem, ipsum dolor sit amet consectetur adipisicing elit. Quaerat nobis iusto facere eius dolore cumque quia, dolorum vero commodi reiciendis! Obcaecati labore sapiente recusandae cupiditate voluptatibus impedit, a natus numquam.</p>
                    </div>
                </div>
            </div>

            <div class="grid-1-title" style="background-color: yellow; display: flex; justify-content: center; align-items: center; height: 100px;">
                <h2 style="color: tomato; margin-top">GRID BY NAMING LINES</h2>
            </div>

            <div class="container">
                <div class="grid-container-one">
                    <h1 style="background-color: aqua;"><span>One</span> </h1>
                    <h2 style="background-color: white;"><span>two</span></h2>
                    <h3 style="background-color: purple;"><span>Three</span></h3>
                    <h4 style="background-color: peru;"><span>Four</span></h4>
                </div>
            </div>

            <div class="black-block" style="background-color: #000; height: 100px;"></div>

            <div class="grid-container-two">
                <h1 style="background-color: aqua;"><span>Heading One</span></h1>
                <h2 style="background-color: white;"><span>Heading Two</span></h2>
                <h3 style="background-color: purple;"><span>Heading Three</span></h3>
                <h4 style="background-color: peru;"><span>Heading Four</span></h4>
            </div>

            <div class="yellow-block" style="background-color: yellow; height: 600px;"></div>
     

       

        

        
    </div>
</template>

<style lang="scss">

.intro-container {
    @include container-fluid;
  
    &__background {
        @include background-cover ('https://picsum.photos/id/102/1140/600');
        height: 600px;
        display: flex;
        justify-content: space-evenly;
        flex-direction: column;
        & .intro-container__text {
            @include flex-center;
            flex-direction: column;
           
        }
    }
}

div h2 {
    margin: 0;
}

.container {
    @include container-fluid;
}

//ONE WAY HOW TO USE GRID 
//by naming lines

.grid-container-one {
    background-color: greenyellow;
    display: grid;
    grid-template-columns: [col-1-start] 300px [col-1-end col-2-start] 300px [col-2-end col-3-start] auto [col-3-end];
    grid-template-rows: [row-1-start] 100px [row-1-end row-2-start] 100px [row-2-end row-3-start] 100px [row-3-end];
    & h1, h2, h3, h4 {
        @include flex-center;
        margin: 0;
    }
    & h1 {
        grid-column-start: col-2-start;
        grid-column-end: col-2-end;
        grid-row-start: row-3-start;
        grid-row-end: row-3-end;
        
        @include desktop-down {
            grid-column-start: col-3-start;
            grid-column-end: col-3-end;
            grid-row-start: row-1-start;
            grid-row-end: row-1-end;
        }
    }
    & h2 {
        grid-column-start: col-3-start;
        grid-column-end: col-3-end;
        grid-row-start: row-2-start;
        grid-row-end: row-2-end;
        @include desktop-down {
            grid-column-start: col-2-start;
            grid-column-end: col-2-end;
            grid-row-start: row-2-start;
            grid-row-end: row-2-end;
        }
    }
    & h3 {
        grid-column-start: col-1-start;
        grid-column-end: col-1-end;
        grid-row-start: row-2-start;
        grid-row-end: row-3-end;
    }
    & h4 {
        grid-column-start: col-1-start;
        grid-column-end: col-3-end;
        @include desktop-down {
            grid-column-start: col-3-start;
            grid-column-end: col-3-end;
            grid-row-start: row-3-start;
            grid-row-end: row-3-end;
        }
    }
}

.grid-container-two {
    display: grid;
    grid-template-columns: repeat(12, 1fr);
    grid-template-rows: auto;
    column-gap: 30px;
    grid-template-areas: "a a a a . . b b b b b b"
                         ". . c c c c d d d d d d";
    & h1, & h2, & h3, & h4 {
        @include flex-center;
        margin: 0;
    }
    & h1 {
        grid-area: a;
    }
    & h2 {
        grid-area: b;
    }
    & h3 {
        grid-area: c;
    }
    & h4 {
        grid-area: d;
    }
}

</style>