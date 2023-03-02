<template>
  <div class="dashboard-container">
    <header data-role="Header" class="dashboard-header">
      <div data-thq="thq-dropdown" class="dashboard-thq-dropdown list-item">
        <div data-thq="thq-dropdown-toggle" class="dashboard-dropdown-toggle">
          <span class="dashboard-text">Menu</span>
          <div
            data-thq="thq-dropdown-arrow"
            class="dashboard-dropdown-arrow"
          ></div>
        </div>
        <ul data-thq="thq-dropdown-list" class="dashboard-dropdown-list">
          <li data-thq="thq-dropdown" class="dashboard-dropdown list-item">
            <router-link to="/dashboard">
              <div
                data-thq="thq-dropdown-toggle"
                class="dashboard-dropdown-toggle1"
              >
                <span class="dashboard-text01">Home</span>
              </div>
            </router-link>
          </li>
          <li data-thq="thq-dropdown" class="dashboard-dropdown1 list-item">
            <router-link to="/map">
              <div
                data-thq="thq-dropdown-toggle"
                class="dashboard-dropdown-toggle2"
              >
                <span class="dashboard-text02">Map</span>
              </div>
            </router-link>
          </li>
        </ul>
      </div>
      <div class="dashboard-container1">
        <router-link to="/dashboard" class="dashboard-home">Home</router-link>
        <router-link to="/map" class="dashboard-map">Map</router-link>
        <span class="dashboard-about-us">About US</span>
      </div>
      <img
        alt="logo"
        src="/playground_assets/1213213213-200w.png"
        class="dashboard-image"
      />
    </header>
    <div class="dashboard-intro">
      <div class="dashboard-container2">
        <h1 class="dashboard-text03">healthsocal.ai</h1>
        <span class="dashboard-text04">
          <span>
            Southern California&apos;s mental health epidemic needs to be
            addressed to:
            <span v-html="rawtkja"></span>
          </span>
          <br />
          <span>
            - provide care to the ever-growing population and increasing number of
            mental illnesses
            <span v-html="rawcjua"></span>
          </span>
          <br />
          <span>
            - give required support to the mental health industry in providing
            those who can make health decisions with health data and solutions.
            <span v-html="rawn4qb"></span>
          </span>
          <span><span v-html="rawm76f"></span></span>
          <span><span v-html="raw6j21"></span></span>
        </span>
        <div class="dashboard-btn-group">
          <router-link to="/map" class="dashboard-navlink2 button">
            Get Started
          </router-link>
          <button class="dashboard-button button">Learn More</button>
        </div>
      </div>
      <img
        alt="image"
        src="/playground_assets/111-1500h.jpeg"
        class="dashboard-image1"
      />
    </div>
    <div class="dashboard-statistic"></div>
    <div class="dashboard-solutions">
      <div class="dashboard-container2">
        <h1 class="dashboard-text13">Solutions</h1>
        <div class="dashboard-container3">
          <div class="dashboard-container-interactivity">
            <span class="dashboard-text14">Interactivity</span>
            <span class="dashboard-text15">
              <span class="dashboard-text16">
                Interactive maps and user-friendly interfaces can be used to help users understand mental health.
              </span>
              <br />
            </span>
          </div>
          <div class="dashboard-container-data">
            <span class="dashboard-text18">Data</span>
            <span class="dashboard-text19">
              <span class="dashboard-text20">
                Provide data to help users analyze the main causes of psychological problems in different regions.
              </span>
              <br class="dashboard-text21" />
              <br />
            </span>
          </div>
        </div>
      </div>
    </div>
    <footer class="dashboard-footer">
      <img alt="logo" class=".dashboard-image2" src="../assets/socalenhance.png"/>
      <span class="dashboard-text23">© 2023 Octane OC, All Rights Reserved.</span>
      <div class="dashboard-icon-group">
        <a
          href="https://twitter.com/octaneoc?lang=en"
          target="_blank"
          rel="noreferrer noopener"
          class="dashboard-link"
        >
          <svg viewBox="0 0 950.8571428571428 1024" class="dashboard-icon">
            <path
              d="M925.714 233.143c-25.143 36.571-56.571 69.143-92.571 95.429 0.571 8 0.571 16 0.571 24 0 244-185.714 525.143-525.143 525.143-104.571 0-201.714-30.286-283.429-82.857 14.857 1.714 29.143 2.286 44.571 2.286 86.286 0 165.714-29.143 229.143-78.857-81.143-1.714-149.143-54.857-172.571-128 11.429 1.714 22.857 2.857 34.857 2.857 16.571 0 33.143-2.286 48.571-6.286-84.571-17.143-148-91.429-148-181.143v-2.286c24.571 13.714 53.143 22.286 83.429 23.429-49.714-33.143-82.286-89.714-82.286-153.714 0-34.286 9.143-65.714 25.143-93.143 90.857 112 227.429 185.143 380.571 193.143-2.857-13.714-4.571-28-4.571-42.286 0-101.714 82.286-184.571 184.571-184.571 53.143 0 101.143 22.286 134.857 58.286 41.714-8 81.714-23.429 117.143-44.571-13.714 42.857-42.857 78.857-81.143 101.714 37.143-4 73.143-14.286 106.286-28.571z"
            ></path>
          </svg>
        </a>
        <a
          href="https://www.instagram.com/octaneoc/?hl=en"
          target="_blank"
          rel="noreferrer noopener"
          class="dashboard-link1"
        >
          <svg viewBox="0 0 877.7142857142857 1024" class="dashboard-icon2">
            <path
              d="M585.143 512c0-80.571-65.714-146.286-146.286-146.286s-146.286 65.714-146.286 146.286 65.714 146.286 146.286 146.286 146.286-65.714 146.286-146.286zM664 512c0 124.571-100.571 225.143-225.143 225.143s-225.143-100.571-225.143-225.143 100.571-225.143 225.143-225.143 225.143 100.571 225.143 225.143zM725.714 277.714c0 29.143-23.429 52.571-52.571 52.571s-52.571-23.429-52.571-52.571 23.429-52.571 52.571-52.571 52.571 23.429 52.571 52.571zM438.857 152c-64 0-201.143-5.143-258.857 17.714-20 8-34.857 17.714-50.286 33.143s-25.143 30.286-33.143 50.286c-22.857 57.714-17.714 194.857-17.714 258.857s-5.143 201.143 17.714 258.857c8 20 17.714 34.857 33.143 50.286s30.286 25.143 50.286 33.143c57.714 22.857 194.857 17.714 258.857 17.714s201.143 5.143 258.857-17.714c20-8 34.857-17.714 50.286-33.143s25.143-30.286 33.143-50.286c22.857-57.714 17.714-194.857 17.714-258.857s5.143-201.143-17.714-258.857c-8-20-17.714-34.857-33.143-50.286s-30.286-25.143-50.286-33.143c-57.714-22.857-194.857-17.714-258.857-17.714zM877.714 512c0 60.571 0.571 120.571-2.857 181.143-3.429 70.286-19.429 132.571-70.857 184s-113.714 67.429-184 70.857c-60.571 3.429-120.571 2.857-181.143 2.857s-120.571 0.571-181.143-2.857c-70.286-3.429-132.571-19.429-184-70.857s-67.429-113.714-70.857-184c-3.429-60.571-2.857-120.571-2.857-181.143s-0.571-120.571 2.857-181.143c3.429-70.286 19.429-132.571 70.857-184s113.714-67.429 184-70.857c60.571-3.429 120.571-2.857 181.143-2.857s120.571-0.571 181.143 2.857c70.286 3.429 132.571 19.429 184 70.857s67.429 113.714 70.857 184c3.429 60.571 2.857 120.571 2.857 181.143z"
            ></path>
          </svg>
        </a>
        <svg viewBox="0 0 602.2582857142856 1024" class="dashboard-icon4">
          <path
            d="M548 6.857v150.857h-89.714c-70.286 0-83.429 33.714-83.429 82.286v108h167.429l-22.286 169.143h-145.143v433.714h-174.857v-433.714h-145.714v-169.143h145.714v-124.571c0-144.571 88.571-223.429 217.714-223.429 61.714 0 114.857 4.571 130.286 6.857z"
          ></path>
        </svg>
      </div>
    </footer>
  </div>
