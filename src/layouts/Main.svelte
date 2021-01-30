<div class="main p-2">
    <div class="grid grid-cols-1 sm:grid-cols-6 lg:grid-cols-3">
        <div class="slide">
            <div class="slideshow-container">
                <div class="slide-item fade">
                    <div class="slide-number-text">1/3</div>
                    <img src="images/img/1.jpg" class="slide-img">
                    <div class="slide-text">Caption Text</div>
                </div>
                <div class="slide-item fade">
                    <div class="slide-number-text">2/3</div>
                    <img class="slide-img" src="images/img/2.jpg">
                    <div class="slide-text">Caption Two Text</div>
                </div>
                <div class="slide-item fade">
                    <div class="slide-number-text">3/3</div>
                    <img class="slide-img" src="images/img/3.jpg" alt="images">
                    <div class="slide-text">Caption Three Text</div>
                </div>
                <a class="slide-prev" href="javascript:0" on:click={()=>plusSlides(-1)}>&#10094;</a>
                <a class="slide-next"  href="javascript:0" on:click={()=>plusSlides(1)}>&#10095;</a>
            </div>
            <div class="slide-circulos">
                <span class="dot" on:click={()=>currentSlide(1)}></span>
                <span class="dot" on:click={()=>currentSlide(2)}></span>
                <span class="dot" on:click={()=>currentSlide(3)}></span>
            </div>
        </div>
    </div>
</div>

<script>
    import {onMount} from "svelte";

    let slideIndex = 1;
    onMount(async () => {
        showSlides(slideIndex)
    })

    //circulo control
    function currentSlide(number) {
        showSlides( slideIndex=number);

    }

    //next and previous controls
    function plusSlides(number) {
        showSlides(slideIndex += number);
        console.log("plusSide" + number)
    }

    function showSlides(number) {
        let i;
        let slides = document.getElementsByClassName("slide-item")
        let circulos = document.getElementsByClassName("dot")
        number > slides.length ? slideIndex = 1 : 0
        number < 1 ? slideIndex = slides.length : 0
        for (i=0;i<slides.length;i++){
            slides[i].style.display="none"
        }
        for (i=0;i<circulos.length;i++){
            circulos[i].classList.remove("slide-dot-active")
        }
        slides[slideIndex-1].style.display="block";
        circulos[slideIndex-1].classList.add("slide-dot-active")

    }
</script>

<style>
    .slide-item {
        background-color: rgba(176, 176, 2, 0.3);
        display: none;
        height: 200px;
        width: 100%;
    }

    .slideshow-container {
        width: 100%;
        position: relative;
        margin: auto;
    }

    .slide-img {
        width: 100%;
        height: 200px;
    }

    .slide {
        margin: auto;
        padding: 10px;
        width: 100%;
        z-index: 1;
    }

    .slide-prev:hover, .slide-next:hover {
        background-color: rgb(235, 238, 236);
    }

    .slide-prev, .slide-next {
        cursor: pointer;
        background-color: white;
        border-radius: 0 3px 3px 0;
        width: auto;
        padding: 12px 16px;
        margin-top: 15px;
        margin-right: 10px;
        text-align: center;
        position: absolute;
        top: 50%;
        user-select: none;
        font-size: 16px;
        transition: 0.6s ease;
    }

    .slide-next {
        right: 0;
        border-radius: 0 3px 3px 0;
    }

    .slide-text {
        padding: 8px 12px;
        position: absolute;
        bottom: 5px;
        color: #f4f4f4;
        width: 100%;
        text-align: center;
    }

    .slide-number-text {
        padding: 8px 12px;
        position: absolute;
        top: 5px;
        left: 0;
        color: #f4f4f4;
        width: 100%;
        text-align: center;
    }

    .slide-circulos {
        text-align: center;
    }

    .slide-circulos .dot {
        background-color: #bbbbbb;
        margin: 2px;
        text-align: center;
        height: 15px;
        width: 15px;
        display: inline-block;
        transition: background-color 0.6s ease;
        border-radius: 50%;
    }

    .slide-circulos .dot:hover {
        cursor: pointer;
        background-color: #585858;
    }

    .fade {
        -webkit-animation-name: fade;
        -webkit-animation-duration: 1.5s;
        animation-name: fade;
        animation-duration: 1.5s;
    }

    @-webkit-keyframes fade {
        from {
            opacity: .4
        }
        to {
            opacity: 1
        }
    }

    @keyframes fade {
        from {
            opacity: .4
        }
        to {
            opacity: 1
        }
    }

    .main {
        background-color: rgba(139, 138, 138, 0.3);
    }
</style>
