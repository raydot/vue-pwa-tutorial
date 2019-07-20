<!-- 
    The panel is a simple component that wraps the input and result components.

    For one-way data binding in Vue we can use textinterprolation.
        
    This "Mustache" syntax interprets data as plain text and not HTML.  That's why we use vue's slot element, which allows us to render child elements of our panel component within the body element. 
-->


<template>
    <div class="panel">
        <div class="header">
            <h2 class="headline">{{ headline }}</h2>
        </div>
        <div class="body">
            <slot />
        </div>
    </div>
</template>

<!--The headline is passed in so the functionality is generic.-->
<script>
    export default {
        name: "Panel",
        props: {
            headline: String
        }
    }
</script> 

