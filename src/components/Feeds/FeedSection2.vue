<template>
  <div class="admin">

    <div class="section-1-alpha">
      <div class="section-1" v-for="child in paginatedData" :key="child.key" >

        <div class="section-1-text">
          <p class="text-1">
            <span class="text-1-link">Financial Advisory, </span>
            <span class="text-1-link">Financial Management, </span>
            <span class="text-1-link">Personal Financial Advisor for WellsFargo, </span>
          </p>
          <p class="text-2">{{child.text2}}</p>
          <p class="text-3">{{child.text3}}</p>
          <p class="text-4">
            <span class="slash">BY ADMIN / </span>
            <span class="slash">{{child.text4}} / </span>
            <span class="slash">1 MIN READ</span>
          </p>
        </div>
        <div class="section-1-image">
          <img :src="child.img" alt="" class="section-1-image" />
        </div>

      </div>

      <div class="pagination">
        <button @click="previousPage" :disabled="currentPage === 1" class="previous">Previous</button>
        <div class="page-indicator">
          Page {{ currentPage }} of {{ totalPages }}
        </div>
        <button @click="nextPage" :disabled="currentPage === totalPages" class="previous">Next</button>
      </div>
    </div>
    <br/>

  </div>
</template>


<script>
export default {
  name: "FeedSection2",
  data () {
    return {
      currentPage: 1,
      itemsPerPage: 5, // Change this as needed to display a number of items per page
      populate: [
        {
          text2 : "The Realities of Forex Trading: Patience, Discipline, and Humility",
          text3 : "Trading demands patience, discipline, and risk management, with a focus on minimizing losses over " +
              "seeking quick profits.",
          text4 : "JUNE 28, 2024",
          img : "https://tomsheldonhaleyfeeds.com/wp-content/uploads/2024/06/1883851332-8ab9ed31ae8a858c13bf43d9faf3d6b40af4f76b2312973a05eebadcf1a5177a-d_1920x1080-1024x576.jpeg",
        },
        {
          text2 : "Webinar: Financial Management",
          text3 : "A David Gibson student , Christian Papworth, ICAEW tutor, gives us an overview of the " +
              "Financial Management module.",
          text4 : "JUNE 26, 2024",
          img : "https://tomsheldonhaleyfeeds.com/wp-content/uploads/2024/06/1884735154-723a272c15d7e97b9d2469f82cce2061d5a1f2dd9334209e95a6918641647e5d-d_1920x1080-1024x576.jpeg",
        },
        {
          text2 : "Assert Yourself: Believe in Your Abilities and Stand Strong",
          text3 : "Don’t be afraid to assert yourself, have confidence in your abilities, and don’t let the bastards get you down",
          text4 : "JUNE 23, 2024",
          img : "https://tomsheldonhaleyfeeds.com/wp-content/uploads/2024/06/1878580167-62a459e9fd685b5ac06aa4d3a031a15b067bdbe63cbd067161cbf6e9d88a5f19-d_1920x1080-1024x576.jpeg",
        },
        {
          text2 : "The Power of High Expectations",
          text3 : "High expectations are the key to everything",
          text4 : "JUNE 23, 2024",
          img : "https://tomsheldonhaleyfeeds.com/wp-content/uploads/2024/06/1878555245-3b7bd894982e489fde36e428d21e470bd7612f3d2bb5a2ff8125dbf4aae7b6e8-d_1920x1080-1024x576.jpeg",
        },
        {
          text2 : "Start Doing: Actions Speak Louder Than Words",
          text3 : "The way to get started is to quit talking and begin doing.",
          text4 : "JUNE 23, 2024",
          img : "https://tomsheldonhaleyfeeds.com/wp-content/uploads/2024/06/1878575645-0ab3e38180d61870ff8b00df96205fd9875e1578b3475c132782f7c7b0ae6aed-d_1920x1080-1024x576.jpeg",
        },
        {
          text2 : "The Profit of Patience",
          text3 : "If most traders would learn to sit on their hands 50 percent of the time, they would make a lot more money.",
          text4 : "FEBRUARY 14, 2024",
          img : "https://tomsheldonhaleyfeeds.com/wp-content/uploads/2024/06/WhatsApp-Image-2024-06-20-at-11.33.15_a6072ecb-840x1024.jpg",
        },
        {
          text2 : "Forex Trading: A Lifestyle Beyond a Profession",
          text3 : "Forex trading is not just a profession, it’s a lifestyle. Balancing family time and trading requires discipline and understanding from both sides.",
          text4 : "JANUARY 22, 2024",
          img : "https://tomsheldonhaleyfeeds.com/wp-content/uploads/2024/06/WhatsApp-Image-2024-06-20-at-11.31.54_9ea12298-842x1024.jpg",
        },
        {
          text2 : "Surround Yourself with Your Aspirations",
          text3 : "The fastest way to change yourself is to hang out with people who are already the way you want to be.",
          text4 : "DECEMBER 19, 2024",
          img : "https://tomsheldonhaleyfeeds.com/wp-content/uploads/2024/06/WhatsApp-Image-2024-06-21-at-07.12.48_f5c3f202-819x1024.jpg",
        },
        {
          text2 : "The Greater Failure: Never Starting",
          text3 : "The only thing worse than starting something and failing… is not starting something.",
          text4 : "NOVEMBER 22, 2024",
          img : "https://tomsheldonhaleyfeeds.com/wp-content/uploads/2024/06/WhatsApp-Image-2024-06-21-at-07.11.23_c8132989-1024x768.jpg",
        },
        {
          text2 : "The Unstoppable Drive",
          text3 : "I’ve always had a passion within me, an engine that drives me forward. Even now, I still feel it pushing me to keep going.",
          text4 : "NOVEMBER 7, 2024",
          img : "https://tomsheldonhaleyfeeds.com/wp-content/uploads/2024/06/WhatsApp-Image-2024-06-21-at-07.10.32_89421470-1024x961.jpg",
        },
        {
          text2 : "Execution Over Ideation",
          text3 : "It’s not about ideas. It’s about making ideas happen.",
          text4 : "OCTOBER 15, 2023",
          img : "https://tomsheldonhaleyfeeds.com/wp-content/uploads/2023/10/WhatsApp-Image-2024-06-21-at-07.10.02_a5450155-1024x878.jpg",
        },
        {
          text2 : "The Wisdom of Caution",
          text3 : "There are old traders and there are bold traders, but there are very few old, bold traders.",
          text4 : "SEPTEMBER 9, 2023",
          img : "https://tomsheldonhaleyfeeds.com/wp-content/uploads/2024/06/WhatsApp-Image-2024-06-21-at-06.46.21_71e3bd9e-1024x855.jpg",
        },
        {
          text2 : "Buyers and Sellers Both Believe They’re Astute",
          text3 : "One of the funny things about the stock market is that every time one person buys, another sells, and both think they are astute.",
          text4 : "AUGUST 19, 2023",
          img : "https://tomsheldonhaleyfeeds.com/wp-content/uploads/2024/06/WhatsApp-Image-2024-06-21-at-06.45.13_24cd458d-826x1024.jpg",
        },
        {
          text2 : "The Life Cycle of Bull Markets",
          text3 : "Bull markets are born on pessimism, grow on skepticism, mature on optimism and die of euphoria.",
          text4 : "JULY 2, 2023",
          img : "https://tomsheldonhaleyfeeds.com/wp-content/uploads/2024/06/WhatsApp-Image-2024-06-21-at-06.43.44_89ad58d9-829x1024.jpg",
        },
        {
          text2 : "Instinct Over Analysis: The Key to Successful Trading",
          text3 : "Successful traders tend to be instinctive rather than overly analytical.",
          text4 : "JUNE 10, 2023",
          img : "https://tomsheldonhaleyfeeds.com/wp-content/uploads/2024/06/WhatsApp-Image-2024-06-20-at-11.38.29_822b8c71-841x1024.jpg",
        },
        {
          text2 : "Learn from Your Losses: The Path to Improved Results",
          text3 : "To improve your financial outcomes, analyze your past account losses, cease harmful practices, and you'll see positive results.",
          text4 : "JUNE 10, 2023",
          img : "https://tomsheldonhaleyfeeds.com/wp-content/uploads/2023/04/WhatsApp-Image-2024-06-20-at-11.36.13_55ce2554-1024x561.jpg",
        },
        {
          text2 : "Avoiding Losses",
          text3 : "Letting losses run is the most serious mistake made by most investors.",
          text4 : "MARCH 14, 2023",
          img : "https://tomsheldonhaleyfeeds.com/wp-content/uploads/2018/05/WhatsApp-Image-2024-06-19-at-19.23.59_c2da4bf2-847x1024.jpg",
        },
        {
          text2 : "Embrace Small Losses to Avoid Catastrophic Ones",
          text3 : "If you can’t take a small loss, sooner or later you will take the mother of all losses.",
          text4 : "FEBRUARY 14, 2023",
          img : "https://tomsheldonhaleyfeeds.com/wp-content/uploads/2024/06/WhatsApp-Image-2024-06-20-at-11.34.09_1063405b-859x1024.jpg",
        },
        {
          text2 : "Market Realities",
          text3 : "The market can stay irrational longer than you can stay solvent.",
          text4 : "JANUARY 30, 2023",
          img : "https://tomsheldonhaleyfeeds.com/wp-content/uploads/2018/05/WhatsApp-Image-2024-06-19-at-19.22.15_d7b559a0-1024x892.jpg",
        },
        {
          text2 : "Elements of good trading",
          text3 : "The elements of good trading are: (1) cutting losses (2) cutting losses, and (3) cutting losses. If you can follow these three rules, you may have a chance.",
          text4 : "SEPTEMBER 10, 2022",
          img : "https://tomsheldonhaleyfeeds.com/wp-content/uploads/2018/05/WhatsApp-Image-2024-06-19-at-19.00.09_656b7b06-833x1024.jpg",
        },
        {
          text2 : "The True Purpose: Start a Company to Change the World",
          text3 : "There are lots of bad reasons to start a company. But there’s only one good, legitimate reason, and I think you know what it is: It’s to change the world.",
          text4 : "SEPTEMBER 5, 2022",
          img : "https://tomsheldonhaleyfeeds.com/wp-content/uploads/2024/06/WhatsApp-Image-2024-06-21-at-07.21.29_9b105660-1024x1024.jpg",
        },
        {
          text2 : "Right Strategy to Outperform",
          text3 : "Many investors make the mistake of buying high and selling low while the exact opposite is the right strategy to outperform over the long term.",
          text4 : "AUGUST 31, 2022",
          img : "https://tomsheldonhaleyfeeds.com/wp-content/uploads/2018/05/WhatsApp-Image-2024-06-19-at-19.05.48_a346efd4-868x1024.jpg",
        },
        {
          text2 : "Emotional discipline Key Success",
          text3 : "The essence of trading success lies in emotional discipline, not intelligence, as most financial losses stem from failing to limit losses promptly.",
          text4 : "AUGUST 28, 2022",
          img : "https://tomsheldonhaleyfeeds.com/wp-content/uploads/2018/05/WhatsApp-Image-2024-06-19-at-18.59.25_10244727-1024x707.jpg",
        },
        {
          text2 : "Risk-Reward Ratio",
          text3 : "You never know what kind of setup market will present to you, your objective should be to find an opportunity where risk-reward ratio is best.",
          text4 : "AUGUST 21, 2022",
          img : "https://tomsheldonhaleyfeeds.com/wp-content/uploads/2018/05/WhatsApp-Image-2024-06-19-at-19.04.30_a30d7f15-824x1024.jpg",
        },
        {
          text2 : "Embrace the Unknown: Your Greatest Asset for Innovation",
          text3 : "Embracing your initial lack of knowledge can uniquely position you to innovate and stand out from others.",
          text4 : "AUGUST 19, 2022",
          img : "https://tomsheldonhaleyfeeds.com/wp-content/uploads/2024/06/WhatsApp-Image-2024-06-21-at-07.15.10_3dfa1088-1024x837.jpg",
        },
        {
          text2 : "Embrace the Unknown: Your Greatest Asset for Innovation",
          text3 : "Embracing your initial lack of knowledge can uniquely position you to innovate and stand out from others.",
          text4 : "AUGUST 19, 2022",
          img : "https://tomsheldonhaleyfeeds.com/wp-content/uploads/2024/06/WhatsApp-Image-2024-06-21-at-07.15.10_3dfa1088-1024x837.jpg",
        },
        {
          text2 : "Investment Psychology",
          text3 : "Investment success primarily hinges on psychology and risk control, rather than the specifics of buying and selling.",
          text4 : "AUGUST 17, 2022",
          img : "https://tomsheldonhaleyfeeds.com/wp-content/uploads/2018/05/WhatsApp-Image-2024-06-19-at-18.57.27_a5244cab-826x1024.jpg",
        },
        {
          text2 : "My Strategy is Dynamic and Ever-Evolving",
          text3 : "The speaker has been a successful, long-standing trader by continuously adapting and evolving their trading strategy, in contrast to many who have come and gone using rigid systems.",
          text4 : "AUGUST 16, 2022",
          img : "https://tomsheldonhaleyfeeds.com/wp-content/uploads/2018/05/WhatsApp-Image-2024-06-19-at-19.01.01_ed1dd945-827x1024.jpg",
        },
        {
          text2 : "Always Dreamed And Never Give Up",
          text3 : "\n" +
              "When hurt by the market, I immediately exit regardless of the market's position, recognizing that pain hinders objective decision-making.",
          text4 : "JULY 27, 2022",
          img : "https://tomsheldonhaleyfeeds.com/wp-content/uploads/2018/05/WhatsApp-Image-2024-06-19-at-18.55.30_5604322b-830x1024.jpg",
        },
        {
          text2 : "Cultivating Fearlessness",
          text3 : "Fearlessness is like a muscle. I know from my own life that the more I exercise it, the more natural it becomes to not let my fears run me.",
          text4 : "APRIL 16, 2022",
          img : "https://tomsheldonhaleyfeeds.com/wp-content/uploads/2024/06/WhatsApp-Image-2024-06-21-at-07.14.41_d68b2286-1024x905.jpg",
        },
        {
          text2 : "Cautious Risk-taking",
          text3 : "Don’t test the depth of the river with both your feet while taking the risk.",
          text4 : "DECEMBER 10, 2021",
          img : "https://tomsheldonhaleyfeeds.com/wp-content/uploads/2018/05/WhatsApp-Image-2024-06-19-at-19.21.16_7df86787-1024x754.jpg",
        },
      ],
    }
  },
  methods: {
    previousPage() {
      if (this.currentPage > 1) {
        this.currentPage--;
      }
    },
    nextPage() {
      if (this.currentPage < this.totalPages) {
        this.currentPage++;
      }
    }
  },
  computed: {
    paginatedData() {
      const start = (this.currentPage - 1) * this.itemsPerPage;
      const end = start + this.itemsPerPage;
      return this.populate.slice(start, end);
    },
    totalPages() {
      return Math.ceil(this.populate.length / this.itemsPerPage);
    },
  }
}
</script>

