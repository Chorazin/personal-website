<template>
  <section>
    <parallax_comp v-bind:parallax_info='parallax_info_12' />
    <article>
      <div class='container'>
        <p>
        <h4 class='underline'>UI-UX</h4>
        </p>
        <p class='date'>
          Written by: Roger Atkins - Dev | Web | Design - 16/1/2024 <br /><br />
        </p>


        <p>
          I have spent a bit of time thinking about a succinct way to unpack my latest UI/UX work project and describe it
          without turning it into an essay. And unfortunately, I think there is no way to get around the fact this is
          going
          to be a long one. So grab yourself a coffee, or hot chocolate, stick a marshmallow in it, put your feet up and
          read on. As I approached this subject I thought a good place to start was with a
          description of the substrate componenets of the project and incorporating my journey through the project, my
          ideation, pitfalls, constraints and all other variables associated with the project.
        </p>
        <div class="spacer_vertical_100"></div>
        <h4>
          AN APPROACH TO DESIGN
        </h4>



        <p>
          Client: Estia Tuition<br />
          Project Scope: To take an older responsive design interface for a PWA to a mobile first approach. Altering the
          parent login portal and thus their interaction with the platform.<br />
          Duration: 10 Months<br />
          Description: A blended learning platform for all ages, covering the core components of the GCSE curriculum. This
          platform enables students to log in at any time and do a series of questions on specific topics they may be
          struggling with.
          The system designs a study plan based upon analysis of the students capabilities, with the focus on sets of
          questions based on the students weaknesses. These questions also feature detailed explanations and examples of
          how to solve the said problem.
          The questions are taken from a large set specific to the topic in question, and online tutors are available to
          answer any questions the student may have if they get stuck on a specific question.
        </p>



        <p>
          Some caveats to begin with:<br />
          As this is an update to an existing system already in use, a lot of specific user interaction data can be pulled
          from core GA4 as to flow within the product. Leveraging this existing data will give some great insights into
          persona research down the track as the demographic is already set and pain points well documented. And also give
          us a good understanding of how we can present relevant data that sweeps up 90%-95% of most use cases. Also to
          note is no other products on the market like this, it serves it's own niche as a blended learning platform.

        </p>
        <div class="spacer_vertical_100"></div>
        <h4 class="cardsec_title">BENEFITS OF A BLENDED LEARNING PLATFORM</h4>
        <!-- ROW 1 -->
        <div class="row">
          <div class="col s12 m6">
            <div class="card card_1">
              <div class="card-content black-text">
                <span class="card-title">PERSISTENT</span>
                <p>
                  The fact the platform is available 24/7 provided the child has internet access is a bonus, a quick login
                  and you can commence a topic based on the course designed to match your weak points whenever time
                  permits.
                </p>
              </div>
            </div>
          </div>
          <div class="col s12 m6">
            <div class="card card_1">
              <div class="card-content black-text">
                <span class="card-title">APPRIZED</span>
                <p>
                  The questions are kept up to date by the tutors who adjust curricula, add and remove questions
                  according and in attendance with changes to the core GCSE
                </p>
              </div>
            </div>
          </div>
        </div>
        <!-- ROW 2 -->
        <div class="row">
          <div class="col s12 m6">
            <div class="card card_1">
              <div class="card-content black-text">
                <span class="card-title">HUMAN TOUCH</span>
                <p>
                  Tutors are available for chat if you have a problem with a specific question and watching the video
                  descriptions and explanations of the answers is still confusing for the student. Unlike other learning
                  platforms that are more an automated experience, a blended learning platform brings a human element to
                  the table. Which is sometimes needed to better explain a given problem and how the solution is found.
                </p>
              </div>
            </div>
          </div>
          <div class="col s12 m6">
            <div class="card card_1">
              <div class="card-content black-text">
                <span class="card-title">ADVANTAGEOUS</span>
                <p>
                  Very economical to sign up for multiple children, because the course is targeted mostly at what a
                  student is struggling with based upon an entrance test you are getting real targeted learning and not
                  wading through the whole curriculum.
                </p>
              </div>
            </div>
          </div>
        </div>
        <!-- ROW 3 -->
        <div class="row">
          <div class="col s12 m6">
            <div class="card card_1">
              <div class="card-content black-text">
                <span class="card-title">MULTIMEDIA</span>
                <p>
                  Interactivity and motion design can bring learning to life via animation and video, this is a real
                  benefit for engaging students over classical learning with say textbooks.
                </p>
              </div>
            </div>
          </div>

        </div>
        <div class="spacer_vertical_100"></div>
        <h4 class="cardsec_title">CHALLENGES OF A BLENDED LEARNING PLATFORM</h4>
        <!-- ROW 4 -->
        <div class="row">
          <div class="col s12 m6">
            <div class="card card_1">
              <div class="card-content black-text">
                <span class="card-title">ROUTINE</span>
                <p>
                  No chronologically structured learning framework, some individuals like to have that rigid routine set
                  in place for them to follow. Whereas with online learning you can do the classes whenever you like, that
                  whenever could turn into a never. There needs to be a degree of agency and self motivation applied to
                  the study plan that is generated.
                </p>
              </div>
            </div>
          </div>
          <div class="col s12 m6">
            <div class="card card_1">
              <div class="card-content black-text">
                <span class="card-title">INFRASTRUCTURE</span>
                <p>
                  Some areas you travel to or visit may not have an internet connection. Lets say you are in the country
                  visiting family and the kids no longer have good, persistent internet access for example. Any sort of
                  disruption with the network means your children are missing classes.
                </p>
              </div>
            </div>
          </div>
        </div>
        <!-- ROW 5 -->
        <div class="row">
          <div class="col s12 m6">
            <div class="card card_1">
              <div class="card-content black-text">
                <span class="card-title">SOCIAL</span>
                <p>
                  Learning as a solo student rather than in a communal social environment. We humans are social creatures
                  and I am sure everyone has heard of the term ‘study partner’. But how does this manifest with children
                  doing classes solo from all over, in this specific case, the UK?
                </p>
              </div>
            </div>
          </div>

        </div>
      </div>
      <div class='spacer_vertical_100'>
        <middle_links />
      </div>
      <img class='responsive-img hide-on-small-only chevron' src='~/assets/spacer_chevron_v001.jpg'
        alt='gold and black chevron'>
      <div class="bgcol_gold black-text">
        <div class="container">

          <div>
            <h3>USER SURVEYS?</h3>
            Because the company wanted to move fast on this we leveraged existing data and well documented pain points
            from user feedback about the system. This was also backed up by behavioural analytics within hotjar to paint a
            clear
            picture as to what a common use case was. Let me be clear, this is not a substitute for well done surveys and
            interviews and I expressed this to the company, but with the timeframe in place and ticking they wanted to
            just
            leverage all the feedback and analytics we already had on hand by stakeholders on the platform.

            <h3>FEEDBACK</h3>
            I spent quite a few hours going over existing feedback for the system and we had some clear recurring issues.
            These I separated into two categories, quick fixes whereby functionality wise from an engineering perspective
            they were easy wins. And engineered fixes in which the underlying architecture of how the app works would need
            altering(more on this later). As I was both the UI/UX designer and front end developer I had a good grasp of
            time frames for these alterations from a developer perspective.

            <h3>OVERVIEW</h3>
            When the parent logs in they are presented with their 'dashboard'. This is a series of cards, each card
            representing a student/child and the usual navigation of the app at the top or on a hamburger in case of
            mobile. I decided to keep this format as I think this is an excellent way to move forward. By having each
            student/child represented as an individual card on the parents dashboard, but there were some key pain points
            that needed to be resolved.
            <div class="row top_margin_100">
              <div class="col s12 m6">
                <div class="card card_2 black">
                  <div class="card-content">
                    <span class="card-title">PRIMARY ACTION</span>
                    <p>
                      IN HERE
                    </p>
                  </div>
                </div>
              </div>
              <div class="col s12 m6">
                <div class="card card_2 black">
                  <div class="card-content">
                    <span class="card-title">ACTIVIY LOG</span>
                    <p>
                      Very economical to sign up for multiple children, because the course is targeted mostly at what a
                      student is struggling with based upon an entrance test you are getting real targeted learning and
                      not
                      wading through the whole curriculum.
                    </p>
                  </div>
                </div>
              </div>
            </div>

          </div>
        </div>
      </div>
      <parallax_comp v-bind:parallax_info='parallax_info_13' />
      <div class='container'>
        <p>
        <h4 class='underline'>Future projects?</h4>
        MORE UI/UX STUFF IN HERE, PICS!
        </p>
      </div>
    </article>
    <br />
    <hr class='gradient' />
    <br />
  </section>
