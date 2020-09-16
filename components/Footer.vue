<template>
    <footer class="footer"  v-scroll-reveal="{ origin: 'bottom', duration: 1000, distance: '25rem', delay: 300 }">
<!--        <div id="map" class="footer__map">-->

<!--        </div>-->
        <GMap
                ref="gMap"
                language="en"
                :cluster="{options: {styles: clusterStyle}}"
                :center="{lat: locations[0].lat, lng: locations[0].lng}"
                :options="{fullscreenControl: false, styles: mapStyle}"
                :zoom="6"
                class="footer__map"
        >
            <GMapMarker
                    v-for="location in locations"
                    :key="location.id"
                    :position="{lat: location.lat, lng: location.lng}"
                    :options="{icon: location === currentLocation ? pins.selected : pins.notSelected}"
                    @click="currentLocation = location"
            >
                <GMapInfoWindow :options="{maxWidth: 200}">
                    <code>
                        lat: {{ location.lat }},
                        lng: {{ location.lng }}
                    </code>
                </GMapInfoWindow>
            </GMapMarker>
            <GMapCircle :options="circleOptions"/>
        </GMap>
        <div class="footer__info">
            <div class="footer__left">
                <p class="footer__address">90802 California<br> Long beach<br> PO Box 68789<br> 300 East Ocean<br> Boulevard</p>
                <p class="footer__contacts">
                    <a class="footer__tel" href="tel:+6493456758">+64 9 345 6758</a>
                    <br>
                    <a class="footer__mail" href="mailto:info@dsgn-studio.com">info@dsgn-studio.com</a>
                </p>
            </div>
            <div class="footer__right">
                <img class="footer__logo"
                     src="~/assets/img/logo.png"
                     alt="Логотип"
                     srcset="~/assets/img/logo.png 1x,
                             ~/assets/img/logo-2x.png 2x"
                >
                <p class="footer__slogan">ASSOCIATES<br> STUDIO<br> DESIGN</p>

                <Social class="footer__socials" />
            </div>
            <p class="footer__copy">&copy; 2014  DSGN. All rights reserved - Designed by theuncreativelab.com</p>
        </div>
    </footer>
</template>

<script>
    import Social from '~/components/Social'

    export default {
        name: "Footer",
        data() {
            return {
                currentLocation: {},
                circleOptions: {},
                locations: [
                    {
                        lat: 44.933076,
                        lng: 15.629058
                    },
                    {
                        lat: 45.815,
                        lng: "15.9819"
                    },
                    {
                        lat: "45.12",
                        lng: "16.21"
                    }
                ],
                pins: {
                    selected: "data:image/png;base64,iVBORw0KGgo...",
                    notSelected: "data:image/png;base64,iVBORw0KGgo..."
                },
                mapStyle: [
                    {
                        "featureType": "water",
                        "elementType": "geometry",
                        "stylers": [
                            {
                                "color": "#e9e9e9"
                            },
                            {
                                "lightness": 17
                            }
                        ]
                    },
                    {
                        "featureType": "landscape",
                        "elementType": "geometry",
                        "stylers": [
                            {
                                "color": "#f5f5f5"
                            },
                            {
                                "lightness": 20
                            }
                        ]
                    },
                    {
                        "featureType": "road.highway",
                        "elementType": "geometry.fill",
                        "stylers": [
                            {
                                "color": "#ffffff"
                            },
                            {
                                "lightness": 17
                            }
                        ]
                    },
                    {
                        "featureType": "road.highway",
                        "elementType": "geometry.stroke",
                        "stylers": [
                            {
                                "color": "#ffffff"
                            },
                            {
                                "lightness": 29
                            },
                            {
                                "weight": 0.2
                            }
                        ]
                    },
                    {
                        "featureType": "road.arterial",
                        "elementType": "geometry",
                        "stylers": [
                            {
                                "color": "#ffffff"
                            },
                            {
                                "lightness": 18
                            }
                        ]
                    },
                    {
                        "featureType": "road.local",
                        "elementType": "geometry",
                        "stylers": [
                            {
                                "color": "#ffffff"
                            },
                            {
                                "lightness": 16
                            }
                        ]
                    },
                    {
                        "featureType": "poi",
                        "elementType": "geometry",
                        "stylers": [
                            {
                                "color": "#f5f5f5"
                            },
                            {
                                "lightness": 21
                            }
                        ]
                    },
                    {
                        "featureType": "poi.park",
                        "elementType": "geometry",
                        "stylers": [
                            {
                                "color": "#dedede"
                            },
                            {
                                "lightness": 21
                            }
                        ]
                    },
                    {
                        "elementType": "labels.text.stroke",
                        "stylers": [
                            {
                                "visibility": "on"
                            },
                            {
                                "color": "#ffffff"
                            },
                            {
                                "lightness": 16
                            }
                        ]
                    },
                    {
                        "elementType": "labels.text.fill",
                        "stylers": [
                            {
                                "saturation": 36
                            },
                            {
                                "color": "#333333"
                            },
                            {
                                "lightness": 40
                            }
                        ]
                    },
                    {
                        "elementType": "labels.icon",
                        "stylers": [
                            {
                                "visibility": "off"
                            }
                        ]
                    },
                    {
                        "featureType": "transit",
                        "elementType": "geometry",
                        "stylers": [
                            {
                                "color": "#f2f2f2"
                            },
                            {
                                "lightness": 19
                            }
                        ]
                    },
                    {
                        "featureType": "administrative",
                        "elementType": "geometry.fill",
                        "stylers": [
                            {
                                "color": "#fefefe"
                            },
                            {
                                "lightness": 20
                            }
                        ]
                    },
                    {
                        "featureType": "administrative",
                        "elementType": "geometry.stroke",
                        "stylers": [
                            {
                                "color": "#fefefe"
                            },
                            {
                                "lightness": 17
                            },
                            {
                                "weight": 1.2
                            }
                        ]
                    }
                ],
                clusterStyle: [
                    {
                        url: "https://developers.google.com/maps/documentation/javascript/examples/markerclusterer/m1.png",
                        width: 56,
                        height: 56,
                        textColor: "#fff"
                    }
                ]
            }
        },
        components: {
            Social
        }

    }
