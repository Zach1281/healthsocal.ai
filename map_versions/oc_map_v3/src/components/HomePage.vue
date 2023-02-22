<template>
    <div class="dashboard-container">
      <header data-role="Header" class="dashboard-header">
        <div data-thq="thq-dropdown" class="dashboard-thq-dropdown list-item">
          <div data-thq="thq-dropdown-toggle" class="dashboard-dropdown-toggle">
            <span class="dashboard-text">Menu</span>
          </div>
          <ul data-thq="thq-dropdown-list" class="dashboard-dropdown-list">
            <li data-thq="thq-dropdown" class="dashboard-dropdown list-item">
              <div
                data-thq="thq-dropdown-toggle"
                class="dashboard-dropdown-toggle1"
              >
                <span class="dashboard-text01">Sub-menu Item</span>
              </div>
            </li>
            <li data-thq="thq-dropdown" class="dashboard-dropdown1 list-item">
              <div
                data-thq="thq-dropdown-toggle"
                class="dashboard-dropdown-toggle2"
              >
                <span class="dashboard-text02">Sub-menu Item</span>
              </div>
            </li>
            <li data-thq="thq-dropdown" class="dashboard-dropdown2 list-item">
              <div
                data-thq="thq-dropdown-toggle"
                class="dashboard-dropdown-toggle3"
              >
                <span class="dashboard-text03">Sub-menu Item</span>
              </div>
            </li>
          </ul>
        </div>
        <img
          alt="logo"
          src="/playground_assets/1213213213-200w.png"
          class="dashboard-image"
        />
      </header>
      <div class="dashboard-cover">
        <div class="dashboard-container1">
          <h1 class="dashboard-text04">healthsocal.ai</h1>
          <span class="dashboard-text05">
            <span>
              Southern California&apos;s mental health epidemic needs to be
              addressed to:
              <span v-html="rawiu0u"></span>
            </span>
            <br />
            <span>
              - provide care to the ever-growing population and increasing number of
              mental illnesses
              <span v-html="rawrurh"></span>
            </span>
            <br />
            <span>
              - give required support to the mental health industry in providing
              those who can make health decisions with health data and solutions.
              <span v-html="rawp9ly"></span>
            </span>
            <span><span v-html="rawp5np"></span></span>
            <span><span v-html="rawycjj"></span></span>
          </span>
          <div class="dashboard-btn-group">
            <router-link to="/map" class="dashboard-navlink button">
              Get Started
            </router-link>
            <button class="dashboard-button button">Learn More</button>
          </div>
        </div>
        <img
          alt="image"
          src="https://images.unsplash.com/photo-1525498128493-380d1990a112?ixid=Mnw5MTMyMXwwfDF8c2VhcmNofDI0fHxtaW5pbWFsaXNtJTIwZ3JlZW58ZW58MHx8fHwxNjI1ODQxMDcw&amp;ixlib=rb-1.2.1&amp;h=1200"
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
                  Interactive maps and user-friendly interfaces can be used to help
                  users understand mental health.
                </span>
                <br />
              </span>
            </div>
            <div class="dashboard-container-data">
              <span class="dashboard-text18">Data</span>
              <span class="dashboard-text19">
                <span class="dashboard-text20">
                  Provide data to help users analyze the main causes of
                  psychological problems in different regions.
                </span>
                <br class="dashboard-text21" />
                <br />
              </span>
            </div>
          </div>
        </div>
      </div>
      <div class="dashboard-hero"></div>
      <footer class="dashboard-footer">
        <img
          alt="logo"
          src="/playground_assets/1213213213-200w.png"
          class="dashboard-image2"
        />
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
        rawiu0u: ' ',
        rawrurh: ' ',
        rawp9ly: ' ',
        rawp5np: ' ',
        rawycjj: ' ',
      }
    },
  }
  </script>
  
  <style scoped>
  .dashboard-container {
    width: 100%;
    display: flex;
    overflow: auto;
    min-height: 100vh;
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
    align-self: flex-start;
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
    font-size: 28px;
    font-style: normal;
    text-align: center;
    font-family: Poppins;
    font-weight: 700;
    margin-right: 4px;
    vertical-align: middle;
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
    color: #595959;
    width: 100%;
    display: inline-flex;
    transition: 0.3s;
    align-items: center;
    padding-top: var(--dl-space-space-halfunit);
    padding-left: var(--dl-space-space-unit);
    border-radius: var(--dl-radius-radius-radius4);
    padding-right: var(--dl-space-space-unit);
    padding-bottom: var(--dl-space-space-halfunit);
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
    color: #595959;
    width: 100%;
    display: inline-flex;
    transition: 0.3s;
    align-items: center;
    padding-top: var(--dl-space-space-halfunit);
    padding-left: var(--dl-space-space-unit);
    border-radius: var(--dl-radius-radius-radius4);
    padding-right: var(--dl-space-space-unit);
    padding-bottom: var(--dl-space-space-halfunit);
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
  .dashboard-dropdown2 {
    cursor: pointer;
    display: inline-block;
    position: relative;
    border-radius: var(--dl-radius-radius-radius2);
  }
  .dashboard-dropdown-toggle3 {
    fill: #595959;
    color: #595959;
    width: 100%;
    display: inline-flex;
    transition: 0.3s;
    align-items: center;
    padding-top: var(--dl-space-space-halfunit);
    padding-left: var(--dl-space-space-unit);
    border-radius: var(--dl-radius-radius-radius4);
    padding-right: var(--dl-space-space-unit);
    padding-bottom: var(--dl-space-space-halfunit);
  }
  .dashboard-dropdown-toggle3:hover {
    fill: #fff;
    color: #fff;
    background-color: #595959;
  }
  .dashboard-text03 {
    width: 100%;
    cursor: pointer;
    display: flex;
    font-size: 14px;
    font-style: normal;
    font-weight: 500;
  }
  .dashboard-image {
    width: var(--dl-size-size-small);
    height: var(--dl-size-size-small);
  }
  .dashboard-cover {
    width: 100%;
    display: flex;
    padding: var(--dl-space-space-threeunits);
    max-width: var(--dl-size-size-maxwidth);
    min-height: 80vh;
    align-items: center;
    flex-direction: row;
    justify-content: space-between;
  }
  .dashboard-container1 {
    display: flex;
    margin-right: var(--dl-space-space-threeunits);
    padding-right: var(--dl-space-space-threeunits);
    flex-direction: column;
  }
  .dashboard-text04 {
    color: rgba(255, 125, 0, 0.8);
    font-size: 3rem;
    max-width: 450px;
    font-family: Poppins;
  }
  .dashboard-text05 {
    margin-top: var(--dl-space-space-twounits);
    margin-bottom: var(--dl-space-space-twounits);
  }
  .dashboard-btn-group {
    display: flex;
    align-items: center;
    flex-direction: row;
  }
  .dashboard-navlink {
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
  .dashboard-navlink:hover {
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
  .dashboard-statistic {
    width: 100%;
    border: 2px dashed rgba(120, 120, 120, 0.4);
    display: flex;
    padding: var(--dl-space-space-threeunits);
    max-width: var(--dl-size-size-maxwidth);
    align-self: center;
    min-height: 80vh;
    align-items: center;
    flex-direction: row;
    background-size: cover;
    justify-content: center;
    background: url('../assets/statistic.png') no-repeat center fixed;     
    background-size: cover;
  }
  .dashboard-solutions {
    width: 100%;
    display: flex;
    padding: var(--dl-space-space-threeunits);
    max-width: var(--dl-size-size-maxwidth);
    min-height: 80vh;
    align-items: center;
    flex-direction: row;
    background-size: cover;
    justify-content: center;
    background-image: url("../assets/solutions.png");
  }
  .dashboard-container2 {
    display: flex;
    align-self: center;
    margin-left: var(--dl-space-space-threeunits);
    margin-right: var(--dl-space-space-threeunits);
    padding-left: var(--dl-space-space-threeunits);
    padding-right: var(--dl-space-space-threeunits);
    flex-direction: column;
  }
  .dashboard-text13 {
    color: rgba(255, 125, 0, 0.8);
    font-size: 3rem;
    max-width: 450px;
    align-self: flex-start;
    font-family: Poppins;
  }
  .dashboard-container3 {
    gap: var(--dl-space-space-threeunits);
    display: flex;
    align-self: flex-start;
    flex-direction: row;
  }
  .dashboard-container-interactivity {
    display: flex;
    align-items: center;
    padding-left: var(--dl-space-space-unit);
    border-radius: var(--dl-radius-radius-radius8);
    padding-right: var(--dl-space-space-unit);
    flex-direction: column;
    justify-content: center;
    background-color: rgba(255,141,0,255);
  }
  .dashboard-text14 {
    color: rgba(255, 255, 255, 0.8);
    font-size: 36px;
    align-self: center;
    margin-top: var(--dl-space-space-twounits);
    font-family: Poppins;
    font-weight: 700;
    margin-bottom: var(--dl-space-space-twounits);
  }
  .dashboard-text15 {
    color: rgba(255, 125, 0, 0.8);
    font-size: 24px;
    margin-top: var(--dl-space-space-twounits);
    font-family: Poppins;
    font-weight: 700;
    margin-bottom: var(--dl-space-space-twounits);
  }
  .dashboard-text16 {
    color: rgba(255, 255, 255, 0.8);
  }
  .dashboard-container-data {
    display: flex;
    align-self: center;
    align-items: center;
    padding-left: var(--dl-space-space-unit);
    border-radius: var(--dl-radius-radius-radius8);
    padding-right: var(--dl-space-space-unit);
    flex-direction: column;
    justify-content: center;
    background-color: rgba(255,223,124,255);
  }
  .dashboard-text18 {
    color: rgba(0, 0, 0, 0.8);
    font-size: 36px;
    margin-top: var(--dl-space-space-twounits);
    font-family: Poppins;
    font-weight: 700;
    margin-bottom: var(--dl-space-space-twounits);
  }
  .dashboard-text19 {
    color: rgba(255, 125, 0, 0.8);
    font-size: 24px;
    margin-top: var(--dl-space-space-twounits);
    font-family: Poppins;
    font-weight: 700;
    margin-bottom: var(--dl-space-space-twounits);
  }
  .dashboard-text20 {
    color: rgba(0, 0, 0, 0.8);
  }
  .dashboard-text21 {
    color: rgba(0, 0, 0, 0.8);
  }
  .dashboard-hero {
    width: 100%;
    border: 2px dashed rgba(120, 120, 120, 0.4);
    display: flex;
    padding: var(--dl-space-space-threeunits);
    max-width: var(--dl-size-size-maxwidth);
    align-self: center;
    min-height: 80vh;
    align-items: center;
    flex-direction: row;
    background-size: cover;
    justify-content: center;
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
    .dashboard-cover {
      flex-direction: column;
    }
    .dashboard-container1 {
      align-items: center;
      margin-right: 0px;
      margin-bottom: var(--dl-space-space-twounits);
      padding-right: 0px;
    }
    .dashboard-text04 {
      text-align: center;
    }
    .dashboard-text05 {
      text-align: center;
      padding-left: var(--dl-space-space-threeunits);
      padding-right: var(--dl-space-space-threeunits);
    }
    .dashboard-statistic {
      flex-direction: column;
    }
    .dashboard-solutions {
      flex-direction: column;
    }
    .dashboard-container2 {
      align-items: center;
      margin-right: 0px;
      margin-bottom: var(--dl-space-space-twounits);
      padding-right: 0px;
    }
    .dashboard-text13 {
      text-align: center;
    }
    .dashboard-text14 {
      text-align: center;
      padding-left: var(--dl-space-space-threeunits);
      padding-right: var(--dl-space-space-threeunits);
    }
    .dashboard-text15 {
      text-align: center;
      padding-left: var(--dl-space-space-threeunits);
      padding-right: var(--dl-space-space-threeunits);
    }
    .dashboard-text18 {
      text-align: center;
      padding-left: var(--dl-space-space-threeunits);
      padding-right: var(--dl-space-space-threeunits);
    }
    .dashboard-text19 {
      text-align: center;
      padding-left: var(--dl-space-space-threeunits);
      padding-right: var(--dl-space-space-threeunits);
    }
    .dashboard-hero {
      flex-direction: column;
    }
  }
  @media(max-width: 767px) {
    .dashboard-header {
      padding-left: var(--dl-space-space-twounits);
      padding-right: var(--dl-space-space-twounits);
    }
    .dashboard-cover {
      padding-left: var(--dl-space-space-twounits);
      padding-right: var(--dl-space-space-twounits);
    }
    .dashboard-text05 {
      padding-left: var(--dl-space-space-unit);
      padding-right: var(--dl-space-space-unit);
    }
    .dashboard-image1 {
      width: 80%;
    }
    .dashboard-statistic {
      padding-left: var(--dl-space-space-twounits);
      padding-right: var(--dl-space-space-twounits);
    }
    .dashboard-solutions {
      padding-left: var(--dl-space-space-twounits);
      padding-right: var(--dl-space-space-twounits);
    }
    .dashboard-text14 {
      padding-left: var(--dl-space-space-unit);
      padding-right: var(--dl-space-space-unit);
    }
    .dashboard-text15 {
      padding-left: var(--dl-space-space-unit);
      padding-right: var(--dl-space-space-unit);
    }
    .dashboard-text18 {
      padding-left: var(--dl-space-space-unit);
      padding-right: var(--dl-space-space-unit);
    }
    .dashboard-text19 {
      padding-left: var(--dl-space-space-unit);
      padding-right: var(--dl-space-space-unit);
    }
    .dashboard-hero {
      padding-left: var(--dl-space-space-twounits);
      padding-right: var(--dl-space-space-twounits);
    }
    .dashboard-footer {
      padding-left: var(--dl-space-space-twounits);
      padding-right: var(--dl-space-space-twounits);
    }
    .dashboard-text23 {
      text-align: center;
      margin-left: var(--dl-space-space-unit);
      margin-right: var(--dl-space-space-unit);
    }
  }
  @media(max-width: 479px) {
    .dashboard-header {
      padding: var(--dl-space-space-unit);
    }
    .dashboard-cover {
      padding-top: var(--dl-space-space-twounits);
      padding-left: var(--dl-space-space-unit);
      padding-right: var(--dl-space-space-unit);
      padding-bottom: var(--dl-space-space-twounits);
    }
    .dashboard-container1 {
      margin-bottom: var(--dl-space-space-unit);
    }
    .dashboard-btn-group {
      flex-direction: column;
    }
    .dashboard-button {
      margin-top: var(--dl-space-space-unit);
      margin-left: 0px;
    }
    .dashboard-statistic {
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
    .dashboard-container2 {
      margin-right: var(--dl-space-space-threeunits);
      margin-bottom: var(--dl-space-space-unit);
      padding-right: var(--dl-space-space-threeunits);
    }
    .dashboard-hero {
      padding-top: var(--dl-space-space-twounits);
      padding-left: var(--dl-space-space-unit);
      padding-right: var(--dl-space-space-unit);
      padding-bottom: var(--dl-space-space-twounits);
    }
    .dashboard-footer {
      height: auto;
      padding: var(--dl-space-space-unit);
      flex-direction: column;
    }
    .dashboard-text23 {
      margin-left: 0px;
      margin-right: 0px;
      margin-bottom: var(--dl-space-space-unit);
    }
  }
  </style>