</template>
  
<script>
import parallax_comp from '../components/parallax_comp.vue'
import middle_links from '../components/middle_links.vue'

export default {

  transition: {
    name: 'fade',
    mode: 'out-in'
  },

  components: {
    parallax_comp,
    middle_links
  },

  head() {
    return {
      title: 'UI/UX',
      meta: [
        {
          hid: 'description',
          name: 'description',
          content: 'A UI/UX case study'
        }
      ]
    }
  },

  data() {
    return {
      parallax_info_12: {
        url: '/javascript_parallax_11_v001.jpg',
        heading: 'UI/UX',
        quote: '- Empathy, Collaboration, Prototyping, Design Thinking'
      },
      parallax_info_13: {
        url: '/javascript_parallax_12_v001.jpg',
        heading: '"Morphology? Longevity?"',
        quote: '- Roy Batty - Nexus 6'
      }
    }
  },

  mounted() {
    //setup materialize parallex on component mount
    const elems = document.querySelectorAll('.parallax');
    const instances = M.Parallax.init(elems);

  }
}
</script>
  
<style scoped>
.card_1 {
  background-color: var(--main_gold_color);
  min-height: 15rem;
  border-radius: 10px;
}

.card_2 {
  min-height: 15rem;
  border-radius: 10px;
  color: var(--main_gold_color);
}

.card-title {
  font-weight: 600;
}

.cardsec_title {
  padding-left: 10px;
}

.bgcol_gold {
  background-color: var(--main_gold_color);
}

.chevron {

  margin-bottom: -35px !important;
}
</style>
