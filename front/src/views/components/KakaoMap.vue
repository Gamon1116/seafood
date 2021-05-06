<template>
  <div id="app">
      <!-- 맵위치 -->
    <div id="map"></div>
    <br>
    <div id="address">
        주소: 전남 여수시 망양로482-9
        <br>
        Tel: 123-456-789
    </div>
    <br>
  </div>
</template>

<script>
export default {
    mounted() {
        if (window.kakao && window.kakao.maps) {
            this.initMap();
        } else {
            const script = document.createElement('script');
            /* global kakao */
            script.onload = () => kakao.maps.load(this.initMap);
            script.src = 'http://dapi.kakao.com/v2/maps/sdk.js?autoload=false&appkey=a7cb307437cf02090b0b5c00c3eb40d9';
            document.head.appendChild(script);
        }
    },
    methods: {
        initMap() {
            var mapContainer = document.getElementById('map'), // 지도를 표시할 div 
            mapOption = {
	        center: new kakao.maps.LatLng(34.78837407579715, 127.7516987402418), // 지도의 중심좌표
	        level: 3, // 지도의 확대 레벨
	        mapTypeId : kakao.maps.MapTypeId.ROADMAP // 지도종류
	    }; 
        // 지도를 생성한다 
        var map = new kakao.maps.Map(mapContainer, mapOption); 
        // 지도에 마커를 생성하고 표시한다
        var marker = new kakao.maps.Marker({
            position: new kakao.maps.LatLng(34.78837407579715, 127.7516987402418), // 마커의 좌표
            map: map // 마커를 표시할 지도 객체
        });
            // map.setMapTypeId(kakao.maps.MapTypeId.HYBRID);
        }
    }
}
</script>

<style>
#map {
    width: 750px;
    height: 350px;
    margin: 0 auto;
}
#address{
    width: 200px;
    margin: 0 auto;
}
</style>

