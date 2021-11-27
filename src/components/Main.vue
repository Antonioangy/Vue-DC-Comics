<template>
    <main>
        <div id="black">
          <div id="comics-container" class="container">
            <div class="btn">
              <button>CURRENT SERIES </button>
            </div>
            <ul class="sub-menu">
              <li v-for="(comic, i) in comics" :key="i" class="comic">
                <img :src="comic.thumb" class="comicimg">
                <div>
                  <h3>{{comic.series}}</h3>
                </div>
              </li>
            </ul>
          </div>
          <div class="btn">
            <button>LOAD MORE</button>
          </div>
        </div>

        <div id="containerblu">
            <div class="list-container">
              <ul class="sub-menu">
                <li v-for="(card, i) in cards" :key="i" class="item">
                  <img :src="require(`../assets/img/${card.image}`)"/>
                  <div class="sub-menu-text">
                    <h3>{{card.text}}</h3>
                  </div>
                </li>
              </ul>
            </div>
        </div>
    </main>
</template>

<script>
export default {
  name: 'Main',
  data () {
    return {
      cards: [
        {
          text: 'Digital Comics',
          image: 'buy-comics-digital-comics.png'
        },
        {
          text: 'DC Merchandise',
          image: 'buy-comics-merchandise.png'
        },
        {
          text: 'Subscriptions',
          image: 'buy-comics-subscriptions.png'
        },
        {
          text: 'Comic Shop Locator',
          image: 'buy-comics-shop-locator.png'
        },
        {
          text: 'DC Power Visa',
          image: 'buy-dc-power-visa.svg'
        }
      ],
      comics: [
        {
          thumb: 'https://www.dccomics.com/sites/default/files/styles/covers192x291/public/comic-covers/2018/09/AC1000_DLX_162-001_HD_5ba13723281ab0.37845353.jpg?itok=ZsI-C5eX',
          price: '$19.99',
          series: 'Action Comics',
          type: 'comic book'
        },
        {
          thumb: 'https://www.dccomics.com/sites/default/files/styles/covers192x291/public/comic-covers/2020/09/AV1976_01_300-001_HD_5f738f6e39ddd7.18205602.jpg?itok=VgdYdJ01',
          price: '$3.99',
          series: 'American Vampire 1976',
          type: 'comic book'
        },
        {
          thumb: 'https://www.dccomics.com/sites/default/files/styles/covers192x291/public/gn-covers/2018/08/AQMv4_UW_153-001_HD_5b7efa1745a9b8.08589135.jpg?itok=HPTtnrsb',
          prices: '$16.99',
          series: 'Aquaman',
          type: 'graphic novel'
        },
        {
          thumb: 'https://www.dccomics.com/sites/default/files/styles/covers192x291/public/comic-covers/2018/06/batgirl_v5_1_5b23e1f1124941.50950783.jpg?itok=VnrJah76',
          prices: '$2.99',
          series: 'Batgirl',
          type: 'comic book'
        },
        {
          thumb: 'https://www.dccomics.com/sites/default/files/styles/covers192x291/public/comic-covers/2018/09/BM_56_300-001_HD_5ba137a85c3bf3.33122291.jpg?itok=3FHJQYJZ',
          prices: '$3.99',
          series: 'Batman',
          type: 'comic book'
        },
        {
          thumb: 'https://www.dccomics.com/sites/default/files/styles/covers192x291/public/comic-covers/2018/09/BM_56_300-001_HD_5ba137a85c3bf3.33122291.jpg?itok=3FHJQYJZ',
          prices: '$2.99',
          series: 'Batman Beyond',
          type: 'comic book'
        },
        {
          thumb: 'https://www.dccomics.com/sites/default/files/styles/covers192x291/public/comic-covers/2019/08/BMSM_5d4361b7116261.74371456.jpg?itok=kEDR2OL8',
          prices: '$3.99',
          series: 'Batman/Superman',
          type: 'comic book'
        },
        {
          thumb: 'https://www.dccomics.com/sites/default/files/styles/covers192x291/public/comic-covers/2020/09/BMSMANN_01_300-001_HD_5f5ff17fa1d665.74704970.jpg?itok=azz5sfGk',
          prices: '$4.99',
          series: 'Batman/Superman Annual',
          type: 'comic book'
        },
        {
          thumb: 'https://www.dccomics.com/sites/default/files/styles/covers192x291/public/comic-covers/2020/09/BMTJWZ_01_300-001_HD_5f5ff2307dcb37.34652945.jpg?itok=VswVjLR8',
          prices: '$5.99',
          series: 'Batman: The Joker War Zone',
          type: 'comic book'
        },
        {
          thumb: 'https://www.dccomics.com/sites/default/files/styles/covers192x291/public/comic-covers/2020/08/cover-v2_5f40314645a734.37285065.png?itok=ImNM2QBY',
          prices: '$6.99',
          series: 'Batman: Three Jokers',
          type: 'comic book'
        },
        {
          thumb: 'https://www.dccomics.com/sites/default/files/styles/covers192x291/public/comic-covers/2020/10/BMWK_HQ_01_300-001_HD_5f7cb4945e13f6.89501032.jpg?itok=sVwALbUX',
          prices: '$4.99',
          series: 'Batman: White Knight Presents: Harley Quinn',
          type: 'comic book'
        },
        {
          thumb: 'https://www.dccomics.com/sites/default/files/styles/covers192x291/public/gn-covers/2019/04/CTWv1_CC_144-001_HD_5ca5299a751963.53054221.jpg?itok=ooPaoLDq',
          prices: '$16.99',
          series: 'Catwoman',
          type: 'graphic novel'
        }
      ]
    }
  }
}

</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
#black {
  display: flex;
  align-items: center;
  height: 400px;
  background-color: black;
  color: white;
  width: 100%;
  .container{
    width: 80%;
    margin: 0 auto;
  }
  .content{
    float: left;
    font-size: 25px;
  }
}
#containerblu {
  height: 150px;
  background-color: #0282f9;
  display: flex;
  align-items: center;
}
.list-container{
  width: 100%;
}
.sub-menu{
  display: flex;
  justify-content: space-around;
  list-style: none;
}
.sub-menu-text{
  display: inline;
  margin-left: 10%;
}
.item{
  display: flex;
  justify-content: center;
  align-items: center;
}
img{
  height: 80px;
  align-items: center;
}
h3{
  color: #d3e9fe;
}
.comics{
  flex-wrap: wrap;
}
.comicimg{
  height: 200px;
}
.btn {
  text-align: center;
  button {
    margin: 0 auto;
    background-color: #0d69f6;
    padding: 10px 30px;
    font-size: .7em;
    color: white;
    font-weight: bold;
    border: 0;
    margin-bottom: 20px;
  }
}
</style>
