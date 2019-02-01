<template>
    <div id="main-content">
        <h1></h1>
        <div class="button-wrap" >
            <button v-on:click="sweetAlert()">get in touch!</button>
            <button v-on:click="sweetAlert2()">Want To Know More</button>
        </div>
    </div>
</template>

<script>

export default {
    data() {
        return {
            buttons: [{
                id: 'in-touch',
                txt: 'get in touch!'
            },  
            {
                id: 'know-more',
                txt: 'want to know more?'
            }
            ]
        } 
    },
    methods: {
        sweetAlert() {
            this.$swal({
                title: '<i class="far fa-envelope"></i>',
                type: '',
                html:'<a href="mailto:turner485@hotmail.co.uk"> ' +
                'Turner485@hotmail.co.uk</a>',
                showCloseButton: true,
                showCancelButton: false,
                focusConfirm: false,
                confirmButtonText:
                'Close',
            });
        }, 
        sweetAlert2() {
             this.$swal({
                title: '<i class="fas fa-user-ninja"></i>',
                type: '',
                html:'<span>Hello</span>My name is Ben, I am a full time web developer currently working in Ecommerce. I am looking for opportunities to further my knowledge within' +
                ' the web indistry. I have a working understanding of HTML5, CSS3, SASS/LESS, JavaScript & PHP & I also have began learning Wordpress, Java, Python&nbsp;&&nbsp;Vue',
                showCloseButton: true,
                showCancelButton: false,
                focusConfirm: false,
                confirmButtonText:
                'Close',
            });
        }
    }
}

var $message = '$benjamin_mcpolin'.split('').reverse();
var $timeout = 400;

var outputSlowly = setInterval(function() {
    
    $('#main-content h1').append($message.pop(),);
    
    if ($message.length === 0) {
        // No more characters. Break out.
        clearInterval(outputSlowly);   
    }
    
}, $timeout);

</script>

<style lang="scss">
@import "../sass/styles.scss";

</style>

