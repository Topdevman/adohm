<template>
  <div class="add-campaign">
    <div id="card" class="campaign-pannel">

    <!-- Title -->
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
        <div class="allcard-height">
          <router-link to="/search/addcampaign/searchnetwork" id="card" class="card-item">
            <div class="content-text-title">
              <span><i class="fa fa-search network" aria-hidden="true"></i>
                    Search Network</span>
            </div>
            <img class="advertise" src="static/images/social.png" />            
            <div class="content-text">
              <span>Reach customers<br />
                    interested in your product<br />
                    or service with text ads</span>
            </div>
          </router-link>
          <router-link to="/search/addcampaign/detail" id="card" class="card-item">
            <div class="content-text-title">
              <span><i class="fa fa-tags network" aria-hidden="true"></i></i>
                    Display Network</span>
            </div>
            <img class="advertise" src="static/images/network.png" />
            <div class="content-text">
              <span>Run different kinds of<br />                   
                    ads across the web</span>
            </div>
          </router-link>
          <router-link to="/search/addcampaign/detail" id="card" class="card-item">
            <div class="content-text-title">
              <span><i class="fa fa-tags network" aria-hidden="true"></i>
                    Shopping</span>
            </div>
            <img class="advertise" src="static/images/shopping.png" />
            <div class="content-text">
              <span>Promote your products<br />                   
                    with Shopping ads</span>
            </div>
          </router-link>
          <router-link to="/search/addcampaign/detail" id="card" class="card-item">
            <div class="content-text-title">
              <span><i class="fa fa-video-camera network" aria-hidden="true"></i></i>
                    Video</span>
            </div>
            <img class="advertise" src="static/images/video.png" />
            <div class="content-text">
              <span>Reach and engage<br />
                    viewers on YouTube and<br />
                    across the web</span>
            </div>
          </router-link>
          <router-link to="/search/addcampaign/detail" id="card" class="card-item">
            <div class="content-text-title">
              <span><i class="fa fa-android network" aria-hidden="true"></i></i>
                    Universal App</span>
            </div>
            <img class="advertise" src="static/images/universal.png" />
            <div class="content-text">
              <span>Drive app installs across<br />                    
                    Google`s networks</span>
            </div>
          </router-link>
        </div>
      <!-- End Cards -->
        </div>
      </div>
		</div>
  </div>
</template>

<script>
  export default {
    name: 'AddSearchCampagin'
  }
</script>
<style>
  .add-campaign {
    display: inline-block;
    width: 100%;
    padding: 40px;
    z-index: 2;
  }
  .campaign-pannel {
    width: 100%;
    padding: 20px 0px 20px 20px;
    display: inline-flex;
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
  .allcard-height {
    display: flex;
  }
  .card-item {
    margin-right: 20px;
    margin: 10px 20px 0px 0px;
    padding: 15px;
    background-color: rgba(0,0,0,0.04) !important;
    width: 20%;
    text-align: center;
  }
  .card-item:hover {
    background-color: rgba(0,0,0,0.08) !important;    
  }
  .advertise {
     padding: 10px 0px 10px 0px;
  }
  @media (max-width: 1350px){
    .allcard-height {
      display: inherit;
    }
    .card-item {
      width: 230px;
      height: 265px;
      float: left;
    }
  }
  
</style>
