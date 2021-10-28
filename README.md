# interior-scene-test.io
testing
Skip to content
Search or jump to…
Pull requests
Issues
Marketplace
Explore
 
@JayDeep2204 
AR-js-org
/
AR.js
Public
132
2.8k478
Code
Issues
141
Pull requests
5
Discussions
Actions
Projects
Wiki
Security
Insights
AR.js/aframe/examples/image-tracking/nft/index.html
@kalwalt
kalwalt fix for nft aframe examples
Latest commit 0cba0b7 on Apr 22
 History
 2 contributors
@nicolocarpignoli@kalwalt
50 lines (45 sloc)  1.5 KB
   
<script src='https://cdn.jsdelivr.net/gh/aframevr/aframe@1c2407b26c61958baa93967b5412487cd94b290b/dist/aframe-master.min.js'></script>

<style>
  .arjs-loader {
    height: 100%;
    width: 100%;
    position: absolute;
    top: 0;
    left: 0;
    background-color: rgba(0, 0, 0, 0.8);
    z-index: 9999;
    display: flex;
    justify-content: center;
    align-items: center;
  }

  .arjs-loader div {
    text-align: center;
    font-size: 1.25em;
    color: white;
  }
</style>

<!-- rawgithack development URL -->
<script src='https://raw.githack.com/AR-js-org/AR.js/master/aframe/build/aframe-ar-nft.js'></script>

<body style='margin : 0px; overflow: hidden;'>
   <!-- minimal loader shown until image descriptors are loaded -->
  <div class="arjs-loader">
    <div>Loading, please wait...</div>
  </div>
    <a-scene
        vr-mode-ui='enabled: false;'
        renderer="logarithmicDepthBuffer: true;"
        embedded arjs='trackingMethod: best; sourceType: webcam; debugUIEnabled: false;'>

        <!-- use rawgithack to retrieve the correct url for nft marker (see 'pinball' below) -->
        <a-nft
            type='nft' url='./aframe/examples/image-tracking/nft/trex/trex-image/trex'
            smooth='true' smoothCount='10' smoothTolerance='0.01' smoothThreshold='5'>
            <a-entity
                gltf-model='./trex/scene.gltf'
                scale="5 5 5"
                position="150 300 -100"
                >
            </a-entity>
        </a-nft>
		<a-entity camera></a-entity>
    </a-scene>
</body>
© 2021 GitHub, Inc.
Terms
Privacy
Security
Status
Docs
Contact GitHub
Pricing
API
Training
Blog
About
Loading complete