</template>

<script>
export default {
  name: 'Dashboard',
  props: {},
  data() {
    return {
      rawtkja: ' ',
      rawcjua: ' ',
      rawn4qb: ' ',
      rawm76f: ' ',
      raw6j21: ' ',
    }
  },
}
</script>

<style scoped>
.dashboard-container {
  width: 100%;
  display: flex;
  overflow: auto;
  min-height: 80vh;
  align-items: center;
  flex-direction: column;
}
.dashboard-header {
  width: 100%;
  display: flex;
  max-width: 100%;
  align-items: center;
  padding-top: var(--dl-space-space-halfunit);
  padding-left: var(--dl-space-space-threeunits);
  padding-right: var(--dl-space-space-threeunits);
  padding-bottom: 3px;
  justify-content: space-between;
  background-color: rgba(255, 192, 3, 0.8);
}
.dashboard-thq-dropdown {
  cursor: pointer;
  display: inline-block;
  position: relative;
  border-radius: var(--dl-radius-radius-radius2);
}
.dashboard-dropdown-toggle {
  fill: #595959;
  color: #595959;
  width: 100%;
  display: inline-flex;
  align-items: center;
  padding-top: var(--dl-space-space-halfunit);
  padding-left: var(--dl-space-space-unit);
  border-radius: var(--dl-radius-radius-radius2);
  padding-right: var(--dl-space-space-unit);
  padding-bottom: var(--dl-space-space-halfunit);
}
.dashboard-text {
  color: rgba(255, 125, 0, 0.8);
  font-size: 20px;
  font-style: normal;
  text-align: center;
  font-weight: 700;
  margin-right: 4px;
  vertical-align: middle;
}
.dashboard-dropdown-arrow {
  transition: 0.3s;
}
.dashboard-dropdown-list {
  left: 0%;
  width: max-content;
  display: none;
  z-index: 100;
  position: absolute;
  min-width: 100%;
  transition: 0.3s;
  align-items: stretch;
  border-color: #D9D9D9;
  border-width: 1px;
  border-radius: var(--dl-radius-radius-radius4);
  flex-direction: column;
  list-style-type: none;
  background-color: var(--dl-color-gray-white);
  list-style-position: inside;
}
.dashboard-dropdown {
  cursor: pointer;
  display: inline-block;
  position: relative;
  border-radius: var(--dl-radius-radius-radius2);
}
.dashboard-dropdown-toggle1 {
  fill: #595959;
  color: rgba(255, 125, 0, 0.8);
  width: 100%;
  display: inline-flex;
  transition: 0.3s;
  align-items: center;
  padding-top: var(--dl-space-space-halfunit);
  padding-left: var(--dl-space-space-unit);
  border-radius: var(--dl-radius-radius-radius4);
  padding-right: var(--dl-space-space-unit);
  padding-bottom: var(--dl-space-space-halfunit);
  text-decoration: none;
}
.dashboard-dropdown-toggle1:hover {
  fill: #fff;
  color: #fff;
  background-color: #595959;
}
.dashboard-text01 {
  width: 100%;
  cursor: pointer;
  display: flex;
  font-size: 14px;
  font-style: normal;
  font-weight: 500;
}
.dashboard-dropdown1 {
  cursor: pointer;
  display: inline-block;
  position: relative;
  border-radius: var(--dl-radius-radius-radius2);
}
.dashboard-dropdown-toggle2 {
  fill: #595959;
  color: rgba(255, 125, 0, 0.8);
  width: 100%;
  display: inline-flex;
  transition: 0.3s;
  align-items: center;
  padding-top: var(--dl-space-space-halfunit);
  padding-left: var(--dl-space-space-unit);
  border-radius: var(--dl-radius-radius-radius4);
  padding-right: var(--dl-space-space-unit);
  padding-bottom: var(--dl-space-space-halfunit);
  text-decoration: none;
}
.dashboard-dropdown-toggle2:hover {
  fill: #fff;
  color: #fff;
  background-color: #595959;
}
.dashboard-text02 {
  width: 100%;
  cursor: pointer;
  display: flex;
  font-size: 14px;
  font-style: normal;
  font-weight: 500;
}
.dashboard-container1 {
  flex: 0 0 auto;
  width: 50%;
  height: auto;
  display: flex;
  align-self: center;
  align-items: center;
  justify-content: space-between;
}
.dashboard-home {
  color: rgba(255, 125, 0, 0.8);
  font-weight: 700;
  text-decoration: none;
}
.dashboard-map {
  color: rgba(255, 125, 0, 0.8);
  font-weight: 700;
  text-decoration: none;
}
.dashboard-about-us {
  color: rgba(255, 125, 0, 0.8);
  font-weight: 700;
}
.dashboard-image {
  width: var(--dl-size-size-small);
  height: var(--dl-size-size-small);
}
.dashboard-intro {
  width: 100%;
  display: flex;
  padding: var(--dl-space-space-threeunits);
  max-width: var(--dl-size-size-maxwidth);
  min-height: 80vh;
  align-items: center;
  flex-direction: row;
  justify-content: space-between;
}
.dashboard-container2 {
  display: flex;
  margin-right: var(--dl-space-space-threeunits);
  padding-right: var(--dl-space-space-threeunits);
  flex-direction: column;
}
.dashboard-text03 {
  color: rgba(255, 125, 0, 0.8);
  font-size: 3rem;
  max-width: 450px;
  font-family: Poppins;
}
.dashboard-text04 {
  margin-top: var(--dl-space-space-twounits);
  margin-bottom: var(--dl-space-space-twounits);
}
.dashboard-btn-group {
  display: flex;
  align-items: center;
  flex-direction: row;
}
.dashboard-navlink2 {
  color: var(--dl-color-gray-black);
  transition: 0.3s;
  font-weight: 700;
  padding-top: var(--dl-space-space-unit);
  padding-left: var(--dl-space-space-twounits);
  padding-right: var(--dl-space-space-twounits);
  padding-bottom: var(--dl-space-space-unit);
  text-decoration: none;
  background-color: rgba(255, 192, 3, 0.8);
}
.dashboard-navlink2:hover {
  color: var(--dl-color-gray-white);
  background-color: var(--dl-color-gray-black);
}
.dashboard-button {
  transition: 0.3s;
  font-weight: 700;
  margin-left: var(--dl-space-space-unit);
  padding-top: var(--dl-space-space-unit);
  border-color: transparent;
  padding-left: var(--dl-space-space-twounits);
  padding-right: var(--dl-space-space-twounits);
  padding-bottom: var(--dl-space-space-unit);
}
.dashboard-button:hover {
  border-color: var(--dl-color-gray-black);
}
.dashboard-image1 {
  width: 400px;
  object-fit: cover;
}
.dashboard-cover1in5 {
  width: 100%;
  display: flex;
  padding: 0px;
  max-width: var(--dl-size-size-maxwidth);
  align-self: center;
  min-height: 80vh;
  align-items: center;
  flex-direction: row;
  justify-content: center;
}
.dashboard-image2 {
  width: 100%;
  height: auto;
  object-fit: cover;
}
.dashboard-solutions {
  width: 100%;
  display: flex;
  padding: 0px;
  max-width: var(--dl-size-size-maxwidth);
  min-height: 80vh;
  align-items: center;
  flex-direction: row;
  justify-content: center;
  background-image: url("../assets/solutions.png");
}
.dashboard-container3 {
  display: flex;
  align-self: center;
  margin-left: var(--dl-space-space-threeunits);
  margin-right: var(--dl-space-space-threeunits);
  padding-left: var(--dl-space-space-threeunits);
  padding-right: var(--dl-space-space-threeunits);
  flex-direction: column;
}
.dashboard-text12 {
  color: rgba(0, 0, 0, 0.8);
  font-size: 3rem;
  max-width: 450px;
  align-self: flex-start;
  font-family: Poppins;
}
.dashboard-container4 {
  gap: var(--dl-space-space-threeunits);
  display: flex;
  align-self: flex-start;
  flex-direction: row;
}
.dashboard-container-interactivity {
  display: flex;
  padding: var(--dl-space-space-unit);
  align-items: center;
  border-radius: var(--dl-radius-radius-radius8);
  flex-direction: column;
  justify-content: center;
  background-color: rgba(255,223,124,255);
}
.dashboard-image3 {
  width: 100px;
  object-fit: cover;
}
.dashboard-text13 {
  color: rgba(0, 0, 0, 0.8);
  font-size: 36px;
  align-self: center;
  margin-top: var(--dl-space-space-twounits);
  font-family: Poppins;
  font-weight: 700;
  margin-bottom: var(--dl-space-space-twounits);
}
.dashboard-text14 {
  color: rgba(255, 125, 0, 0.8);
  font-size: 24px;
  margin-top: var(--dl-space-space-twounits);
  font-family: Poppins;
  font-weight: 700;
  margin-bottom: var(--dl-space-space-twounits);
}
.dashboard-text15 {
  color: rgba(14, 13, 13, 0.8);
}
.dashboard-container-data {
  display: flex;
  padding: var(--dl-space-space-unit);
  align-self: center;
  align-items: center;
  padding-left: var(--dl-space-space-unit);
  border-radius: var(--dl-radius-radius-radius8);
  padding-right: var(--dl-space-space-unit);
  flex-direction: column;
  justify-content: center;
  background-color: rgba(255,223,124,255);
}
.dashboard-image4 {
  width: 100px;
  object-fit: cover;
}
.dashboard-text17 {
  color: rgba(0, 0, 0, 0.8);
  font-size: 36px;
  margin-top: var(--dl-space-space-twounits);
  font-family: Poppins;
  font-weight: 700;
  margin-bottom: var(--dl-space-space-twounits);
}
.dashboard-text18 {
  color: rgba(255, 125, 0, 0.8);
  font-size: 24px;
  margin-top: var(--dl-space-space-twounits);
  font-family: Poppins;
  font-weight: 700;
  margin-bottom: var(--dl-space-space-twounits);
}
.dashboard-text19 {
  color: rgba(0, 0, 0, 0.8);
}
.dashboard-text20 {
  color: rgba(0, 0, 0, 0.8);
}
.dashboard-product {
  width: 100%;
  display: flex;
  padding: 0px;
  max-width: var(--dl-size-size-maxwidth);
  min-height: 80vh;
  align-items: center;
  flex-direction: row;
  justify-content: center;
  background-color: rgba(255,223,124,255);
}
.dashboard-container5 {
  display: flex;
  align-self: center;
  align-items: center;
  margin-left: var(--dl-space-space-threeunits);
  margin-right: var(--dl-space-space-threeunits);
  padding-left: var(--dl-space-space-threeunits);
  padding-right: var(--dl-space-space-threeunits);
  flex-direction: column;
  justify-content: center;
}
.dashboard-text22 {
  color: rgba(0, 0, 0, 0.8);
  font-size: 3rem;
  max-width: 450px;
  align-self: flex-start;
  font-family: Poppins;
}
.dashboard-container6 {
  gap: var(--dl-space-space-threeunits);
  display: flex;
  align-self: center;
  align-items: center;
  flex-direction: row;
  justify-content: center;
}
.dashboard-container1 {
  display: flex;
  padding: var(--dl-space-space-unit);
  align-self: center;
  align-items: center;
  border-radius: var(--dl-radius-radius-radius8);
  flex-direction: column;
  justify-content: center;
  background-color: rgba(255, 125, 0, 0.8);
}
.dashboard-image5 {
  width: 100px;
  object-fit: cover;
}
.dashboard-text25 {
  color: rgba(0, 0, 0, 0.8);
  font-size: 36px;
  align-self: center;
  margin-top: var(--dl-space-space-twounits);
  font-family: Poppins;
  font-weight: 700;
  margin-bottom: var(--dl-space-space-twounits);
}
.dashboard-text26 {
  color: rgba(255, 125, 0, 0.8);
  font-size: 24px;
  margin-top: var(--dl-space-space-twounits);
  font-family: Poppins;
  font-weight: 700;
  margin-bottom: var(--dl-space-space-twounits);
}
.dashboard-text27 {
  color: rgba(0, 0, 0, 0.8);
}
.dashboard-container2 {
  display: flex;
  padding: var(--dl-space-space-unit);
  align-self: center;
  align-items: center;
  border-radius: var(--dl-radius-radius-radius8);
  flex-direction: column;
  justify-content: center;
  background-color: rgba(255, 125, 0, 0.8);
}
.dashboard-image6 {
  width: 100px;
  object-fit: cover;
}
.dashboard-text29 {
  color: rgba(0, 0, 0, 0.8);
  font-size: 36px;
  margin-top: var(--dl-space-space-twounits);
  font-family: Poppins;
  font-weight: 700;
  margin-bottom: var(--dl-space-space-twounits);
}
.dashboard-text30 {
  color: rgba(0, 0, 0, 0.8);
  font-size: 24px;
  margin-top: var(--dl-space-space-twounits);
  font-family: Poppins;
  font-weight: 700;
  margin-bottom: var(--dl-space-space-twounits);
}
.dashboard-footer {
  width: 100%;
  height: 77px;
  display: flex;
  max-width: 100%;
  align-items: center;
  padding-top: var(--dl-space-space-twounits);
  padding-left: var(--dl-space-space-threeunits);
  padding-right: var(--dl-space-space-threeunits);
  flex-direction: row;
  padding-bottom: var(--dl-space-space-twounits);
  justify-content: space-between;
  background-color: rgba(255, 192, 3, 0.8);
}
.dashboard-image2 {
  width: var(--dl-size-size-small);
  height: var(--dl-size-size-small);
}
.dashboard-icon-group {
  display: flex;
  align-items: center;
  flex-direction: row;
  justify-content: space-between;
}
.dashboard-link {
  display: contents;
}
.dashboard-icon {
  width: var(--dl-size-size-xsmall);
  height: var(--dl-size-size-xsmall);
  margin-right: var(--dl-space-space-twounits);
  text-decoration: none;
}
.dashboard-link1 {
  display: contents;
}
.dashboard-icon2 {
  width: var(--dl-size-size-xsmall);
  height: var(--dl-size-size-xsmall);
  margin-right: var(--dl-space-space-twounits);
  text-decoration: none;
}
.dashboard-icon4 {
  width: var(--dl-size-size-xsmall);
  height: var(--dl-size-size-xsmall);
}
@media(max-width: 991px) {
  .dashboard-intro {
    flex-direction: column;
  }
  .dashboard-container2 {
    align-items: center;
    margin-right: 0px;
    margin-bottom: var(--dl-space-space-twounits);
    padding-right: 0px;
  }
  .dashboard-text03 {
    text-align: center;
  }
  .dashboard-text04 {
    text-align: center;
    padding-left: var(--dl-space-space-threeunits);
    padding-right: var(--dl-space-space-threeunits);
  }
  .dashboard-cover1in5 {
    flex-direction: column;
  }
  .dashboard-solutions {
    flex-direction: column;
  }
  .dashboard-container3 {
    align-items: center;
    margin-right: 0px;
    margin-bottom: var(--dl-space-space-twounits);
    padding-right: 0px;
  }
  .dashboard-text12 {
    text-align: center;
  }
  .dashboard-text13 {
    text-align: center;
    padding-left: var(--dl-space-space-threeunits);
    padding-right: var(--dl-space-space-threeunits);
  }
  .dashboard-text14 {
    text-align: center;
    padding-left: var(--dl-space-space-threeunits);
    padding-right: var(--dl-space-space-threeunits);
  }
  .dashboard-text17 {
    text-align: center;
    padding-left: var(--dl-space-space-threeunits);
    padding-right: var(--dl-space-space-threeunits);
  }
  .dashboard-text18 {
    text-align: center;
    padding-left: var(--dl-space-space-threeunits);
    padding-right: var(--dl-space-space-threeunits);
  }
  .dashboard-product {
    flex-direction: column;
  }
  .dashboard-container5 {
    align-items: center;
    margin-right: 0px;
    margin-bottom: var(--dl-space-space-twounits);
    padding-right: 0px;
  }
  .dashboard-text22 {
    text-align: center;
  }
  .dashboard-text23 {
    text-align: center;
  }
  .dashboard-text25 {
    text-align: center;
    padding-left: var(--dl-space-space-threeunits);
    padding-right: var(--dl-space-space-threeunits);
  }
  .dashboard-text26 {
    text-align: center;
    padding-left: var(--dl-space-space-threeunits);
    padding-right: var(--dl-space-space-threeunits);
  }
  .dashboard-text29 {
    text-align: center;
    padding-left: var(--dl-space-space-threeunits);
    padding-right: var(--dl-space-space-threeunits);
  }
  .dashboard-text30 {
    text-align: center;
    padding-left: var(--dl-space-space-threeunits);
    padding-right: var(--dl-space-space-threeunits);
  }
}
@media(max-width: 767px) {
  .dashboard-header {
    padding-left: var(--dl-space-space-twounits);
    padding-right: var(--dl-space-space-twounits);
  }
  .dashboard-intro {
    padding-left: var(--dl-space-space-twounits);
    padding-right: var(--dl-space-space-twounits);
  }
  .dashboard-text04 {
    padding-left: var(--dl-space-space-unit);
    padding-right: var(--dl-space-space-unit);
  }
  .dashboard-image1 {
    width: 80%;
  }
  .dashboard-cover1in5 {
    padding-left: var(--dl-space-space-twounits);
    padding-right: var(--dl-space-space-twounits);
  }
  .dashboard-image2 {
    width: 80%;
  }
  .dashboard-solutions {
    padding-left: var(--dl-space-space-twounits);
    padding-right: var(--dl-space-space-twounits);
  }
  .dashboard-text13 {
    padding-left: var(--dl-space-space-unit);
    padding-right: var(--dl-space-space-unit);
  }
  .dashboard-text14 {
    padding-left: var(--dl-space-space-unit);
    padding-right: var(--dl-space-space-unit);
  }
  .dashboard-text17 {
    padding-left: var(--dl-space-space-unit);
    padding-right: var(--dl-space-space-unit);
  }
  .dashboard-text18 {
    padding-left: var(--dl-space-space-unit);
    padding-right: var(--dl-space-space-unit);
  }
  .dashboard-product {
    padding-left: var(--dl-space-space-twounits);
    padding-right: var(--dl-space-space-twounits);
  }
  .dashboard-text25 {
    padding-left: var(--dl-space-space-unit);
    padding-right: var(--dl-space-space-unit);
  }
  .dashboard-text26 {
    padding-left: var(--dl-space-space-unit);
    padding-right: var(--dl-space-space-unit);
  }
  .dashboard-text29 {
    padding-left: var(--dl-space-space-unit);
    padding-right: var(--dl-space-space-unit);
  }
  .dashboard-text30 {
    padding-left: var(--dl-space-space-unit);
    padding-right: var(--dl-space-space-unit);
  }
  .dashboard-footer {
    padding-left: var(--dl-space-space-twounits);
    padding-right: var(--dl-space-space-twounits);
  }
  .dashboard-text33 {
    text-align: center;
    margin-left: var(--dl-space-space-unit);
    margin-right: var(--dl-space-space-unit);
  }
}
@media(max-width: 479px) {
  .dashboard-header {
    padding: var(--dl-space-space-unit);
  }
  .dashboard-intro {
    padding-top: var(--dl-space-space-twounits);
    padding-left: var(--dl-space-space-unit);
    padding-right: var(--dl-space-space-unit);
    padding-bottom: var(--dl-space-space-twounits);
  }
  .dashboard-container2 {
    margin-bottom: var(--dl-space-space-unit);
  }
  .dashboard-btn-group {
    flex-direction: column;
  }
  .dashboard-button {
    margin-top: var(--dl-space-space-unit);
    margin-left: 0px;
  }
  .dashboard-cover1in5 {
    padding-top: var(--dl-space-space-twounits);
    padding-left: var(--dl-space-space-unit);
    padding-right: var(--dl-space-space-unit);
    padding-bottom: var(--dl-space-space-twounits);
  }
  .dashboard-solutions {
    padding-top: var(--dl-space-space-twounits);
    padding-left: var(--dl-space-space-unit);
    padding-right: var(--dl-space-space-unit);
    padding-bottom: var(--dl-space-space-twounits);
  }
  .dashboard-container3 {
    margin-right: var(--dl-space-space-threeunits);
    margin-bottom: var(--dl-space-space-unit);
    padding-right: var(--dl-space-space-threeunits);
  }
  .dashboard-product {
    padding-top: var(--dl-space-space-twounits);
    padding-left: var(--dl-space-space-unit);
    padding-right: var(--dl-space-space-unit);
    padding-bottom: var(--dl-space-space-twounits);
  }
  .dashboard-container5 {
    margin-right: var(--dl-space-space-threeunits);
    margin-bottom: var(--dl-space-space-unit);
    padding-right: var(--dl-space-space-threeunits);
  }
  .dashboard-footer {
    height: auto;
    padding: var(--dl-space-space-unit);
    flex-direction: column;
  }
  .dashboard-text33 {
    margin-left: 0px;
    margin-right: 0px;
    margin-bottom: var(--dl-space-space-unit);
  }
}
</style>   