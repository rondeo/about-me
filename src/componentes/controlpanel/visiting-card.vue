<template>
    <div>
        <span class="p-1 text-white h5">Eugen Demidcik</span>
        <button class="navbar-toggler border bg-dark p-1 btn-group-vertical text-white ml-1" data-toggle="collapse" data-target="#info">?</button>
        <div class="collapse text-white w-100 position-absolute fixed-top mt-5" id="info">
                <div class="card mt-3">
                    <div class="topic text-center w-100 border-bottom border-white p-0">F a c h i n f o r m a t i k e r</div>
                    <div class="text-center">E u g e n &nbsp;&nbsp; D e m i d c i k<br>Mobil:&nbsp;&nbsp;0176 69558695</div>
                    <div class="bottom text-right mt-4 p-1">Heppacher Str. 8<br>70327 Stuttgart<br>Mobil:&nbsp;&nbsp;0176 69558695<br>E-Mail: eugen.dem@gmx.de</div>
                </div>
        </div>
    </div>

</template>

<script>
    export default {
        name: "visiting-card"
    }
</script>

<style scoped>
    button {
        min-width: 18px;
        max-height: 18px;
        box-shadow: 0px 0px 2px #fff;
        font-size: 12px;
    }
    .card {
        width: 				85mm;
        height:				55mm;
        background-image:	url(../../img/netz.jpeg);
        background-size:	85mm 55mm;
        border:				2px dotted;
        border-radius:		3mm;

    }
    .topic {
        background-color:	rgba(0,102,153,.4);
        height:				8mm;
        font-size:			5mm;
        font-weight:		bold;
        text-shadow:		-1px 2px 2px rgba(255,255,0,.7);
        padding:			1mm;

    }
    .bottom{
        text-shadow:		-1px 2px 2px rgba(0,0,0,.9);
    }
</style>