</script>

<style>
    .GMap__Wrapper {
        height: 100%!important;
    }
</style>
<style lang="postcss" scoped>
    .footer {
        display: grid;
        grid-template-columns: repeat(2, 1fr);

        @media (max-width: 768px) {
            grid-template-columns: 1fr;
        }

        &__left {
            margin-left: 15.3%;
            margin-top: 20%;

            @media (max-width: 768px) {
                margin-left: 5%;
            }
            @media (max-width: 560px) {
                text-align: center;
                margin-right: 5%;
                margin-top: 10%;
            }
        }
        &__right {
            margin-right: 22%;
            margin-top: 20%;

            @media (max-width: 1500px) {
                margin-right: 2%;
            }
            @media (max-width: 768px) {
                margin-right: 5%;
            }
            @media (max-width: 560px) {
                text-align: center;
                margin-left: 5%;
                margin-top: 5%;
            }
        }
        &__map {
            grid-column: span 1;

            @media (max-width: 768px) {
                height: 400px;
                /*padding-bottom: 75%;*/
            }
        }
        &__info {
            display: flex;
            flex-wrap: wrap;
            justify-content: space-between;
            grid-column: span 1;

            @media (max-width: 560px) {
                display: block;
            }
            @media (max-width: 380px) {
                justify-content: center;
            }
        }
        &__logo {
            display: block;
            max-width: 100%;

            @media (max-width: 560px) {
                margin: 0 auto;
            }
        }
        &__slogan {
            font-size: 18px;
            color: var(--colorText);
            text-transform: uppercase;
            line-height: 1;
            margin: 5px 0 0;
        }
        &__socials {
            margin-top: 60px;
            margin-left: 15px;
            margin-bottom: 15px;

            @media (max-width: 560px) {
                margin-left: 0;
                justify-content: center;
            }
        }
        &__address {
            font-size: 13px;
            color: var(--colorText);
            text-transform: uppercase;
            line-height: 1.077;
            margin: 10% 0;
        }
        &__contacts {
            font-size: 13px;
            color: var(--colorText);
            text-transform: uppercase;
            line-height: 1.077;
            margin: 10% 0;
        }
        &__tel, &__mail {
            color: var(--colorText);
            line-height: 1.077;
            text-decoration: none;
            display: inline-block;
            transition-property: color;
            transition-duration: 500ms;

            &:hover {
                color: var(--activeTextColor);
            }

        }
        &__copy {
            font-size: 12px;
            color: var(--colorText);
            line-height: 1.8;
            text-align: center;
            flex-basis: 100%;
            margin: 9% 0 7% 0;
        }
    }
</style>