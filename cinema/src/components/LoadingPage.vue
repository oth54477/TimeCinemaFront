<template>
  <div class="container">
    <div class="box">
      <div class="outter">
        <div class="inner">
          <div class="clock"></div>
          <h1>Loading...</h1>
        </div>
      </div>
    </div>
  </div>
</template>

<script>

export default {
  name: 'LoadingPage',
  methods: {
    
  }

}
</script>

<style scoped>
@import url(https://fonts.googleapis.com/css?family=Lato:300);


.container{
  text-align: center;
  /* background-color: gray; */
  overflow: hidden;
  display: flex;
  justify-content: center;
  align-items: center;
  width: 75%;
  height: 75%;
}

/* .box:nth-child(2n-1){
  background-color: rgba(0,0,0,0.05);
} */

.box{
  display: inline-block;
  /* display: flex; */
  /* justify-content: center; */
  /* align-items: center; */
  height: 100%;
  /* width: 33.3%; */
  width: 100%;
  position: relative;
  /*margin:0 -4px -5px -2px;*/
  transition: all .2s ease;
}

.outter {
  display: flex;
  justify-content: center;
  align-items: center;
}

.inner {
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
}
.box2 {
  height: 100%;
  width: 100%;
}
.box h1{
  color: #777;
  font-family:  Lato,"Helvetica Neue" ;
  font-weight: 300;
  position: absolute;
  font-size: 20px;
  width: 100%;
  height: 25px;
  text-align: center;
  bottom: 0px;
  margin: 0;
  top:160px;
  /* background-color: #fff; */
  opacity: 1;
  text-transform: uppercase;
  transition: all .2s ease;
}
/* 
.cir {
  background-color: white;
  position: absolute;
  top: 2px;
  left: 48%;
  width: 100px;
  height: 10px;
} */

/* MEDIA QUERIES */
@media (max-width: 700px){
  .box{
    width: 50%;
  }

  .box:nth-child(2n-1){
    background-color: inherit;
  }

  .box:nth-child(4n),.box:nth-child(4n-3) {
    background-color: rgba(0,0,0,0.05);
  }

}

@media (max-width: 420px){
  .box{
    width: 100%;
  }

  .box:nth-child(4n),.box:nth-child(4n-3){
    background-color: inherit;
  }

  .box:nth-child(2n-1){
    background-color:rgba(0,0,0,0.05);
  }

}


/* -------------- Clock -------------- */

.clock{
  border-radius: 1000px;
  border: 10px solid #fff;
  height: 300px;
  width: 300px;
  position: relative;

  /* top: 28%; */
  top: 110px;
  top: -webkit-calc(50% - 43px);
  top: calc(50% - 43px);
  /* left: 35%; */
  left: 110px;
  left: -webkit-calc(50% - 43px);
  left: calc(50% - 43px);
}
.clock:after{
  content: "";
  position: absolute;
  background-color: #fff;
  top: 2px;
  left: 48%;
  height: 150px;
  width: 4px;
  border-radius: 5px;
  -webkit-transform-origin: 50% 97%;
      transform-origin: 50% 97%;
  -webkit-animation: grdAiguille 2s linear infinite;
      animation: grdAiguille 2s linear infinite;
}

@-webkit-keyframes grdAiguille{
    0%{-webkit-transform:rotate(0deg);}
    100%{-webkit-transform:rotate(360deg);}
}

@keyframes grdAiguille{
    0%{transform:rotate(0deg);}
    100%{transform:rotate(360deg);}
}

.clock:before{
  content: "";
  position: absolute;
  background-color: #fff;
  top: 2px;
  left: 48%;
  height: 150px;
  width: 4px;
  border-radius: 5px;
  -webkit-transform-origin: 50% 94%;
      transform-origin: 50% 94%;
  -webkit-animation: ptAiguille 12s linear infinite;
      animation: ptAiguille 12s linear infinite;
}

@-webkit-keyframes ptAiguille{
    0%{-webkit-transform:rotate(0deg);}
    100%{-webkit-transform:rotate(360deg);}
}

@keyframes ptAiguille{
    0%{transform:rotate(0deg);}
    100%{transform:rotate(360deg);}
}



</style>