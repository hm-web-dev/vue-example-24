<script>
import NewsItem from "../widgets/NewsItem.vue";
import NewsItemFooter from "../widgets/NewsItemFooter.vue";
import TimeStamp from "../widgets/TimeStamp.vue";
export default {
    data() {
        return {
            featuredArticle: {
                imageUrl: "https://images.performgroup.com/di/library/omnisport/79/d8/6c9b4b26f64a40ea89b7f69ccd088d40.jpg?t=-955230179&w=640",
                title: "Inter boss Simone Inzaghi reveals admiration for Diego Simeone ahead of clash",
                gmtTime: "2024-02-19T20:04:27.000Z",
                source: "FotMob",
                lead: "Simone Inzaghi and Diego Simeone, now boss of Atletico Madrid, helped Lazio win Serie A as players in 2000.",
                sourceIconUrl: "https://images.fotmob.com/image_resources/news/fotmob.png",
                pageURL: "https://www.fotmob.com/news/138lzxhk8mmsi1nflku3xemdte-inter-boss-simone-inzaghi-reveals-admiration-diego-simeone-ahead-clash"
            },
            articles: [
                {
                    imageUrl: "https://images.performgroup.com/di/library/omnisport/79/d8/6c9b4b26f64a40ea89b7f69ccd088d40.jpg?t=-955230179&w=640",
                    title: "Inter boss Simone Inzaghi reveals admiration for Diego Simeone ahead of clash",
                    gmtTime: "2024-02-19T20:04:27.000Z",
                    source: "FotMob",
                    lead: "Simone Inzaghi and Diego Simeone, now boss of Atletico Madrid, helped Lazio win Serie A as players in 2000.",
                    sourceIconUrl: "https://images.fotmob.com/image_resources/news/fotmob.png",
                    pageURL: "https://www.fotmob.com/news/138lzxhk8mmsi1nflku3xemdte-inter-boss-simone-inzaghi-reveals-admiration-diego-simeone-ahead-clash"
                },
                {
                    imageUrl: "https://images.performgroup.com/di/library/omnisport/79/d8/6c9b4b26f64a40ea89b7f69ccd088d40.jpg?t=-955230179&w=640",
                    title: "Inter boss Simone Inzaghi reveals admiration for Diego Simeone ahead of clash",
                    gmtTime: "2024-02-19T20:04:27.000Z",
                    source: "FotMob",
                    lead: "Simone Inzaghi and Diego Simeone, now boss of Atletico Madrid, helped Lazio win Serie A as players in 2000.",
                    sourceIconUrl: "https://images.fotmob.com/image_resources/news/fotmob.png",
                    pageURL: "https://www.fotmob.com/news/138lzxhk8mmsi1nflku3xemdte-inter-boss-simone-inzaghi-reveals-admiration-diego-simeone-ahead-clash"
                },
                {
                    imageUrl: "https://images.performgroup.com/di/library/omnisport/79/d8/6c9b4b26f64a40ea89b7f69ccd088d40.jpg?t=-955230179&w=640",
                    title: "Inter boss Simone Inzaghi reveals admiration for Diego Simeone ahead of clash",
                    gmtTime: "2024-02-19T20:04:27.000Z",
                    source: "FotMob",
                    lead: "Simone Inzaghi and Diego Simeone, now boss of Atletico Madrid, helped Lazio win Serie A as players in 2000.",
                    sourceIconUrl: "https://images.fotmob.com/image_resources/news/fotmob.png",
                    pageURL: "https://www.fotmob.com/news/138lzxhk8mmsi1nflku3xemdte-inter-boss-simone-inzaghi-reveals-admiration-diego-simeone-ahead-clash"
                },
                {
                    imageUrl: "https://images.performgroup.com/di/library/omnisport/79/d8/6c9b4b26f64a40ea89b7f69ccd088d40.jpg?t=-955230179&w=640",
                    title: "Inter boss Simone Inzaghi reveals admiration for Diego Simeone ahead of clash",
                    gmtTime: "2024-02-19T20:04:27.000Z",
                    source: "FotMob",
                    lead: "Simone Inzaghi and Diego Simeone, now boss of Atletico Madrid, helped Lazio win Serie A as players in 2000.",
                    sourceIconUrl: "https://images.fotmob.com/image_resources/news/fotmob.png",
                    pageURL: "https://www.fotmob.com/news/138lzxhk8mmsi1nflku3xemdte-inter-boss-simone-inzaghi-reveals-admiration-diego-simeone-ahead-clash"
                },
            ],
        }
    },
    components: {
        NewsItem,
        TimeStamp, 
        NewsItemFooter
    }
}
</script>

<template>
    <header class="WorldNewsHeader">
        <h1>World News</h1>
    </header>
    <div class="layout">
        <div class="featuredArticle">
            <div class="featuredImage">
                <img :src="featuredArticle.imageUrl" alt="featured article image" />
            </div>
            <div class="featuredArticleText">
                <h3>{{ featuredArticle.title }}</h3>
                <NewsItemFooter :article="featuredArticle" />
            </div>
        </div>
        <div class="articleGrid">
            <NewsItem v-for="article in articles" :newsItem="article" :key="article.title" />
        </div>
    </div>
</template>

<style scoped>
.WorldNewsHeader {
    display: flex;
    -webkit-box-align: center;
    align-items: center;
    margin: 0px 30px;
}
.featuredArticle {
    cursor: pointer;
    display: grid;
    grid-template-columns: 1fr 1fr;
    grid-auto-rows: 1fr;
    padding: 0px 30px;
    position: relative;
}
.featuredImage {
    width: 100%;
    height: 100%;
    max-width: 640px;
}
.featuredImage>img {
    /* needs to also specify child to resize */
    width: 100%;
    height: 100%;
    object-fit: cover;
}
.featuredArticleText {
    display: flex;
    -webkit-box-align: center;
    align-items: center;
    -webkit-box-pack: center;
    justify-content: center;
    background: var(--GlobalColorScheme-Background-background2);
    height: 100%;
    width: 100%;
    flex-direction: column;
    gap: 24px;
    padding: 20px;
}
.articleGrid {
    margin-top: 48px;
    padding: 0px 30px;
    display: grid;
    grid-template-columns: repeat(auto-fill, minmax(250px, 1fr));
    gap: 40px 24px;
    -webkit-box-align: start;
    align-items: start;
}
</style>