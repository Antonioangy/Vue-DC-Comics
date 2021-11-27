<template>
   <footer>
       <div class="center">
            <div class="signup-social">
                <button>SIGN-UP NOW!</button>
            </div>
            <div class="social-box">
                <span>FOLLOW US</span>
                <img src="@/assets/img/footer-facebook.png" alt="#">
                <img src="@/assets/img/footer-twitter.png" alt="#">
                <img src="@/assets/img/footer-youtube.png" alt="#">
                <img src="@/assets/img/footer-pinterest.png" alt="#">
                <img src="@/assets/img/footer-periscope.png" alt="#">
            </div>
       </div>
   </footer>
</template>

<script>
export default {
  name: 'Footer'
}
</script>

<style scoped lang="scss">
footer{
    display: flex;
    background-color: #303030;
    justify-content: space-between;
    align-items: center;
    height: 100px;
    button {
    background-color: #303030;
    border: 3px solid #1462ab;
    color: white;
    padding: 15px 32px;
    text-align: center;
    text-decoration: none;
    display: inline-block;
    font-size: 16px;
    }
    .center{
        display: flex;
        width: 80%;
        margin: 0 auto;
        align-items: center;
        justify-content: space-between;
    }
    span{
        color: #0689ff;
        margin: 0 20px;
    }
    .social-box{
        display: flex;
        align-items: center;
        justify-content: flex-end;
    }
    img{
        margin: 0 7px;
    }
}
</style>
