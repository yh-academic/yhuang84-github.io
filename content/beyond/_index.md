---
title: "Beyond"
url: /beyond/
---

Things I enjoy outside of work.

## Kendo

I started practicing Kendo in 2024, and I’d like to pursue it as a lifelong journey.

<div class="img-pair">
  <figure>
    <img src="/images/Kendo_001.jpg" alt="Kendo practice">
    <figcaption>At Nanto Bukan East Georgia Kendo Club</figcaption>
  </figure>
  <figure>
    <img src="/images/Kendo_002.jpg" alt="Kendo practice">
    <figcaption>At Costa Mesa Kendo Dojo</figcaption>
  </figure>
</div>

## Movie

I love watching movies in my spare time. I enjoy spending time at independent movie theaters and attending film festivals.

<div class="img-pair">
  <figure>
    <img src="/images/Jet_Li.jpg" alt="Jet Li as guest speaker for Once Upon a Time in China">
    <figcaption>Jet Li as guest speaker for Once Upon a Time in China.</figcaption>
  </figure>
  <figure>
    <img src="/images/Bong_Fincher.jpg" alt="Q&A for Zodiac with Bong Joon-ho and David Fincher">
    <figcaption>Q&A for Zodiac with Bong Joon-ho and David Fincher.</figcaption>
  </figure>
  <figure>
    <img src="/images/Park_Lee.jpg" alt="Q&A for Joint Security Area with Park Chan-wook and Lee Byung-hun">
    <figcaption>Q&A for Joint Security Area with Park Chan-wook and Lee Byung-hun.</figcaption>
  </figure>
  <figure>
    <img src="/images/zhizhi.jpg" alt="Q&A for Still Walking with Hirokazu Kore-eda">
    <figcaption>Q&A for Still Walking with Hirokazu Kore-eda.</figcaption>
  </figure>
</div>


## Travled Cities

Cities that I have traveled since 2019

<link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/leaflet/1.9.4/leaflet.min.css">

<div id="travel-map" style="height: 460px; border-radius: 8px; overflow: hidden; margin: 1.5rem 0; border: 0.5px solid #cdd4e5;"></div>

<script src="https://cdnjs.cloudflare.com/ajax/libs/leaflet/1.9.4/leaflet.min.js"></script>
<script>
const map = L.map('travel-map', { zoomControl: true, scrollWheelZoom: false }).setView([30, 15], 2);

L.tileLayer('https://server.arcgisonline.com/ArcGIS/rest/services/Canvas/World_Light_Gray_Base/MapServer/tile/{z}/{y}/{x}', {
    attribution: 'Powered by Esri',
    maxZoom: 16
}).addTo(map);

const markerStyle = `
    width: 14px; height: 14px;
    background: #2774AE;
    border: 3px solid #FFD100;
    border-radius: 50%;
    cursor: pointer;
`;

const cities = [
    { name: "Athens", coords: [33.9519, -83.3576], photo: "/images/cities/Athens.jpg" },
    { name: "Atlanta", coords: [33.7490, -84.3880], photo: "/images/cities/Atlanta.jpg" },
    { name: "Chengdu", coords: [30.5728, 104.0668], photo: "/images/cities/Chengdu.jpg" },
    { name: "Chicago", coords: [41.8781, -87.6298], photo: "/images/cities/Chicago.jpg" },
    { name: "Washington D.C.", coords: [38.9072, -77.0369], photo: "/images/cities/Washington D.C..jpg" },
    { name: "Death Valley", coords: [36.5323, -116.9325], photo: "/images/cities/Death Valley.jpg" },
    { name: "Denver", coords: [39.7392, -104.9903], photo: "/images/cities/Denver.jpg" },
    { name: "Joshua Tree", coords: [33.8734, -115.9010], photo: "/images/cities/Joshua tree.jpg" },
    { name: "Kyoto", coords: [35.0116, 135.7681], photo: "/images/cities/Kyoto.jpg" },
    { name: "Las Vegas", coords: [36.1699, -115.1398], photo: "/images/cities/Las Vegas.jpg" },
    { name: "New York", coords: [40.7128, -74.0060], photo: "/images/cities/New York.jpg" },
    { name: "Osaka", coords: [34.6937, 135.5023], photo: "/images/cities/Osaka.jpg" },
    { name: "Philadelphia", coords: [39.9526, -75.1652], photo: "/images/cities/Philadephia.jpg" },
    { name: "Qingtian", coords: [28.1374, 120.2904], photo: "/images/cities/Qingtian.jpg" },
    { name: "Salt Lake City", coords: [40.7608, -111.8910], photo: "/images/cities/Salt Lake City.jpg" },
    { name: "Shanghai", coords: [31.2304, 121.4737], photo: "/images/cities/Shanghai.jpg" },
    { name: "Singapore", coords: [1.3521, 103.8198], photo: "/images/cities/Sinapore.jpg" },
    { name: "Smoky Mountains", coords: [35.6532, -83.5070], photo: "/images/cities/Smoky Mountains.jpg" },
    { name: "Xi'an", coords: [34.3416, 108.9398], photo: "/images/cities/Xi'an.jpg" },
    { name: "Yellowstone", coords: [44.4280, -110.5885], photo: "/images/cities/Yellowstone.jpg" },
];

cities.forEach(city => {
    const icon = L.divIcon({
        className: '',
        html: `<div style="${markerStyle}"></div>`,
        iconSize: [14, 14],
        iconAnchor: [7, 7],
        popupAnchor: [0, -10]
    });

    L.marker(city.coords, { icon }).addTo(map).bindPopup(`
        <div style="width: 200px; font-family: 'Geist', sans-serif;">
            <img src="${city.photo}"
                 style="width: 100%; height: 130px; object-fit: cover; border-radius: 4px; display: block; margin-bottom: 8px;">
            <div style="font-weight: 600; font-size: 13px; color: #0d2550; text-align: center;">${city.name}</div>
        </div>
    `, { maxWidth: 220 });
});
</script>