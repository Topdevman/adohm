<template>
  <div class="search-detail">
    <div id="card" class="detail-pannel">

    <!-- Title -->
      <div class="top-area">
        <div class="title-area">
          <span class="pannel-title">Campaign type</span>
        </div>
      <!-- End Title -->
      <!-- Sub Title -->
        <div class="items-area">
          <div>            
            <span class="pannel-title">Select a campaign type
                <i class="fa fa-question-circle" aria-hidden="true"></i></span>
          </div>
      <!-- End Sub Title -->        
      <!-- Cards -->
          <div class="menutab-area">
            <router-link to="/search/addcampaign/searchnetwork"
                id="card"
                class="tab-card"
                v-bind:class="{activetab: isSearchActive}">
              <div class="content-text-title">
                <i class="fa fa-search"
                  aria-hidden="true"
                  v-bind:class="{network: !isSearchActive}"></i>
                  <span>Search Network</span>
              </div>            
            </router-link>
            <router-link to="/search/addcampaign/displaynetwork"
                id="card"
                class="tab-card"
                v-bind:class="{activetab: isDisplayActive}">
              <div class="content-text-title">
                <i class="fa fa-rss-square"
                  aria-hidden="true"
                  v-bind:class="{network: !isDisplayActive}"></i>
                  <span>Display Network</span>
              </div>            
            </router-link>
            <router-link to="/search/addcampaign/shopping"
                id="card"
                class="tab-card"
                v-bind:class="{activetab: isShopActive}">
              <div class="content-text-title">
                <i class="fa fa-tags"
                  aria-hidden="true"
                  v-bind:class="{network: !isShopActive}"></i>
                  <span>Shopping</span>
              </div>            
            </router-link>
            <router-link to="/search/addcampaign/video"
                id="card"
                class="tab-card"
                v-bind:class="{activetab: isVideoActive}">
              <div class="content-text-title">
                <i class="fa fa-video-camera"
                  aria-hidden="true"
                  v-bind:class="{network: !isVideoActive}"></i>
                  <span>Video</span>
              </div>            
            </router-link>
            <router-link to="/search/addcampaign/universalapp"
                id="card"
                class="tab-card"
                v-bind:class="{activetab: isAppActive}">
              <div class="content-text-title">
                <i class="fa fa-android"
                  aria-hidden="true"
                  v-bind:class="{network: !isAppActive}"></i>
                  <span>Universal App</span>
              </div>            
            </router-link>
          </div>
        </div>
      <!-- End Cards -->        
      </div>
      <router-view></router-view>
		</div>
  </div>
</template>
<script>
export default {
  name: 'SearchNetwork',
  data: function () {
    return {
      isSearchActive: false,
      isDisplayActive: false,
      isShopActive: false,
      isVideoActive: false,
      isAppActive: false
    }
  },
  mounted: function () {
    switch (this.$route.name) {
      case 'UniversalApp':
        this.isAppActive = true
        break
      case 'DisplayNetwork':
        this.isDisplayNetwork = true
        break
      case 'Shopping':
        this.isShopActive = true
        break
      case 'Video':
        this.isVideoActive = true
        break
      default:
        this.isSearchActive = true
        break
    }
  }
}
</script>
<style>
  .search-detail {
    width: 100%;
    padding: 40px;
  }
  .detail-pannel {
    display: block;
    width: 100%;
  }
  .top-area {
    display: inline-flex;
    width: 100%;
    padding: 20px 0px 0px 20px;
  }
  .title-area, .items-area, .card-item {
    display: inline-block !important;
  }
  .title-area {
    width: 20%;
  }
  .items-area {
    width: 100%;
  }
  .network {
    border-style: solid;
    border-color: rgba(0,0,0,0.04);
    border-width: 2px;
    background-color: rgba(0,0,0,0.7);
    border-radius: 2px;
    color: #ffffff;
  }
  .content-text {
    text-align: center;
  }
  .content-text span {
    font-size: smaller;
  }
  .pannel-title {
    padding: 0px 40px 0px 0px;
  }
  .menutab-area {
    width: 100%;
    display: inline-flex;
  }  
  .tab-card {
    margin: 10px 20px 0px 0px;
    padding: 10px 15px 10px 15px;
    background-color: rgba(0,0,0,0.04) !important;
    width: 20%;
    text-align: center;
  }
  .card-item:hover {
    background-color: rgba(0,0,0,0.08) !important;    
  }
  .activetab {
    color: #ffffff !important;
    background-color: #1e72de !important;
    border-top-left-radius: 3px;
    border-top-right-radius: 3px;
  }
  @media (max-width: 1350px){
    .content-text-title span {
      display: none;
    }
}
  
</style>

