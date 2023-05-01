<template>
    <div v-if="response">
        <b-skeleton-wrapper :loading="loading">
            <template #loading>
                <b-card>
                    Fetching weather details...
                    <b-skeleton width="85%"></b-skeleton>
                    <b-skeleton width="55%"></b-skeleton>
                    <b-skeleton height="70%"></b-skeleton>
                    <b-skeleton width="85%"></b-skeleton>
                    <b-skeleton height="55%"></b-skeleton>
                    <b-skeleton height="70%"></b-skeleton>
                    <b-skeleton width="85%"></b-skeleton>
                    <b-skeleton width="55%"></b-skeleton>
                    <b-skeleton height="70%"></b-skeleton>
                    <b-skeleton width="85%"></b-skeleton>
                    <b-skeleton height="55%"></b-skeleton>
                    <b-skeleton height="70%"></b-skeleton>
                </b-card>
            </template>
            <b-card id="weather-card">
                <h3 class="text-center"> Weather</h3>
                <div>
                    <b-row>
                        <b-col sm="9">
                            <b-form-input v-model="input_city" placeholder="Search City"></b-form-input>
                        </b-col>
                        <b-col sm="3">
                            <button class="btn btn-success" @click="fetchWeather()">
                                <b-icon icon="search"></b-icon> Search
                            </button>
                        </b-col>
                    </b-row>
                </div>
                <div class="text-center">
                    <br>
                    <h4>
                        <b-icon :icon="sky_icon" font-scale="3"></b-icon><br>
                        {{ sky }}
                    </h4>
                    <div>
                        <h2>
                            <b>
                                {{ temperature }}°C
                            </b>
                        </h2>
                    </div>
                    <div>
                        <h2>
                            <b>
                                {{ city }}
                            </b>
                        </h2>
                    </div>
                </div>
                <div class="d-flex justify-content-between">
                    <div>
                        <div>
                            <b-icon icon="thermometer-half" font-scale="3"></b-icon>
                        </div>
                        {{ humidity }} <br>
                        Humidity
                    </div>
                    <div>
                        <div>
                            <b-icon icon="wind" font-scale="3"></b-icon>
                        </div>
                        {{ wind }} km/h <br>
                        Wind Speed
                    </div>
                </div>
            </b-card>
        </b-skeleton-wrapper>
    </div>
</template>

<script>
export default {
    name: 'Weather',
    props: { selectedGender: String },
    data() {
        return {
            api_key: "a1f36eee2f5b7bee1e2932180facf9ad",
            api_url: "https://api.openweathermap.org/data/2.5/weather?units=metric",
            input_city: "kerala",
            city: "",
            temperature: 0,
            wind: "",
            humidity: "",
            response: null,
            sky: [],
            sky_icon: "",
            loading: true
        }
    },
    methods: {
        async fetchWeather(city = null) {
            if (!this.input_city) {
                return;
            }
            this.loading = true;
            let self = this;
            if (city) {
                this.input_city = city;
            }
            try {
                this.response = await fetch(self.api_url + `&q=${self.input_city}&appid=${self.api_key}`);
                this.response = await this.response.json();
                if (this.response) {
                    this.loading = false;
                    console.log(this.response);
                    this.city = this.response.name;
                    this.temperature = this.response.main.temp;
                    this.wind = this.response.wind.speed;
                    this.humidity = this.response.main.humidity;
                    this.sky = this.response.weather[0].main;
                    this.sky_icon = this.renderSky(this.sky);
                    this.changeBg();
                }
            } catch (e) {
                alert(`${this.response.message}, try other city`);
                await this.fetchWeather("kerala");
            }

        },
        renderSky(sky) {
            switch (sky) {
                case "Rain":
                    return "cloud-rain";
                case "Haze":
                    return "cloud-haze";
                case "Clouds":
                    return "clouds";
                case "Clear":
                    return "sun";
                case "Snow":
                    return "cloud-snow";
                default:
                    return "cloud-sun";
            }
        },
        changeBg() {
            if (this.temperature < 20) {
                $('#weather-card').css("background", "blue");
            }
            else if (this.temperature > 25) {
                $('#weather-card').css("background", "red");
            }
        }
    },
    async mounted() {
        await this.fetchWeather();
    }
}
</script>

<style>
#weather-card {
    background: linear-gradient(139deg, rgba(2, 230, 199, 1) 0%, rgba(9, 152, 200, 1) 67%);
    color: white;
    padding: 10px;
}
</style>