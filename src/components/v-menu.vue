<template>
  <div class="menu">
    <div class="profile-wrap">
      <div class="profile">
        <div class="thrum">
          <img src="../assets/images/thrum.jpg" alt="">
        </div>
        <div class="name">天璇真人™</div>
      </div>
    </div>
    <div class="nav-wrap" v-iscroll>
      <div>
        <v-nav :typeTitle="'音乐馆'" :typeName="musicHall"></v-nav>
      </div>
    </div>
  </div>
</template>

<script>
  import VNav from '@/components/v-nav'
  export default {
    name: 'menu',
    components: {
      VNav
    },
    created () {
      this.musicHall = [
        {
          link: '/selected',
          name: '精选',
          iconName: 'icon-selected'
        },
        {
          link: '/rank',
          name: '排行',
          iconName: 'icon-rank'
        },
        {
          link: '/sheet',
          name: '歌单',
          iconName: 'icon-sheet'
        },
        {
          link: '/singer',
          name: '歌手',
          iconName: 'icon-singer'
        }
      ]
    }
  }
</script>

<style lang="scss" scoped>
  @import '~@/assets/scss/variable';
  .nav-wrap {
    position: absolute;
    left: 0;
    right: 0;
    top: 128px;
    bottom: 0;
    width: 100%;
    overflow: hidden;
  }
  .menu {
    position: relative;
    float: left;
    width: $menu-width;
    height: 100%;
    background-color: $menu-bg-color;
  }
  .profile-wrap {
    padding: 0 $module-padding;
  }
  .profile {
    padding: $module-padding*2 0 $module-padding;
    border-bottom: 1px solid #d5d3d2;
    .thrum {
      width: 48px;
      height: 48px;
      margin: 0 auto;
      border-radius: 50%;
      overflow: hidden;
    }
    .name {
      height: 34px;
      line-height: 34px;
      text-align: center;
      font-size: $font-size-base;
      color: $black;
    }
    img {
      width: 100%;
      height: 100%;
    }
  }
</style>
