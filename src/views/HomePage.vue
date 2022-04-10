<template>
  <div>
      <header>
        <h1>大数据可视化 - vue3与echarts</h1>
      </header>
      <section class="container">
             <!-- 左容器 -->
              <section class="itemleft">
                <ItemPage>
                   <ItemOne></ItemOne>
                </ItemPage>
                <ItemPage>
                   <ItemTwo></ItemTwo>
                </ItemPage>
              </section>
            <!-- 中容器 -->
              <section class="itemcenter">
                <MapPage></MapPage>
              </section>
             <!-- 右容器 -->
             <section class="itemright">
               <ItemPage>
                   <ItemThree></ItemThree>
                </ItemPage>
                <ItemPage>
                   <ItemFour></ItemFour>
                </ItemPage>
             </section>
      </section>
  </div>
</template>

<script>
import ItemPage from '@/components/ItemPage.vue'
import ItemOne from '@/components/ItemOne.vue'
import ItemTwo from '@/components/ItemTwo.vue'
import ItemThree from '@/components/ItemThree.vue'
import ItemFour from '@/components/ItemFour.vue'
import MapPage from '@/components/MapPage.vue'
export default {
  components: {
    ItemPage,
    ItemOne,
    ItemTwo,
    ItemThree,
    ItemFour,
    MapPage
  },
  setup () {

  }
}
</script>

<style lang="scss" scoped>
header {
  height: 1rem;
  width: 100%;
  background-color: rgba(0, 0, 255, 0.2);
  h1 {
    font-size: .375rem;
    color: #fff;
    text-align: center;
    line-height: 1rem;
  }
}
.container {
   min-width: 1200px;
   max-width: 2048px;
   margin: 0 auto;
   border: 1px solid red;
   padding: .125rem .125rem 0;
   display: flex;
   .itemleft,.itemright {
     flex: 3;
   }
   .itemcenter {
     flex: 5;
     height: 10.5rem;
     border: 1px solid blue;
     padding: .125rem;
     margin: .25rem;
   }
}
</style>