<style scoped>
.section-1-alpha{
  margin-top: 2.5%;
}

.section-1{
  display: flex;
  justify-content: center;
  margin-top: 2.5%;
  margin-bottom: 2.5%;
}

.section-1-text{
  padding: 1.5rem 2rem 1.5rem 3rem;
  width: 55%;
  border: 0.5px solid rgba(0, 0, 0, 0.2);
  border-right: none;
  transition: border 200ms ease;
  border-radius: 6px 0 0 6px;
  height: 310px;
  box-shadow: rgba(100, 100, 111, 0.2) 0px 7px 29px 0px;
}

.section-1-image{
  width: 350px;
  border-radius: 0 6px 6px 0;
  height: 310px;
  box-shadow: rgba(100, 100, 111, 0.2) 0px 7px 29px 0px;
}

.text-1{
  padding-top: 1rem;
  padding-bottom: 1rem;
  font-size: 0.875rem;
  text-transform: uppercase;
  font-weight: 700;
  line-height: 1.5;
  color: #51cbce;
}

.text-2{
  margin-bottom: 1.3rem;
  font-family: 'BR-Firma-Bold', sans-serif;
  font-weight: bold;
  letter-spacing: 0px;
  line-height: 1.2;
  color: #333333;
  font-size: 1.5rem;
}

.text-3{
  font-size: 1rem;
  letter-spacing: 0px;
}

.text-4{
  padding-top: 4%;
  font-size: 0.9rem;
}

.pagination{
  display: flex;
  align-content: center;
  align-items: center;
  justify-content: space-between;
  margin-left: 10.5%;
  margin-right: 10.5%;
}

.previous{
  /*display: flex;*/
  /*align-content: center;*/
  /*align-items: center;*/
  text-align: center;
  padding: 8px 20px;
  gap: 8px;
  font-size: 12px;
  width: 100px;
  height: 35px;
  background-color: #333;
  border: 1px solid #333;
  color: #FFFFFF;
  box-shadow: 0 1px 2px rgba(16, 24, 40, 0.05);
  border-radius: 4px;
}

.previous:hover{
  box-shadow: 0 0 5px rgba(16, 24, 40, 0.2);
}

.page-indicator{
  color: #333333;
  font-weight: 200;
  font-size: 13px;
}
</style>