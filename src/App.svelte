<script>
  import Avatar from "./lib/Avatar.svelte";
  import Banner from "./lib/Banner.svelte";
  import Slider from "./lib/Slider.svelte";
  import TaskItem from "./lib/TaskItem.svelte";
  import Footer from "./lib/Footer.svelte";
</script>

<div class="row between flex-start">
  <div class="col flex-start">
    <h1 class="title">My tasks</h1>
    <h4>
      4 tasks for <select class="header-select">
        <option value="value2">Yesterday</option>
        <option value="value1" selected>Today</option>
        <option value="value3">Tomorrow</option>
      </select>
    </h4>
  </div>
  <div class="col avatar"><Avatar size={60} src="/img/1.webp" /></div>
</div>

<Slider>
  <Banner --color1="#feccd1" --color2="244,182,189">
    <div slot="header" class="header gap">
      <img width="16" src="/img/hotjar-brands.svg" alt="hot" />
      <span>UI Concept</span>
    </div>
    <div class="row between" slot="footer">
      <div class=" gap">
        <Avatar size={40} src="/img/1.webp" />
        <Avatar size={40} src="/img/2.jpg" />
      </div>
      <div class=" gap">
        <img width="22" src="/img/calendar-regular.svg" alt="calendar" />
        <span class="banner-date">10 june</span>
      </div>
    </div>
  </Banner>
  <Banner --color1="#947DFF" --color2="0,0,0" background={2}>
    <div slot="header" class="header gap">
      <img width="16" src="/img/hotjar-brands.svg" alt="hot" />
      <span>UI Concept</span>
    </div>
    <div class="row between" slot="footer">
      <div class=" gap">
        <Avatar size={40} src="/img/1.webp" />
        <Avatar size={40} src="/img/2.jpg" />
      </div>
      <div class=" gap">
        <img width="22" src="/img/calendar-regular.svg" alt="calendar" />
        <span class="banner-date">20 june</span>
      </div>
    </div>
  </Banner>
</Slider>
<TaskItem label="Inspiration" separated checked />
<TaskItem label="Concept 1 - buisness style" separated />
<TaskItem label="Concept 2 - funny style" separated />
<TaskItem label="Concept 3 - minimalism" />

<Footer />

<style>
  .header {
    display: flex;
    flex-direction: row;
    color: #0b113c;
    font-weight: 600;
  }
  .gap {
    gap: 6px;
  }
  .banner-date {
    color: #0b113c;
    align-items: center;
  }
</style>
