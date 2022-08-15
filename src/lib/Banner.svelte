<script>
  export let background = 1;
</script>

<div class="wrapper bg-{background}">
  <div class="header">
    <slot name="header" />
  </div>
  <div class="footer">
    <slot name="footer" />
  </div>
</div>

<style>
  .wrapper {
    display: flex;
    border-radius: 30px;
    width: 358px;
    height: 188px;
    background-color: var(--color1);
    flex-direction: column;
    justify-content: space-between;
    padding: 30px 38px;
  }
  .bg-1 {
    background-color: var(--color1);
    opacity: 1;
    background: linear-gradient(
          135deg,
          rgba(var(--color2), 0.55) 25%,
          transparent 25%
        ) -16px 0/ 32px 32px,
      linear-gradient(225deg, rgb(var(--color2)) 25%, transparent 25%) -16px 0/
        32px 32px,
      linear-gradient(315deg, rgba(var(--color2), 0.55) 25%, transparent 25%)
        0px 0/ 32px 32px,
      linear-gradient(45deg, rgb(var(--color2)) 25%, var(--color1) 25%) 0px 0/ 32px
        32px;
  }
  .bg-2 {
    background-color: var(--color1);
    opacity: 1;
    background-image: repeating-radial-gradient(
        circle at 0 0,
        transparent 0,
        var(--color1) 16px
      ),
      repeating-linear-gradient(rgba(var(--color2), 0.55), rgb(var(--color2)));
  }
</style>
